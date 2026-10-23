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

