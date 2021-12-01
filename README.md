# azure-devops-dd-monitor-gate-extension

The Azure Devops extension for adding Datadog monitors as gates. Includes a
listing as well as the source code.

## Notes

- Two manifests are defined, one for development (`vss-extension-dev.json`) and
  one for production (`vss-extension.json`). When testing, the development
  manifest should be used to create a dev .vsix package, which can then be
  uploaded to the marketplace by upgrading the version of the existing dev
  plugin.

## Resources

Packaging commands:
- https://docs.microsoft.com/en-us/azure/devops/extend/publish/overview?view=azure-devops#package-your-extension-in-a-vsix-file

Custom service endpoint docs:
- https://github.com/microsoft/azure-pipelines-extensions/blob/master/docs/authoring/endpoints/serviceEndpoints.md#customizinginputs

Datadog VS Marketplace:
- https://marketplace.visualstudio.com/manage/publishers/datadog

## License

Unless explicitly stated otherwise all files in this repository are licensed
under the Apache 2 License.

This product includes software developed at Datadog
(https://www.datadoghq.com/). Copyright 2021 Datadog, Inc.

