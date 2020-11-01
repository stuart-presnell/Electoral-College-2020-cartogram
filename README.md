# Electoral-College-2020-cartogram

A cartogram of the US with states sized by their number of Electoral College votes in the 2020 general election

This kind of map is a more informative way to judge who's winning, since some physically small states like Massachusetts (MA) have relatively large populations and more Electoral College votes, whereas some physically large states like Montana (MT) only have a relatively small number of Electoral College votes.

main.tex is the main file to compile to produce the map.  Compile it with a LaTeX editor or drop this file and the other two .tex files into a new project at https://www.overleaf.com/

main.tex defines the shapes for each state and draws them, and also defines five colour styles: 

  wait (white)

  Dwin (dark blue, for Democrat wins)

  Rwin (dark red, for Republican wins)

  Dfav (light blue, for states expected to go Democrat)

  Rfav (light red, for states expected to go Republican)

In main.tex each state (plus DC) is given its own style, named for its two letter abbreviation from AK to WY.  
These styles are defined separately in the supplementary files blank.tex and results.tex.
Choose which one to use by uncommenting one of the following lines in main.tex:

% \input{results.tex}

\input{blank.tex}


blank.tex has all states set to [wait], to produce a blank map that you can print and colour by hand.

results.tex initialises the map with some states (*) set to [Dfav] and [Rfav]  and leaves the others blank.  


As results come in on election night you can edit results.tex and recompile to update the map.

For example, change

\tikzstyle{CA}=[Dfav]	% California

to

\tikzstyle{CA}=[Dwin]	% California 

to turn California dark blue



(*)  Specifically, any state that is forecast on https://projects.fivethirtyeight.com/2020-election-forecast/ to have 55% chance or better of going to one party or the other is set as Dfav or Rfav respectively.
