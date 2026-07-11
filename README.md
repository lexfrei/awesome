# Awesome lexfrei

> A curated list of my pet projects and open-source work — mostly Go, Kubernetes, and self-hosting.

Everything lives at [github.com/lexfrei](https://github.com/lexfrei).

## Contents

- [Kubernetes — controllers and operators](#kubernetes--controllers-and-operators)
- [Helm charts](#helm-charts)
- [GitOps and infrastructure](#gitops-and-infrastructure)
- [Terraform](#terraform)
- [Claude Code](#claude-code)
- [MCP servers](#mcp-servers)
- [Libraries](#libraries)
- [Bots and apps](#bots-and-apps)
- [Hardware, 3D printing, networking](#hardware-3d-printing-networking)
- [Beyond my repos](#beyond-my-repos)

## Kubernetes — controllers and operators

- [cloudflare-tunnel-gateway-controller](https://github.com/lexfrei/cloudflare-tunnel-gateway-controller) — Gateway API implemented on top of Cloudflare Tunnel.
- [extractedprism](https://github.com/lexfrei/extractedprism) — per-node TCP load balancer for kube-apiserver, the Talos KubePrism idea as a standalone project.
- [kuberture](https://github.com/lexfrei/kuberture) — publishes Kubernetes EndpointSlices to DNS.
- [ouroboros](https://github.com/lexfrei/ouroboros) — fixes hairpin-NAT for Ingress/Gateway-API behind PROXY protocol.
- [external-dns-unifios-webhook](https://github.com/lexfrei/external-dns-unifios-webhook) — External DNS webhook provider for UniFi OS.
- [wish-operator](https://github.com/lexfrei/wish-operator) — Kubernetes-native, CRD-based wishlist operator with an HTMX web UI.

## Helm charts

[charts](https://github.com/lexfrei/charts) — Helm charts published to GHCR as cosign-signed OCI artifacts and indexed on [Artifact Hub](https://artifacthub.io/packages/search?user=lexfrei); they fill the gaps where upstream ships no usable chart:

- **cloudflare-tunnel** — cloudflared for Zero Trust access without inbound ports.
- **extractedprism** — per-node TCP load balancer for the API server, no VIP/keepalived.
- **system-upgrade-controller** — repackaged Rancher SUC for declarative node upgrades.
- **obico** — self-hosted 3D-print monitoring with AI failure detection.
- **spoolman** — filament spool inventory.
- **transmission** — torrent client.

## GitOps and infrastructure

- [k8s](https://github.com/lexfrei/k8s) — my reference home cluster: ARM64, Cilium (kube-proxy replacement, L2 announcements), HA control plane via extractedprism.
- [cozylex](https://github.com/lexfrei/cozylex) — external-apps catalog for Cozystack.
- [cozyboard](https://github.com/lexfrei/cozyboard) — PR-review board for the cozystack org, a static SPA in TypeScript + Svelte running entirely in the browser.

## Terraform

- [terraform-provider-namedotcom](https://github.com/lexfrei/terraform-provider-namedotcom) — Terraform provider for name.com.
- [terraform-cloudflare-icloud](https://github.com/lexfrei/terraform-cloudflare-icloud) — Cloudflare DNS module for iCloud Mail.
- [terraform-cloudflare-adobe-portfolio](https://github.com/lexfrei/terraform-cloudflare-adobe-portfolio) — Cloudflare DNS module for Adobe Portfolio.

## Claude Code

- [claudeline](https://github.com/lexfrei/claudeline) — Claude Code statusline with real usage limits from the Anthropic API.
- [ccc](https://github.com/lexfrei/ccc) — Claude Code Companions, a third-party plugin marketplace.
- [macro-claude](https://github.com/lexfrei/macro-claude) — live Claude Code session status on a Logitech MX Creative Console.
- [occ](https://github.com/lexfrei/occ) — bridge between Claude Code Channels and OpenClaw Gateway.

## MCP servers

All written in Go.

- [mcp-tg](https://github.com/lexfrei/mcp-tg) — Telegram Client API over MTProto (user account).
- [mcp-loki](https://github.com/lexfrei/mcp-loki) — queries against Grafana Loki logs.
- [mcp-raker](https://github.com/lexfrei/mcp-raker) — monitor and control a Klipper 3D printer via Moonraker.
- [pogo-pvp-mcp](https://github.com/lexfrei/pogo-pvp-mcp) — Pokémon GO PvP: battle simulator, rankings, counters, team builder.
- [mcp-rutracker](https://github.com/lexfrei/mcp-rutracker) — search and .torrent download from RuTracker.
- [mcp-transmission](https://github.com/lexfrei/mcp-transmission) — full Transmission RPC.
- [mcp-lostfilm](https://github.com/lexfrei/mcp-lostfilm) — release feed, search, and .torrent from LostFilm.TV.
- [mcp-myshows](https://github.com/lexfrei/mcp-myshows) — MyShows.me series tracker.
- [mcp-godville](https://github.com/lexfrei/mcp-godville) — Godville hero state for LLMs.

## Libraries

- [keychain](https://github.com/lexfrei/keychain) — cgo-free Go library for the native OS secret store (macOS Keychain, Linux Secret Service, Windows Credential Manager).

## Bots and apps

- [transmission-bot](https://github.com/lexfrei/transmission-bot) — Telegram bot for Transmission.
- [estimator](https://github.com/lexfrei/estimator) — humorous task-time estimator (×π, PERT); live at [eta.lex.la](https://eta.lex.la) and [job.lex.la](https://job.lex.la).

## Hardware, 3D printing, networking

- [sovol-zero-mainline](https://github.com/lexfrei/sovol-zero-mainline) — migrating the Sovol Zero printer to mainline Klipper.
- [piwrt](https://github.com/lexfrei/piwrt) — Raspberry Pi 5 + OpenWrt routing all traffic through an AmneziaWG VPN.

## Beyond my repos

Projects I maintain:

- [Cozystack](https://github.com/cozystack/cozystack) — open-source PaaS and framework for building clouds, a CNCF Sandbox project; maintaining it as part of my work at [Ænix](https://aenix.io).
- [obico-server](https://github.com/TheSpaghettiDetective/obico-server) — self-hosted smart 3D printing platform with AI failure detection.
- [prometheus-ipmi-exporter](https://github.com/prometheus-community/helm-charts/tree/main/charts/prometheus-ipmi-exporter) — Helm chart in prometheus-community.
- [robotlb](https://github.com/Treetscom/robotlb) — Hetzner load balancer controller for bare-metal Kubernetes clusters.

My contributions also landed in [external-dns](https://github.com/kubernetes-sigs/external-dns), [Gateway API](https://github.com/kubernetes-sigs/gateway-api), [MetalLB](https://github.com/metallb/metallb), [jellyfin-helm](https://github.com/jellyfin/jellyfin-helm), and [some 60 more repos](https://github.com/search?q=is%3Apr+is%3Amerged+author%3Alexfrei+-user%3Alexfrei+-org%3Acozystack+-org%3Aaenix-org&type=pullrequests).
