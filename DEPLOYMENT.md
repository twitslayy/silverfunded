# Silver Funded deployment

1. Run `npm install`.
2. Copy `.env.example` to `.env` on the server.
3. Put the PostgreSQL connection string in `DATABASE_URL`. The password must be URL-encoded if it contains reserved characters. Never put this value in browser JavaScript or commit it.
4. Run `psql "$DATABASE_URL" -f supabase-schema.sql` or paste the SQL into Supabase SQL Editor.
5. Set a strong random `JWT_SECRET`.
6. Configure SMTP for automatic order/support emails.
7. Configure Stripe (or another provider) and implement/verify the provider webhook before enabling live payments.
8. Put the site behind HTTPS. Configure HSTS/security headers at the edge/server.
9. Replace all NOT CONFIGURED legal entity/address/jurisdiction fields before launch.
10. Add your actual analytics ID only after deciding your consent/legal basis.
11. Configure SPF, DKIM and DMARC for the domain email.
12. Submit sitemap.xml in Google Search Console and test Core Web Vitals.

The supplied PostgreSQL credential is intentionally NOT embedded in the ZIP. If that credential is real, rotate it because it was shared in chat.
