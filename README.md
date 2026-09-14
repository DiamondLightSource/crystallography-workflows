# Crystallography Workflows

Go to: https://argo-cd.workflows.diamond.ac.uk/applications/argocd/i15-1-group

Also see: https://github.com/DiamondLightSource/XRPD-Toolbox 

Navigate to https://workflows.diamond.ac.uk/templates and then filter by Crystallography

# Docs for workflows

https://diamondlightsource.github.io/workflows/docs/

see also the examples shown here:

https://github.com/DiamondLightSource/workflows/tree/main/examples

# manually building a container images

You must first commit your changes to a repo. Then do this to build the container image:

```bash

podman login ghcr.io -u YOUR_GITHUB_USERNAME -p YOUR_TOKEN

podman build -t ghcr.io/diamondlightsource/crystallography-workflows:NAME .

podman push ghcr.io/diamondlightsource/crystallography-workflowsx:NAME

```
