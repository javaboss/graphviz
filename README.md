# graphviz
Graphviz Projects

dot -Tpng graph.dot > graph.png

if you wish to use other rendering engines, some options are:

neato
twopi

for example, for a mindmap like layout:

neato -Tpng graph.dot > graph.png

to install graphviz (via homebrew)

brew install graphviz

useful tool in VSCode:
Install the Graphviz Preview plugin
ctrl + shift + P
"Open Preview to the side" to show graph previews

To render in github README.md:
https://github.com/TLmaK0/gravizo

https://g.gravizo.com

gravizo
=======

How to include graphviz graphs in github README.md

![Alt text](https://g.gravizo.com/svg?
  digraph G {
    size ="4,4";
    main [shape=box];
    main -> parse [weight=8];
    parse -> execute;
    main -> init [style=dotted];
    main -> cleanup;
    execute -> { make_string; printf}
    init -> make_string;
    edge [color=red];
    main -> printf [style=bold,label="100 times"];
    make_string [label="make a string"];
    node [shape=box,style=filled,color=".7 .3 1.0"];
    execute -> compare;
  }
)