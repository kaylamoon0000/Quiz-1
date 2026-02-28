# Name: Kayla Moon
# Tools used: ChatGPT, Colab, Browser

# Q1:

## Key finding (2-4 sentences): 

The chart demonstrates a strong positive linear correlation between study hours and exam scores. As study time increases from 2 to 10 hours, exam scores rise consistently from 55 to 90 points. This suggests that for this group of students, academic performance is highly predictable based on the time invested in preparation.

## Outlier: 

There is a slight outlier at the 4-hour mark, where one student achieved a score of approximately 72, which is higher than the trendline's predicted value for that duration.

# Q2:

What was broken: The navigation menu was not centering properly on mobile devices; despite being stacked in a column, the links remained stuck to the left side of the screen.

What I changed: I updated the CSS media query for the .nav-list to include align-items: center and added vertical margins to the list items to prevent the links from crowding each other.

# Q3:
## Prompt 1 (plan, no code):

"I am creating a responsive webpage using only HTML and CSS. I want help deciding how to organize responsiveness for navigation, a hero section, and a project gallery. Specifically, explain how I should think about: When elements should resize versus stack, how to choose breakpoint ranges, and how to keep spacing consistent across screen sizes. Provide a conceptual implementation strategy without showing code."

## Response snippet:

"Design mobile responsiveness around content readability... Prioritize stacking elements on small screens rather than just shrinking them to maintain touch targets and legibility."

## Accepted:

Prioritizing content readability by stacking elements on mobile.

Using standard device category breakpoints (mobile, tablet, desktop) for a predictable layout.

## Rejected:

Complex multi-layer breakpoints for specific device models (rejected because it makes debugging and maintenance unnecessarily difficult).

## Prompt 2 (debug):

"My navigation menu was not centering properly on mobile devices. Instead of appearing stacked and centered, the links stayed aligned to the left side of the screen. My CSS for the navigation was: .nav-list { display: flex; flex-direction: column; } but I did not have any alignment properties."

## Response snippet:

"Flexbox controls layout direction, but you must also explicitly control alignment using align-items: center when working with column layouts."

## What I verified:

viewport sizes tested: 360px (Small mobile), 480px (Large phone), 768px (Tablet), 1024px (Small desktop), 1366px (Laptop).

what I checked visually: Verified the header navigation stacked and centered on mobile; confirmed the hero section and grid layout transitioned correctly from 4 columns (desktop) to 2 (tablet) and 1 (mobile).

# Q4:

Chart caption: This scatter plot illustrates a strong positive linear relationship where exam scores increase consistently as students spend more hours studying.

Decision based on chart: Based on this data, I would decide to recommend a minimum of 8 study hours for students aiming to achieve a score of 85 or higher.


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

Header Navigation: verified menu stacked vertically on mobile; confirmed horizontal centering

Hero Section: verified text and KPI card stayed horizontally aligned on desktop; confirmed vertical stacking on mobile.

Grid Section: 4 columns on desktop, 2 columns on tablet, 1 column on mobile

Buttons: confirmed hover color change worked without shifting layout.
