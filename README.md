# chuktaiwai.com — how this site works

Plain HTML. No build step, no command line, no framework. You can edit every
word of it inside your web browser on github.com.

## Files

| File | What it is |
| --- | --- |
| `index.html` | Home page: bio, current work, honours, education |
| `research.html` | Research statement, work in progress, interests, coursework |
| `review.html` | CU Philosophy Review |
| `service.html` | Teaching, mentoring, service learning |
| `style.css` | All the styling. Change a colour or a size once here and every page follows |
| `favicon.svg` | The small icon shown in the browser tab |
| `images/portrait.svg` | Placeholder portrait. Replace this |
| `files/Chuk-Tai-Wai-CV.pdf` | The PDF the CV link in the menu points to |

## Publishing it free on GitHub Pages

1. Create a free account at github.com. Choose the username carefully, because
   the free address will be `username.github.io`. Something like `chuktaiwai`
   works.
2. Click the plus sign, top right, then **New repository**.
3. Name the repository exactly `username.github.io`, using your own username.
   Set it to **Public**. Click **Create repository**.
4. On the new repository page click **uploading an existing file**.
5. Drag in everything from this folder, including the `images` and `files`
   folders. Click **Commit changes**.
6. Wait two or three minutes, then visit `https://username.github.io`.

That address is free forever and costs nothing.

## Putting your own domain on it

1. Buy `chuktaiwai.com` from Cloudflare Registrar, roughly USD 10.50 a year,
   sold at cost with no first-year discount trick and free WHOIS privacy.
2. In the domain's DNS settings add four **A** records for `@`, pointing to
   `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`.
   Add a **CNAME** record for `www` pointing to `username.github.io`.
3. In the repository go to **Settings**, then **Pages**, and type
   `chuktaiwai.com` into the custom domain box. Save.
4. Come back within a day and tick **Enforce HTTPS**.

GitHub keeps serving the `username.github.io` address as well, so nothing
breaks and no link you have already sent stops working.

## Updating the site later

On github.com open the file you want to change, click the pencil icon, edit the
text, then click **Commit changes**. The live site updates in about a minute.

Every page contains HTML comments that begin with `EDIT:` marking the places
most likely to need changing. To add a new item to a list, copy an existing
`<li>` or `<div class="entry">` block, paste it below, and change the words
inside. Never delete the closing tag.

When you publish something, move it from **Work in progress** into a new
**Publications** section on `research.html`, in the same shape Isaac Wilhelm
uses: title, year, journal in italics.

Change the **Last updated** line at the foot of each page when you edit it. A
visitor who sees a recent date reads the site as alive.

## Replacing the portrait

Put your headshot in the `images` folder, named `portrait.jpg`, square, at
least 512 by 512 pixels. Then in `index.html` change

    <img src="images/portrait.svg"

to

    <img src="images/portrait.jpg"

## Replacing the CV

Upload the new PDF into the `files` folder with exactly the name
`Chuk-Tai-Wai-CV.pdf`, overwriting the old one. Every CV link on the site keeps
working, including in emails you sent months ago.
