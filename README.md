# The Gorkin Laboratory

Source for [gorkinlab.org](https://gorkinlab.org) — Researching epigenome biology at Emory University.

Built with [al-folio](https://github.com/alshedivat/al-folio). Deploys via GitHub Actions to GitHub Pages on push to `main`.

## Local development

```bash
docker compose pull
docker compose up
```

Site at http://localhost:8080.

## Structure

- `_pages/` — top-level pages (about, research, people, publications, DEI, opportunities)
- `_data/people.yml` — current members and alumni
- `_bibliography/papers.bib` — publications (BibTeX; auto-rendered on the publications page)
- `assets/img/` — images

## Contact

David Gorkin — david.gorkin@emory.edu

---

Theme © [Maruan Al-Shedivat](https://github.com/alshedivat) et al., MIT License. Content © The Gorkin Lab.
