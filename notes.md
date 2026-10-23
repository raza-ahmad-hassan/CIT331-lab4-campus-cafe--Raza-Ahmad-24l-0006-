# HTTP observations (Lab 4, Task 1)

| Question | My answer |
|----------|-----------|
| Request method for index.html | GET |
| Status code with Disable cache ticked | 304 Not Modified |
| Status code on a normal reload | 304 Not Modified |
| Status code for /nothing-here.html | 404 Not Found |
| Value of the Content-Type response header | text/html |
| Remote Address (IP and port) | 127.0.0.1:5500 |
| Protocol in the address bar (http or https) | http |

## Why is this address http and not https?

Localhost traffic stays on my own computer, so it does not travel across an external network. HTTPS protection is more important when data travels across a network.

## Task 3 — Forms, Validation and localStorage

### HTML Validation Tests
- Empty name: Browser validation worked.
- Name shorter than 3 characters: Validation worked.
- Invalid mobile number: Validation worked.
- Valid mobile number: Accepted.
- Invalid quantity: Validation worked.
- Pickup time outside the allowed range: Validation worked.
- No item selected: Validation worked.

### localStorage Tests
- Orders remained saved after refreshing the page.
- Orders remained saved after navigating to another page.
- Clear all orders removed the saved orders.
- Damaged localStorage data did not crash the page.
- HTML-like input was displayed as plain text.

## Specificity experiment

The `#main p` selector has higher specificity than `.hero p`, so it overrides the hero paragraph color. The `main p` selector has lower specificity than `.hero p`, so the hero paragraph stays white.

## Selectors I used

| Selector kind | Example from my CSS |
|---|---|
| Element | `body` |
| Class | `.card` |
| ID | `#main` |
| Grouping | `h1, h2, h3` |
| Descendant | `.site-footer p` |
| Child | `form > fieldset` |
| Adjacent sibling | `h1 + p` |
| Compound | `a.active` |
| Attribute | `a[href^="http"]` |
| Pseudo-class | `a:hover` |
| Pseudo-element | `a[href^="http"]::after` |

## Bug log (Lab 4, Task 6)

| # | What was wrong (file and line) | Which tool showed it | My fix |
|---|---|---|---|
| 1 | `debug/bugs.html` linked to `style.css`, but the actual CSS file was `bugs.css`. | Network tab | Changed `style.css` to `bugs.css`. |
| 2 | The navigation links were inside a `<div>` instead of a `<nav>` element. | Accessibility tree | Replaced `<div class="menu">` with `<nav class="menu">`. |
| 3 | The heading jumped from `<h1>` to `<h4>`, skipping heading levels. | Accessibility tree | Changed `<h4>` to `<h2>`. |
| 4 | The logo image had no `alt` attribute. | Lighthouse accessibility audit | Added `alt="Campus Cafe logo"` to the image. |
| 5 | The `<html>` element had no language attribute. | Lighthouse accessibility audit | Added `lang="en"` to the `<html>` element. |
| 6 | The label used `for="mail"`, but the input ID was `email`. | W3C validator / Lighthouse | Changed the label to `for="email"`. |
| 7 | The CSS used `colour` instead of the correct property `color`. | Styles pane | Changed `colour` to `color`. |
| 8 | The `.btn:hover` background declaration was missing a semicolon. | Styles pane | Added a semicolon after `background: #0b1f3a`. |
| 9 | The CSS selector `.notes` did not match the HTML class `.note`. | Styles pane | Changed `.notes` to `.note`. |
| 10 | The note text color `#999999` had insufficient contrast against the white background. | Lighthouse accessibility audit | Changed the text color to a darker color, such as `#6b5a4e`. |

