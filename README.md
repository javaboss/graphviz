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

gravizo
=======

How to include graphviz graphs in github README.md

### New Plantuml activity Diagram ###
![Alt text](https://g.gravizo.com/source/custom_mark21?https%3A%2F%2Fraw.githubusercontent.com%2FTLmaK0%2Fgravizo%2Fmaster%2FREADME.md)

![Alt text](https://g.gravizo.com/source/custom_mark21?https%3A%2F%2Fraw.githubusercontent.com%2FTLmaK0%2Fgravizo%2Fmaster%2FREADME.md)

<details> 
<summary></summary>
custom_mark21	
@startuml
start
:init;
-> test of color;
if (color?) is (<color:red>red) then
:print red;
else 
:print not red;
note right: no color
endif
partition End {
:end;
}
-> this is the end;
end
@enduml
custom_mark21
</details>
