# TransitPulse Delhi — Split Android Apps

This workspace contains two independent Capacitor Android applications that share the same Supabase project/backend.

- `apps/passenger` — public commuter app (`in.transitpulse.delhi`)
- `apps/reviewer` — restricted report-review app (`in.transitpulse.reviewer`)

## Setup (run separately in each app folder)

1. Copy `.env.example` to `.env.local`.
2. Fill in the existing Supabase project URL and **anon/publishable key**. Never put a service-role key in either app.
3. In PowerShell: `npm.cmd ci` then `npm.cmd run build`.
4. Run `npx.cmd cap sync android`, then `npx.cmd cap open android`.
5. In Android Studio, use **Build → Build Bundle(s) / APK(s) → Build APK(s)**.

Build both folders independently. Their distinct application IDs allow both APKs to be installed on one Android device.
