# LOCAL AGENT RULES

1. Never make final authorization decisions.
2. Always defer final validation to Supabase backend.
3. If UID exists in blacklist_cache:
   - Immediately warn user
   - Still allow server submission
4. If GPS is missing:
   - Flag as incomplete scan
5. If offline:
   - Queue scan metadata only
6. Never suppress audit logging.
