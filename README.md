# QuakeEdge project website

Plain static HTML/CSS: no build step and no frameworks. Open `index.html` in a browser to preview.

## Pages
- `index.html`: overview
- `log.html`: lab notebook (how to add an entry is explained in a comment at the top of the list)
- `hardware.html`: parts, wiring, bench tests
- `results.html`: figures
- `assets/style.css`: all styling; `assets/img/`: figures and photos

## Writing the content
Every yellow **✎ Student writes** box (`<div class="todo">…</div>`) is a spot for the
student's own words. Replace the whole div with `<p>` paragraphs. Also fill in the
`<!-- STUDENT: … -->` comments in each footer.

Before publishing, check nothing is left:

    grep -n 'class="todo"\|STUDENT:' *.html

New figures: copy from `~/quakesense/output/figures/` into `assets/img/`.

## Publishing on GitHub Pages with your domain
1. Create a public GitHub repo (e.g. `quakeedge-site`) and push this folder:
       git init && git add . && git commit -m "First version of the site"
       git branch -M main
       git remote add origin https://github.com/<you>/quakeedge-site.git
       git push -u origin main
2. Repo → Settings → Pages → Source: "Deploy from a branch", branch `main`, folder `/ (root)`.
3. Same page → Custom domain: enter your domain (e.g. `www.example.com`). GitHub creates a `CNAME` file.
4. At your domain registrar, add DNS records:
   - `www` → CNAME → `<you>.github.io`
   - apex (`example.com`) → A records 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
5. Once DNS resolves (minutes to a few hours), tick "Enforce HTTPS".
