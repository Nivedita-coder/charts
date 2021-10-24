## Kyverno Policy Integration

PodSecurityPolicy(PSP) is being deprecated in Kubernetes v1.21 and will be removed in v1.25. So, the suitable alternative is Kyverno.

<img width="200" align="right" alt="Kyverno Logo" src="https://github.com/cncf/artwork/blob/master/projects/kyverno/stacked/color/kyverno-stacked-color.png" xmlns="http://www.w3.org/1999/html">

Kyverno is an Open source policy engine designed specifically for Kubernetes. The word "Kyverno" is a Greek word for "Govern". It was originally developed by Nirmata and is now a CNCF sandbox project. It can validate, mutate, and generate configurations using admission controls and background scans.

### Installation

1.Install kyverno via [Helm](https://kyverno.io/docs/installation/#install-kyverno-using-helm) or [YAMLs](https://kyverno.io/docs/installation/#install-kyverno-using-yamls) in Kubernetes cluster.

2.After that install kyverno policies with OpenEBS using flag 'rbac.kyvernoEnabled=true'.

`helm install openebs openebs/openebs --namespace openebs --create-namespace --set legacy.enabled=false --set cstor.enabled=true --set openebs-ndm.enabled=true`

3.Check the list of policies which has been created by using.

`kubectl get pol`