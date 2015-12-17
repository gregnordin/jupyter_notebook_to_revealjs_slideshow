Let's figure out what the different pieces are.

__Directories__

    jupyter --paths
        config:
            /Users/nordin/.jupyter
            /Users/nordin/anaconda/etc/jupyter (doesn't exist)
            /usr/local/etc/jupyter (doesn't exist)
            /etc/jupyter (doesn't exist)
        data:
            /Users/nordin/Library/Jupyter
            /Users/nordin/anaconda/share/jupyter (doesn't exist)
            /usr/local/share/jupyter
                (contents: nbextensions)
            /usr/share/jupyter (doesn't exist)
        runtime:
            /Users/nordin/Library/Jupyter/runtime

__Directories (another method)__ (from 151214_jupyter_nbextensions_explore.ipynb)

_jupyter_config_dir()_ = /Users/nordin/.jupyter  
_jupyter_config_path()_ = ['/Users/nordin/.jupyter', '/Users/nordin/anaconda/etc/jupyter', '/usr/local/etc/jupyter', '/etc/jupyter']  
_jupyter_data_dir()_ = /Users/nordin/Library/Jupyter  
_jupyter_path()_ = ['/Users/nordin/Library/Jupyter', '/Users/nordin/anaconda/share/jupyter', '/usr/local/share/jupyter', '/usr/share/jupyter']

~/.jupyter

    custom
        custom.js
            contents:
                require(["base/js/events"], function (events)
                {events.on("app_initialized.NotebookApp", function ()
                { IPython.load_extensions('usability/linenumbers') }
        migrated (don't know what this is)
        nbconfig
            notebook.json
                contents:
                    { "load_extensions": {"livereveal/main": true} }

~/Library/Jupyter

    kernels
        python2
        python3
    nbextensions
        bibtex.js
        calico-cell-tools.css
        calico-cell-tools.js
        calico-document-tools.js
        linenumbers.js
        livereveal
            main.css
            main.js
            main.orig.css
            reset_reveal.css
            reveal.js (dir)
                css
                    reveal.css
                    reveal.min.css
                    theme (dir with all of the themes)
                Gruntfile.js
                index.html (this is the example slideshow that comes with reveal.js)
                js
                    reveal.js
                    reveal.min.js
                lib
                    css (dir)
                    font (dir)
                    js (dir)
                LICENSE
                package.json
                plugin (dir)
                README.md
                test (dir)
        toc.css
        toc.js

~/.ipython

    extensions (dir)
        circuitikz.py
        tikzmagic.py
        version_information.py
        watermark.py
    kernels (dir)
    nbextensions (dir)
        bibtex.js
        calico-cell-tools.css
        calico-cell-tools.js
        calico-document-tools.js
        linenumbers.js
        toc.css
        toc.js
    profile_default
    README
