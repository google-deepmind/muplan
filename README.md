# μPLAN: Summarizing using a Content Plan as Cross-Lingual Bridge

This repository includes the  plan-annotated data used in our [µPLAN paper](https://aclanthology.org/2024.eacl-long.131/) (EACL 2024).

## Abstract

Cross-lingual summarization aims to generate a summary in one language given input in a different language, allowing for the dissemination of relevant content among different language speaking populations.  The task is challenging mainly due to the paucity of cross-lingual datasets and the compounded difficulty of summarizing *and* translating.
This work presents µPLAN, an approach to cross-lingual summarization that uses an intermediate planning step as a cross-lingual bridge. We formulate the plan as a sequence of entities capturing the summary's content and the order in which it should be communicated. Importantly, our plans abstract from surface form: using a multilingual knowledge base, we align entities to their canonical designation across languages and generate the summary conditioned on this cross-lingual bridge and the input. Automatic and human evaluation on the  XWikis dataset (across four language pairs) demonstrates that our planning objective achieves state-of-the-art performance in terms of informativeness and faithfulness. Moreover, µPLAN models improve the *zero-shot* transfer to new cross-lingual language pairs compared to baselines without a planning component.


## Data
The plan-annotated dataset is available in JSONL format at: [link](https://console.cloud.google.com/storage/browser/xwikis-with-plans). This dataset is derived from [XWikis (Perez-Beltrachini
and Lapata, 2021)](https://github.com/lauhaide/clads). Each *(document, summary)* pair is annotated with a multilingual content plan, stored under the header key `plan`.

## Models
All the models in the paper are based on the [mT5 model (Xue et al., 2021)](https://aclanthology.org/2021.naacl-main.41.pdf) using the checkpoints available at: [link](https://github.com/google-research/multilingual-t5?tab=readme-ov-file#released-model-checkpoints).

## Citing this work
If you use any of the material here, please cite the following paper:

```
@inproceedings{huot-etal-2024-mplan,
    title = "$\mu${PLAN}: Summarizing using a Content Plan as Cross-Lingual Bridge",
    author = "Huot, Fantine  and
      Maynez, Joshua  and
      Alberti, Chris  and
      Amplayo, Reinald Kim  and
      Agrawal, Priyanka  and
      Fierro, Constanza  and
      Narayan, Shashi  and
      Lapata, Mirella",
    editor = "Graham, Yvette  and
      Purver, Matthew",
    booktitle = "Proceedings of the 18th Conference of the European Chapter of the Association for Computational Linguistics (Volume 1: Long Papers)",
    month = mar,
    year = "2024",
    address = "St. Julian{'}s, Malta",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2024.eacl-long.131",
    pages = "2146--2163",
    abstract = "Cross-lingual summarization aims to generate a summary in one languagegiven input in a different language, allowing for the dissemination ofrelevant content among different language speaking populations. Thetask is challenging mainly due to the paucity of cross-lingualdatasets and the compounded difficulty of summarizing andtranslating.This work presents $\mu$PLAN, an approach to cross-lingual summarization that uses an intermediate planning step as a cross-lingual bridge. We formulate the plan as a sequence of entities capturing thesummary{'}s content and the order in which it should becommunicated. Importantly, our plans abstract from surface form: usinga multilingual knowledge base, we align entities to their canonicaldesignation across languages and generate the summary conditioned onthis cross-lingual bridge and the input. Automatic and human evaluation on the XWikis dataset (across four language pairs) demonstrates that our planning objective achieves state-of-the-art performance interms of informativeness and faithfulness. Moreover, $\mu$PLAN modelsimprove the zero-shot transfer to new cross-lingual language pairscompared to baselines without a planning component.",
}
```

## License and disclaimer

Copyright 2024 DeepMind Technologies Limited

The dataset is licensed under the Creative Commons Attribution-ShareAlike 4.0
International License (CC-BY-SA).
You may obtain a copy of the CC-BY-SA license
at:
https://creativecommons.org/licenses/by-sa/4.0/legalcode

Unless required by applicable law or agreed to in writing, all software and
materials distributed here under the CC-BY-SA licenses are
distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND,
either express or implied. See the licenses for the specific language governing
permissions and limitations under those licenses.

This is not an official Google product.
