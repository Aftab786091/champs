# Rice CHAMPs website

Plain HTML, CSS, and one logo file. No build step. Pages link to each other with relative links, so the folder works on any host.

## Files
- `index.html` Home
- `program.html` Program
- `team.html` Team (officer names, photos, and contact are placeholders in [brackets])
- `faq.html` FAQ (two answers are placeholders: premed policy and missed-deadline policy)
- `apply.html` Application form
- `style.css` All colors, fonts, and layout for every page. Brand colors are at the top, in `:root`.
- `logo.png` Logo and browser tab icon

## Put it live on GitHub Pages
1. Sign in to GitHub. Click your profile picture, then **Your organizations**, then **New organization**. Choose the **Free** plan and name it something like `rice-champs`.
2. Inside the organization, click **New repository**. Name it `ricechamps`, make it **Public**, and create it.
3. On the repository page, click **Add file**, then **Upload files**. Drag in every file from this folder (unzip it first, and upload the files, not the zip). Click **Commit changes**.
4. Go to **Settings**, then **Pages**. Under **Build and deployment**, set Source to **Deploy from a branch**, Branch to **main**, folder **/ (root)**, and Save.
5. Wait 1 to 2 minutes. The site will be at `https://ORGNAME.github.io/ricechamps/`. The Pages settings screen shows the exact link once it's ready.
6. Go to the organization's **People** tab and invite the other officers as **Owners**. Turn on two-factor authentication on your account.

## Editing text
1. Open the repository, click the file (for example `faq.html`), then click the pencil icon.
2. Change the words between tags, for example `<p>your text</p>`. Leave the `<` and `>` parts alone.
3. Click **Commit changes**. The site updates in about a minute.

Yellow highlighted text on the FAQ and Apply pages is a placeholder to replace.

## Changing colors or fonts
Edit the color values at the top of `style.css`, in the `:root` block. The change applies to every page.

## Connecting the application form
In `apply.html`, find the line `var FORM_URL="";` and this is where the form connection will go. Until it's connected, the Submit button shows a "preview only" notice and sends nothing.

## Adding a custom domain later
In **Settings**, then **Pages**, enter the domain under **Custom domain** and follow GitHub's DNS instructions. The site files don't need to change.
