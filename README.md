# esy-ci-scripts
---
### Azure CI Pipeline for building esy projects

## Usage

- Create a new [build pipeline](https://dev.azure.com) for your project in Azure DevOps
- Copy `azure-pipelines.yml` and `esy-build-steps.yml` to your project's directory
- PROFIT

## Customization

- For steps that need to be run on all platforms, modify `esy-build-steps.yml`.
- For steps that need to be run on a single machine / platform, modify `azure-pipelines.yml`

## Special Thanks

- [Azure DevOps](https://azure.microsoft.com/en-us/services/devops/) for the great tooling!
- @ulrikstrid for teaching me everything I know about Azure CI :)

## License

[MIT License](LICENSE)
