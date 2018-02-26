<div style="text-align:right; margin-bottom:50px;" width="90%">
  <a href="motivation/">Motivation</a> |
  <a href="use-cases/">Use Cases</a> |
  <a href="https://github.com/kaml-d/design/issues/new">Leave a comment …</a>
</div>

![KAML-D high level system architecture](img/kaml-d_system-architecture.png)

## System Architecture

KAML-D can be deployed on any cloud (or on-premises) platform that allows you to run Kubernetes. Most of the components are open source. As a SaaS, it integrates with the cloud providers (user) identity management system, on-prem something like LDAP.

Existing open source components KAML-D uses:

- [Kubernetes](https://kubernetes.io/) for workload management and to ensure portability
- [TensorFlow](https://www.tensorflow.org/) for machine learning execution
- [JupyterHub](https://github.com/jupyterhub/jupyterhub) for data scientists (dev/test of algorithms)
- Storage layer: To hold the datasets, [Minio](https://www.minio.io/), [Ceph](https://ceph.com/), as well as cloud-provider specific offerings such as [EBS](https://aws.amazon.com/ebs/), with built-in [dotmesh](https://dotmesh.com/) support for snapshots

New components KAML-D introduces:

- _KAML-D Workbench_: a graphical UI for data scientists, data engineers, developers, and SREs to manage datasets as well as to test and deploy ML algorithms. Builds on the metadata layer to find and visualize datasets. Builds on the storage layer to store and load datasets.
- _KAML-D Metadata Hub_: a data and metadata layer using [PrestoDB](https://prestodb.io/) and [Elasticsearch](https://www.elastic.co/products/elasticsearch) for indexing and querying datasets.
- _KAML-D Observation Hub_: a comprehensive observability suite for SREs and admins (as well as developers on the app level) to understand the health of the KAML-D platform and troubleshoot issues on the platform and application level:
  - [Prometheus](https://prometheus.io/) and [Grafana](https://grafana.com/) for end-to-end metrics and monitoring/alerting
  - [EFK stack](https://kubernetes.io/docs/tasks/debug-application-cluster/logging-elasticsearch-kibana/) for (aggregrated) logging
  - [Jaeger](http://jaegertracing.io/) for (distributed) tracing

The user management and access control part is outside of the scope of KAML-D but standard integration points such as LDAP are offered.

## User Experience

The UX is central to KAML-D. Users can have different roles (data scientists, data engineers, developers, SREs, admins) and for each role the UX should be pleasing and rich. UX over performance, strive for simplicity and cleanliness.

![KAML-D UX](img/kaml-d_ux.png)
