# CNB-STACK

Custom stack for cloud native buildpacks.

## Public Images Available

- [dashaun/cnb-stack-base](https://hub.docker.com/r/dashaun/cnb-stack-base)
- [dashaun/cnb-stack-build](https://hub.docker.com/r/dashaun/cnb-stack-build)
- [dashaun/cnb-stack-run](https://hub.docker.com/r/dashaun/cnb-stack-run)

## Why?

To better understand cloud native buildpacks, and because COBOL was in the news during COVID-19.
We began to build a cloud native buildpack for COBOL.

In order to get [GnuCOBOL](https://sourceforge.net/projects/open-cobol/) compiled into a [cloud native buildpack](https://buildpacks.io), we needed a few extra dependencies.
The best option was to create a new stack.

## Development

To build the stack use the `./build-stack` script:

```text
./build-stack.sh [-p <prefix> -v <version>] <dir>
  -p    prefix to use for images      (default: sample/stack)
  -v    version to tag images with    (default: latest)
  <dir>  directory of stack to build
```

Example:

```bash
./build-stack.sh bionic
```

To use this stack see the [cnb-builder](https://github.com/dashaun/cnb-builder)

### Additional Resources
* [GnuCOBOL on Sourceforge](https://sourceforge.net/projects/open-cobol/)
* [GnuCOBOL Guide](https://open-cobol.sourceforge.io/)
* [Stacks documentation](https://buildpacks.io/docs/using-pack/stacks/)
