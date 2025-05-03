# K8s-Manifest-Templates

This repository contains a collection of reusable **Kubernetes manifest templates** for common and advanced use cases. It’s designed to **speed up resource creation and editing**, making it easier to test, deploy, and debug Kubernetes workloads without rewriting YAML from scratch.

---

## 🎯 Purpose

* Rapidly scaffold K8s resources from templates
* Modify manifests easily for new environments or use cases
* Reduce boilerplate and ensure consistency
* Act as a reference during development, troubleshooting, or learning

---

## 🗂️ Repository Hierarchy

```text
01.Core-Architecture/
├── A.kube‑apiserver-Static-Pod.yaml
├── B.etcd-Static-Pod.yaml
├── C.kube‑scheduler-Static-Pod.yaml
├── D.kube‑controller‑manager-Static-Pod.yaml
└── E.cloud‑controller‑manager-Static-Pod.yaml

02.Workloads-Scheduling/
├── A.Advanced-Pod-Template.yaml
├── B.Deployment-Template.yaml
├── C.StatefulSet-Template.yaml
├── D.DaemonSet-Template.yaml
├── E.Job-Template.yaml
├── F.CronJob-Template.yaml
└── G.PodDisruptionBudget-Template.yaml

03.Networking/
├── A.Service-Template.yaml
├── B.Ingress-Template.yaml
├── C.NetworkPolicy-Template.yaml
└── D.Calico-CNI-Plugin.yaml

04.Storage/
├── A.Pod-with-Multiple-Volume-Types.yaml
├── B.PersistentVolume-Template-with-CSI.yaml
├── C.PersistentVolumeClaim-Template.yaml
└── D.StorageClass-Template.yaml

05.Security/
├── A.ServiceAccount-Template.yaml
├── B.Role-ClusterRole.yaml
├── C.RoleBinding-ClusterRoleBinding.yaml
├── D.Secret-Template.yaml
├── E.OPA-Gatekeeper-Constraint-Template.yaml
├── F.PodSecurityPolicy-Template.yaml
├── G.CertificateSigningRequest-Templat.yaml
├── H.cert‑manager-Certificate-Template.yaml
└── I.cert‑manager-ClusterIssuer.yaml

06.Observability-Troubleshooting/
├── A.Fluentd-DaemonSet.yaml
├── B.Metrics-Server-Deployment.yaml
├── C.Debug-Pod-Template.yaml
└── D.Loki-Deployment-Snippet.yaml

07.Cluster-Operations/
├── A.Horizontal-Pod-Autoscaler-Template.yaml
├── B.ResourceQuota-Template.yaml
├── C.LimitRange-Template.yaml
└── D.Velero-Backup-Schedule-Template.yaml

08.Extensibility-Ecosystem/
├── A.Kustomize-Example.yaml
├── B.ArgoCD-Application-Template.yaml
├── C.Istio-Gateway-Templates.yaml
├── D.Istio-VirtualService-Templates.yaml
└── E.Operator-CRD-Template.yaml

09.Edge-Specialized-Workloads/
├── A.KubeEdge-Edge-Node-Deployment.yaml
└── B.Kubeflow-InferenceService-Template.yaml

10.Developer-Experience/
├── A.Skaffold-Configuration.yaml
└── B.Krew-Plugin-Manifest.yaml
```

---

## 🚀 Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/MoAboDaif/K8s-Manifest-Templates.git
   ```

2. Choose a manifest, make quick edits, and apply:

   ```bash
   cp K8s-Manifest-Templates/02.Workloads-Scheduling/B.Deployment-Template.yaml deployment.yaml
   vi depolyment.yaml
   kubectl apply -f depolyment.yaml
   ```

3. Modify and reuse as needed for your cluster.

---

## ✅ Notes

* All templates are **baseline examples** — tailor them to match your cluster's specifics (e.g. namespaces, image tags, resource limits).
* Some manifests (e.g., static pods, CNI plugins) require special contexts like kubeadm setup or advanced networking.
* File naming follows an alphabetical prefix to retain a logical order.

