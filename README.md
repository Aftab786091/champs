# Rice CHAMPs website

Plain HTML, CSS, and one logo file. No build step. Pages link to each other with relative links, so the folder works on any host.

## Files
- `index.html` Home
- `program.html` Program
- `team.html` Team (officer names, photos, and contact are placeholders in [brackets])
- `faq.html` FAQ (premed policy and missed-deadline answers are placeholders; TIRR Memorial Hermann details are general until the program is finalized)
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
`apply.html` posts to a Google Form. The form ID and entry numbers are in the `E` block at the top of the script. To find an entry number, open the form's pre-filled link ("Get pre-filled link") and look for `entry.NNNNNNN` next to each question.

The volunteer questions use these entries: `program` (which program), `cmhOk` and `tirrOk` (Yes/No: can you commit to the weekly shifts), `tirrWhy` (the TIRR "stayed patient and supportive" answer), and the existing `supported` entry for the CMH answer. Shifts are not collected; students only confirm they can commit. If a question is ever recreated in the form, update its entry number in `E`.

Option text in multiple-choice and checkbox questions must match the site exactly, or Google will reject the response:
- **Roles** (checkboxes): `Pediatric Volunteer`, `Education Committee`, `Outreach Committee`, `Socials Committee`. The volunteer option keeps the original text `Pediatric Volunteer`.
- **Program** (multiple choice): `CMH Only`, `TIRR MH Only`, `Both, TIRR MH First Choice`, `Both, CMH First Choice`.

The CMH "helped someone feel supported" answer still goes to the existing `supported` entry. The commitment checkboxes are checked on the page only and are not sent to the form.

## Adding a custom domain later
In **Settings**, then **Pages**, enter the domain under **Custom domain** and follow GitHub's DNS instructions. The site files don't need to change.
