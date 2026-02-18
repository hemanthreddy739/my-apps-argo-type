# helm-note-app

This repository contains a Helm chart for deploying the `note-app` container image.

## Chart Details

The chart is located in the `note-app` directory and includes:

- `Deployment` with configurable replica count, resource requests/limits, probes, and security context.
- `Service` exposing the application on port 80.
- Template helpers for consistent naming and labels.

## Usage

```bash
# install the chart
helm install my-note-app ./note-app \
  --set image.repository=hemanthreddy739/note-app \
  --set image.tag=v1.0.0

# upgrade
helm upgrade my-note-app ./note-app --set image.tag=v1.0.1

# uninstall
helm uninstall my-note-app
```

Adjust values in `note-app/values.yaml` or override with `--set`/`--values` as needed.
