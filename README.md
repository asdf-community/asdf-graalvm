# asdf-graalvm

[GraalVM](https://www.graalvm.org/) plugin for [asdf](https://github.com/asdf-vm/asdf) version manager

## Install

```shell
asdf plugin add graalvm https://github.com/asdf-community/asdf-graalvm.git
```

## Use

Check [asdf](https://github.com/asdf-vm/asdf) readme for instructions on how to install & manage versions of Graal.

`asdf list all graalvm` shows builds available for your operating system and architecture.
Community builds include older Java-suffixed versions such as `22.3.1-java17`, JDK versions such as `25.0.2`, and iteration builds such as `25i5-25.0.5.0.3`.
The plugin requires `curl`, `jq`, and `tar`.
Set `GITHUB_API_TOKEN` if you reach GitHub's unauthenticated API rate limit.

### Liberica Native Image Kit

[BellSoft Liberica NIK](https://bell-sw.com/pages/downloads/native-image-kit/) JDK 25
releases use the `liberica-nik-` prefix. The plugin selects the standard bundle
for macOS or Linux (glibc or musl) on x86_64 or AArch64 and checks its SHA-256
digest before extracting it.

```shell
asdf list all graalvm liberica-nik-
asdf install graalvm latest:liberica-nik-
```

The Liberica installer also requires `sha256sum` or `shasum`.
