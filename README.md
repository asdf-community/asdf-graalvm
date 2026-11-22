# asdf-graalvm

[GraalVM](https://www.graalvm.org/) plugin for [asdf](https://github.com/asdf-vm/asdf) version manager

## Install

```shell
asdf plugin-add graalvm https://github.com/asdf-community/asdf-graalvm.git
```

## Use

Check [asdf](https://github.com/asdf-vm/asdf) readme for instructions on how to install & manage versions of Graal.

### Liberica Native Image Kit

[BellSoft Liberica NIK](https://bell-sw.com/pages/downloads/native-image-kit/) JDK 25
releases use the `liberica-nik-` prefix. The plugin selects the standard bundle
for macOS or Linux (glibc or musl) on x86_64 or AArch64 and checks its SHA-256
digest before extracting it.

```shell
asdf list all graalvm liberica-nik-
asdf install graalvm latest:liberica-nik-
```

The Liberica installer requires `curl`, `jq`, `tar`, and either `sha256sum` or `shasum`.
