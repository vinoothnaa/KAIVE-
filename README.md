# Kaive Dashboard (live)

Static site: `index.html` + `vercel.json`. No build step.

- Data: Supabase project **kaive-dashboard** (KAIVE org, Mumbai), table `public.app_store`.
- Access list: table `public.allowed_users` (role `admin` sees payslips, `member` does not).
- Logins: Supabase → Authentication → Users → Add user.

To update the site: replace `index.html` in this GitHub repo. Vercel redeploys on every commit.
