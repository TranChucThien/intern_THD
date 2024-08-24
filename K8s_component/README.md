# K8s Component Metrics Collection with Datadog Integration

## Project Description
This project stores the source code and configurations required to collect metrics from various Kubernetes components using Datadog Integration. The components covered include:

- kube-controller-manager
- kube-proxy
- kube-apiserver
- kube-scheduler
- kubelet

## Notes
- Ensure that the Kubernetes components are accessible from the Datadog Agent.
- Create services for the pods of the Kubernetes components to enable Datadog auto-discovery.
- Validate your configuration by checking the Datadog dashboard for the metrics.
- Use the following command to apply the manifest files:
  ```bash
  kubectl apply -f <manifest-file>

## How to Collect Kubernetes Component Metrics

### 1. Enable Metrics for Kubernetes Components
To collect metrics from Kubernetes components, you need to enable them by modifying the manifest file of the specific component. This can be done by setting the `--bind-address` flag.

Refer to the sample configurations in the provided `K8s_component_metrics.docx` file for details on how to configure each component.

### 2. Test the Metric Endpoint
Once the metrics are enabled, you can test the endpoints by using `curl`. Example:

```bash
curl http://<component-bind-address>:<port>/metrics  
