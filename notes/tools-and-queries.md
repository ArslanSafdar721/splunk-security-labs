# Tools And Queries

## Tools

- Splunk
- SPL
- Audit log dataset

## SPL Query Notes

### Log Ingestion Check

```spl
index=auditlab | head 10
```

Used to confirm that the dataset was imported and searchable.

### Top Source IP Analysis

```spl
index=auditlab
| spath input=AuditData
| stats count by ClientIP
| sort - count
| head 10
```

Used to identify the most active client IP addresses in the authentication logs.

### Failed Login Investigation

```spl
index=auditlab
| spath input=AuditData
| search ResultStatus="Failure"
| stats count by ClientIP Operation ResultStatus ErrorNumber
```

Used to investigate failed authentication events and related error codes.
