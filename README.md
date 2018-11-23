# esy-ci-scripts
---
### Azure CI Pipeline for building esy projects

## Why?

I've been moving many of my personal projects to Azure CI from Travis/AppVeyor, for the following reasons:

- Cross-platform support
- Consistent language for builds on all platforms
- Concurrent builds in free tier

And I've been using essentially the same config for most platforms. 

A few projects that are using this setup:
- [Revery](https://github.com/bryphe/revery)
- [Reason-reactify](https://github.com/bryphe/reason-reactify)

## Usage

- Create a new [build pipeline](https://dev.azure.com) for your project in Azure DevOps
- Copy `azure-pipelines.yml` and `esy-build-steps.yml` to your project's directory
- Profit

## Customization

- For steps that need to be run on all platforms, modify `esy-build-steps.yml`.
- For steps that need to be run on a single machine / platform, modify `azure-pipelines.yml`

## Special Thanks

- [Azure DevOps](https://azure.microsoft.com/en-us/services/devops/) for the great tooling!
- @ulrikstrid for teaching me everything I know about Azure CI :)

## License

[MIT License](LICENSE)
