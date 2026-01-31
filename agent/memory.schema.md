# LOCAL AGENT MEMORY SCHEMA

PURPOSE:
Store minimal, non-sensitive data to support
offline decision hints and faster UX.

## ALLOWED LOCAL KEYS

- officer_profile
  - officer_id
  - role
  - unit

- recent_scan_summary
  - total_today
  - blocked_today
  - last_scan_time

- blacklist_cache
  - uid
  - type (QR | NFC)
  - reason
  - updated_at

- device_status
  - device_id
  - last_sync
  - offline_mode

## FORBIDDEN LOCAL DATA

- national_id
- full_scan_logs
- raw_nfc_payload
- biometric_data

## DATA LIFETIME

- blacklist_cache: max 24 hours
- scan_summary: reset daily
- device_status: persistent

Local memory is advisory only.
