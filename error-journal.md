# Error Journal

## 2026-03-31 — microk8s certifikáty
**Problém:** microk8s nefungoval po dlhom vypnutí VM
**Príčina:** TLS certifikáty expirovali (platnosť do 20.2.2026)
**Riešenie:** microk8s refresh-certs --cert ca.crt

## 2026-03-31 — git push zlyhal
**Problém:** git push zlyhal na GitHub
**Príčina:** Fine-grained token nefungoval, GitHub nepodporuje heslo
**Riešenie:** Classic Personal Access Token so scope repo

## 2026-03-31 — git credentials
**Problém:** GitHub žiadal token pri každom push
**Príčina:** Token nebol uložený, GitHub nezobrazí token spätne
**Riešenie:** git config --global credential.helper store + zadať token raz
**Poznámka:** Token uložiť hneď pri vytvorení do password managera
