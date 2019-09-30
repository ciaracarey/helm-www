## helm fetch

Download a chart from a repository and (optionally) unpack it in local directory

### Synopsis


Retrieve a package from a package repository, and download it locally.

This is useful for fetching packages to inspect, modify, or repackage. It can
also be used to perform cryptographic verification of a chart without installing
the chart.

There are options for unpacking the chart after download. This will create a
directory for the chart and uncompress into that directory.

If the --verify flag is specified, the requested chart MUST have a provenance
file, and MUST pass the verification process. Failure in any part of this will
result in an error, and the chart will not be saved locally.


```
helm fetch [flags] [chart URL | repo/chartname] [...]
```

### Options

```
      --ca-file string       Verify certificates of HTTPS-enabled servers using this CA bundle
      --cert-file string     Identify HTTPS client using this SSL certificate file
  -d, --destination string   Location to write the chart. If this and tardir are specified, tardir is appended to this (default ".")
      --devel                Use development versions, too. Equivalent to version '>0.0.0-0'. If --version is set, this is ignored.
  -h, --help                 help for fetch
      --key-file string      Identify HTTPS client using this SSL key file
      --keyring string       Keyring containing public keys (default "~/.gnupg/pubring.gpg")
      --password string      Chart repository password
      --prov                 Fetch the provenance file, but don't perform verification
      --repo string          Chart repository url where to locate the requested chart
      --untar                If set to true, will untar the chart after downloading it
      --untardir string      If untar is specified, this flag specifies the name of the directory into which the chart is expanded (default ".")
      --username string      Chart repository username
      --verify               Verify the package against its signature
      --version string       Specific version of a chart. Without this, the latest version is fetched
```

### Options inherited from parent commands

```
      --debug                           Enable verbose output
      --home string                     Location of your Helm config. Overrides $HELM-HOME (default "~/.helm")
      --host string                     Address of Tiller. Overrides $HELM-HOST
      --kube-context string             Name of the kubeconfig context to use
      --kubeconfig string               Absolute path of the kubeconfig file to be used
      --tiller-connection-timeout int   The duration (in seconds) Helm will wait to establish a connection to Tiller (default 300)
      --tiller-namespace string         Namespace of Tiller (default "kube-system")
```

### SEE ALSO

* [helm](../../docs/helm/#helm)	 - The Helm package manager for Kubernetes.

###### Auto generated by spf13/cobra on 16-May-2019