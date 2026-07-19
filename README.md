# Containerlab Workbooks

Hands-on networking labs built with [Containerlab](https://containerlab.dev/).

Each lab includes a Containerlab topology, topology annotations, and a standalone HTML workbook. Workbooks contain lab objectives, configuration steps, checkpoints, verification commands, failure tests, and troubleshooting exercises.

## Repository Structure

```text
routed-access-dual-isp/
├── workbook.html
├── routed-access-dual-isp.clab.yml
└── routed-access-dual-isp.clab.yml.annotations.json
```

Each lab follows the same three-file format:

```text
<lab-name>/
├── workbook.html
├── <lab-name>.clab.yml
└── <lab-name>.clab.yml.annotations.json
```

## Requirements

Requirements vary by lab. Check the workbook before deploying the topology.

General requirements:

- Linux host or virtual machine
- Docker
- Containerlab
- Vendor container images required by the topology
- Web browser for the HTML workbook

Vendor images are not included in this repository. Users must obtain and build required images under applicable vendor licenses.

## Using a Lab

Clone the repository:

```bash
git clone https://github.com/angeljmercado/containerlab-workbooks.git
cd containerlab-workbooks
```

Enter the lab directory:

```bash
cd routed-access-dual-isp
```

Open the HTML workbook in a browser, then deploy the topology:

```bash
sudo containerlab deploy \
  --topo routed-access-dual-isp.clab.yml
```

Follow the workbook steps and checkpoints.

Destroy the lab when finished:

```bash
sudo containerlab destroy \
  --topo routed-access-dual-isp.clab.yml \
  --cleanup
```

## Topology Annotations

Files ending in `.annotations.json` store topology layout and visualization metadata. Keep the annotation file beside its matching topology:

```text
routed-access-dual-isp.clab.yml
routed-access-dual-isp.clab.yml.annotations.json
```

## Notes

- Labs target specific network operating system versions.
- Commands may differ on other software releases.
- Review topology resource requirements before deployment.
- Labs are built for isolated learning environments.
