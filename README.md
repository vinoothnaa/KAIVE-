# Kaive Dashboard (live)

Static site: `index.html` + `vercel.json`. No build step.

- Data: Supabase project **kaive-dashboard** (KAIVE org, Mumbai), table `public.app_store`.
- Access list: table `public.allowed_users` (role `admin` sees payslips, `member` does not).
- Logins: Supabase → Authentication → Users → Add user.

To update the site: replace `index.html` in this GitHub repo. Vercel redeploys on every commit.

## Field capture (`/capture`)
`capture.html` — mobile page for Valence field workers: GPS fix → USC lookup → in-page camera only (no gallery upload) → GPS/time stamp burned into the photo + GPS in EXIF → offline-safe upload queue → visit submit.
Backend: Supabase edge function `field-capture`, private schema `vfield` (houses, photos, visits), storage bucket `valence-photos/<VILLAGE>/<USC>/`. Link needs `?k=<team key>` (stored in `vfield.config`).
