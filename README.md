Shield: [![CC BY 4.0][cc-by-shield]][cc-by]

This work is licensed under a
[Creative Commons Attribution 4.0 International License][cc-by].

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg

# cantonese-phonotactic-features
Cantonese phonotactic features including initial, final and tone surprisal values

From the [HKCanCor](https://github.com/fcbond/hkcancor) corpus, the surprisal values for Cantonese initial, final and tones are computed.

Run everything in `code\compute_subsyllabic_surprisal_hkcancor.ipynb` to reproduce the results.

The computation procedures in brief:
1. Use [pycantonese](https://github.com/jacksonllee/pycantonese) to parse HKCanCor sentences into jyutping
2. Set `onset` as the initial, merge `nucleus` and `coda` as the final.
3. Map initials and finals to their corresponding IPA representations.
4. After mapping, compute initial/final surprisal values.
5. The tone surprisal values can then be computed after step 4.

The two output dataframes are:
1. `output\hkcancor_initial_final_ipa_surprisal.xlsx` - surprisal values for initials and finals
2. `output\hkcancor_tone_surprisal` - surprisal values for tones, conditioned on initials and finals

The `code\jyutping_ipa_mapping.xlsx` file required for running the code is created manually based on the mapping provided in https://jyutping.org/blog/table/.

Note that these values are thus specific to the HKCanCor corpus, and therefore may not generalize well to other Cantonese speech materials.

We appreciate you cite the following paper if it's useful for you:

Ma, M. K.-H., Fong, M. C.-M., Feng, Y., Li, C. P.-H., & Wang, W. S. (2025). More than a feeling: Expressive style influences cortical speech tracking in subjective cognitive decline (No. arXiv:2509.21277). arXiv. https://doi.org/10.48550/arXiv.2509.21277
