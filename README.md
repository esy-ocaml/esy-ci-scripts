[![Build Status](https://bryphe.visualstudio.com/esy-ci-scripts/_apis/build/status/bryphe.esy-ci-scripts)](https://bryphe.visualstudio.com/esy-ci-scripts/_build/latest?definitionId=11)

# esy-ci-scripts
##### Azure CI Pipeline for building esy projects

## Why?

I've been moving many of my personal projects to Azure CI, for the following reasons:

- Cross-platform support
- Consistent language for builds on all platforms
- Concurrent builds in free tier

And I've been using essentially the same config for most platforms. 

## Usage

- Copy [`azure-pipelines.yml`](azure-pipelines.yml) and [`esy-build-steps.yml`](esy-build-steps.yml) to your project's directory
- Create a new [build pipeline](https://dev.azure.com) for your project in Azure DevOps

You can see the example pipeline in action [here](https://bryphe.visualstudio.com/esy-ci-scripts/_build?definitionId=11).

## Customization

- For steps that need to be run on all platforms, modify `esy-build-steps.yml`.
- For steps that need to be run on a single machine / platform, modify `azure-pipelines.yml`

## Examples

- [Revery](https://github.com/bryphe/revery)
- [Rejest](https://github.com/bryphe/rejest)
- [Reason-reactify](https://github.com/bryphe/reason-reactify)
- [Reason-glfw](https://github.com/bryphe/reason-glfw)
- [esy-freetype2](https://github.com/esy-packages/esy-freetype2)
- [esy-harfbuzz](https://github.com/esy-packages/esy-harfbuzz)

## Special Thanks

- [Azure DevOps](https://azure.microsoft.com/en-us/services/devops/) for the great tooling!
- @ulrikstrid for teaching me everything I know about Azure CI :)

## License

[MIT License](LICENSE)
