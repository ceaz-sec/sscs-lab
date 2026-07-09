# Isolation Levels 

| Isolation               | Use Case                                                                         |
| ----------------------- | -------------------------------------------------------------------------------- |
| Docker `--network none` | Safe static inspection and install behavior without outbound communication.      |
| Docker monitored bridge | Observe DNS, HTTP/S, and other network activity.                                 |
| gVisor                  | Analyze higher-risk samples while reducing kernel attack surface.                |
| QEMU/KVM snapshots      | Full-system malware analysis, persistence testing, or suspected escape attempts. |


