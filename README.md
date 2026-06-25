# RCV Site Look Up

**Site Look Up** is a site / network lookup module for the Root Chain Ventures
NOC Portal platform.

This repository is an **operator pointer only**. Site Look Up is distributed as a
container image from GHCR and is installed **through the NOC Portal** — not on
its own.

## License

**RCV Community License 1.0** — free for personal / home-lab use and any
organization's own internal operations; a paid commercial license is required to
offer it to third parties as a hosted/managed/SaaS service. See [`LICENSE`](LICENSE).
Commercial inquiries: **legal@rootchainventures.com**.

## Install

Site Look Up is added from the Portal — you never hand-wire its credentials:

1. Install the **NOC Portal** first — see
   [RCV-NOC-Portal](https://github.com/Root-Chain-Ventures-LLC/RCV-NOC-Portal).
2. Sign in, open **Modules**, choose **Site Look Up**, and click **Install**. The
   Portal mints its OIDC client + API key and deploys it for you — on Docker (via the Portal's bundled deployer) or Kubernetes (in-cluster).


> On Docker you can alternatively scaffold this module manually with `./install.sh add-module site-look-up` from the Portal repo, then register it in the Portal UI.

Image: `ghcr.io/root-chain-ventures-llc/site-look-up`.
