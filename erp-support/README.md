# ERP Application Support & Developer Coordination

## Scope

This section describes the operational support role between ERP users, infrastructure teams, database administrators and application developers.

The objective is to restore business service safely, collect useful diagnostic information and coordinate changes without making unapproved production modifications.

## Support Workflow

1. Record the issue, affected module, user role, time and business impact.
2. Determine whether the issue affects one user, a group or the whole application.
3. Check basic service availability, DNS, network path and authentication.
4. Capture exact error messages and reproducible steps, avoiding sensitive data.
5. Check application logs and relevant service health with authorized access.
6. Determine whether the issue is configuration, access, data, integration, application code or infrastructure related.
7. Escalate to the developer/vendor with evidence, timestamps and expected behavior.
8. Test the fix in a non-production environment where available.
9. Obtain approval, schedule the change and define rollback.
10. Confirm with the requester and document resolution.

## Developer Handover Template

| Field | Information to capture |
|---|---|
| Issue summary | Short, factual description |
| Affected module | Module, screen or workflow |
| Business impact | Users/processes affected and urgency |
| Reproduction | Numbered steps with sanitized test data |
| Expected result | What should happen |
| Actual result | What happens instead |
| Timestamp | Include time zone |
| Evidence | Sanitized screenshot, error ID or log excerpt |
| Recent changes | Release, configuration or infrastructure change |
| Validation | Test cases and acceptance criteria |

## Change & Release Controls

- Maintain separate development, test/UAT and production environments where possible.
- Use approved source-control and release procedures.
- Back up relevant data and configuration before changes.
- Apply least-privilege access for developers and support staff.
- Do not run unreviewed SQL updates directly against production.
- Record change owner, approval, maintenance window, validation and rollback.

## Common Triage Categories

- Login, role and permission issues.
- Slow pages or report generation.
- Incorrect or delayed data synchronization.
- Printing, export and document-generation issues.
- Integration/API failures.
- Application service or database availability.
- User training and workflow clarification.

## Related References

- [System & Server Virtualization Portfolio](https://github.com/thnayem/system-server-virtualization-portfolio)
- [Network Engineering Portfolio](https://github.com/thnayem/network-engineering-portfolio)

---

**A note on this documentation:** The technical work and experience behind these notes are mine. Some wording and the way I have organized the material have had AI assistance, mainly to make the writing clearer and save time. The examples, decisions and work described are not AI-generated. I check what I publish and stand behind it.
