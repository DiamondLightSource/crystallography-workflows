<img width="468" height="100" alt="image" src="https://github.com/user-attachments/assets/d927dfbc-1c0c-4f45-b0c4-01559f043489" /># Crystallography Workflows


Go to: https://argo-cd.workflows.diamond.ac.uk/applications/argocd/i15-1-group

Also see: https://github.com/DiamondLightSource/XRPD-Toolbox 

Navigate to https://workflows.diamond.ac.uk/templates and then filter by Crystallography


If the workflows uses the pdfgetx3 package, a container image should already be available, if you need to build a new images go to gitlab, and clone the repo that contains the pdfgetx3pod repo. 

The pdfgetx3 is not freely distributed and so cannot be pip installed. But is free for academic and non-commercial use. The python .whl's are available once a license is obtained. The whl's and everything required to build the pdfgetx3pod is in the gitlab repo. If new wh;'s are avaialble, download then through the normal mean, put them in the repo. Then do this to build the container image:

podman login ghcr.io – YOUR-GITHUB-USERNAME
podman build -t ghcr.io/diamondlightsource/crystallography-workflows:NAME .
podman push ghcr.io/diamondlightsource/crystallography-workflowsx:NAME
