# teshrij.xyz customer portal — how it is published (since 2026-11-27)

`index.html` is a blank shell (logo + "Loading..."). With `?id=<secret>` it fetches the portal script from the
edge function **view**, which answers only when the id is a `gpt_subs.secret_id` (404 otherwise; the shell then
shows "This link is not active"). Without an id the shell redirects to `/go/`. The real portal is
`app/portal.html` and is NOT published (`_config.yml` excludes `app/`, README.md and this file).

**Changing the portal = edit `app/portal.html`, push, AND run `~/Projects/ui_gate/deploy.sh portal`.**
build.py expects exactly one `<style>` in its head and one inline `<script>` in its body.
