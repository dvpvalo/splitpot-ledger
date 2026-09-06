# Splitpot ledger page

The public read-only page players open from a Splitpot game link.

One self-contained file. It calls the `get_ledger` RPC on the Splitpot Supabase project with
the publishable key, which is safe to ship: every table is behind row-level security and the
anonymous role holds no table grants, so this page can read one game's ledger and nothing else.

Served by GitHub Pages at <https://dvpvalo.github.io/splitpot-ledger/>. Links from the app go
to a redirect shim on Supabase, which points here via the `LEDGER_PAGE_URL` secret — so the
host can change without shipping a new build of the app.

The source of truth is `web/ledger.html` in the Splitpot project. Edit it there, copy it here
as `index.html`.
