# RCV Site Look Up

**Site Look Up** is a site/network lookup module for the Root Chain Ventures NOC
Portal platform.

This repository holds **operator install artifacts only**. Site Look Up is
distributed as a container image and a Helm chart from GHCR; no application
source lives here.

## License

**RCV Community License 1.0** — free for personal / home-lab use and any
organization's own internal operations; a paid commercial license is required to
offer it to third parties as a hosted/managed/SaaS service. See [`LICENSE`](LICENSE).
Commercial inquiries: **legal@rootchainventures.com**.

## Install (recommended: with the Portal)

Site Look Up runs behind the NOC Portal. The simplest path is the platform
umbrella chart — install the Portal and enable this module together. See the
[RCV-NOC-Portal](https://github.com/Root-Chain-Ventures-LLC/RCV-NOC-Portal)
quickstart, then add:

```bash
--set siteLookUp.enabled=true --set siteLookUp.postgres.password=<pg-password>
```

## Install (standalone, advanced)

Install on its own via the generic `rcv-module` chart, pointed at a running
Portal. Copy [`values.example.yaml`](values.example.yaml), fill it in, then:

```bash
helm install site-look-up oci://ghcr.io/root-chain-ventures-llc/helm/rcv-module \
  --version 0.1.0 -n rcv -f values.example.yaml
```

Image: `ghcr.io/root-chain-ventures-llc/site-look-up`.
