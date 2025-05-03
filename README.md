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
../K8s-Manifest-Templates
├── README.md
├── 01.Core-Architecture
│   ├── README.md
│   ├── manifests
│   │   ├── ConfigMap.yaml
│   │   ├── Endpoints.yaml
│   │   ├── Events.yaml
│   │   ├── Namespace.yaml
│   │   └── Node.yaml
│   └── static-pods
│       ├── cloud-controller-manager.yaml
│       ├── etcd.yaml
│       ├── kube-apiserver.yaml
│       ├── kube-controller-manager.yaml
│       └── kube-scheduler.yaml
├── 02.Workloads-Scheduling
│   ├── README.md
│   ├── advanced
│   │   ├── AdvancedPod.yaml
│   │   ├── PodDisruptionBudget.yaml
│   │   └── PriorityClass.yaml
│   └── controllers
│       ├── CronJob.yaml
│       ├── DaemonSet.yaml
│       ├── Deployment.yaml
│       ├── Job.yaml
│       ├── ReplicaSet.yaml
│       └── StatefulSet.yaml
├── 03.Networking
│   ├── CalicoCNI.yaml
│   ├── EndpointSlice.yaml
│   ├── NetworkPolicy.yaml
│   ├── README.md
│   ├── Service.yaml
│   └── ingress
│       ├── Ingress.yaml
│       └── IngressClass.yaml
├── 04.Storage
│   ├── MultiVolumePod.yaml
│   ├── PersistentVolume.yaml
│   ├── PersistentVolumeClaim.yaml
│   ├── README.md
│   ├── StorageClass.yaml
│   ├── VolumeSnapshot.yaml
│   ├── VolumeSnapshotClass.yaml
│   └── csi
│       ├── CSIDriver.yaml
│       ├── CSINode.yaml
│       └── VolumeAttachment.yaml
├── 05.Security
│   ├── CertificateSigningRequest.yaml
│   ├── Lease.yaml
│   ├── OPAGatekeeperConstraint.yaml
│   ├── PodSecurityAdmission.yaml
│   ├── PodSecurityPolicy.yaml
│   ├── README.md
│   ├── RoleAndClusterRole.yaml
│   ├── RoleBindingAndClusterRoleBinding.yaml
│   ├── Secret.yaml
│   ├── ServiceAccount.yaml
│   └── cert-manager
│       ├── Certificate.yaml
│       └── ClusterIssuer.yaml
├── 06.Observability-Troubleshooting
│   ├── DebugPod.yaml
│   ├── Fluentd.yaml
│   ├── Loki.yaml
│   ├── MetricsServer.yaml
│   ├── README.md
│   └── ServiceMonitor.yaml
├── 07.Cluster-Operations
│   ├── HPA.yaml
│   ├── LimitRange.yaml
│   ├── README.md
│   ├── ResourceQuota.yaml
│   ├── SchedulingAPI.yaml
│   ├── VPA.yaml
│   └── VeleroBackupSchedule.yaml
├── 08.Extensibility-Ecosystem
│   ├── APIService.yaml
│   ├── ArgoCDApplication.yaml
│   ├── CRD.yaml
│   ├── Kustomize.yaml
│   ├── MutatingWebhook.yaml
│   ├── OperatorCRD.yaml
│   ├── README.md
│   ├── ValidatingWebhook.yaml
│   └── istio
│       ├── Gateway.yaml
│       └── VirtualService.yaml
├── 09.Edge-Specialized-Workloads
│   ├── InferenceService.yaml
│   ├── KubeEdgeNode.yaml
│   └── README.md
└── 10.Developer-Experience
    ├── KrewPlugin.yaml
    ├── README.md
    └── Skaffold.yaml

19 directories, 80 files
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

