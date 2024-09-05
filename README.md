`index.html`
    `head`
        *   connects fontawesome
        *   connects my stylesheet
        *   connects Google Fonts
        *   3 fonts:
            1.  DM Sans
            2.  Red Hat Display
            3.  Sarabun
        *   title and other defaults
    `body`
        *   no margin
        *   font set to DM Sans
        *   each element has a `.disappear` animation
            based on the viewport of the webpage
            *   i.e. disappear after reaching top and appear
                when at the bottom
        *   `header`
            *   contains nav of name and other page
        *   `page`
            *   contains everything BUT the header
            *   helps differentiate style and maintain
                navbar's width to be along the entire page,
                as well as page animations and dimensions
            * `splash`
                *   the main info with my name, blurb, address,
                    and image
                *   `info`
                    *   separator to allow text and image to be
                        side-by-side
                    *   `text`
                        *   separator to allow text to be
                            organized in one column
            *   `section` (Education)
            *   `section` (Honors and Awards)
            *   `section` (Skills)
            *   `section` (Leadership and Experience)
            *   `section` (Projects)
            *   `footer`
                *   contains my name and a link to my LinkedIn
CSS
    animations
        *   `fadeInDelayedxx`
            *   each variation delays it briefly from showing up
                to give a loading feel
            *   `xx` is the % of when it shows up during the
                animation time (e.g. 50% of 1.5s is .75s -- the
                start of when it fades in)
            *   each delay has a corresponding class describing
                the order in which it is to be used
                *   following format: `.fadeDelayedx`
                    *   `x` can be `1-5` for between delays
                        `1` and `2`; it is designed for tall
                        elements such as an image on the same
                        line as another element
                    *   other `x-5` classes and delays have not
                        been implemented because there is currently
                        no need
            *   what it means for `index.html`
                *   for `splash`, each element loads in order
                *   for `hr`, it loads in brief moment AFTER the
                    title (same delay as the tagline/blurb)
                *   anything following `hr` is then loaded in
                    one-after the other HOWEVER it's max delay
                    is `.fadeInDelay4`
                    *   this is to prevent a person scrolling
                        and waiting a while for everything to load; the start time of `4` is .6s
                    *   this also differentiates the `splash`
                        with the rest of the page and makes it
                        appear as two different sections
            *   what it means for `contact.html`
                *   the following logic for `splash` applies;
                    it merely makes it appear in order
                *   it does not follow a load order described for
                    `hr` and after because the entire page can be
                    loaded at once
        *   `kineticUp`
            *   used in the class `.disappear`, it allows for each
                element to appear and disappear as they are scrolled
                into and out of view
            *   what it means for `index.html` and `contact.html`
                *   each element has a `div` or something similar
                    surrounding it containing the `disappear` class,
                    which allows each individual element to have a
                    `fadeDelayedx` class AND interact with the
                    viewport to disappear and reappear
    animation classes
        *   described above
    default elements
        *   the default page elements have changes, some of which
            are not listed because they are minor/only exist
            for maintaining a certain look and not intended as
            changes to the default appearance
        *   `body`
            *   font is DM Sans
            *   margins removed to allow header to rest at top on load
                and as per project requirements
            *   display is flex which allows for centering the page
                along with other elements
            *   text align is justify to make it have a more boxy look
        *   `nav`
            *   flex display to create space between my name and the link
            *   set a max width so that it will always be same size as
                the page and the ends of the `nav` will always be aligned
                with the ends of the page
            *   minimum width is `320px` so nothing starts breaking
            *   it's `width` is `100%` so it can fill up the `header`
            *   elements inside have padding to make the `nav` pretty
            *   font is Red Hat Display and background color
                is dulled red/pink
            *   see `nav-header` class for more info about
                changes to nav
        *   `footer`
            *   font size smaller and text color is gray
        *   `hr`
            *   size is larger, rounded, and different color
            *   margin is altered to make bottom margin larger
        *   individual elements/containers
            *   each gets an animation such that it can
                disappear and reappear
        *   `a`
            *   default color matches text color
            *   hover makes it move up and change color
            *   no underline
TODO:
* WRITE ABOUT SECTIONS
