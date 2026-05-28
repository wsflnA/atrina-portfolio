README
Website Overview

This website is a four-page personal portfolio consisting of:

index.html (Home) - Hero section, about section, and contact form
projects.html (Projects) - Project list, skills table, and images
creative.html (Creative Work) - Photography slideshow gallery
media.html (Media) - Video, audio, and social media content

Each page is connected through a consistent responsive navigation bar
located at the top of the page. All files are organized within a
parent folder structure.

========================================
File Structure
========================================

A2_zi373237

index.html
projects.html
creative.html
media.html
style.css
favicon.ico
code review.pdf

/images/
    profile.jpg
    workshop.jpg
    awslogo.jpg
    Rednote.jpg
    photo1.jpg
    photo2.jpg
    photo3.jpg
    photo4.jpg
    photo5.jpg
    photo6.jpg

/videos/
    intro.mp4

/audio/
    intro.mp3

All media assets are stored in child folders and accessed using
relative paths.

========================================
Relative Paths Explanation
========================================

Images:
Example: <img src="images/profile.jpg">
Purpose: Loads image from images folder relative to current HTML file.

Videos:
Example: <source src="videos/intro.mp4">
Purpose: Loads local video file from videos folder.

Audio:
Example: <source src="audio/intro.mp3">
Purpose: Loads local audio file from audio folder.

Stylesheet:
Example: <link rel="stylesheet" href="style.css">
Purpose: Loads shared CSS file from the same folder.

Navigation:
Example: <a href="projects.html">
Purpose: Links to another page in the same parent folder.

External Link:
Example: <a href="https://www.xiaohongshu.com/...">
Purpose: Links to an external website outside project directory.

========================================
Code Structure and Functional Components
========================================

1. Navigation Bar

Purpose:
Provides consistent navigation across all pages. On mobile screens
(under 600px), collapses into a "Menu" button that toggles the links.

Function: toggleMenu()
Input: None
Output: Shows or hides the navigation link list on mobile.
Dependent Structure: <nav>, <ul class="nav-links">, classList.toggle()

2. Colour Scheme Changer

Purpose:
Allows the user to switch between three colour schemes by clicking
buttons at the top of each page.

Function: setScheme(n)
Input: n (integer: 1, 2, or 3)
Output: Applies corresponding CSS class to <body> element.
Example: setScheme(2) applies class "scheme-2" to the body.
Dependent Structure: body.scheme-1 / scheme-2 / scheme-3 in style.css

3. Photo Slideshow

Purpose:
Displays six landscape photographs one at a time with navigation
arrows and a counter.

Function: changeSlide(direction)
Input: direction (1 for next, -1 for previous)
Output: Updates displayed image and counter text.
Example: changeSlide(1) advances to the next photo.
Dependent Structure: images array, current variable, #slide-img, #counter

4. Contact Form Validation

Purpose:
Validates the contact form before submission. Uses a conditional
to check whether all fields are filled.

Function: handleSubmit()
Input: None (reads form field values directly)
Output: Alert message. If any field is empty, shows error. If all
fields are filled, shows thank you message with user's name.
Example: If name field is empty, displays "Please fill in all
fields before sending."
Dependent Structure: input[type="text"], input[type="email"], textarea

5. Image Display

Purpose:
Displays visual content with responsive sizing.

Input: Image file located in images folder.
Output: Image rendered on webpage, scales to screen width.
Dependent Structure: <img> tag with src, alt attributes, and CSS
max-width rules.

6. Local Video Player

Purpose:
Displays embedded local video with controls.

Input: Video file located in videos folder.
Output: Video player with play, pause, and volume controls.
Dependent Structure: <video> and <source> elements.

7. External Video Embed

Purpose:
Embeds external Bilibili video using iframe.

Input: External URL with Bilibili embed format.
Output: Embedded video player within webpage.
Dependent Structure: <iframe> element.

8. Audio Player

Purpose:
Plays local audio file with controls.

Input: Audio file in audio folder.
Output: Audio player with play/pause functionality.
Dependent Structure: <audio> and <source> elements.

9. Skills Table

Purpose:
Displays technical and language skills in a structured format.

Input: Static content.
Output: Styled table with category, skill, and level columns.
Dependent Structure: <table class="skills-table">, <th>, <td>

10. Lists

Unordered List:
Used in projects.html to organize project descriptions.

Ordered List:
Used in media.html to present selected media highlights.

Nested List:
Used in projects.html to structure project details.

========================================
CSS Selectors
========================================

All selectors are located in style.css.

Universal Selector (*)
- Location: style.css line 1
- Purpose: Applies box-sizing, margin, and padding reset to all elements.

Multiple Selector (h1, h2, h3)
- Location: style.css line 7
- Purpose: Applies letter-spacing to all heading elements.

Child Selector (nav > ul > li)
- Location: style.css line 11
- Purpose: Targets direct list items inside the navigation bar.

Sibling Selector (h1 ~ p)
- Location: style.css line 15
- Purpose: Applies increased line-height to all paragraphs following an h1.

Adjacent Sibling Selector (h2 + p)
- Location: style.css line 19
- Purpose: Applies top margin to a paragraph immediately following an h2.

Attribute Selector (a[target="_blank"])
- Location: style.css line 23
- Purpose: Underlines links that open in a new tab.

Pseudo-element Selector (p::first-line)
- Location: style.css line 27
- Purpose: Bolds the first line of every paragraph.

========================================
Colour Schemes
========================================

Scheme 1 (Default): Black background (#000000), white text (#ffffff)
Scheme 2 (Dusk):    Dark grey background (#1c1c1c), light grey text (#d0d0d0)
Scheme 3 (Pale):    Off-white background (#f0eeeb), dark charcoal text (#2a2a2a)

========================================
Reuse from Previous Assignments
========================================

Biographical text, project descriptions, and media content have been
carried over and expanded from Assignment 1.
========================================
Asset List
========================================

images/profile.jpg      - Profile photo (personal)
images/workshop.jpg     - Web design workshop photo (personal)
images/awslogo.jpg      - AWS Cloud Club logo (personal)
images/Rednote.jpg      - Rednote page screenshot (personal)
images/photo1.jpg       - Landscape photography (personal)
images/photo2.jpg       - Landscape photography (personal)
images/photo3.jpg       - Landscape photography (personal)
images/photo4.jpg       - Landscape photography (personal)
images/photo5.jpg       - Landscape photography (personal)
images/photo6.jpg       - Landscape photography (personal)
videos/intro.mp4        - Dining Hall Challenge video (personal)
audio/intro.mp3         - Audio essay excerpt (personal)
favicon.ico             - Browser tab icon (personal)
code review.pdf         - Part 1 Code Review document

========================================
References
========================================

All photographs, videos, and audio are original works by the author.

MDN Web Docs. (2024). HTML: HyperText Markup Language. Mozilla.
  https://developer.mozilla.org/en-US/docs/Web/HTML

MDN Web Docs. (2024). CSS: Cascading Style Sheets. Mozilla.
  https://developer.mozilla.org/en-US/docs/Web/CSS

MDN Web Docs. (2024). JavaScript. Mozilla.
  https://developer.mozilla.org/en-US/docs/Web/JavaScript