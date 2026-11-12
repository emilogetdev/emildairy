# Emil Tagebuch

Öffentliches, responsives Tagebuch auf GitHub Pages. Besucher können Einträge lesen und durchsuchen. Nur das festgelegte Supabase-Admin-Konto darf Einträge erstellen, bearbeiten oder löschen.

## Bereits verbunden
- Verwendet dasselbe Supabase-Projekt wie Wildora: `dzwgomgrtlsqksnjclje` (EU).
- Eigene Tabelle `diary_entries`, getrennt von Wildoras Tabellen.
- Supabase Publishable Key im `config.js`; niemals den Service-Role-/Secret-Key in den Browser oder ins Repository legen.
- Admin-Berechtigung wird serverseitig durch Row Level Security (RLS) geprüft.

## Einmalige Supabase-Einrichtung
1. Im Supabase-Projekt `dzwgomgrtlsqksnjclje` im SQL Editor den Inhalt von `supabase-setup.sql` ausführen.
2. Vorher in den drei Admin-Policies `REPLACE-WITH-ADMIN-EMAIL@example.com` durch die E-Mail-Adresse des einen Admin-Kontos ersetzen.
3. Falls das Wildora-Konto bereits existiert, kann dasselbe Supabase-Login verwendet werden. Andernfalls das Admin-Konto unter Authentication → Users anlegen. Öffentliche Registrierung deaktivieren.

## GitHub Pages
Repository: https://github.com/emilogetdev/emildairy
Website: https://emilogetdev.github.io/emildairy/
GitHub Actions deployed automatisch bei Pushes auf `main`.

Admin: auf **Admin** klicken oder **Ctrl+4**, dann innerhalb von zwei Sekunden **Ctrl+3** drücken. Die Tastenkombination öffnet nur das Login; sie gewährt keine Rechte.
