\def\ddp#1{d^3\vp_{#1}}
\def\dvx{\int d^3\vx}
\def\ddpp#1{d^3\vpp_{#1}}
\def\tf {\tilde{f}}
\def\ff{{\mathcal{F}}}
\def\fjl {\Phi\left(\frac{n}{q}j,\frac{n}{q} l\right)}
\def\F#1#2{\Phi\left(\frac{n}{q}{#1},\frac{n}{q}{#2}\right)}
%\def\F#1 {\Phi\left(\frac{n}{q}{#1},\frac{n}{q}{}\right)}
\def\fc#1#2 {\frac{n}{q}#1\frac{n}{q}#2}

\def\e#1{\langle#1\rangle_0}
\def\ee#1{\left\langle#1\right\rangle}
\def\di#1{\left(\vcenter{\xymatrix{#1}}\right)}
%\def\vpp{V^{\prime\prime}}
\def\vppp{V^{\prime\prime\prime}}
\def\kt{\kappa}
\def\kt{\mathfrak{K}}
\def\ks{|\kt\rangle}
\def\bdk{B^\ddag_{\kt}}
\def\bk{B_{\kt}}
\def\hf{H\p_{f_0}}
\def\hpt{H_{\rm{free}}}
\def\hp{H^{\prime(t)}}
\def\rv{{\rm{vac}}}


%\def\th#1#2{\ensuremath{\theta_{#1#2}}}
%\def\th#1#2{\theta_{#1#2}}
\def\bp{\mathbf{P}}
\def\thet#1#2{\theta_{#1#2}}
\def\Os{{\ovac}}
\def\mo#1{\int\frac{d{#1}}{2\pi}}
%\def\th13{\ensuremath{\theta_{13}}}
%\def\th23{\ensuremath{\theta_{23}}}
\def\c#1#2{\hbox{\rm cos}(\thet#1#2)}
\def\s#1#2{\hbox{\rm sin}(\thet#1#2)}
%\def\c13{\hbox{\rm cos}(\th13)}
%\def\s13{\hbox{\rm sin}(\th13)}
%\def\c23{\hbox{\rm cos}(\th23)}
%\def\s23{\hbox{\rm sin}(\th23)}
\def\an{\ensuremath{\alpha_n}}
%\newcommand{\C}{\ensuremath{\mathbb C}}
%\newcommand{\Z}{\ensuremath{\mathbb Z}}
%\newcommand{\R}{\ensuremath{\mathbb R}}
%\newcommand{\rp}{\ensuremath{\mathbb {RP}}}
%\newcommand{\cp}{\ensuremath{\mathbb {CP}}}
\newcommand{\vac}{\ensuremath{|0\rangle}}
\newcommand{\ovac}{\ensuremath{|\Omega\rangle}}
\newcommand{\ps}{\ensuremath{|\vp_0\rangle}}
\newcommand{\stt}{\ensuremath{|\psi\rangle}}
\newcommand{\vact}{\ensuremath{|00\rangle}                    }
%\newcommand{\oc}{\ensuremath{\overline{c}}}
\renewcommand{\cos}{\textrm{cos}}
\renewcommand{\sin}{\textrm{sin}}
\newcommand{\asin}{\textrm{arcsin}}
\renewcommand{\sinh}{\textrm{sinh}}
\renewcommand{\cosh}{\textrm{cosh}}
\renewcommand{\tanh}{\textrm{tanh}}
\newcommand{\sech}{\textrm{sech}}
\newcommand{\csch}{\textrm{csch}}
\renewcommand{\cot}{\textrm{cot}}
\def\exp#1{\hbox{\rm exp}\left[#1\right]}
\def\re#1{{\rm Re}\left(#1\right)}
\def\sign#1{{\rm sign}\left(#1\right)}



