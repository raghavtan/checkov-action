# Checkov IaC security scan action

This Github Action runs [Checkov](https://github.com/bridgecrewio/checkov) against an Infrastructure-as-Code repository. Checkov performs static security analysis of Terraform & CloudFormation Iaac.

## Inputs
(None) 

## Outputs
(None)

## Example usage

```yaml
jobs:
  checkov-job:
    runs-on: ubuntu-latest
    name: checkov-action
    steps:
      - name: Checkout repo
        uses: actions/checkout@v2

      - name: Run Checkov action
        id: checkov
        uses: cmavr8/checkov-action@master
```
Note that this example uses the latest version (`master`) but you could also use `static a version (e.g. `v3`).