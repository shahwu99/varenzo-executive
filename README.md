# Varenzo Executive website

A responsive, multi-page static website for Varenzo Executive, built with HTML, CSS and vanilla JavaScript. It is designed for GitHub Pages and uses relative paths so it works both at a domain root and in a GitHub Pages project subpath.

## Run locally

From this folder, start any static HTTP server. For example, with Python 3:

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000>. You can also open `index.html` directly, although a local HTTP server more closely matches deployment.

## Replace the placeholder photography

The approved Lexus RX 450h and Infiniti Q50 vehicle photographs are stored locally in `assets/lexus-rx-450h-vehicle.jpg` and `assets/infiniti-q50-awd.jpg`. To update a vehicle image, replace its asset while retaining the same relative path, or update all references in the HTML and CSS. Use compressed, appropriately sized WebP or AVIF files in `assets/` for future production imagery; retain descriptive alt text. The remote Google Fonts and remaining Unsplash images require an internet connection.

## Update contact information

Edit `contact.html` to add the approved business email, phone number and service area. Until these details are ready to publish, the site correctly displays that contact details are not yet available. The enquiry form is deliberately not wired to a fake success state: it tells visitors that no message was sent.

## Add future fleet vehicles

In `fleet.html`, update the current vehicle card with verified vehicle details and add another vehicle card using the same `.fleet-detail` / `.fleet-detail-copy` structure. Move a category from the future fleet section into the current fleet only after the vehicle is actually owned and available to the business. Do not describe future categories as bookable. Update the fleet feature on `index.html` when appropriate.

## Connect a working enquiry form

The form currently validates required fields in the browser but does not transmit or store information. To activate submissions, choose and configure a form backend (for example, a hosted form endpoint or a serverless function), set its production endpoint in `contact.html` or `js/script.js`, and handle success and failure responses explicitly. Review the provider's privacy, data-retention and consent requirements before collecting personal information. Test delivery on the deployed site; only show a success message after the service confirms receipt. Do not use the form for confirmed reservations, payments or deposits unless the business is ready and legally permitted to do so.

## Deploy with GitHub Pages

1. Push these website files to a GitHub repository.
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**, choose the branch containing the site (commonly `main`) and select `/ (root)`.
4. Save and wait for GitHub Pages to publish the site. The `index.html` file is the home page.
5. Confirm all pages and assets load at the published Pages URL, especially if using a project site URL with a repository subpath.

## Connect `varenzoexecutive.com`

After purchasing the domain, add it under **Settings → Pages → Custom domain** in the repository. Configure the DNS records at the domain registrar to match the current GitHub Pages custom-domain instructions for the account and site type (typically `A` records for an apex domain and a `CNAME` for `www`). Set up a redirect between the apex and `www` host as desired, wait for DNS propagation, then enable **Enforce HTTPS** in Pages once GitHub reports the certificate is available. Keep the DNS records aligned with GitHub's current documentation.

## Project files

- `index.html` — home page
- `services.html` — service descriptions and destinations
- `fleet.html` — current vehicle and future fleet categories
- `corporate.html` — corporate travel information
- `about.html` — company vision
- `contact.html` — pre-launch enquiry form
- `css/style.css` — shared responsive styling
- `js/script.js` — mobile navigation, reveal effects and honest form status
- `assets/` — reserved for locally hosted production imagery

Varenzo Executive is currently preparing for launch. Transportation services will commence subject to applicable licensing, insurance and regulatory approvals.
