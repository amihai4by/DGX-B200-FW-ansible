# DGX-B200-FW-ansible

Ansible-based firmware update automation for NVIDIA DGX B200 systems.

## 📦 Components Updated
- BMC
- Motherboard Tray
- GPU Tray (transition + latest)

## 🚀 Usage

1. Edit `inventory/hosts.ini` with your 12 BMC IPs and credentials.
2. Place official `.fwpkg` files in the `files/` folder.
3. Run:

```bash
ansible-playbook -i inventory/hosts.ini playbook.yaml -f 12
```

## ⚠️ Notes
- AC Power Cycle **must** be performed manually after GPU tray final update.
- Ensure no workload or `nvidia-smi` is running during updates.
# DGX-B200-FW-ansible
