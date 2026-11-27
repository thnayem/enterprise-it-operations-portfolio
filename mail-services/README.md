# Mail Server Administration, Mailbox Creation & Outlook Configuration

## Scope

This section documents common enterprise email administration tasks: mail service preparation, user mailbox creation, mailbox lifecycle management, Outlook client configuration, troubleshooting and security practices.

The procedures are platform-neutral references. Exact steps depend on whether the organization uses Microsoft Exchange Server, Microsoft 365/Exchange Online, or another supported mail platform. Do not mix settings from different platforms.

## Mail Service Components

- **Mail platform:** Exchange Server, Exchange Online/Microsoft 365, or another organizational mail service.
- **Domain and DNS:** Public MX, SPF, DKIM and DMARC records; internal DNS where required.
- **Identity:** Active Directory or cloud identity, mailbox licensing and access policies.
- **Client access:** Outlook desktop, Outlook on the web and supported mobile clients.
- **Protocols:** Modern authentication and Autodiscover where supported; IMAP/SMTP only when enabled and approved by the mail administrator.

## New Email ID / Mailbox Creation Workflow

1. Receive an approved user or HR request with the required display name, department and email alias.
2. Check the organization's naming convention and confirm that the requested address is available.
3. Create or verify the user's identity in the approved directory or cloud tenant.
4. Assign the required mail service/license where applicable.
5. Create or enable the mailbox using the platform's supported administration interface.
6. Set the primary SMTP address and any approved aliases.
7. Apply mailbox size, retention, archive and access policies according to organizational standards.
8. Configure group membership, distribution lists and shared mailbox access only with approval.
9. Provide initial sign-in instructions through an approved secure channel; require the user to set their own password and MFA.
10. Test internal and external mail flow, then document completion.

## Mailbox Administration Checklist

- Create, disable, rename or remove mailbox access according to approved joiner/mover/leaver processes.
- Manage aliases and distribution group membership.
- Configure shared mailbox permissions using least privilege.
- Apply retention, archive and mailbox quota policies.
- Review forwarding rules and delegation permissions.
- Preserve mailbox data according to legal, HR and organizational retention requirements.
- Never share passwords or export mailbox contents without authorization.

## Outlook Desktop Setup

### Preferred setup

1. Confirm the user can sign in to the mailbox through the organization's approved webmail portal.
2. Install a supported and licensed Outlook version.
3. Open Outlook and add the user's organizational email address.
4. Complete the organization's approved sign-in and MFA process.
5. Allow Autodiscover and modern authentication to configure the profile automatically where supported.
6. Confirm mailbox folders, calendar, contacts and address book access.
7. Send a test message to an internal recipient and an approved external recipient.
8. Confirm replies, attachments, calendar availability and shared mailbox access if applicable.

### Manual configuration when explicitly required

Use only the server names and settings supplied by the organization's mail administrator or provider. Do not guess server hostnames or ports.

| Setting | What to obtain/verify |
|---|---|
| Email address | User's full primary email address |
| Username | Usually full email address, but platform policy may differ |
| Incoming server | Approved Exchange/IMAP endpoint and security method |
| Outgoing server | Approved SMTP submission endpoint and authentication policy |
| Encryption | TLS settings required by the mail platform |
| Authentication | Modern authentication preferred where supported; basic authentication may be disabled |
| Autodiscover | DNS/service configuration for supported Outlook clients |

For Microsoft 365 or Exchange environments, prefer the supported modern sign-in and automatic profile configuration rather than manually entering legacy IMAP/SMTP settings.

## Common Outlook Troubleshooting

| Symptom | Checks |
|---|---|
| Outlook cannot find mailbox | Address spelling, account status, license/mailbox provisioning and Autodiscover |
| Password prompt repeats | Sign-in status, MFA, modern authentication, stale cached credentials and account policy |
| Cannot send email | Outgoing mail service, recipient restrictions, mailbox quota, message size and service health |
| Cannot receive email | MX/mail flow, mailbox quota, spam/quarantine and service health |
| Outlook works on web but not desktop | Outlook profile, supported client version, Autodiscover and local cache |
| Shared mailbox missing | Permission assignment, propagation time and correct Outlook profile |
| Emails delayed or rejected | Message trace, DNS authentication records, transport rules and recipient response |

## Mail Flow & DNS Checks

- **MX:** Directs inbound mail for the domain to the designated mail service.
- **SPF:** Identifies authorized sending sources for the domain.
- **DKIM:** Adds a cryptographic signature to supported outbound messages.
- **DMARC:** Defines domain policy and reporting for SPF/DKIM alignment.
- **Autodiscover:** Helps supported Outlook clients locate mailbox configuration.

DNS values must come from the actual mail provider and domain administrator. Incorrect records can interrupt mail delivery or authentication. Plan DNS changes, verify propagation and retain a rollback record.

## Security & Operational Practices

- Enforce MFA and conditional access/security policies where available.
- Use least privilege for mail administrators and mailbox delegates.
- Disable or restrict legacy authentication according to platform support.
- Review external forwarding, inbox rules and suspicious sign-in activity.
- Maintain audit logging and follow the organization's retention requirements.
- Protect mail backups and test restore processes where the platform supports them.
- Do not publish real email addresses, tenant IDs, server hostnames, DNS records, credentials or user mailbox data in this public portfolio.

## Related References

- [System & Server Virtualization Portfolio](https://github.com/thnayem/system-server-virtualization-portfolio)
- [Enterprise IT Operations Portfolio Home](../README.md)
