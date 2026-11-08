# Ankita & Akash — the invitation

A sealed digital wedding invitation: guests tap the wax seal, the envelope opens and the card unfolds.
Plain HTML, no build step, hosted on GitHub Pages.

## Addresses

Once GitHub Pages is on (Settings → Pages → Deploy from a branch → `main`, folder `/ (root)`):

| Who        | Page                    | Address                                                   |
|------------|-------------------------|-----------------------------------------------------------|
| Guests     | Invitation, English     | https://amitdhakite.github.io/Invitation/                 |
| Guests     | Invitation, Hindi       | https://amitdhakite.github.io/Invitation/hi.html          |
| Organizers | Organizers' page        | https://amitdhakite.github.io/Invitation/organizers/      |

Personal links add the guest's name: `…/Invitation/?to=Priya%20Sharma` (English) or
`…/Invitation/hi.html?to=Priya%20Sharma` (Hindi). Make them for the whole list on the
organizers' page → **Guest links**.

## What's where

```
index.html          the invitation (English, and Hindi with ?lang=hi)
hi.html             the Hindi address: a Hindi link preview, then on to the invitation in Hindi
organizers/
  index.html        the organizers' page: start here
  links.html        paste guest names → a personal link each, with copy buttons
```

Design drafts (colour palettes, seal emblems) live in a `drafts/` folder on the organizers'
computer only. Don't upload it: when dragging files onto GitHub, `.gitignore` doesn't apply.

Nothing on the invitation links to `organizers/`, and every page asks search engines not to list it.
It isn't secret, though: this repository is public, so anyone who knows or finds the address can open it.
Nothing private lives there: names typed into Guest links stay in that browser.

## Editing

- **Words, date, venue, reply address:** the `INVITE` block in `index.html` (marked *EDIT EVERYTHING HERE*).
  The Hindi words are in `INVITE_HI` just below it.
- **Link previews** (the title WhatsApp shows): the `og:` tags at the top of `index.html` and `hi.html`.
  Previews can't run code, so keep these in step with the wording by hand.
- **Colours:** the twelve palette lines at the top of the `<style>` in `index.html` (alternatives in `drafts/palettes.html`).

The venue, date and reply address in this repository are visible to anyone who opens it on GitHub.
