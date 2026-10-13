# Throughline demo

Published static build of the custom B2C CRM prototype.

- App: https://jothiram98.github.io/throughline-demo/
- BA & competitor guide: https://jothiram98.github.io/throughline-demo/throughline-ba-review.html

Use synthetic data only. Records are stored in each visitor’s browser, not shared between teammates. No real authentication, messaging or backend is connected.

This repository contains the compiled release and review guide only. Application source and private project documents remain in the development workspace.

## Phase One Prototype

- [Open the interactive Phase One Prototype](https://jothiram98.github.io/throughline-demo/phase-one-prototype/)
- Editable React source: `phase-one-prototype-source/`.
- Publish build: run `npm ci` and `npm run build -- --base ./` in the source directory, then copy `dist/` contents into `phase-one-prototype/`.
- Dark Inter theme, campaign flows and interactive simulated WhatsApp conversations. All records are synthetic; no live provider APIs are connected.
