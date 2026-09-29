# Physis-Lang

**Self-Evolving Language as a Physical Representation for Video World Models**

Video world models can produce visually plausible clips that do not follow physical principles. Physis-Lang treats language as a shared representation of physical processes: descriptions make causes, interactions, governing principles, temporal evolution, and effects explicit, and are refined with feedback. The resulting representation connects data curation, model training, and video generation.

## Method

Physis-Lang has three connected stages:

1. **Evolve physical-language guidelines.** A physics-aware critic identifies missing or unsupported claims in captions. An agent uses this feedback to refine shared captioning guidelines while keeping the captioner fixed. PhysCapBench evaluates caption precision and recall and is used to select the evolved guidelines.
2. **Retrieve data for missing physics.** Model deficiencies are expressed as textual physics queries. Language-guided retrieval finds visually diverse videos covering those underrepresented physical processes.
3. **Train and generate.** The evolved language is used to recaption training videos and construct video-language data. At inference, physical descriptions and scene-specific negative descriptions guide generation.

## Evaluation

The paper evaluates physical video generation on four benchmarks:

- [PhyGenBench](https://github.com/OpenGVLab/PhyGenBench): physical commonsense in generated videos.
- [Physics-IQ Verified](https://github.com/google-deepmind/physics-IQ-benchmark): physical outcome fidelity.
- [VideoPhy-2](https://videophy2.github.io/): action-centric physical commonsense; the paper reports the full set and also analyzes its Hard subset.
- **PhyGround**: physical-law adherence, including general quality and physics scores.

Experiments cover Wan and Cosmos backbones. The paper reports consistent improvements across the four benchmarks; its main Cosmos3-Nano comparison and additional backbone results are in the paper and project page.

## Resources

- [Paper (PDF)](./assets/Physis-Lang_arxiv.pdf)
- [Project page](https://elemmire1.github.io/physis-lang/)
- [Interactive overview](https://elemmire1.github.io/physis-lang/#demo)
- [Method figure](https://elemmire1.github.io/physis-lang/assets/method.png)

This repository currently provides the paper and project references. It does not currently contain the model implementation or evaluation code.

## Citation

```bibtex
@misc{lu2026physislang,
  title        = {Physis-Lang: Self-Evolving Language as a Physical Representation for Video World Model},
  author       = {Lu, Liming and Ma, Xianzheng and He, Wenkun and Zhan, Guanqi and Zhao, Yilin and Chen, Junyu and Xu, Mengyao and Fan, Jiaojiao and Ge, Wenhang and Gu, Yuchao and Liu, Yunze and Li, Boyi and Dong, Zhen and Prisacariu, Victor and Liu, Ming-Yu and Han, Song and Cai, Han},
  year         = {2026},
  institution  = {NVIDIA},
  howpublished = {\url{https://elemmire1.github.io/physis-lang/}}
}
```
