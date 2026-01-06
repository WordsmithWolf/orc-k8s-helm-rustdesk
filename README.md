# RustDesk Helm Chart

A Helm chart for deploying RustDesk self-hosted server on Kubernetes with ARM64 support and Bitwarden Secrets Manager integration.

## Features

- 🏗️ Complete RustDesk server deployment (hbbs + hbbr)
- 🔐 Bitwarden Secrets Manager integration for secure key management
- 🎯 ARM64/Raspberry Pi optimized
- 🌐 MetalLB LoadBalancer support
- 📦 Persistent storage for encryption keys
- 🔑 Automatic key extraction and management
- 📊 Optional Ingress for web clients

## Quick Start

### Add Helm Repository

```bash
helm repo add rustdesk https://sachajw.github.io/orc-k8s-helm-rustdesk/
helm repo update
```

### Install Chart

```bash
helm install rustdesk-server rustdesk/rustdesk-server \
  --namespace netops-systems \
  --create-namespace
```

## Documentation

- [Installation Guide](charts/rustdesk-server/README.md)
- [Quick Start Guide](charts/rustdesk-server/QUICKSTART.md)
- [Bitwarden Integration](charts/rustdesk-server/BITWARDEN_INTEGRATION.md)
- [Publishing to Artifact Hub](charts/rustdesk-server/PUBLISHING.md)

## Configuration

See [values.yaml](charts/rustdesk-server/values.yaml) for configuration options.

### Key Configuration Examples

#### Enable Bitwarden Integration

```yaml
bitwarden:
  enabled: true
  organizationId: "your-org-id"
  secretMappings:
    - bwSecretId: "your-secret-uuid"
      secretKeyName: PUBLIC_KEY
```

#### Configure MetalLB

```yaml
loadBalancer:
  enabled: true
  annotations:
    metallb.universe.tf/allow-shared-ip: "rustdesk"
    metallb.universe.tf/loadBalancerIPs: "192.168.1.100"
```

#### ARM64 Node Selection

```yaml
hbbs:
  nodeSelector:
    kubernetes.io/arch: arm64

hbbr:
  nodeSelector:
    kubernetes.io/arch: arm64
```

## Requirements

- Kubernetes 1.19+
- Helm 3.0+
- LoadBalancer service support (e.g., MetalLB)
- Optional: Bitwarden Secrets Manager for production deployments

## Port Requirements

The following ports need to be accessible:

- **21115** (TCP): NAT type test
- **21116** (TCP/UDP): ID registration and heartbeat
- **21117** (TCP): Relay service
- **21118** (TCP): Web client support (optional)
- **21119** (TCP): Web client support (optional)

## Support

For issues, questions, or contributions, please visit:
- [GitHub Issues](https://github.com/sachajw/orc-k8s-helm-rustdesk/issues)
- [RustDesk Documentation](https://rustdesk.com/docs/)

## License

MIT License - See [LICENSE](LICENSE) file for details

## Maintainers

- Sacha Wharton (@sachajw)
