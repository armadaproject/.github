<img src="https://raw.githubusercontent.com/armadaproject/armada/efa679c8d637d3b74bb71b787bb22e39f2bd0209/logo.svg" width="200"/>

Armada is a [CNCF](https://www.cncf.io/) Sandbox project used in production at [G-Research](https://www.gresearch.co.uk/).
It was written by G-Research, with contributions from [G-Research Open Source](https://opensource.gresearch.co.uk/) members
and others.

For an overview of Armada, see these videos:

- [Armada - high-throughput batch scheduling](https://www.youtube.com/watch?v=FT8pXYciD9A)
- [Building Armada - Running Batch Jobs at Massive Scale on Kubernetes](https://www.youtube.com/watch?v=B3WPxw3OUl4)

The Armada Project adheres to the CNCF [Code of Conduct](https://github.com/cncf/foundation/blob/master/code-of-conduct.md).

Armada is a multi-[Kubernetes](https://kubernetes.io/docs/concepts/overview/) cluster batch job scheduler.

Armada is designed to address the following issues:

1. A single Kubernetes cluster cannot be scaled indefinitely, and managing very large Kubernetes clusters is [challenging](https://openai.com/blog/scaling-kubernetes-to-7500-nodes/). Hence, Armada is a multi-cluster scheduler built on top of several Kubernetes clusters.
2. Achieving very high throughput using the in-cluster storage backend, etcd, is [challenging](https://etcd.io/docs/v3.5/op-guide/performance/). Hence, queueing and scheduling is performed partly out-of-cluster using a specialized storage layer.

Armada is designed primarily for machine learning, AI, and data analytics workloads, and to:

- Manage compute clusters composed of tens of thousands of nodes in total.
- Schedule a thousand or more pods per second, on average.
- Enqueue tens of thousands of jobs over a few seconds.
- Divide resources fairly between users.
- Provide visibility for users and admins.
- Ensure near-constant uptime.

## Documentation

For an overview of the architecture and design of Armada, and instructions for submitting jobs, see:

- [System overview](https://github.com/armadaproject/armada/blob/master/docs/design.md)
- [User guide](https://github.com/armadaproject/armada/blob/master/docs/user.md)
- [Quickstart](https://github.com/armadaproject/armada/blob/master/docs/quickstart/index.md)

We expect readers of the documentation to have a basic understanding of Docker and Kubernetes; see, e.g., the following links:

- [Docker overiew](https://docs.docker.com/get-started/overview/)
- [Kubernetes overview](https://kubernetes.io/docs/concepts/overview/)
