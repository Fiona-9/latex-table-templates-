# latex-table-templates-
## table1
![示例图片](https://raw.githubusercontent.com/Fiona-9/latex-table-templates-
/4781687223122_.pic_thumb.jpg)
```latex
% tikz.vn 
% Le Huy Tien, HUS-VNU
%\documentclass[tikz,border=5mm]{standalone}
\documentclass{article}
\usepackage[margin=3.5cm]{geometry}
\usepackage[utf8]{vietnam}
\usepackage{tikz,amsmath,amssymb,amsthm,lipsum}
\usetikzlibrary{matrix}
\begin{document}
\centerline{\huge\bfseries\color{teal}HÌNH VẼ 100 DÒNG CODE}
\vspace{5mm}

\centerline{Lê Huy Tiễn, HUS-VNU}
\begin{center}
\begin{tikzpicture}
\fill[yellow] (20:1) arc(20:160:1)--cycle;
\fill[cyan!50] (20:1) arc(20:-200:1)--cycle;
\path[teal]
(0,.6) node[black]{tikZ.vn}	
(0,0) node{Elegant}
(0,-.4) node{Simplicity};
\end{tikzpicture}	
\end{center}

\lipsum[1]
\begin{center}
\tikzset{declare function={f(\x)=(\x)^2 -2*\x+3;},	
paranegative/.pic={
\draw 
(-2,0)--(4,0) node[below]{$x$}
(0,-1)--(0,6) node[left]{$y$}
(1,0) node[below right]{$1$}
(0,3) node[below left]{$3$};
\fill[magenta] (0,0) circle(4pt);
\draw[dashed] (1,-1)--(1,6);	
\draw[cyan,thick] plot[domain=-1:3] (\x,{f(\x)});
},% end of pic paranegative
parazero/.pic={
\draw 
(-2,0)--(4,0) node[below]{$x$}
(0,-1)--(0,6) node[left]{$y$}
(1,0) node[below right]{$1$}
(0,1) node[above right]{$1$};
\fill[magenta] (0,0) circle(4pt);
\draw[dashed] (1,-1)--(1,6);	
\draw[cyan,thick] plot[domain=-1:3] (\x,{f(\x)-2});
},% end of pic parazero
parapositive/.pic={
\draw 
(-2,0)--(4,0) node[above]{$x$}
(0,-5)--(0,2) node[left]{$y$}
(-1,0) node[below left]{$-1$}
(3,0) node[below right]{$3$}
(0,-3) node[below left]{$-3$};
\fill[magenta] (0,0) circle(4pt);
\draw[dashed] (1,-5)--(1,2);	
\draw[cyan,thick] plot[domain=-1.5:3.5] (\x,{f(\x)-6});
},% end of pic parapositive
}% end of tikzset

\begin{tikzpicture}
\matrix (m) [matrix of nodes,
nodes in empty cells,
ampersand replacement=\&,
row sep=-\pgflinewidth,
column sep=-\pgflinewidth,
nodes={minimum width=4cm,anchor=center,draw},
row 1/.style={nodes={fill=brown!50}},
row 2/.style={nodes={minimum height=4cm}},
row 3/.style={nodes={minimum height=1.8cm}},
row 4/.style={nodes={minimum height=6mm}},
row 5/.style={nodes={minimum height=8mm}},
]{
$y=x^2-2x+3$ \& $y=x^2-2x+1$ \& $y=x^2-2x-3$\\
\&\&\\
\&\&\\
$\Delta<0$\&$\Delta=0$\&$\Delta>0$\\
không cắt trục $x$\&tiếp xúc trục $x$\&cắt trục $x$\\
};
\path (m-3-1.center) node{
\begin{minipage}{3cm}
\noindent\begin{align*}
\Delta
&=b^2-4ac\\[-2pt]
&=(-2)^2-4\cdot 1 \cdot 3\\[-2pt] 
&=-8
\end{align*}
\end{minipage}
};
\path (m-3-2.center) node{
\begin{minipage}{3cm}
\noindent\begin{align*}
\Delta
&=b^2-4ac\\[-2pt]
&=(-2)^2-4\cdot 1 \cdot 1\\[-2pt] 
&=0
\end{align*}
\end{minipage}
};
\path (m-3-3.center) node{
\begin{minipage}{3cm}
\noindent\begin{align*}
\Delta
&=b^2-4ac\\[-2pt]
&=(-2)^2-4\cdot 1 \cdot (-3)\\[-2pt] 
&=16
\end{align*}
\end{minipage}
};
\path 
(m-2-1.center) pic[shift={(-.5,-1.3)},scale=.5]{paranegative}
(m-2-2.center) pic[shift={(-.5,-1.3)},scale=.5]{parazero}
(m-2-3.center) pic[shift={(-.5,.7)},scale=.5]{parapositive};
\end{tikzpicture}
\end{center}
\lipsum[2]
\end{document}	
```
