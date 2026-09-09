# Atlas Ski & Snowboard Club — GitHub Pages rebuild

A no-build, static redesign of the public Atlas Ski & Snowboard Club website, ready for GitHub Pages.

## What is included

- Modern responsive homepage
- Full 2025–26 published event archive with six event-detail pages
- Current-member resources page
- Ski & Snowboard Waiver page linking to the club's current published PDF
- Privacy page
- Mobile navigation, region filters, subtle scroll animation, 404 page, favicon, and SEO basics
- No framework and no build step

## Publish on GitHub Pages

1. Create a new GitHub repository.
2. Upload **all files and folders from this directory to the repository root**.
3. In GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select `main` and `/ (root)`, then save.
6. GitHub will provide a URL like `https://USERNAME.github.io/REPOSITORY/`.

All internal links are relative, so the site works both on a user/organization Pages domain and inside a project subdirectory.

## Important migration notes

### Member authentication
GitHub Pages is static and cannot securely replace Wix member authentication by itself. The redesign intentionally keeps **Member Access** pointed at the existing Wix profile/member area. If you later want authentication fully off Wix, use a real auth/backend service (for example Cloudflare Access, Supabase Auth, Firebase Auth, Auth0, or a separate member portal) and update the links in the HTML.

### Event data
The current public Atlas site still shows its published **2025–26** events. They are presented here as an archive because the dates have passed. Update `events.html` and the pages under `/events/` when the next season is announced.

### Images
The rebuild references the club's existing Wix-hosted image assets so the design uses the club's current visuals without bundling copies of those files. For a fully independent migration, download the original image files you own, place them under `assets/img/`, and replace the `static.wixstatic.com` image URLs in the HTML.

### Waiver
The waiver button points to the currently published waiver PDF on the existing Atlas site. If you move the PDF into the repository, update the button in `waiver.html` to point to the local file.

### Privacy policy
The privacy page is a modernized restatement of the substance of the existing policy rather than a legal redline. Compare it with the club's approved legal language before replacing the live policy.

## Customize the look
Most visual settings are at the top of `assets/css/styles.css` under `:root`. The mountain/logo SVGs are in `assets/img/`.
