# CEAZ SSCS Research Lab

A practical research environment for investigating software supply chain threats through OSINT, static analysis, artifact verification, and runtime behavior analysis.

## Research Workflow Example

```text
Package
  ↓
OSINT
  ↓
Static Analysis
  ↓
Artifact Verification
  ↓
Sandbox Execution
  ↓
Behavior Monitoring
  ↓
Verdict
```

## Core Investigation Areas

- Package trust & maintainer history
- Artifact integrity & provenance
- Malicious behavior analysis
- Dependency & supply chain attacks
- Runtime monitoring

## Core Tooling

| Category | Tools |
|----------|-------|
| Source Analysis | Git, ripgrep, jq |
| SBOM & Verification | Syft, Grype, Cosign |
| Runtime Analysis | strace, tcpdump, tshark, Falco |
| Isolation | Docker |
| Editor | Neovim |

## Research Environment

```text
sscs-lab/
├── research-workbench/
├── sandboxes/
│   ├── python/
│   ├── node/
│   ├── rust/
│   └── go/
├── samples/
├── reports/
└── pcaps/
```

Each ecosystem is analyzed in an isolated sandbox.

## Investigation Process

1. Collect package metadata
2. Review source and build artifacts
3. Verify integrity and provenance
4. Execute in an isolated sandbox
5. Monitor filesystem, processes, and network activity
6. Produce a research verdict

## Common Questions

- Is the maintainer trustworthy?
- Does the published artifact match the source?
- Are dependencies introducing risk?
- Does the package exhibit unexpected behavior?
- Could this be part of a supply chain attack?

## Advanced Isolation (Optional)

- gVisor
- QEMU/KVM
- Suricata
- auditd
- Ghidra
