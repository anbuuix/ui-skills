# Ekko landing page

A standalone landing page for [ekkomd.com](https://www.ekkomd.com/). Open `index.html` in a browser; there is no build step.

## How it was made

Built with this repo's own process. Following `skills/ui-skills-root`, the CLI (`node bin/ui-skills.js`) was used to pick at most three skills for a new landing page:

1. **`nutlope/hallmark`** drives the design: theme, page shape, type scale, spacing, and its gates against generated-looking pages.
2. **`mengto/landing-page`** sets the structure: one offer, one primary action (Start free), proof next to the claim, and the action repeated at the close.
3. **`ibelick/baseline-ui`**, the repo's own skill, was used as the final check.

The current ekkomd.com look was not used as a reference. Only its facts were kept: copy, the testimonial, blog posts, offices and links.

### Hallmark decisions

- **Theme:** Console, graphite colourway. It was picked by hand from Hallmark's theme index, because the session could not run Hallmark's scripts. Its rule is that amber marks a person and cool blue marks the instrument. On this page, what the doctor and patient say is amber and what Ekko writes into the record is blue.
- **Shape:** Workbench. The product is the content, and every section shows a piece of the record instead of icon tiles.
- **Job:** sign up. The page has one primary action, Start free, in the nav, the hero and the close.
- **Sections:**
  1. Stage hero with the sample visit filling in live.
  2. A switcher with the five features, each shown on the record.
  3. A split showing mixed-language lines.
  4. A before-and-after comparison of a handwritten card against an Ekko note.
  5. The testimonial as a statement.
  6. Blog posts as rows.
  7. A closing band with the contact details.
  8. The footer.
- **Fonts:** Host Grotesk for reading, and Atkinson Hyperlegible Mono only for measured things (times, vitals, doses). Noto Sans Tamil and Devanagari are fallbacks for the Indian-language lines.
- **Gates checked by hand** (Hallmark's `sloplint` was not run):
  - No em dashes, dot-joined meta text, eyebrows or tracked capital labels.
  - Every colour is a token, and spacing comes from the scale.
  - Visible focus rings, and content that is complete with scripts off.
  - Reduced-motion fallbacks.
  - No sideways scroll from 390px to 1920px.
  - Headline, line and action all visible at 1280×800.

### Where the skills disagree

`baseline-ui` says never to change letter spacing, never to use custom easing, and never to add animation unless asked. Hallmark's Console theme sets display tracking and its own ease-out curve. The hero also plays the sample visit once, in under five seconds. Hallmark's theme rules won on those three points. Hover transitions are 180ms, which keeps them inside baseline-ui's 200ms limit.

## Handoff

- **Product samples:** the hero visit, the switcher states, the language panel and the comparison table are built in HTML inside `data-slot` elements. Replace them with screenshots of the real app once there is a sample account with no patient data.
- **Clinical sample content:** the patient, vitals and amlodipine plan are illustrative. Have a clinician review them before this goes live.
- **Sign-up and log-in links:** these point at `auth.ekkomd.com/u/signup/identifier` and `/u/login/identifier` without the `state` parameter the live site adds. Confirm the right entry URLs.
- **Testimonial:** shortened from the version on the live site. Confirm Dr. Arjun Patel is happy with this wording.
