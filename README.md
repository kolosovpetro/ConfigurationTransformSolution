# File Transform Automation

Automate configuration file transformations using Azure DevOps or GitHub Actions pipelines.

## Features

### Replace Tokens

- Scans specified files for tokens like `#{VariableName}#`
- Replaces each token with the corresponding pipeline or environment variable value
- Supports any text format

### FileTransform@2 (Azure DevOps)

- Supports XML and JSON configuration file transformations
- Automatically substitutes values from pipeline variables
- XML transformations support XDT transforms (Windows only)
- JSON substitutions update specified key paths

## Supported Pipelines

### Azure DevOps

- Token replacement via [Replace Tokens task](https://marketplace.visualstudio.com/items?itemName=qetza.replacetokens)
- XML/JSON substitution via [FileTransform@2 task](https://learn.microsoft.com/en-us/azure/devops/pipelines/tasks/reference/file-transform-v2?view=azure-pipelines)

### GitHub Actions

- Token and JSON substitution via [devops-actions/variable-substitution](https://github.com/devops-actions/variable-substitution)
- Token and JSON substitution [Example](https://github.com/kolosovpetro/AzureAppServiceDeployments/blob/master/.github/workflows/app-service-deploy.yml)

## Changelog

### v1.0.0 - In Progress

#### Changed

- Implemented `ReplaceTokens` transformation pipeline
- Implemented `FileTransform@2` XML transformation pipeline (Windows only)
- Implemented `FileTransform@2` JSON transformation pipeline
