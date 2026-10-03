# Vaultly — Student Digital Locker

Responsive student document locker built with HTML, CSS, JavaScript, Supabase Auth, PostgreSQL and private Supabase Storage.

## Features
- Google sign-in and sign-out
- Per-student profile and document metadata
- Upload, search, categorize, download and delete files
- Private storage bucket and Row Level Security policies
- Responsive dark navy/violet interface

## Setup
1. Create a Supabase project at https://supabase.com/.
2. Run `supabase-schema.sql` in Supabase SQL Editor.
3. Edit `config.js` with the Supabase Project URL and public publishable/anon key.
4. In Google Cloud Console, create a Web OAuth client. Add the callback URL shown by Supabase's Google provider as an authorized redirect URI.
5. Enable Google in Supabase Authentication > Providers. Set Site URL and allowed Redirect URLs in Supabase Auth URL Configuration.
6. Run locally with VS Code Live Server or `python -m http.server 5500`.
7. Publish with GitHub Pages: repository Settings > Pages > Deploy from a branch > main > /(root).

## Security
The public key is designed for browser use; never commit a `service_role` key, secret key or database password. RLS and private Storage policies are essential. Test cross-account access before uploading real student records. This is a hackathon starter, not a security audit.
