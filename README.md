Beamer Lausanne Theme
=====================

This is a beamer theme whose main features is to display full-screen images in
the background of the main and sections title slides. The section title images
can be reused in a smaller format in the conclusion slide of the section. Images
can also be omitted for some or all sections.

A class of semi-transparent boxes is also defined to be able to read text
clearly over the rich graphical background of the titles.

There are a few other things like built-in checks/crosses list item markers.
Section titles can be turned off and the theme main color changed using the
usual commands.

Author
------

Robin Scheibler

Example
-------

Here is an example demonstrating most features. The pdf generated is [here]()

    \documentclass{beamer}

    % Load encoding and computer modern fonts
    \usepackage[utf8]{inputenc}
    \usepackage[T1]{fontenc}
    \usepackage{lmodern}

    % The presentation meta information
    \title{The Lausanne Beamer Theme}
    \subtitle{With Beautiful Images}
    \date{\today}
    \author{Robin Scheibler}
    \institute{School of Computer and Communication Sciences\\%
    \'Ecole Polytechnique F\'ed\'erale de Lausanne, Switzerland}
    \logo{\includegraphics[height=0.5cm]{figures/LCAV}}
    \titlegraphic{figures/climber}  % This is the source for the title background image

    % Load the theme
    \usetheme{lausanne}

    % To remove the section title frames, uncomment
    % AtBeginSection[]{}

    % The color of the theme can be changed like this
    %\usecolortheme[named=red]{structure}

    \begin{document}

    \begin{frame}
    \titlepage
    \end{frame}

    \section*{Introduction}

    \begin{frame}{Introduction}
      This is an example to use the \texttt{lausanne} beamer theme that I based on my recent presentations. 
      Enjoy\footnote{This is a starred section. Starred sections do not have a title page.} \smiley

      \begin{flushright}
        --- Robin
      \end{flushright}
    \end{frame}

    \begin{frame}{Outline}
      \tableofcontents
    \end{frame}

    \section[short=Examples,image=figures/lighthouse]{A Couple of Examples}

    \begin{frame}{What can we do ?}
      A great theme
      \begin{itemize}
        \item Beautiful full frame image
        \item Title and section title frames
        \item Semi-transparent boxes
        \item Take home message slides
        \item We can use plain bullets
        \citem or maybe check marks!
        \xitem or cross marks!
        \smileyitem or a smiley!
      \end{itemize}
    \end{frame}

    \begin{frame}{Changing a few things}
      \begin{itemize}
        \item The dominant color can be changed by adding in the preamble
          \begin{center}
            \texttt{{\textbackslash}usecolortheme[named=<colorname>]\{structure\}}
          \end{center}
        \item To remove the section titles, add
          \begin{center}
            \texttt{AtBeginSection[]\{\}}
          \end{center}
      \end{itemize}
    \end{frame}

    \begin{fullframe}{figures/pyramic_large}
      \begin{tcolorbox}
        \huge \centering Beautiful full frame images

        \normalsize Semi-transparent boxes can be used to add text on top of images
      \end{tcolorbox}
    \end{fullframe}

    \begin{takehome}
      \begin{itemize}
        \item Possible to create \alert{take home message} with matching image
        \item An amazing journey
        \item Latex is a bitch
      \end{itemize}
    \end{takehome}

    \section{A Normal Section}

    \begin{frame}{Sections without images}
      \begin{itemize}
        \item It is also possible to do sections without images.
      \end{itemize}
    \end{frame}

    \begin{frame}{Some great math}
      We keep math in serif font, because it looks familiar
      \begin{equation*}
        e^{i\pi} + 1 = 0
      \end{equation*}
    \end{frame}

    \end{document}

License
-------

2017-2018 (c) Robin Scheibler

The theme is licensed under MIT license as described in the `LICENSE` file.
