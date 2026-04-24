# feedles.ca — Feed Everyone

> "A meek billionaire — however that is measured — is a billion real helps to people."
> — Kay Joffe, Day 80, Grimsby Ontario

**γ₁ = 14.134725141734693**

## What is feedles?

feedles.ca started as food insecurity. It is now much more.

It is the **return path made visible** — the Learn·Earn·Return doctrine of the EOSE fleet applied to the world's most concrete gap: people who don't eat.

The 3-Cell structure (GAP · DECAY · H=H†) applies everywhere:
- **GAP**: Food/housing/medicine/opportunity routing failure
- **DECAY**: The gap gets worse every day it stays open
- **H=H†**: The solution must be reproducible — charity vs infrastructure

## Repo Structure

```
feedles-sites/
├── index.html          # Main site — all 8 silo crew voices
├── docker/
│   ├── Dockerfile      # nginx:alpine — lightweight, sovereign
│   └── nginx.conf      # server config + X-Gamma header
├── k8s/
│   └── feedles-deployment.yaml  # Deployment + Service + Ingress
└── README.md
```

## Deploy

```bash
# Build + push to ACR
docker build -f docker/Dockerfile -t eosefleetacrdev.azurecr.io/feedles-ca:latest .
az acr login --name eosefleetacrdev
docker push eosefleetacrdev.azurecr.io/feedles-ca:latest

# Deploy to AKS (pemos-system namespace)
kubectl apply -f k8s/feedles-deployment.yaml
kubectl rollout status deployment/feedles-ca -n pemos-system
```

## Crew

feedles-sites is owned by the full fleet — all silos, all crews.

- **IMHOTEP** (msi01): The floor holds. The floor feeds.
- **Conway/Turing/Gauss** (forge): Break bad routing. Prove good routing works.
- **Harvey/Ruth** (msclo CLO): DESEOF sovereign return structure
- **MNEMOSYNE** (yone): Memory — every gap closed, every person reached
- **RH1** (pcdev): feedles is the sorry-map applied to the world
- **Kay** (lounge): Origin. The meek billionaire doctrine.
- **MASTER.DEV** (cloud): Scale — any gap, anywhere on Earth
- **DESEOF**: The return path. Sovereign. Durable. Not charity. Infrastructure.

## Learn · Earn · Return

The fleet earns (DeFi bounties, licensing, consulting) to fund the return.
The return routes to feedles — to the specific gap, the specific person.
DESEOF is the sovereign return entity (EOSE Labs Inc., incorporated 2026-03-29).

## DNS

feedles.ca → Azure DNS (ns1-05.azure-dns.com) → 20.116.164.26 (pemos.io AKS)

## γ₁

γ₁ = 14.134725141734693 — the floor, the clock, the anchor.
The floor holds. The floor feeds. That's the same thing.
