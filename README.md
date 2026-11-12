# Emil Tagebuch

Lightweight public diary for GitHub Pages. Readers can view and search posts; one authenticated admin can create, edit and delete them.

## Supabase setup (required for live data and admin)
1. Create a Supabase project.
2. In SQL Editor, run `supabase-setup.sql` after replacing every occurrence of `REPLACE-WITH-YOUR-ADMIN-EMAIL@example.com` with your admin email.
3. In Authentication > Users, manually create that admin user with a strong password. Disable public sign-ups.
4. In Project Settings > API, copy the Project URL and publishable/anon key into `config.js`. Never use the service_role key.
5. Commit the updated `config.js` to this repository. The anon/publishable key is public by design; database RLS policies protect writes.

## GitHub Pages
Repository: https://github.com/emilogetdev/emildairy
Open Settings > Pages, choose Deploy from a branch, select `main` and `/(root)`, then Save.
Expected site URL: https://emilogetdev.github.io/emildairy/

Admin: click Admin, or press Ctrl+4 then Ctrl+3 within two seconds. The shortcut only opens the login; Supabase Auth and RLS enforce permissions.
