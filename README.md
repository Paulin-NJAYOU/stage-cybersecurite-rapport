# Rapport de stage — DESS STI — UQO

**Sécurisation des applications SmartClinic et Plateforme OBNL**  
Threat Modeling · Contrôle d'accès · DevSecOps · Tests de pénétration éthiques

---

## Structure du projet

```
rapport-stage/
├── rapport.tex                   # Fichier principal
├── references/
│   └── bibliography.bib          # Bibliographie BibTeX
├── figures/                      # Images et schémas
├── chapitres/
│   ├── introduction.tex          # Chapitre 1
│   ├── etat_art.tex              # Chapitre 2
│   ├── contexte.tex              # Chapitre 3
│   ├── analyse_securite.tex      # Chapitre 4
│   ├── controle_acces.tex        # Chapitre 5
│   ├── devsecops.tex             # Chapitre 6
│   ├── pentest.tex               # Chapitre 7
│   ├── resultats.tex             # Chapitre 8
│   ├── recommandations.tex       # Chapitre 9
│   └── conclusion.tex            # Conclusion
└── .github/
    └── workflows/
        └── compile-latex.yml     # CI/CD GitHub Actions
```

---

## Compilation locale

### Avec `latexmk` (recommandé)
```bash
latexmk -pdf -biber rapport.tex
```

### Manuellement (4 passes)
```bash
pdflatex rapport.tex
biber    rapport
pdflatex rapport.tex
pdflatex rapport.tex
```

---

## Compilation automatique (GitHub Actions)

À chaque `git push`, le workflow `.github/workflows/compile-latex.yml` :
1. Compile `rapport.tex` en `rapport.pdf`
2. Rend le PDF téléchargeable dans l'onglet **Actions → Artifacts**

[![Compiler le rapport LaTeX](https://github.com/VOTRE_USERNAME/VOTRE_DEPOT/actions/workflows/compile-latex.yml/badge.svg)](https://github.com/VOTRE_USERNAME/VOTRE_DEPOT/actions/workflows/compile-latex.yml)

> Remplacez `VOTRE_USERNAME/VOTRE_DEPOT` par vos vraies valeurs.

---

## Synchronisation avec Overleaf

Pour lier Overleaf à ce dépôt GitHub :  
**Overleaf → Menu → GitHub → Connect to GitHub**  
Vous pourrez ensuite faire `Push` / `Pull` directement depuis Overleaf.
