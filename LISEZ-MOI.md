# Site public de Mikhmon

Page d'accueil (`index.html`) en français et en anglais, avec les boutons de téléchargement, les guides d'installation et la politique de confidentialité (`confidentialite.html`).

- **Adresse du site** : https://abousoumahoro.github.io/mikhmon/
- **Fichiers téléchargés** : page Releases du dépôt public `Abousoumahoro/mikhmon`, toujours la dernière version (noms fixes : `Mikhmon-android.apk`, `Mikhmon-windows.exe`, `Mikhmon-linux.AppImage`, `Mikhmon-iphone.ipa`).
- **Réglages** : en bas de `index.html`, objet `REGLAGES` (dépôt, numéro WhatsApp, version).

## Mise en place (une seule fois)

1. **Créer le dépôt public** : https://github.com/new → nom `mikhmon` → **Public** → Create repository.
2. **Créer une clé d'accès** : https://github.com/settings/personal-access-tokens/new
   - Nom : `site-mikhmon` ; expiration : 1 an.
   - Repository access : **Only select repositories** → `Abousoumahoro/mikhmon`.
   - Permissions → Repository permissions → **Contents : Read and write**.
   - Generate token, puis copier la clé (elle ne s'affiche qu'une fois).
3. **Donner la clé à GitHub Actions** : dépôt privé `Abousoumahoro/Abousoumahoro` → Settings → Secrets and variables → Actions → **New repository secret** → nom `SITE_TOKEN`, valeur : la clé.
4. **Activer le site** : dépôt public `mikhmon` → Settings → Pages → Source : **Deploy from a branch** → branche `main`, dossier `/ (root)` → Save.

Ensuite, à chaque nouvelle version testée, GitHub Actions publie les applications sur le dépôt public et met le site à jour.
