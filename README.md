# Prompt I gave to ChatGPT
I am building a responsive portfolio-style webpage using only HTML and CSS.
I need help thinking through how to structure responsive behavior for three major parts:

The header navigation
The hero section with a text block and KPI card
The project grid gallery

Please explain how I should approach implementing responsive breakpoints and layout behavior at a high level without writing any code.

# What I accepted from the response
1. The suggestion to design desktop layout first before mobile adjustments.
This helped me visually confirm spacing and alignment before worrying about stacking. It reduced debugging time later.

2. The recommendation to group related elements into layout wrappers.
Using wrapper containers for the header, hero section, and grid allowed me to control spacing without affecting content styling.

# What I rejected
The AI suggested adding extra decorative animations for mobile interactions. I rejected this because the assignment emphasized clean layout structure rather than visual effects. Adding animations could also distract from evaluating responsive layout behavior.

# Debug Prompt

## One bug I hit
My navigation menu was not centering properly on mobile devices.
Instead of appearing stacked and centered, the links stayed aligned to the left side of the screen.

## Exact CSS snippet
My CSS for the navigation was:

.nav-list {
  display: flex;
  flex-direction: column;
  
## Most important part of AI response
The AI said:

Flexbox controls layout direction, but you must also explicitly control alignment using align-items: center when working with column layouts.

## What I changed
I changed the CSS snippet to:

@media (max-width: 600px) {
  .nav-list {
    flex-direction: column;
    align-items: center;
  }

  .nav-list li {
    margin: 8px 0;
  }
}

# Viewport sizes I tested
360px — Small mobile device

480px — Large phone

768px — Tablet portrait

1024px — Small desktop

1366px — Standard laptop display

# What I checked visually
Header Navigation: verified menu stacked vertically on mobile; confirmed links were horizontally centered

Hero Section: verified text and KPI card stayed horizontally aligned on desktop; confirmed vertical stacking on mobile.

Grid Section: 4 columns on desktop, 2 columns on tablet, 1 column on mobile

Buttons: onfirmed hover color change worked without shifting layout.
