# Context Codec: Rate-Distortion Optimization for Persistent LLM State

**Author**: Tae-Seon Oh
**DOI**: [10.5281/zenodo.19250206](https://doi.org/10.5281/zenodo.19250206)

---

## Abstract

Stateful LLM systems must decide how much prior context to include in each inference window. We formalize this as a rate-distortion (R-D) problem: minimizing token budget (rate) while maximizing Behavioral Consistency Score (BCS), a probe-based metric measuring how faithfully encoded state reconstructs target operating behavior. Applying R-D theory to a longitudinal personal AI assistant deployment, validated with subject ≠ judge model separation (subject: claude-opus-4-6; judge: claude-sonnet-4-6), we find: (1) an R-D curve knee at ~992 tokens (BCS rising from 0.480 at zero context to 0.954 at the knee), above which additional tokens yield diminishing returns; (2) a Scalable Vector Context (SVC) layered encoding scheme at 518 tokens outperforms random selection at 730 tokens by +0.10 BCS; (3) the structure advantage replicates across 10 synthetic personas (knee detected in 10/10). These results establish that compression structure rather than token count determines reconstruction quality in persistent LLM deployments.

---

## Key Findings

- R-D curve knee at **~992 tokens** (BCS 0.480 → 0.954); beyond this, additional tokens yield diminishing returns
- **Scalable Vector Context (SVC)** at 518 tokens outperforms random 730-token selection by +0.10 BCS
- Structure advantage replicates across **10 synthetic personas** (knee detected 10/10)

---

## Files

```
context_codec_arxiv.pdf       — Final PDF
arxiv_submission/
  main.tex                    — LaTeX source
  references.bib              — BibTeX bibliography
figures/
  rd_curve.pdf                — R-D curve figure (vector)
  rd_curve.png                — R-D curve figure (raster)
```

---

## Citation

```bibtex
@misc{oh2026contextcodec,
  title   = {Context Codec: Rate-Distortion Optimization for Persistent {LLM} State},
  author  = {Oh, Tae-Seon},
  year    = {2026},
  doi     = {10.5281/zenodo.19250206},
  url     = {https://doi.org/10.5281/zenodo.19250206}
}
```

---

## License

MIT License — see [LICENSE](LICENSE).
