<!-- LOVABLE:BEGIN -->
> [!IMPORTANT]
> This project is connected to [Lovable](https://lovable.dev). Avoid rewriting
> published git history — force pushing, or rebasing/amending/squashing commits
> that are already pushed — as it rewrites history on Lovable's side and the
> user will likely lose their project history.
>
> Commits you push to the connected branch sync back to Lovable and show up in
> the editor, so keep the branch in a working state.
<!-- LOVABLE:END -->

## CivicIA architecture
- Domain catalogs, priority scoring and thresholds live only in src/lib/civic.ts — single source to avoid magic numbers.
- src/lib/store.ts holds session + cached data and exposes one `actions` API backed by src/lib/cloud.ts; there is no demo/offline mode — every screen requires a real signed-in account.
- Maps use Leaflet + OpenStreetMap tiles loaded via dynamic import inside MapView (browser-only, no API key).
- Districts live in the districts table and are mirrored as DISTRICTS in src/lib/civic.ts (same ids).
- Roles live in user_roles (never on profiles); staff scope = user_roles.municipality_id, checked by is_muni_staff() in RLS.
- Codes, initial status, priority level, history and notifications are set by DB triggers, never trusted from the client.
- Citizen screens under /app (bottom nav), municipal screens under /admin (sidebar); shared UI in src/components/civic.
