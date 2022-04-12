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

<img src='https://g.gravizo.com/svg?
/**
*Structural Things
*@opt commentname
*@note Notes can
*be extended to
*span multiple lines
*/
class Structural{}

/**
*@opt all
*@note Class
*/
class Counter extends Structural {
        static public int counter;
        public int getCounter%28%29;
}

/**
*@opt shape activeclass
*@opt all
*@note Active Class
*/
class RunningCounter extends Counter{}
'>
