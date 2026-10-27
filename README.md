# Macey's website

A simple personal site made of plain HTML and CSS. [GitHub Pages](https://pages.github.com/) serves it at <https://maceface13.github.io> from the `main` branch. There is no build step. Edit a file, commit, and push to `main`. The live site usually updates within a minute or two.

The empty `.nojekyll` file tells GitHub Pages to publish these files as they are.

## What's in this repo

| File | What it is |
| --- | --- |
| `index.html` | Home page |
| `resume.html` | Resume |
| `blog/index.html` | Blog list |
| `blog/hello-world.html` | First blog post |
| `css/styles.css` | All of the styling |
| `favicon.svg` | The small icon in the browser tab |
| `images/headshot.jpg` | Photo used on the home page, resume, and blog |

## Preview on your computer

Links and styles use paths like `css/styles.css`, so open the site through a small local server instead of double-clicking a file.

From this folder, run:

```bash
python3 -m http.server 8000
```

Then visit <http://localhost:8000>. Stop the server with Ctrl+C when you're done.

## Edit a page

1. Open the HTML file for that page.
2. Change the words between the tags. Leave the tags (`<h1>`, `<p>`, `<a>`, and so on) in place unless you mean to change the structure.
3. Save the file.
4. Commit and push to `main`.

The row of links at the top (Home, Resume, Blog) is copied onto every page. Pages in the `blog` folder start those links with `../` so they can reach the files one folder up. If you rename a page, update the link on each page.

## Replace the photo

The home page, the resume, and the blog all use `images/headshot.jpg`. To change the picture, save a new photo over that file and keep the name. The round crop is the `.headshot` rule in `css/styles.css`. The blog uses the smaller `.headshot-thumb` size.

## Add a blog post

Posts are normal HTML files in the `blog` folder. The blog list is written by hand in `blog/index.html`, so a new post shows up only after you add a link there.

1. In the `blog` folder, copy `hello-world.html`.
2. Rename the copy to a short name with hyphens, ending in `.html`. Example: `notes-from-class.html`.
3. Open the new file and change three things:
   - the `<title>` in the head
   - the `<h1>` heading and the date in `<time>`
   - the paragraphs

   Leave the byline as it is: the small round photo and the name Macey. Copying `hello-world.html` already includes that line, so every new post gets the same author credit.
4. Open `blog/index.html`. Copy the existing `<li>...</li>` block and paste the copy **above** it, so the newest post is first. Update the link (`href`), the date, the title, and the one-line summary.
5. Commit and push to `main`.

The new post's address will look like `https://maceface13.github.io/blog/notes-from-class.html`.

## Change the look

Colors and fonts are at the top of `css/styles.css`, inside `:root`. Change those values to restyle every page at once. You don't need to edit each HTML file to change a color.

## Please leave these off the site

Don't add a phone number, email address, home address, school name, family names, or Niko's birthdate. Job cities on the resume are fine. The skills list is a placeholder: there's a note in `resume.html`, right above the list, asking you to review it.
