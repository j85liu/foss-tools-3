# Section 3: CD (Continuous Deployment)
Led by the CD Lead — do this after CI and Version Control are done

**Real parallel:** even a correctly-sized command needs a consistent,
automatic way to confirm and communicate that it ran safely — not a
step someone can forget under time pressure.

## Your task
Enable GitHub Pages (Settings → Pages → Source: "GitHub Actions").
Add a second job to the workflow that runs only after the check
passes and only on `main`, publishing `cd/public/` as a live status
page.

```yaml
  deploy:
    needs: check
    if: github.ref == 'refs/heads/main'
    runs-on: ubuntu-latest
    permissions:
      pages: write
      id-token: write
    steps:
      - uses: actions/checkout@v4
      - uses: actions/configure-pages@v4
      - uses: actions/upload-pages-artifact@v3
        with:
          path: 'cd/public'
      - uses: actions/deploy-pages@v4
```

Edit `cd/public/index.html` to say something real, like "✅
Harborlight — command within safe threshold," commit, and watch the
page go live.

## Success looks like
A real, live URL showing your status text, updating automatically on
every push.

## What to hand the Presenter
A screenshot of the live status page, or the actual link. This
becomes the other half of Slide 3 (shared with Version Control).