# Frontend Mentor - Bento Grid Solution (SBA 3: Design and Development)

This is my solution to the [Bento grid challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/bento-grid-RMydElrlOj), built with HTML and Tailwind CSS (used in place of Bootstrap).

## Overview

### The challenge

Build a responsive bento grid of 8 feature tiles that matches the provided design as closely as possible. Users should see the best layout for their screen size.

### Links

- Live site: https://mrg-repo.github.io/SBA3-Design-Development/
- Repository: https://github.com/mrg-repo/SBA3-Design-Development

## My process

### Built with

- Semantic HTML5 (`main`, `article`, one `h1`, `h2` tile headings)
- Tailwind CSS for colors, spacing, typography, flexbox, and the responsive grid
- A small `style.css` for the DM Sans font and the desktop grid layout

### Approach

- Before building, I researched which parts of the design were better handled with Tailwind and which with plain CSS, so I could plan my approach.
- I used `tailwind.config` to turn the style guide's colors and the DM Sans font into short class names (for example, `bg-purple-500` instead of `bg-[hsl(256,67%,59%)]` on every tile). Defining them once saved time.
- I styled the page tile by tile, setting each tile up for mobile, tablet, and desktop as I went, which made the process easier.
- I think of Tailwind as styling that builds up by screen size. A class with no prefix applies to every screen. An `md:` class takes over from 768px and up, while anything smaller keeps the original style. An `xl:` class takes over again from 1280px and up.

### Challenges and how I addressed them

- **Splitting the grid between Tailwind and CSS.** I used Tailwind to build the grid itself: turning it on, setting 1, 2, or 4 columns by screen size, and controlling the gaps and widths. The one part I moved to CSS was placing each tile in its exact spot on the desktop layout. In Tailwind, that would have meant 3–4 extra position classes on each of the 8 tiles. In CSS, a `grid-template-areas` map draws the same layout in a few readable lines that look like the design.
- **A gap at tablet size.** The design only included mobile and desktop. While testing screen sizes, I noticed a visual gap: the layout jumped from one column straight to the 4-column desktop grid. I added Tailwind's `md:` breakpoint with a 2-column layout, which made the flow between sizes smoother.

## Author

- GitHub - [mrg-repo](https://github.com/mrg-repo)

## Acknowledgments

Challenge and design by [Frontend Mentor](https://www.frontendmentor.io).