%\setlength{\mathindent}{.3in}
\newcommand{\feynslash}[1]{#1\hspace{-9pt}\slash\hspace{6pt}}
%\newcommand{\feynslash}[1]{#1\hspace{-7pt}\slash\hspace{4pt}}
\renewcommand{\theequation}{\arabic{section}.\arabic{equation}}
\renewcommand{\(}{\begin{equation}}
\renewcommand{\)}{end{equation} \vspace{-.05in}\linebreak}
\newcommand{\numeq}{\renewcommand{\theequation}{\arabic{section}.
\arabic{equation}}}
\newcommand{\nonumeq}{\renewcommand{\theequation}{}}
\newcounter{saveeqn}
\newcounter{savealpheqn}
\newcounter{savesection}
\newcommand{\alpheqn}{\setcounter{saveeqn}{\value{equation}}%
  \stepcounter{saveeqn}\setcounter{equation}{0}%
  \renewcommand{\theequation}{\mbox{\arabic{section}.\arabic{saveeqn}
\alph{equation}}}
  \renewcommand{\)}{\end{equation}}}
\def\part#1{\frac{\partial}{\partial{#1}}}%
\def\group#1{\refstepcounter{equation}\setcounter{saveeqn}
 {\value{equation}}%
  \label{#1}\setcounter{equation}{0}%
  %\lineskip -2.4in%
\renewcommand{\theequation}{\mbox{\arabic{section}.\arabic{saveeqn}
%\renewcommand{\theequation}{\mbox{\arabic{saveeqn}
\alph{equation}}}
  \renewcommand{\)}{\end{equation}}}
\newcommand{\reseteqn}{\setcounter{equation}{\value{saveeqn}}%
  %\baselineskip 1.5pt%
  \renewcommand{\theequation}{\arabic{section}.\arabic{equation}}%
  \renewcommand{\)}{\end{equation}}}
\newcounter{alphcount}

\newcommand{\aalpheqn}{\setcounter{saveeqn}{\value{equation}}%
  \stepcounter{saveeqn}\setcounter{equation}{0}%
  \renewcommand{\theequation}{\mbox{
        \Alph{subsection}.\arabic{saveeqn}\alph{equation}}}
   \renewcommand{\)}{\end{equation}}}
\newcommand{\areseteqn}{\setcounter{equation}{\value{saveeqn}}%
  \renewcommand{\theequation}{\Alph{subsection}.\arabic{equation}}%
  \renewcommand{\)}{\end{equation}}}
\newcommand{\unalph}{\setcounter{savealpheqn}{\value{equation}}%
  \renewcommand{\theequation}{\mbox{\arabic{section}.\arabic{saveeqn}}}}
\newcommand{\realph}{\setcounter{equation}{\value{savealpheqn}}}
\renewcommand{\=}{\hspace{-.03in}=\hspace{-.02in}}
%\newcommand{\+}{\hspace{-.03in}+\hspace{-.02in}}
\renewcommand{\thefootnote}{\alph{footnote}}
\renewcommand{\(}{\begin{equation}}
\renewcommand{\)}{\end{equation}}
\newcommand{\ba}{\begin{eqnarray}}
\newcommand{\ea}{\end{eqnarray}}
%\renewcommand{\l}{\lambda}
\renewcommand{\a}{\alpha}
\renewcommand{\b}{\beta}
\renewcommand{\r}{\rho}
\renewcommand{\sl}{{\sqrt{\lambda}}}
\newcommand{\vt}{V^{(3)}(\sqrt{\lambda}f(x))}
%\newcommand{\bp}{\mathop{\vtop{\ialign{##\crcr
%   $\hfil\displaystyle{}\hfil$\crcr\noalign{\kern-13pt\nointerlineskip}
%   \BIG{(}\hskip0pt\crcr\noalign{\kern3pt}}}}}
\newcommand{\cbp}{\mathop{\vtop{\ialign{##\crcr
   $\hfil\displaystyle{}\hfil$\crcr\noalign{\kern-13pt\nointerlineskip}
   \BIG{)}\hskip0pt\crcr\noalign{\kern3pt}}}}}
\newcommand{\pa}{\mathop{\vtop{\ialign{##\crcr

$\hfil\displaystyle{\oplus}\hfil$\crcr\noalign{\kern+1pt\nointerlineskip
}
   \hspace{.08in}$^{\alpha=0}$\hskip6pt\crcr\noalign{\kern3pt}}}}}
