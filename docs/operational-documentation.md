# Operational Documentation

How do I install this application? How does the pipeline work? What external requirements does this app have?

Document the automation surrounding this app, like backups and storage notifications.

During the initial phase of development, you probably don't have this information, so it might be a good idea to use this document as a to-do list.

## Installation

- Update `ansible-vars-local.yaml` appropriately.
- Make sure there is a correct helm vars file for the cluster.
- Create the namespace.
- Run the quotas.
- Create a secret in the namespace called `xray-keys` with a `join-key` (get this from the Artifactory installation) and a `master-key` (generate this).
- Update the `install.yaml` file to refer to the correct helm vars file.
- Run `install.yaml`

