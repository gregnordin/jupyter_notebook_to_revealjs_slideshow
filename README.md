Purpose
----
Play around with creating a reveal.js slideshow from a jupyter notebook. I am running Jupyter 4.0.6.

Note that I just grabbed a random jupyter notebook to play with and arbitrarily assigned reveal.js slide elements to various cells. The result is not a nice presentation, but simply a quick exploratory test.

### Instructions

- Download [RISE](https://github.com/damianavila/RISE) (Reveal.js Ipython/Jupyter Slideshow Extension), also known as live_reveal
- From the command line on your local computer navigate to RISE directory and run `python setup.py install`
    - This will install the RISE nbextension and enable it
- Start ipython notebook and open up a notebook
- At top of notebook in _Cell Toolbar_ dropdown menu, select _Slideshow_
    - This adds a _Slide Type_ dropdown menu at the top of every cell
- In each cell, select what type of slide or slide element you want it to be (or set to _Skip_ so it doesn't show up in slideshow)
- To run the slideshow live, click the _Enter/Exit Live Reveal Slideshow_ button just to the right of the _Cell Toolbar_ dropdown menu at the top of the notebook
    - Slides that are taller than a page cannot be scrolled. Why??
- To create a static reveal.js slideshow execute
    - `jupyter nbconvert --to slides <notebook filename>`
        - Creates the reveal.js slideshow html file
        - Note that you can't just open this file and have it function as a slideshow in a browser because it doesn't have all of the css and js files it needs. I think this can probably be fixed by putting it into a folder that has all of this other stuff.
    - `jupyter nbconvert --to slides --post serve <notebook filename>`
        - The `--post serve` starts up a webserver and opens the slides in a browser window.
        - The slides act as expected to give a slideshow.
        - Slides that are taller than a page can be scrolled.
