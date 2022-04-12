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
digraph Devops {
    label=<<b>CI/CD Challenges</b>>
    labelloc=t
    page = "16.5,11.7"
    ratio = "auto"
    overlap = "false"
    size = "16.5, 11.7"
    splines = "curved"
    node [fontname="calibri", margin="0.1,0.1", shape=circle, style="filled,rounded", color="lightgrey"]
        "Challenges"
    node [fontname="calibri", margin="0.1,0.1", shape=rect, style="filled,rounded", color="lightgrey"]
        "Challenges" -> "Cycle time is too long"
        "Challenges" -> "Builds"
        "Builds" -> "Availability of Runners"
        "Builds" -> "Troubleshooting failed builds"
        "Troubleshooting failed builds" -> "Limited visibility over Runner health"
        "Availability of Runners" -> "Runners are centrally owned + managed"
        "Challenges" -> "Test Suite Execution Time"
        "Test Suite Execution Time" -> "UI end-to-end"
        "Test Suite Execution Time" -> "Test Acceptance"
        "Test Suite Execution Time" -> "Non-functional Tests"
        "Challenges" -> "Auto-deployment to UAT"
        
        "Challenges" -> "CI/CD Automation"
        "Challenges" -> "Quality Gates"
        "Quality Gates" -> "Maintaining compliance with Veracode rules"
        "Challenges" -> "DORA Metrics"
        "DORA Metrics" -> "Metrics are not generated in GCP"
        "Cycle time is too long" -> "Infra changes require feature branch/PR/merge/apply"
        "Cycle time is too long" -> "Changes on sensitive repos require additonal approvals"
        "Cycle time is too long" -> "Terraform changes cannot be tested locally %28TF plan%29"
        "Cycle time is too long" -> "UI changes must be deployed to an environment for demo"
    node [fontname="calibri", margin="0.1,0.1", shape=oval, style="filled,rounded", color="darkgrey"]
        "CI/CD Automation" -> "Automate remaining controls"
        "CI/CD Automation" -> "Implement SDLC Gonverance Pipeline"
        "Auto-deployment to UAT" -> "Implemented on-prem - required in GCP"
        "Metrics are not generated in GCP" -> "Create metric definitons"
        "Metrics are not generated in GCP" -> "Port / Implement Metrics in GCP"
	}

'>