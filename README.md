# Cooke Psychology: static site

One page, plain HTML. All styling is inside `index.html` (search for `<style>`), so there is no separate CSS file to lose.
Colours and fonts (matched to the logo) are at the top of the style block under `:root`.

## Preview it
Double-click `index.html`.

## Images (all in `images/`)
- `hero.jpg`: the watercolour beach behind the top banner
- `brooke.jpg`: Brooke's photo (top of the page)
- `logo.png`: full logo, transparent background
- `logo-mark.png`: circle and grass only, used in the header
- `favicon.png` and `apple-touch-icon.png` (site root): browser tab and phone home-screen icons
To change one, replace the file and keep the same name.

## Still to add (search index.html for the comments)
- Booking button: paste the Halaxy link and uncomment
- Address / hours in the Contact section
- More about Brooke, under her name at the top

## Publish on GitHub Pages
1. Create a repo and upload everything in this folder to the root.
2. Settings > Pages > Deploy from a branch > `main` / root.
3. Confirm the custom domain reads `cookepsychology.com.au`, then tick Enforce HTTPS when available.

## DNS
| Type  | Name | Value |
|-------|------|-------|
| A     | @    | 185.199.108.153 |
| A     | @    | 185.199.109.153 |
| A     | @    | 185.199.110.153 |
| A     | @    | 185.199.111.153 |
| AAAA  | @    | 2606:50c0:8000::153 |
| AAAA  | @    | 2606:50c0:8001::153 |
| AAAA  | @    | 2606:50c0:8002::153 |
| AAAA  | @    | 2606:50c0:8003::153 |
| CNAME | www  | `<your-github-username>`.github.io |

On Cloudflare, use "DNS only" (grey cloud) until GitHub issues the HTTPS certificate.
Check the IPs against GitHub's docs ("Managing a custom domain for your GitHub Pages site") before setting them.
With `CNAME` present, the `github.io` address redirects to the custom domain, so delete `CNAME` if you want to preview on `github.io` first.
