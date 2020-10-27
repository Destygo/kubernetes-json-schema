# kubernetes-json-schema

A repo to host custom resource definitions to be use with `kubeval`. Fixes this [issue](https://github.com/instrumenta/kubeval/issues/47).

1. Obtain the link to the YAML for the CRD you want to validate and add it to build.sh

2. Run build.sh

3. Upload the resulting schema on github, in a repository that container the `master-standalone` folder at the root (you can use a branch different from `master`, just amend the `--additional-schema-locations` flag below).

4. Validate CRDs:

```bash
kubeval --additional-schema-locations https://raw.githubusercontent.com/Destygo/kubernetes-json-schema/master
```

## Requirements

You need to install `yq` and `sponge` to run the script `build.sh`
