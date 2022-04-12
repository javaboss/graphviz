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
digraph Devops {
    label=<<b>CI/CD Challenges</b>>
    labelloc=t
    page = "16.5,11.7"
    ratio = "auto"
    overlap = "false"
    size = "16.5, 11.7"
    splines = "curved"

//[label="0"]
    node [fontname="calibri", margin="0.1,0.1", shape=circle, style="filled,rounded", color="lightgrey"]
        "Challenges"

    // Challenges
    node [fontname="calibri", margin="0.1,0.1", shape=rect, style="filled,rounded", color="lightgrey"]
        "Challenges" -> "Cycle time is too long"

        "Challenges" -> "Builds"
        "Builds" -> "Availability of Runners"
        "Builds" -> "Troubleshooting failed builds"
        "Troubleshooting failed builds" -> "Limited visibility over Runner health"
}