\renewcommand{\hsp}{,\hspace{.3in}}
%\newcommand{\newsection}{\setcounter{equation}{0}\section}
\newcommand{\p}{^\prime}
\newcommand{\pp}{^{\prime\prime}}
\newcommand{\w}{\omega}
%\newcommand{\mod}{{\textup{\scriptsize{ mod }}}}
\newcommand{\rank}{{\textup{\scriptsize{rank}}}}
\newcommand{\rrank}{{\textup{rank}}}
\newcommand{\rmod}{{\textup{ mod }}}
\newcommand{\appendixa}
  {\renewcommand{\theequation}{\Alph{subsection}.\arabic{equation}}%
   \renewcommand{\thesubsection}%
                {Appendix \Alph{subsection}.\setcounter{equation}{0}}%
   \renewcommand{\alpheqn}{\aalpheqn}%
   \renewcommand{\reseteqn}{\areseteqn}
   \newcounter{savesec}}
\newcommand{\appendices}{\appendix\appendixa}
\newcommand{\Z}{\ensuremath{\mathbb Z}}
\newcommand{\ci}{\ensuremath{{C^\infty}}}
\def\dwn{\downarrow}
\def\updwn{\updownarrow}
\def\H{\ensuremath{\ES{H}}}
%\def\i{\ensuremath{\dot\imath}}
\def\S{\ensuremath{\ES{S}}}
%\def\L{\ensuremath{{\cal L}}}
\def\D{\ensuremath{{\cal D}}}
%\def\O{\ensuremath{{\cal O}}}
\newcommand{\del}{\ensuremath{\partial}}

%\numberwithin{equation}{section}
%\renewcommand{\theequation}{\mbox{\arabic{equation}}}


%\def\journal{\topmargin .5in    \oddsidemargin .5in
%         \headheight 0pt \headsep 0pt
%         \textwidth 5.625in % 1.2 preprint size  %6.5in
%         \textheight 8.25in % 1.2 preprint size 9in
%        \marginparwidth 1.5in
%         \parindent 2em
%         \parskip .5ex plus .1ex         \jot = 1.5ex}



\def\baselinestretch{1.1}


\def\rf#1{\ref{ref#1}}
\def\comment#1{\hsp{.3}\textup{#1}}

\def\lsim{\mathrel{\mathpalette\vereq\langle}}
\def\gsim{\mathrel{\mathpalette\vereq\rangle}}
\catcode`\@=11
\def\vereq#1#2{\lower3pt\vbox{\baselineskip1.5pt \lineskip1.5pt
\ialign{$\m@th#1\hfill##\hfil$\crcr#2\crcr\sim\crcr}}}
\catcode`\@=12

%\renewcommand{\textfraction}{0.15}
%\renewcommand{\topfraction}{0.85}
%\renewcommand{\bottomfraction}{0.65}
%\renewcommand{\floatpagefraction}{0.60}
%\makeatletter
%\newcommand\figcaption{\def\@captype{figure}\caption}
%\newcommand\tabcaption{\def\@captype{table}\caption}
%\makeatother


\renewcommand{\(}{\begin{equation}}
\renewcommand{\)}{\end{equation}}
\newcommand{\etab}{{\overline{\eta}}}

\def\vx{{\vec{x}}}
\def\vp{{\vec{p}}}
\def\vpp{{\vec{p}^{
\hspace{.05cm}\prime
}}}
\def\vk{{\vec{k}}}
\def\vkp{{\vec{k}\p}}

