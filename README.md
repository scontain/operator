# SCONE operator

The [SCONE Kubernetes operator](https://sconedocs.github.io/1_scone_operator/) facilitates a declarative description of SCONE-related custom resources. These custom resources include

- SCONE CAS (`cas.services.scone.cloud`): deploys a high-availability CAS using a primary/backup approach.
- SCONE LAS (`las.base.scone.cloud`): deploys local attestation service on all SGX-capable nodes of a Kubernetes cluster,
- SCONE SGXPlugin (`las.base.scone.cloud`): identifies and labels all SGX-capable Kubernetes nodes and ensures that containers can use SGX on these nodes,
- SCONE signed policies (`signedpolicies.cas.scone.cloud`): security policies uploaded to CAS via 
- SCONE signed and encrypted policies (`encryptedpolicies.cas.scone.cloud`), and
- confidential Vault (`vaults.services.scone.cloud`).

These custom resources are associated with controllers bringing or keeping these resources in their target state. For each of these custom resources, a custom resource definition (CRD) specifies how to define a custom resource.

This repo contains the helm chart to install the SCONE Operator. We maintain a [script](https://sconedocs.github.io/2_operator_installation/#tldr) to install 

- the SCONE operator, and 
- LAS, SGXPlugin, as well as 
- our [`kubectl provision` plugin](https://sconedocs.github.io/5_kubectl/)
