# Assignment 2 · Task 3 screenshots

Alimzhan Almukhambetov · IT-2510

Source: `task3.html`, `task3.css`, and the shared Bookbound theme in `task2.css`.
All images below are actual Chrome screenshots. CSS images show excerpts with the original source line numbers.

| Layout | Report view at 1440 px | All twelve notes | Key CSS |
| --- | --- | --- | --- |
| Grid | [First eight notes](result-grid.png) | [Full page](full-grid.png) | [Grid and item rules](css-grid.png) |
| List | [First five notes](result-list.png) | [Full page](full-list.png) | [Grid, image, text and date rules](css-list.png) |
| Magazine | [Lead and four surrounding notes](result-magazine.png) | [Full page](full-magazine.png) | [Grid and lead span rules](css-magazine.png) |

| Layout at 390 px | Viewport | Full page |
| --- | --- | --- |
| Grid | [Mobile grid](mobile-grid.png) | [All notes](mobile-full-grid.png) |
| List | [Mobile list](mobile-list.png) | [All notes](mobile-full-list.png) |
| Magazine | [Mobile magazine](mobile-magazine.png) | [All notes](mobile-full-magazine.png) |

## Captions and explanation for the report

- **Grid:** Grid uses `auto-fit` and `minmax()` to adjust the number of columns, while Flexbox arranges each card's contents vertically.
- **List:** Grid creates one column of items, while Flexbox places each image, text block and date in a row with the date at the right edge.
- **Magazine:** Grid gives the lead item a two-column, two-row span, while Flexbox arranges the contents of the lead and surrounding articles.

I kept all twelve articles in one container and changed only its mode class: `view-grid`, `view-list`, or `view-magazine`. The grid track minimum can shrink with the available space, so the cards fit a narrow screen without media queries. In magazine mode, the minimum track size always allows two columns, which keeps the lead item's span inside the container. In list mode, the text flexes between the image and date; `min-inline-size: 0` and word wrapping prevent long content from pushing the row wider than the screen.

The visible preview controls are native radios styled with CSS. No radio is initially checked, so the source class determines the initial view. During the screenshots, only the container class was changed; the twelve article elements stayed identical.

The journal shares Bookbound's colors, typography, spacing and header with Task 2. All cover illustrations are original local SVGs. The pages contain no JavaScript, Bootstrap, or media queries.

## Verification

All three modes passed browser checks at 320, 375, 390, 500, 768, 1024, 1440 and 1920 px, including long titles and unbroken words. Checks confirmed loaded images, unchanged article markup, no horizontal overflow, the list's image/text/date order, the lead's two-column/two-row span, all nine source-class/preview combinations, and keyboard operation of the controls.
