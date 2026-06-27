# Lessons Learned

Use this file to summarize the main Splunk skills developed across the labs.

## Key Takeaways

- Always verify log ingestion before analysis.
- Use `spath` when audit data is stored in structured JSON-style fields.
- High-volume client IPs can reveal authentication patterns worth reviewing.
- Failed login analysis is stronger when grouped by IP address, operation, result status, and error code.

## Improvements For Future Labs

- Add an alert configuration screenshot if available.
- Add a short timeline if the dataset contains useful timestamps.
- Map authentication failures to MITRE ATT&CK where appropriate.
