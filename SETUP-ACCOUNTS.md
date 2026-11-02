# KO TECH — Activate real login, orders and notifications on Netlify

The website's HTML/CSS is deployable as-is. **To activate persistent accounts and orders, connect your own Supabase project.** Until configured, the existing browser-only demo stays available; it is not a live store.

## 1. Create the database and authentication service

1. Create a project at https://supabase.com/dashboard (or use an existing project).
2. Open the project's **SQL Editor**. Paste the entire `setup/ko-tech-supabase.sql` file and click **Run**. This creates 62 products, user-protected orders, saved wishlists, notifications, and server-side order price validation.
3. Under **Authentication → Providers**, enable **Email**. For a real customer-facing store, keep email confirmation enabled. Supabase's default email service can be rate-limited; set up custom SMTP for production signup and password-reset emails.
4. Under **Authentication → URL Configuration**, set **Site URL** to your deployed Netlify site, e.g. `https://YOUR-SITE.netlify.app`, and add `https://YOUR-SITE.netlify.app/**` to redirect URLs. If testing locally, add the local URL too.

## 2. Connect the website

1. In Supabase Project Settings → API / API Keys, copy your **Project URL** and **publishable key** (or legacy `anon` key).
2. Edit `js/backend-config.js`:

```js
window.KO_CLOUD_CONFIG = {
  url: 'https://YOUR-PROJECT.supabase.co',
  publishableKey: 'sb_publishable_YOUR_PUBLIC_KEY'
};
```

**Never use a secret or `service_role` key in website files.** The public key is safe to publish because the SQL grants and row-level security enforce account permissions.
3. Save the file. Extract and drag the **KO-TECH-Accounts-Orders-Notifications** folder into Netlify Drop, or push your changed files to your connected GitHub repository. Do not drag the ZIP file itself. If GitHub manages your site, push the updated folder contents to its publishing branch.
4. Netlify site must be HTTPS; the default `*.netlify.app` URL is HTTPS.

## 3. Test

1. Open `Register.html` on the live Netlify URL, sign up, and check your email for the confirmation link (if confirmations enabled).
2. Log in through `Login.html`. Add products to cart and go to `Checkout.html`. The checkout requires sign-in when Supabase is connected.
3. Submit an order. The server validates product IDs, quantities, discounts, delivery fees, and creates a real database order request (not a payment).
4. Open `Account.html` to view stored orders and notifications, and `Track-Order.html` to see order details. The tracking page also lists your orders after login, so you do not need to remember an order number. You can sign in on another device and see the same order.
5. Enable browser alerts in `Account.html` if desired. **Browser pop-up notifications only arrive while the site is open and permission is granted.** In-site notifications are saved in the account and remain available later.
6. For a status change, in Supabase SQL Editor run (using a real order number):

```sql
update public.ko_orders set status = 'Confirmed' where order_number = 'KOT-REPLACEWITHREALNUMBER';
```

This automatically adds a status history entry and a customer notification. The customer can refresh the tracking page to see the new step. Repeat with `Packed`, `Shipped`, `Delivered`, or `Cancelled` as applicable. Browser notification polling runs about every 45 seconds while the site is visible.

## Important limitations

- **No real payment gateway is installed.** Orders are saved requests awaiting the store's confirmation; do not tell customers they have paid.
- Orders, passwords and address information are not exposed to other accounts. A customer needs to be signed in to view their cloud orders; tracking links are not public guest-order links.
- Order-confirmation and status notifications are **inside the website**, with optional browser alerts while open. **Order emails, text messages and background push are not configured.** Supabase can send sign-up and password-reset emails after its mail service is configured.
- The `Admin.html` page from the earlier Node-based project is not active on static Netlify; manage order statuses in the Supabase dashboard using the Table Editor or SQL Editor.
- Keep your Supabase and Netlify accounts secure. Review privacy terms and a retention policy before using real customers' personal information.
- Forms (Contact/Enquiry) still use Netlify Forms and require Netlify form detection to be enabled.
- `js/backend-config.js` holds public project identifiers only. DO NOT upload Supabase secret keys to Netlify files.

## Troubleshooting

- Login form still says not connected: check config values and browser console; redeploy after edits.
- "Could not load the secure account library": ensure internet access and script from jsDelivr isn't blocked.
- `relation public.ko_orders does not exist` or `function ko_place_order does not exist`: run the complete SQL setup in the correct Supabase project.
- No confirmation/reset email: inspect Supabase Auth email settings and deliverability, use custom SMTP for production.
- "permission denied": ensure you are logged in and the SQL script finished successfully.
