# Venn board

A growing Venn diagram for planning a project. Add cards to the three circles (Audience, Product / concept, Process), their overlaps (Stakeholders, Relevance, Quality) and the centre (Impact). Each circle grows as it fills, and every card can hold as much context as you need.

Built for the Context Quest course of the Creative Business graduation track at BUas, but it works for any project.

## Using it

- Tap a zone name in the diagram, or **Add card** in the list, to create a card.
- Tap a card title to open it and write your context.
- Rename any zone by tapping its name in the list.
- **Zoom** by scrolling or pinching, by double-clicking an empty spot, or with the + and − buttons and keys. **Move around** by dragging the background, or with the arrow keys when the diagram is selected. From 160% the cards open up to show the start of their description, and from 260% they show more. **Fit** (or 0) shows the whole diagram again.
- **Drag a card** to place it exactly where you want. Drop it in another zone to move it there. It keeps its spot, and moves to the nearest free space if it would cover something.

## How saving works

There is no server and no account. Everything stays in your own browser.

- Your board saves automatically while you type, and immediately when you close or leave the tab.
- It survives closing the browser, restarting, and turning off your device.
- **Save** (or Ctrl/Cmd + S) saves right away and shows the time.
- **Versions** keeps named snapshots you can restore later.

Your board is lost if you clear your browser data (cookies and site data) for this site, or if you use a private or incognito window. A board made in one browser also won't appear in another browser or on another device. On iPhone and iPad, Safari can delete data from sites you haven't opened for about 7 days. Adding the page to your Home Screen prevents that.

**Download a backup regularly.** Go to **Export / import**, then **Download backup**. The .json file holds your board and all versions, and **Load backup** brings it back on any device.

## Word export and import

**Export as Word** creates a .docx file:

- Title: your project title
- Heading 1: each part of the diagram
- Heading 2: each card
- Normal text: the card's description

Word's navigation pane shows this as a table of contents.

**Import from Word** reads the same structure back in, including documents you've edited in Word. Add a card by adding a Heading 2 under the right Heading 1. Headings that don't match a zone are skipped, and the page tells you which ones. Before any import, your current board is saved as a version, so you can undo it.

## Claude ILO Check

The page has no server, so it cannot call Claude itself and never asks for an API key. Instead it copies ready-made prompts that you paste into a chat at claude.ai:

- **Claude ILO Check** (top bar) asks Claude whether the whole diagram reads as one line of thinking, measured against ILOs 3.13, 3.10 and 3.02.
- **Copy tighten prompt** (inside a card) asks Claude to make your own text more concise, without adding anything.
- **Copy gap check prompt** (inside a card) asks which points are missing for that zone's ILO, phrased as questions.

## Time tracker

The timer in the top bar records how long you spend **writing** (typing, plus 8 seconds after your last keystroke) and **thinking** (on the page and active, but not typing). It stops after 5 minutes with no activity and whenever the tab is in the background. Tap it for daily totals, pause, reset, and a time log you can copy. The time log is included in your full backup.

## Light and dark mode

Use the sun or moon button to switch. Dark is the default, and your choice is remembered.

## Help

The **?** button, or the ? key, explains every button and what each zone means.

## Accessibility

The page is built to meet WCAG 2.2 level AA in both light and dark mode:

- All text meets at least 4.5:1 contrast, including zone names on top of the tinted circles. Field borders and focus outlines meet 3:1.
- Everything works with a keyboard. Pop-up panels keep focus inside while open, close with Esc, and return focus to where you were.
- Buttons and card titles are at least 24 by 24 pixels, and the layout works down to 320 pixels wide without sideways scrolling.
- When you pan the diagram, parts of it can slide under the top bar or card panel. Every action in the diagram is also available through a full-size button in the card panel (Add card, and each card in the list), which is WCAG 2.5.8's "equivalent" exception. Cards you reach with the keyboard are moved into view automatically.
- Zooming has button and keyboard alternatives to pinching and dragging, and animations respect the reduced motion setting.

It was checked with axe-core and by calculating contrast for every colour pair. Automated tools can't catch everything, so testing with a real screen reader is still worthwhile.

## Privacy

Your cards never leave your device. The only outside request is for the Instrument Sans font from Google Fonts. To avoid that request, delete the three font `<link>` lines in `index.html`. The page then falls back to your system font.

## Publishing your own copy on GitHub Pages

1. Create a public repository and upload `index.html` and `README.md`.
2. Go to **Settings**, then **Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, pick `main` and `/ (root)`, and save.
4. After a minute or two, the site is live at `https://<your-username>.github.io/<repository-name>/`.

Saved boards belong to the exact web address. If you rename the repository or move the site, download a backup first and load it at the new address.
