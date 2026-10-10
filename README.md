# NeuroLipin — Multi-Level Structural & Functional Annotation of Neuropilin-2 (NRP2)

An integrated in-silico study of NRP2, a transmembrane co-receptor in neuronal signalling and angiogenesis, combining sequence, topology, domain, structure and interaction-network evidence.

## Live links

- **Website (GitHub Pages):** https://harshini-suresha.github.io/neurolipin/
- **Source code:** https://github.com/Harshini-Suresha/neurolipin
- **Notebook in Colab:** https://colab.research.google.com/github/Harshini-Suresha/neurolipin/blob/main/NeuroLipin.ipynb
- **Notebook file (.ipynb):** https://github.com/Harshini-Suresha/neurolipin/blob/main/NeuroLipin.ipynb

## What's inside

| File | What it is | Where it runs |
|---|---|---|
| `index.html` | Interactive static website (workflow tabs, domain map, network topology, force-directed + circular interactomes, Live Sequence Lab, MSA studio, 3D explorer, generative art) | GitHub Pages (free, no server) |
| `NeuroLipin.ipynb` | Companion notebook: UniProt fetch (O60462), ProtParam-style properties, hydropathy + TM scan, domain map, interactome, cleavage counts | Colab / Jupyter |

The notebook reproduces the core sequence-level calculations from the site in Python (`numpy` + `matplotlib` only); the site re-implements them in JavaScript for in-browser interactivity.

## Analysis layers (8) and tools (20)

1. Sequence comparison — Clustal Omega, BLAST, COBALT
2. Physicochemical — UniProt, ProtParam
3. Membrane topology — TMHMM, DeepTMHMM
4. Proteolysis — PeptideCutter
5. Domains & motifs — InterProScan, PROSITE, CDD, PDBsum
6. 3D structure — PDB, Mol*
7. Interactions — IntAct, STRING
8. Cross-reference — DATAVSE, OPM, PDBTM, TOPCONS

See the **Methods in depth** section on the site for algorithm, contribution and limitation of each layer.

## Run locally

```bash
# Static website (no server needed)
open index.html

# Notebook
pip install -r requirements.txt
jupyter notebook NeuroLipin.ipynb
```

## Open in Colab

No setup needed once pushed. Just visit:

```
https://colab.research.google.com/github/Harshini-Suresha/neurolipin/blob/main/NeuroLipin.ipynb
```

## Turn on the website (GitHub Pages)

1. Push (see below).
2. GitHub repo → **Settings → Pages**.
3. **Source:** Deploy from a branch → **Branch:** `main`, folder `/ (root)`.
4. Save. Site is live at `https://harshini-suresha.github.io/neurolipin/` in ~1 min.

## Push to GitHub

```bash
git init
git add index.html NeuroLipin.ipynb requirements.txt README.md .gitignore .nojekyll
git commit -m "NeuroLipin: website, notebook, pages"
git branch -M main
git remote add origin https://github.com/Harshini-Suresha/neurolipin.git
git push -u origin main
```

Contact: harshinisuresha7@gmail.com
