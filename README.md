## Add new chart

1. Place the chart in `.helm/charts/<new chart name>`
1. Add dependency for it:
    ```yaml
    .helm/requirements.yaml:
    ===============================
    - name: <new chart name>
      condition: <new chart name>.enabled
      version: ~<major version only, minor/patch not required>
    ```
1. Chart should be disabled by default:
     ```yaml
    .helm/charts/<new chart name>/values.yaml:
    =================================================
    enabled: false
    ```
