# Mubiligi Visit Day

Visitor management app built with Vite, React, and Supabase.

## Configure Supabase

1. Create or select a Supabase project.
2. Apply the SQL migrations in `supabase/migrations` in filename order, using the Supabase SQL Editor or Supabase CLI.
3. Copy `.env.example` to `.env` and set `VITE_SUPABASE_URL` and `VITE_SUPABASE_ANON_KEY` from the Supabase project settings.
4. In Supabase Authentication URL Configuration, set the production Site URL and add the local and production app URLs to the allowed redirect URLs.

The browser app only needs the Supabase anon/publishable key. Never put a Supabase service-role key in a `VITE_` variable or client-side file.

## Run and build

```powershell
npm.cmd ci
npm.cmd run dev
```

Before hosting, verify the app and create its static production bundle:

```powershell
npm.cmd run lint
npm.cmd run typecheck
npm.cmd run build
```

Deploy the generated `dist` directory to a static hosting provider. Set `VITE_SUPABASE_URL` and `VITE_SUPABASE_ANON_KEY` in that provider's build environment; Vite embeds these values at build time, so rebuild after changing them.

Attendance reports can be downloaded as CSV or as a `.docx` Word document. The Word report uses landscape A4 layout and can be opened, edited, and printed in Microsoft Word or a compatible word processor.