% math blackboard
%\def\th#1#2{\ensuremath{\theta_{#1#2}}}
%\def\th13{\ensuremath{\theta_{13}}}
%\def\th23{\ensuremath{\theta_{23}}}
\def\pin#1{\int \frac{d#1}{2\pi}}
\def\ppin#1{\int\hspace{-17pt}\sum \frac{d#1}{2\pi}}
\def\ppink#1{\int\hspace{-17pt}\sum\frac{d^{#1}\vk}{(2\pi)^{#1}}}
\def\ppinkk#1#2{\int\hspace{-17pt}\sum\frac{d^{#1}\vk_{#2}}{(2\pi)^{#1}}}
\def\ppinkp#1{\int\hspace{-17pt}\sum\frac{d^{#1}\vk\p}{(2\pi)^{#1}}}
\def\dint{\int\hspace{-12pt}\sum }
\def\pink#1{\int \frac{d^{#1}k}{(2\pi)^{#1}}}
\def\pinq#1{\int \frac{d^{#1}q}{(2\pi)^{#1}}}
\def\pinqp#1{\int \frac{d^{#1}q\p}{(2\pi)^{#1}}}
\def\pinkp#1{\int \frac{d^{#1}k\p}{(2\pi)^{#1}}}
\def\pinpp#1{\int \frac{d^{#1}p\p}{(2\pi)^{#1}}}
\def\pinvp#1{\int \frac{d^{#1}\vp}{(2\pi)^{#1}}}
\def\pinvk#1{\int\hspace{-17pt}\sum \frac{d^{#1}\vk}{(2\pi)^{#1}}}
\def\kinv#1#2{\int\hspace{-17pt}\sum \frac{d^{#1}\vec{#2}}{(2\pi)^{#1}}}
\def\pinv#1#2{\int \frac{d^{#1}\vec{#2}}{(2\pi)^{#1}}}
\def\ppinv#1#2{\int \frac{d^{#1}\vec{#2}^{
\hspace{.07cm}\prime
}}{(2\pi)^{#1}}}
\def\sq#1#2{\sqrt{\frac{\omega_{#1}}{\omega_{#2}}}}
\def\bd#1{b^\dag_{k_{#1}}}
\def\bm#1{b_{-k_{#1}}}
\def\Bd#1{B^\ddag_{k_{#1}}}
\def\Ad#1{A^\ddag_{\vp_{#1}}}
\def\Btd#1{B^{(t)\ddag}_{k_{#1}}}
\def\Bt#1{B^{(t)}_{k_{#1}}}
\def\Bdp#1{B^\ddag_{k\p_{#1}}}
\def\Bm#1{B_{-k_{#1}}}
\def\t#1#2{\hbox{\rm tan}(\thet#1#2)}
\def\tp#1#2#3{\hbox{\rm tan}^#1(\thet#2#3)}
\def\m#1#2{\ensuremath{\Delta M_{#1#2}^2}}
\def\mn#1#2{\ensuremath{|\Delta M_{#1#2}^2}|}
\def\u#1#2{\ensuremath{{}^{2#1#2}\mathrm{U}}}
\def\pu#1#2{\ensuremath{{}^{2#1#2}\mathrm{Pu}}}
\def\meff{\ensuremath{\Delta M^2_{\rm{eff}}}}
\def\cc{\mathcal{C}}
\def\df{\mathcal{D}_{f}}
\def\dv{\mathcal{D}_{v}}
\def\dft{\mathcal{D}_{f}^{(t)}}
\def\dfd{\mathcal{D}_{f}^{(t)\dag}}
\def\dfe{\mathcal{D}_{f_\epsilon}}
\def\dfx{\mathcal{D}_{f_{x_0}}}
\def\dF{\mathcal{D}_F}

% hengyuan definition: begin
\def\avkd{A^\ddag_{\vec{k}}}
\def\avpd{A^\ddag_{\vec{p}}}
\def\avkm{A_{-\vec{k}}}
\def\avpm{A_{-\vec{p}}}
\def\avk{A_{\vec{k}}}
\def\avp{A_{\vec{p}}}
\def\omvk{\omega_{\vec{k}}}
\def\omvp{\omega_{\vec{p}}}

\def\navkd#1{A^\ddag_{\vec{k}_{#1}}}
\def\navpd#1{A^\ddag_{\vec{p}_{#1}}}
\def\navkm#1{A_{-\vec{k}_{#1}}}
\def\navpm#1{A_{-\vec{p}_{#1}}}
\def\navk#1{A_{\vec{k}_{#1}}}
\def\navp#1{A_{\vec{p}_{#1}}}
\def\nomvk#1{\omega_{\vec{k}_{#1}}}
\def\nomvp#1{\omega_{\vec{p}_{#1}}}
% hengyuan definition: end


\def\B#1{B^\ddag_{k_{#1}}}
\def\Bp#1{B^\ddag_{k\p_{#1}}}
\def\I{\mathcal{I}}
\def\vl#1#2#3{\vector(#1,#2){#3}\line(#1,#2){#3}}
%\def\g{\mathfrak g}
\def\os{\omega_S}
\def\op{\omega_p}
\def\gx{(\gamma(x-vt))}
\def\as{|\alpha;\sigma\rangle}
\def\asb{\langle\alpha;\sigma|}
\def\red#1{\textcolor{red}{Jarah: #1}}
\def\npb#1{{#1}}
\def\npbb#1{{#1}}
\def\npbbb#1{\textcolor{red}{#1}}
\def\blu#1{\textcolor{blue}{Baiyang: #1}}
\usepackage[dvipsnames]{xcolor}
\def\gre#1{\textcolor{ForestGreen}{Hengyuan: #1}}
\def\hui#1{\textcolor{Mulberry}{Hui: #1}}


\newcommand{\beas}{\begin{eqnarray*}}
\newcommand{\eeas}{\end{eqnarray*}}
\newcommand{\defi}{\stackrel{\rm def}{=}}
\newcommand{\non}{\nonumber}
\newcommand{\bquo}{\begin{quote}}
\newcommand{\enqu}{\end{quote}}
\def\Om{\ensuremath{\Omega}}
\def\lim#1{\stackrel{\rm{lim}}{{}_{#1}}}

\newcommand{\attn}[1]{\begin{center}\framebox{\begin{minipage}{8cm}#1
\end{minipage}}\end{center}}

\newcommand{\pic}{\hspace{-.05cm},\hspace{-.05cm}}



%}{}

\def\Tr{ \hbox{\rm Tr}}
\newcommand{\C}{{\mathbb C}}
\newcommand{\cp}{{\mathrm{\mathbb CP}}}
\newcommand{\R}{{\mathbb R}}
\renewcommand{\Z}{{\mathbb Z}}
\newcommand{\QQ}{{\mathbb Q}}
    \newcommand{\g}{\mathfrak g}
\def\bp{{\bf{p}}}
\def\bq{{\bf{q}}}
\def\bk{{\bf{k}}}
\def\ch{{\mathcal{H}}}
\def\co{{\mathcal{O}}}
\def\tp{{\tilde{\phi}}}
\def\op#1{\omega_{p_{#1}}}
\def\ok#1{\omega_{k_{#1}}}
\def\okp#1{\omega_{k\p_{#1}}}
\def\ovp#1{\omega_{\vp_{#1}}}
\def\ovpp#1{\omega_{\vpp_{#1}}}
\def\okt#1{\omega_{\kt_{#1}}}
\def\V#1{V^{(#1)}(\sqrt{\lambda}f(x))}
\def\Vg#1{V^{(#1)}(\sqrt{\lambda}f(\gamma(x-vt))}
%\def\v#1{V^{(#1)}[f(x),x]}
\def\ck{\csch\left(\frac{\pi k}{2\b}\right)}
\def\cks{\csch^2\left(\frac{\pi k}{2\b}\right)}
\def\mb{\mathcal{B}}
\def\mc{\mathcal{C}}
\def\md{\mathcal{D}}
\def\me{\mathcal{E}}
\def\gt{\tilde{\g}}
\def\dim{2}
\def\dimtwo{4}
\def\dimthree{6}
\def\phip{\phi}
\def\pip{\pi}

\newcommand{\beq}{\begin{equation}}
\newcommand{\eeq}{\end{equation}}
\newcommand{\bea}{\begin{eqnarray}}
\newcommand{\eea}{\end{eqnarray}}


\newskip\humongous \humongous=0pt plus 1000pt minus 1000pt
\def\caja{\mathsurround=0pt}
\def\eqalign#1{\,\vcenter{\openup1\jot \caja
  \ialign{\strut \hfil$\displaystyle{##}$&$
  \displaystyle{{}##}$\hfil\crcr#1\crcr}}\,}
\newif\ifdtup
\def\panorama{\global\dtuptrue \openup1\jot \caja
  \everycr{\noalign{\ifdtup \global\dtupfalse
  \vskip-\lineskiplimit \vskip\normallineskiplimit
  \else \penalty\interdisplaylinepenalty \fi}}}
\def\eqalignno#1{\panorama \tabskip=\humongous
  \halign to\displaywidth{\hfil$\displaystyle{##}$
  \tabskip=0pt&$\displaystyle{{}##}$\hfil
  \tabskip=\humongous&\ll ap{$##$}\tabskip=0pt
  \crcr#1\crcr}}