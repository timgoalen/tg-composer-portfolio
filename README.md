# Tim Goalen - Composer Website

![Image of the website on multiple devices](documentation/responsive-site-preview.png)

[View the live project here](https://timgoalen.github.io/tg-composer-portfolio)

**TIM GOALEN *composer*** is a portfolio website for myself that showcases my work as a TV composer. The goal of this website is to provide a place where:
1. TV professionals (directors, producers and production managers) can find my credits, listen to my work and easily contact me.
2. Audience members can listen to music from programmes that they’ve seen and get in touch.

## Design
The design is based on an original prototype that I previously built using Squarespace.

[View the prototype Squarespace site here](https://www.timgoalen.com)

Aims for improvements on the Squarespace version include:
- improving performance & accessibility
- increasing the ease of implementing future custom features
- reducing yearly subscription cost

The main design updates include:
- simplifying the site from a multi-page to a single-page design
- omitting the separate landing page, improving UX by taking the user directly to content
- featuring selected credits - rather than comprehensive credits - in the Credits and Listen sections
- improving the colour scheme and typography
- improving feedback from user interactions, such as:
    - hover effects on menu items and input fields
    - transition effects on page load and when navigation scrolls to a section

The site was built with a **mobile-first** approach, using responsive units (`%`, `vh` and `vw`) where possible, to keep media queries to a minimum.

### Colour Scheme

The site has a contemporary minimalist aesthetic, based on a monochrome colour palette of white and black, with red and blue accent colours being used sparingly.

![Image of the colour palette](documentation/colour-palette.png)

### Typography
The site uses a single font - 'Poppins' - with the browser-default sans serif as a fallback in case the main font fails to load correctly. Poppins is a contemporary font that fit the minimalist aesthetic by it by it's design being based on pure geometry.

The oversized section titles use the thin 100-weight version of the font, with a responsive font-size of
`calc(4rem + 0.5vw)`.

Similar responsive font-sizes are also used for the logo, navbar links and 'About' section paragraph text.

Google Fonts was used to import the font at the top of the linked CSS file.

### Imagery

Site imagery consists of a profile headshot at the top of the page and the project promotional images in the 'Credits' section.

## Features

### Navigation Bar
![Image of the navigation bar](documentation/desktop-navbar.png)

- A fixed navigation bar is available on every page. 
- Clicking a link takes the user to the desired page section with a smooth-scroll effect, and triggers an opacity transition in the selected section, via a `:target` pseudo-class selector.
- The text turns blue as the cursor hovers over it, and remains blue after being clicked to indicate the users current position within the page.

### Mobile Navigation Menu
![Image of the mobile navigation menu](documentation/mobile-nav-menu.png)

- On mobile screens the navigation is displayed as an expandable menu via a hamburger icon.
- Once a destination is clicked the menu collapses.

### About
![Image of the about section](documentation/about-section.png)

- Displayed as one column on mobile screens and two columns on tablet screens and larger.
- Features a headshot and two paragraphs detailing work highlights.

### Listen
![Image of the listen section](documentation/listen-section.png)

- A seven-track audio showreel, made with HTML `<audio>` elements.
- JavaScript is used to pause the currently playing audio element if another is played, which is crucial for good UX.

### Credits
![Image of the credits section](documentation/credits-section.png)

- List of selected credits, with official photos, programme title, production company, runtime and broadcaster information.
- Single-column layout on mobile devices and two columns on desktop screens.
### Contact & Footer
![Image of the contact section with footer](documentation/contact-section.png)

- Includes a contact form, with input validation on all fields.
- The footer includes links to my Spotify, Twitter and IMDb pages.

### Message Received Page
![Image of the message received page](documentation/message-received-page.png)

- The user is taken to this Message Received page after successfully submitting the contact form. They offered a new 'Home' button to return home, as well as access to the nav bar and footer.

### 404 Error Page
![Image of the 404 error page](documentation/error-404-page.png)

- A custom page if the user tries to navigate to a page URL that doesn't exist or can't be found within the site.

## Future Implementations

- A custom audio player, built with JavaScript, with the ability to not display controls such as 'download', 'playback speed', 'forward/backward skip'; and design improvements.
- Connect the form submit information to an email account, using EmailJS or similar.
- Improve the hamburger navigation menu, with opening & closing transitions.
- Sections that take up 100% of the viewport height, with animation effects on scroll.
- Link the deployed site with the timgoalen.com domain.

## Technologies Used

- Languages Used:
    - [HTML](https://en.wikipedia.org/wiki/HTML5)
    - [CSS](https://en.wikipedia.org/wiki/Cascading_Style_Sheets)
    - [JavaScript](https://en.wikipedia.org/wiki/JavaScript)
- [Visual Studio Code](https://code.visualstudio.com/) - as the code editor.
- [Git](https://git-scm.com/) - for version control, using the Gitpod IDE.
- [GitHub](https://github.com/) - for storing the project.
- [Chrome Developer Tools](https://developer.chrome.com/docs/devtools/) - to troubleshoot code.
- [Google Fonts](https://fonts.google.com/) - used to import the 'Poppins' font.
- [Font Awesome](https://fontawesome.com/) - for the social media icons in the footer and the award icons in the 'Credits' section.
- [Favicon.io](https://favicon.io/) - to create the favicons.
- [Birme](https://www.birme.net/) - to convert the images into WebP format.
- [TinyPNG](https://tinypng.com/) - to compress the images.
- [Am I Responsive](https://ui.dev/amiresponsive) - to create the responsive demo image at the top of the readme.
- [Autoprefixer](https://autoprefixer.github.io/) - to add vendor prefixes. 
- [PageSpeed Insights](https://pagespeed.web.dev/) - for automated testing of performance, accessibility, best practices and SEO.
- [WebAIM WAVE](https://wave.webaim.org/) - for automated testing of accessibility.
- [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/) - to check colour contrast accessibility.
- [Eightshapes Contrast Grid](https://contrast-grid.eightshapes.com/) - to visualise the contrast accessibility of the whole site colour palette. 
- [W3C Markup Validator](https://validator.w3.org) - to test the HTML code.
- [W3C CSS Validator](https://jigsaw.w3.org/css-validator) - to test the CSS code.
- [JSHint](https://jshint.com/) - to test the JavaScript code.

## Testing

Syntax errors were tested for with [W3C Markup Validator](https://validator.w3.org) and [W3C CSS Validator](https://jigsaw.w3.org/css-validator). No errors were found in the published version of the site.

Improvements following initial testing:
- After the first W3C markup validator test, the `controlslist` attribute on the `<audio>` elements were removed. Being an experimental attribute it failed the validator. It had been included for the `nodownload` and `noplaybackrate` values, which disable the controls for downloading the audio file and changing the playback speed. In future I will build a custom audio player for the site using JavaScript, to include this functionality.
- Correctly nesting the footer within the `<body>` element in the 'message-received.html' and '404.html' pages.

### PageSpeed Insights

The [PageSpeed Insights](https://pagespeed.web.dev/) results for the published site are - 

#### Desktop:
![PageSpeed Insights ???](documentation/pagespeedinsights-index-desktop.png)

#### Mobile:
![PageSpeed Insights ???](documentation/pagespeedinsights-index-mobile.png)

Which is a large improvement on the prototype Squarespace site:
<details><summary>Desktop</summary>
<img src="documentation/pagespeedinsights-squarespace-desktop.png">
</details>
<details><summary>Mobile</summary>
<img src="documentation/pagespeedinsights-squarespace-mobile.png">
</details>

Changes made following initial testing:
- Resizing images to 150% of their max displayed size.
- Serving images in WebP format, with a JPEG as a fallback for browsers that don't support WebP, by nesting `<source>` elements within the `<picture>` element.
- Adding explicit `width` and `height` values to all images, to reduce layout shift as the browser loads the image.
- `loading="lazy"` was tested on the Credits images to increase performance, but was removed after no performance increase was measured.

- Insufficient contrast was found in some of the originally chosen red and blue text colours.

Original colours:
![Image of the original colour palette](documentation/eightshapesgrid-original-colours.png)

After using [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/) the red and blue colours were updated to slightly darker shade, to improve contrast and eligibility:

![Image of the WebAIM Contrast Checker for the blue colour](documentation/webaim-contrast-checker.png)

Updated colours:

![Image of the updated colour palette](documentation/eightshapesgrid-updated-colours.png)

### WebAIM WAVE
Site accessibility was checked with [WebAIM WAVE](https://wave.webaim.org/). There are no errors on the published site.

![Image of WebAIM WAVE results](documentation/index-webaim-wave-results.png)
![Image of WebAIM WAVE alerts](documentation/index-webaim-wave-alerts.png)

After the initial test, an `<h1>` tag was used to nest the site logo, after the results showed the alert "missing first level heading".

All other HTML pages were tested, with no errors present.

### Devices & Browsers Used for Manual Testing
- iPhone SE (2020)
    - Safari (v16.1)
    - Chrome (v112)
- iPad (6th Generation)
    - Chrome (v111)
    - Safari (v15)
- Mac Pro (Mid 2012)
    - Chrome (v112)
    - Safari (v12.1.2)
    - Firefox (v112.0)
- Dell Chromebook 3120
    - Chrome (v103)

### Manual Testing of User Actions
| Feature | Action | Expected Behaviour | Pass/fail |
|---|---|---|---|
| Navbar | Click on logo | Navigates back to the top of the page | PASS |
| Navbar | Click on "About" | Scrolls to the "About" section | PASS |
| Navbar | Click on "Listen" | Scrolls to the "Listen" section | PASS |
| Navbar | Click on "Credits" | Scrolls to the "Credits" section | PASS |
| Navbar | Click on "Contact" | Scrolls to the "Contact" section | PASS |
| Navbar | Click on any link | Opacity transition on target section | PASS |
| Mobile menu | Click on hamburger icon | Shows navigation menu and icon changes to "X" | PASS |
| Mobile menu | Click on "X" icon | Collapses navigation menu | PASS |
| Mobile menu | Click on link | Navigates to the selected section and menu collapses | PASS |
| About | Page Load | Opacity transition | PASS |
| Listen | Click on a play button | Plays an audio element | PASS |
| Listen | Click on a pause button | Pauses an audio element | PASS |
| Listen | Click on a transport slider | Navigates to the selected position in the audio file (once buffered) | PASS |
| Listen | Click on a volume icon | Opens the volume control | PASS |
| Listen | Click on the expanded controls three dots | Opens the "Download" and "Playback speed" controls | PASS |
| Listen | Click on a play button when another audio element is playing | Mutes the previously playing audio element | PASS |
| Contact | Click on the "Send" button without filling in the "Name" field | Shows an error message pointing to the "Name" field | PASS |
| Contact | Click on the "Send" button without filling in the "Email" field | Shows an error message pointing to the "Email" field | PASS |
| Contact | Click on the "Send" button without including an @ in the "Email" field | Shows an error message pointing to the "Email" field | PASS |
| Contact | Click on the "Send" button without filling in the "Message" field | Shows an error message pointing to the "Message" field | PASS |
| Contact | Click on the "Send" button | Sends the form and navigates to the "message-received-page.html" | PASS |
| Footer | Click on the Spotify icon | Opens Tim Goalen's Spotify page in a new tab | PASS |
| Footer | Click on the Twitter icon | Opens Tim Goalen's Twitter page in a new tab | PASS |
| Footer | Click on the IMDb icon | Opens Tim Goalen's IMDb page in a new tab | PASS |
| Message Received Page | Click on the "Home" link | Navigates back to the top of the main page | PASS |
| 404 Page | Enter an non-existing url within the site | Displays the "404.html" page | PASS |
| 404 Page | Click on the "Home" link | Navigates back to the top of the main page | PASS |

### Fixed Bugs
| Bug | Fix |
|---|---|
| 'Send' text on the contact form submit button not visible on the deployed site with an iPhone or iPad (but fine on the simulators in Chrome Dev Tools) | Added an explicit `color: #000` to the `input[type=submit]` style rule|
| Overspill from the image in the grid at the bottom of the 'Credits' page, bleeding into the contact form below | Added `padding-top` to the `<h2>` below, as a workaround |

### Known Bugs

- The navbar menu items are bunched together when viewed on older Safari browsers. Support for the flexbox `gap` property isn't available on versions older than 14.1 (2021).
- The hamburger menu icon is blue, rather than black, when the deployed site is viewed on an iPhone.

## Deployment

### GitHub Pages

The project was deployed to GitHub Pages using the following steps...

Note: Any code committed to the "main" branch will automatically update the live site.
1. Log in to GitHub and locate the [GitHub Repository](https://github.com/timgoalen/tg-composer-portfolio)
2. At the top of the Repository (not top of page), locate the "Settings" Button on the menu.
3. In the left sidebar, click on "Pages" in the "Code and automation" section.
4. Under "Source", click on the dropdown menu and choose "Deploy from a branch".
5. Under "Branch", from the "Select a branch" dropdown menu choose "main"; and from the "Select a folder" dropdown menu choose "/ (root)"; then click the "Save" button in the "Branch" section.
6. Locate the now published site at the top of the "GitHub Pages" page.

### Forking the GitHub Repository

By forking the GitHub Repository we make a copy of the original repository on our GitHub account to view and/or make changes without affecting the original repository by using the following steps...

1. Log in to GitHub and locate the [GitHub Repository](https://github.com/timgoalen/tg-composer-portfolio)
2. At the top right of the Repository, just below the GitHub navbar, click on the "Fork" Button.
3. You should now have a copy of the original repository in your GitHub account.

### Making a Local Clone

1. Log in to GitHub and locate the [GitHub Repository](https://github.com/timgoalen/tg-composer-portfolio)
2. Above the list of files, click "Code".
3. To clone the repository using HTTPS, under "Clone with HTTPS", copy the link.
4. Open Git Bash
5. Change the current working directory to the location where you want the cloned directory to be made.
6. Type `git clone`, and then paste the URL you copied in Step 3.

```
$ git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY
```

7. Press Enter. Your local clone will be created.

```
$ git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY
> Cloning into `CI-Clone`...
> remote: Counting objects: 10, done.
> remote: Compressing objects: 100% (8/8), done.
> remove: Total 10 (delta 1), reused 10 (delta 1)
> Unpacking objects: 100% (10/10), done.
```

Click [Here](https://help.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository#cloning-a-repository-to-github-desktop) to retrieve pictures for some of the buttons and more detailed explanations of the above process.

8. For changes you've made to reflect on the live site:

    -   Type `git add <files changed> `
    -   Type `git commit -m <description of change> `
    -   Type `git push`

## Credits

### Code

- Responsive Navbar:
    - [codebubb](https://www.youtube.com/watch?v=c9jNIYQ1IuI)
- Underline active section in menu:
    - [W3Schools](https://www.w3schools.com/howto/howto_js_active_element.asp)
- Pause playing audio when different audio is played:
    - Javascript solution from [Stack Overflow](https://stackoverflow.com/questions/19790506/multiple-audio-html-auto-stop-other-when-current-is-playing-with-javascript)
- Footer social links using Font Awesome:
    - Code Institute ['Love Running'](https://github.com/Code-Institute-Org/love-running-2.0) walkthrough project

### Content

- All content written by the developer.

### Media

- All audio content owned by the developer.
- Image credits:
    - Headshot - owned by the developer.
    - Running with the Devil: The Wild World of John McAfee - owned by NETFLIX/Curious Films, used for promotional purposes only.
    - Running with the Devil: The Wild World of John McAfee - owned by NETFLIX/Curious Films, used for promotional purposes only.
    - Being Frank: The Frank Gardner Story - owned by BBC TWO/Curious Films, used for promotional purposes only.
    - The Parkinson's Drug Trial: A Miracle Cure? - owned by BBC TWO/Passionate Productions, used for promotional purposes only.
    - Driven: The Billy Monger Story - owned by BBC TWO/Oxford Scientific Films, used for promotional purposes only.
    - Animals with Cameras - owned by BBC ONE/BBC Natural History Unit, used for promotional purposes only.
    - Terry Pratchett: Back in Black - owned by BBC TWO/BBC Studios, used for promotional purposes only.
    - The Hungry Corpse - owned by Rankin Film Productions/Beakus, used for promotional purposes only.
    - Terry Pratchett: Choosing to Die - owned by BBC TWO/Keo Films, used for promotional purposes only.

### Acknowledgements

- My mentor Brian Macharia for his invaluable guidance.

- Tutor support at Code Institute for their help with troubleshooting.