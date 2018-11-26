[![Build Status](https://bryphe.visualstudio.com/esy-ci-scripts/_apis/build/status/bryphe.esy-ci-scripts)](https://bryphe.visualstudio.com/esy-ci-scripts/_build/latest?definitionId=11)

# esy-ci-scripts
##### Azure CI Pipeline for building esy projects

## Why?

I've been moving many of my personal projects to Azure CI, for the following reasons:

- Cross-platform support
- Consistent language for builds on all platforms
- Concurrent builds in free tier

And I've been using essentially the same config for most platforms. 

A few projects that are using this setup:
- [Revery](https://github.com/bryphe/revery)
- [Reason-reactify](https://github.com/bryphe/reason-reactify)

## Usage

- Create a new [build pipeline](https://dev.azure.com) for your project in Azure DevOps
- Copy the `.yml` files to your project's directory
- Profit!

You can see the example pipeline in action [here](https://bryphe.visualstudio.com/esy-ci-scripts/_build?definitionId=11).

## Pipeline types

### `basic-esy-project`

This is the minimal `esy` pipeline that builds cross-platform. It simply spins up a windows, linux, and mac machine, and runs `esy install` and `esy build`.

### `basic-esy-project-withcaching`

This is a slightly more advanced variation of the `basic-esy-project` pipeline, that incorporates caching the `esy` store. This is really helpful for Windows, as the `ocaml` compiler can take ~15 minutes to build. 

You can enable the restoration of the cache once you have a green build (and the artifacts have been published) - just uncomment the lines in `azure-pipelines.yml` that reference `restore-build-cache.yml`.

## Customization

- For steps that need to be run on all platforms, modify `esy-build-steps.yml`.
- For steps that need to be run on a single machine / platform, modify `azure-pipelines.yml`

## Special Thanks

- [Azure DevOps](https://azure.microsoft.com/en-us/services/devops/) for the great tooling!
- @ulrikstrid for teaching me everything I know about Azure CI :)

## License

[MIT License](LICENSE)
