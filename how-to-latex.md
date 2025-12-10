When working with more complex documents, some errors showed up in my setup, so I wanted to make a quick guide to remember this in the future 
and maybe someone can benefit from this, too.

I use TeXShop Version 5.54 (on macOS) and have pdfTeX 3.141592653-2.6-1.40.27 (TeX Live 2025) installed in this path: /Library/TeX/texbin/pdflatex

- Problem: Missing packages. 
- Solution: Install them via Terminal: 

In my case: 

# Install the missing packages
sudo tlmgr install koma-script
sudo tlmgr install blindtext
sudo tlmgr install imakeidx
sudo tlmgr install paralist
sudo tlmgr install epigraph
sudo tlmgr install glossaries
sudo tlmgr install acronym
sudo tlmgr install wrapfig
sudo tlmgr install csquotes
sudo tlmgr install biblatex
sudo tlmgr install biblatex
sudo tlmgr install verbatimbox
sudo tlmgr install subfigure  

etc.

- Problem: Wrong path in TexShop. 
- Solution: In my case I had to set it this way:

In TeXShop, go to Preferences -> Engine. There I set the distiller as follows: 

Path settings: /Library/TeX/texbin (default)

Distiller: /usr/local/texlive/2025/bin/universal-darwin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin (default: usr/local/bin)

Alternate Path: ~/bin/context/tex/texmf-osx-arm64/bin (default)

Now it is possible to typeset the document :)



