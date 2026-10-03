# Contributing to Awesome Meshless CAE

Thanks for helping improve this list. Contributions from users and developers of meshless / mesh-free / mesh-light CAE tools are welcome.

## What belongs in this list

A tool is in scope if it avoids or greatly simplifies conventional mesh generation:

- Particle methods (SPH, MPS)
- Lattice Boltzmann Method (LBM)
- Meshfree solid mechanics (EFG, peridynamics, MPM)
- Voxel / immersed boundary methods
- Isogeometric Analysis (IGA)
- AI / surrogate models for simulation

Not in scope: tools that only use conventional FEM/FVM meshes, unrelated general-purpose libraries, and dead links.

## Entry format

One tool per line, in the matching category, in alphabetical order within each group:

```
- 🆓 [Tool Name](https://link) - Short description (one sentence, no trailing marketing words).
- 💼 [Tool Name](https://link) - Short description.
```

- 🆓 = open source, 💼 = commercial.
- Use the official repository or vendor page.
- Do not add the same tool twice. Search the README first.

## Pull request checklist

- [ ] The tool fits a category in the README (or you propose a new one in the PR)
- [ ] Link works and points to an official page
- [ ] OSS: has a license and a commit within the last 24 months (or marked as unmaintained)
- [ ] Description is one sentence and neutral in tone
- [ ] Entry follows the format above and is in alphabetical order
- [ ] No duplicate entry

## Maintainer weekly checklist

Used for the weekly update (direct commits to `main`).

1. **New tools** - search GitHub and vendor news for new meshless / LBM / SPH / MPM / AI-surrogate tools; add worthwhile ones.
2. **Links** - confirm every link opens (fix redirects, remove dead ones).
3. **Maintenance status** - check the last commit of each OSS tool; add "(unmaintained)" if inactive for 24+ months.
4. **Commercial tools** - check vendor pages for renamed or discontinued products.
5. **Caveats / How to Choose** - revise if the guidance has changed.
6. **Commit** - use a clear message such as `Weekly update: add X, fix links`.

## Reporting problems

Open an issue for broken links, wrong descriptions, or tool suggestions.

## License

By contributing, you agree that your contributions are released under CC0 1.0.
