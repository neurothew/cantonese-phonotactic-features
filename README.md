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

The computation procedures in brief:
1. Use [pycantonese](https://github.com/jacksonllee/pycantonese) to parse HKCanCor sentences into jyutping
2. Set `onset` as the initial, merge `nucleus` and `coda` as the final.
3. Map initials and finals to their corresponding IPA representations.
4. After mapping, compute initial/final surprisal values.
5. The tone surprisal values can then be computed after step 4.

The two output dataframes are:
1. `hkcancor_initial_final_ipa_surprisal.xlsx` - surprisal values for initials and finals
2. `hkcancor_tone_surprisal` - surprisal values for tones, conditioned on initials and finals

Note that these values are thus specific to the HKCanCor corpus, and therefore may not generalize well to other Cantonese speech materials.

