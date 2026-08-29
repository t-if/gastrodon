# Gastrodon

![Gastrodon theme preview](https://github.com/user-attachments/assets/0d44e306-dabb-4392-a68d-8f7e3e911c06)

Gastrodon is a productivity-focused remix of [Chime](https://github.com/Bluemoondragon07/chime-theme) by Ha'ani Whitlock (Bluemoondragon07). It keeps Chime's rounded, colorful foundation while updating the workspace for current Obsidian releases and adding the note layouts, callouts, and small quality-of-life features I use every day.

The goal is convenience rather than minimal CSS: useful pieces of several snippets are built into the theme so they do not need to remain enabled separately.

## Installation

### BRAT

1. Install and enable the BRAT community plugin.
2. Choose **Add a beta theme** in BRAT.
3. Add `https://github.com/t-if/gastrodon`.
4. Select **Gastrodon** under **Settings → Appearance → Themes**.

The [Style Settings](https://github.com/mgmeyers/obsidian-style-settings) plugin is optional but strongly recommended. Gastrodon works without it, but Style Settings exposes the theme presets and most visual toggles described below.

### Public and personal files

- `theme-beta.css` is the public/BRAT variant. Optional convenience effects use conservative defaults.
- `theme.css` is my personal variant. It contains the same features, but several Style Settings options default to my preferences.

Neither variant requires the original Chime theme or the full Banner/MCL snippets. Gastrodon intentionally includes only the MCL features documented here: list grids/cards, floating callouts, blank callouts, and multi-column callouts.

## How Gastrodon differs from Chime

Gastrodon retains many of Chime's theme presets, rounded workspace, colorful headings, tag/link styles, blockquote styles, focus modes, Dataview cards, and rainbow folders, then changes or extends the following areas.

### Added or substantially changed

- Corrected side-panel boundaries and resize handles for current Obsidian layouts.
- Optional dimming of inactive Markdown panes.
- Optional hover-expanding left ribbon that preserves Gastrodon's fading buttons.
- Optional dark-mode dimming for images and PDFs.
- Optional bullet threading in Live Preview and threaded navigation in the Outline panel.
- Updated callout rendering for Obsidian 1.13+, four global callout styles, and hover-to-expand behavior.
- Legal, email, conversation, timeline, theorem, polaroid, blank, and multi-column callouts.
- Floating callouts with left/right placement and three width presets.
- Embedded-note cleanup, image alignment aliases, Mermaid sizing, and print-friendly styling.
- Banner and fading-banner layouts adapted from the Obsidian Banner Snippet.
- List grids and list-card grids adapted from MCL Multi Column.
- More checklist states, priority tags, ordered-list cycling, and tagged tree-view lists.
- Bases utilities, including compact cards, case-summary cards, Pokémon-box cards, and a vinyl-record music shelf.
- Current styling for Commander, Dataview, Bases, Calendar, and Kanban.

### Removed from Chime

- Cards Sidebar Layout and Classic Layout modes.
- Workspace background images and blur controls.
- The `wiki-page` and `novel` note classes.
- The Novelist and Notion theme presets.
- Old Page Gallery, Database Folder, CardBoard, and other unused/deprecated plugin rules.
- Chime's old increased-line-height and checkbox-style settings; Gastrodon uses its own list and checkbox system.

## Style Settings

Open **Settings → Style Settings → Gastrodon**. The BRAT build enables only the broadly useful defaults, including hidden workspace dividers, inactive-pane dimming, rainbow folder titles, the styled horizontal rule, smaller headings, bullet threading, and Outline threading. More intrusive effects remain opt-in.

| Section         | Available controls                                                                                                                                                                               |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Theme           | Macaroon, Ash, Ash (old), Anytype, Celestial, Chinchilla, Spring, Nord, Solarized, Gruvbox, Obsidian, and Light & Bright presets                                                                 |
| Layout          | Workspace dividers, inactive-pane dimming, line style, border width/roundness, file icons, rainbow folders, and active-tab color                                                                 |
| Editor          | Readable line width, horizontal-rule icon, blockquote style, callout style, hover-to-expand callouts, list threading, Outline threading, tag style, link style, seamless embeds, and code colors |
| Headings        | Default or two colorful palettes, smaller headings, and per-level weight, font variant, centering, and bottom borders                                                                            |
| Text            | Colored bold/italic text, underlined highlights, and optional Google Fonts (internet access is required to download them)                                                                        |
| Dark Mode Media | Independent image and PDF dimming with brighter hover states                                                                                                                                     |
| Focus Mode      | Fading buttons; hover-expanding ribbon; hidden tabs, titlebar, scrollbars, vault name; and Ultra Focus                                                                                        |

The four global callout styles are **Default**, **Bordered**, **Outlined**, and **Card**. The seven blockquote styles are **Chime**, **Simple Block**, **Obsidian**, **Minimalist**, **Card**, **Sleek**, and **Basic**.

## Note `cssclasses`

Add page-level classes in Properties:

```yaml
---
cssclasses:
  - width-1000
  - no-backlinks
---
```

Several Style Settings classes can also be applied to one note instead of the entire vault.

### General note classes

| Class                                                                        | Effect                                                               |
| ---------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `width-800`, `width-900`, `width-1000`, `width-1200`, `width-1600` | Override Readable Line Length for one note                           |
| `no-backlinks`                                                             | Hide the embedded backlinks/linked-mentions section                  |
| `no-count`                                                                 | Hide Dataview's result count                                         |
| `no-fold`                                                                  | Hide callout fold arrows                                             |
| `clean-embed`                                                              | Make embedded notes seamless and reveal their link controls on hover |
| `colorful-headings`, `colorful-headings-alt`                            | Apply either colorful heading palette                                |
| `h1-center` through `h6-center`                                          | Center an individual heading level                                   |
| `h1-bottom-border` through `h6-bottom-border`                            | Add a bottom rule to an individual heading level                     |
| `underlined-highlight`                                                     | Render highlights as underlined text                                 |

### Banners

Place a banner image near the top of a note and give it the `banner` alias:

```markdown
![[image.jpg|banner]]
```

Then add `banner` to the note's `cssclasses`. For the fading version, use both classes:

```yaml
---
cssclasses:
  - banner
  - banner-fade
---
```

The banner works in Live Preview and Reading view and becomes shorter in narrow panes.

### Bases classes

| Class           | Effect                                                                  |
| --------------- | ----------------------------------------------------------------------- |
| `no-head`     | Hide the toolbar/header of embedded Bases                               |
| `case-card`   | Clamp long Bases card text to a compact case-summary height             |
| `center-card` | Center Bases card titles                                                |
| `oneline`     | Use compact label/value rows and centered titles                        |
| `pokemonbox`  | Style a Bases card view like a Pokémon storage box                     |
| `musicshelf`  | Style a Bases card view like an album shelf with animated vinyl records |

The Pokémon and music styles are also applied automatically when the Bases view label contains `Pokémon` or `Music`.

### Dataview card classes

Use `cards` on a note containing a Dataview table to turn its rows into cards. Optional companion classes are:

- `cards-cols-1` through `cards-cols-8` for a fixed column count.
- `table-100` for full-width card/table spacing.
- `trim-cols` to allow wrapped cell content.

These classes require the Dataview community plugin and a Dataview table query.

### Aside element classes

`aside-left` and `aside-right` float an individual HTML element into the page margins in Reading view. They fade slightly until hovered and fall back to smaller floats when space is limited. These are element classes, not page-level `cssclasses`.

```HTML
<span class="aside-left">Text in left margin</span>
```

```HTML
<span class="aside-right">Text in right margin</span>
```

## Images

Image aliases can contain:

| Alias text | Effect                                                                    |
| ---------- | ------------------------------------------------------------------------- |
| `center` | Center the image                                                          |
| `right`  | Float the image right                                                     |
| `banner` | Use the image as a page banner when the note also has the`banner` class |

Examples: `![[image.png|center]]` and `![[image.png|right]]`.

## List layouts

### Tree view

Put `#tree-view` in a list to replace its normal bullets with collapsible threaded dots in Reading view:

```markdown
- Parent
  - Child
  - Child
- #tree-view
```

This is separate from the **Bullet Threading** Style Setting, which adds branch highlighting to ordinary nested lists in Live Preview.

### List grid

Put `#mcl/list-grid` in the same top-level list:

```markdown
- First column
  - Detail
- Second column
  - Detail
- #mcl/list-grid
```

### List cards

Use `#mcl/list-card` for bordered card tiles:

```markdown
- Card one
  - Supporting text
- Card two
  - Supporting text
- #mcl/list-card
```

The `#mcl/list-grid` and `#mcl/list-card` tags are intentionally hidden in Reading view but remain visible while editing.

## Callouts

### Custom callout types

| Type                                                                                                    | Purpose                                                                                        |
| ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `facts`, `posture`, `issue`, `rule`, `analysis`, `conclusion`, `concurrence`, `dissent` | Color-coded case briefing and legal analysis                                                   |
| `email`                                                                                               | Email/message layout; nested callouts become labeled rows                                      |
| `conversation`                                                                                        | Alternating chat bubbles                                                                       |
| `conversation-outline`                                                                                | Alternating outlined conversation rows                                                         |
| `conversation-minimalist`                                                                             | Frameless alternating conversation content                                                     |
| `timeline`                                                                                            | Vertical or horizontal timeline made from direct child blocks/callouts                         |
| `theorem`                                                                                             | Formal serif theorem box with italic content                                                   |
| `polaroid`                                                                                            | Square photo with a caption-like title; supports left/right floating                           |
| `multi-column`                                                                                        | Responsive container for nested callouts, quote blocks, lists, or paragraphs                   |
| `blank`                                                                                               | Fully expanded, frameless container; useful with Hover to Expand for content that merely fades |

#### Basic syntax

```markdown
> [!issue] Issue
> What legal question must be resolved?
```

### Blank callout

```markdown
> [!blank]
> This content has no visible callout frame or title.
```

When **Hover to Expand Callout** is enabled, blank callouts remain fully expanded and frameless; only their opacity changes.

### Multi-column callout

```markdown
> [!multi-column]
>
> > [!note] Column one
> > First column content.
>
> > [!warning] Column two
> > Second column content.
```

Columns wrap when the pane becomes too narrow.

### Floating callouts

Add a float and optional size to any callout's metadata:

```markdown
> [!note|float-right-small] A small float
> Text wraps around this callout in sufficiently wide panes.
```

Supported placements are `left`, `right`, `float-left`, and `float-right`. Append `-small`, `-medium`, or `-large` for widths of approximately 300px, 400px, or 600px. Floats become normal blocks in panes narrower than 500px.

### Callout metadata

Metadata follows the pipe in a callout header. Multiple values can be separated by spaces, for example `[!timeline|horizontal numbered purple]`.

| Metadata                                                                                                  | Effect                                                       |
| --------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| `gray`, `brown`, `red`, `orange`, `yellow`, `green`, `cyan`, `blue`, `purple`, `pink` | Override the callout color                                   |
| `no-bg`, `no-background`                                                                             | Remove the background                                        |
| `no-icon`                                                                                               | Hide the icon                                                |
| `no-title`                                                                                              | Hide the title row                                           |
| `blank`                                                                                                 | Strip the frame/title from any callout type                  |
| `wide`                                                                                                  | Expand a callout beyond Readable Line Length in Reading view |
| `left`, `right`, `float-left`, `float-right`                                                   | Float the callout                                            |
| `black-and-white`, `b-w`                                                                             | Grayscale images inside the callout                          |
| `horizontal`                                                                                            | Make a`timeline` horizontal                                |
| `numbered`                                                                                              | Number timeline points                                       |
| `skip`                                                                                                  | Do not number that nested timeline callout                   |
| `sep`                                                                                                   | Add a separator after a nested`email` row                  |

## Checkboxes and priority tags

Gastrodon supports the standard `- [ ]` and `- [x]` states plus:

| Marker | Meaning     | Marker | Meaning    |
| ------ | ----------- | ------ | ---------- |
| `/`  | Incomplete  | `-`  | Canceled   |
| `>`  | Forwarded   | `<`  | Scheduling |
| `?`  | Question    | `!`  | Important  |
| `*`  | Star        | `"`  | Quote      |
| `l`  | Location    | `b`  | Bookmark   |
| `i`  | Information | `I`  | Idea       |
| `S`  | Savings     | `p`  | Pros       |
| `c`  | Cons        | `f`  | Fire       |
| `k`  | Key         | `w`  | Win        |
| `u`  | Up          | `d`  | Down       |
| `R`  | Rule        |        |            |

Add `#p1`, `#p2`, or `#p3` to a task for high, medium, or low priority styling.

## Optional plugin styling

Gastrodon does not require these plugins, but includes targeted styling when they are installed:

- **Commander:** ribbon icon color fixes.
- **Dataview:** inline fields, hidden result counts, and card tables.
- **Bases:** compact embeds and the card classes documented above.
- **Calendar:** colors, navigation, week numbers, selected dates, and event dots.
- **Kanban:** lifted cards plus automatic styling for `#A`, `#B`, `#C`, `#rsvp`, `#show`, and `#productivity`. These layout tags are hidden on Kanban cards.

## Credits

Gastrodon is a remix of [Chime](https://github.com/Bluemoondragon07/chime-theme). Additional focused adaptations include:

- [MCL Multi Column](https://github.com/efemkay) by Faiz Khuzaimah/efemkay.
- [Obsidian Banner Snippet](https://github.com/HandaArchitect/obsidian-banner-snippet) by HandaArchitect.
- Callout metadata, email, timeline, conversation, list-tree, and aside ideas by [ElsaTam](https://elsatam.github.io/obsidian-fancy-a-story/).
- Dataview cards and many checkbox states from [Minimal](https://github.com/kepano/obsidian-minimal) by kepano.
- Priority checkboxes and theorem-callout work adapted from [r-u-s-h-i-k-e-s-h&#39;s snippet collection](https://github.com/r-u-s-h-i-k-e-s-h/Obsidian-CSS-Snippets).
- Rainbow folders originally by [Lithou](https://forum.obsidian.md/t/adding-color-to-obsidian-a-rainbow-of-possibility/12805/11).
- Image alignment adapted from [gautamneeraj&#39;s Obsidian Forum snippet](https://forum.obsidian.md/t/align-image/78050).
- Outline threading and dark-mode media dimming adapted from [Maple by subframe7536](https://github.com/subframe7536/obsidian-theme-maple).
- Hover-expanding ribbon behavior adapted from [Adrenaline by Spekulucius]().

See the comments in `theme-beta.css` for source-specific attribution and licensing notes.
