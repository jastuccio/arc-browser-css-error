Update:

I dug into this issue again tonight.  I removed most of the CSS iin the simplify-css branch.

Arc is incorrectly translating 64rem​ in the media query to 1280px.  Safari and Chrome correctly set 64rem to 1204px.

```css
/* Desktop - 1024px */
@media only screen and (min-width: 1023px) {
  body {
    background: var(--secondary);
  }
}
```
--------------------------

Between 1024px and 1279px width the navbar loses styling in my Arc browser. I do not see this bug happening in Chrome or Safari. Arc v1.31.0 (46662) Chromium Engine Version 122.0.6261.57

Bug video: https://imgur.com/a/8t3ygJp