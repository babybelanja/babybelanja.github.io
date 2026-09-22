# PT Babybelanja Berkah Bersama — Company Profile

Situs profil perusahaan (holding group) untuk **PT Babybelanja Berkah Bersama**.

- Domain: https://babybelanja.com
- Dibangun dengan **Jekyll 4.4.1**
- Deploy: **GitHub Actions** (`.github/workflows/pages.yml`) — build & deploy otomatis setiap push ke `master`

## Struktur

```
_config.yml              # konfigurasi situs (title, description, url)
_layouts/default.html    # layout utama (head, header, konten, footer)
index.html               # halaman utama (front matter + konten)
404.html                 # halaman tidak ditemukan
assets/css/style.css     # stylesheet
CNAME                    # domain kustom (babybelanja.com)
```

## Menjalankan secara lokal

```sh
bundle install
bundle exec jekyll serve
# buka http://127.0.0.1:4000
```

## Deploy

Push ke branch `master` akan memicu workflow GitHub Actions untuk build dengan
Jekyll 4.4.1 dan menerbitkan situs ke GitHub Pages.

> Pages **Source** harus disetel ke **GitHub Actions** di
> Settings → Pages → Build and deployment.

## Catatan

- `opencode.json` bersifat lokal dan tidak diikutsertakan ke repositori (lihat `.gitignore`).
- `Gemfile.lock` di-commit agar build Actions reprodusibel.
