<h1 align="center">
The Impact of Large Language Models on Scientific Discovery:
  
A Preliminary Study using GPT-4
</h1>

<div align="center">
<h3>Microsoft Research AI4Science, Microsoft Azure Quantum</h3>
  
[![](https://img.shields.io/badge/paper-arxiv2311.07361-red?style=plastic&logo=GitBook)](https://arxiv.org/abs/2311.07361)

</div>

# Introduction

<p align="center">
  <img src="overview.png" width="1000">
</p>

Large language models (LLMs) have showcased remarkable capabilities across a vast array of domains. In this report, we delve into the performance of **LLMs within the context of scientific discovery**, focusing on GPT-4. Our investigation spans a diverse range of scientific areas encompassing:
* [Drug discovery](#drug-discovery)
* [Biology](#biology)
* [Computational chemistry](#computational-chemistry) (density functional theory (DFT) and molecular dynamics (MD))
* [Materials design](#materials-design)
* [Partial differential equations](#partial-differential-equations) (PDE)

Our exploration methodology primarily consists of **expert-driven case assessments**, which offer qualitative insights into the model's comprehension of intricate scientific concepts and relationships, and occasionally **benchmark testing**, which quantitatively evaluates the model's capacity to solve well-defined domain-specific problems. Our preliminary exploration indicates that **GPT-4 exhibits promising potential for a variety of scientific applications, demonstrating its aptitude for handling complex problem-solving and knowledge integration tasks**. Broadly speaking, we evaluate GPT-4's knowledge base, scientific understanding, scientific numerical calculation abilities, and various scientific prediction capabilities.

# ❤️Contribution Invitation (call for participation)
Though we have initially conducted some preliminary experiments to explore the application prospects of LLM models in scientific discovery (case analyses can be found in our [report](https://arxiv.org/abs/2311.07361)). However, we recognize that this is still far from enough, and the potential of LLM models in this field remains to be tapped.

***Therefore, we hope to advance the development of LLM in scientific discovery through the joint efforts of our community. We have created this GitHub repository to collect interesting findings and feedback on LLM's current capabilities from community members in their exploration process.***

We invite all researchers interested in advancing the capabilities of large language models for scientific discovery applications. Whether you have relevant expertise or not, as long as you think LLM may have value in scientific discovery and hope this area can be further optimized, you are welcome to join us. Every sharing and suggestion will provide reference value for LLM applications in this field. 
Let us work together to explore new frontiers of LLM applications in scientific discovery! 

Some goals of this ongoing project include:

* Reporting novel findings or use cases uncovered through rigorous testing and experimentation
* Providing feedback to help prioritize model enhancements that address key limitations
* Proposing new evaluation benchmarks and experimental protocols
* Discussing interdisciplinary research opportunities and challenges
* Connecting domain experts with NLP researchers to foster collaboration


# ❗Important on how you can contribute
To contribute your discovery, for a template and the details on how to structure your contributions, please see the [Discussions](https://github.com/microsoft/LLM4ScientificDiscovery/discussions) channel and [here](https://github.com/microsoft/LLM4ScientificDiscovery/discussions/2#discussion-6071507) is a specific case a template. 

**We look forward to your participation and sharing!**


# Observation and Summary
We summarize what we have observed in our report to let you have some initial understanding of our evaluation.
👍represents strength of the abilities, 😵 represents the abilities need to be improved. 

## Drug Discovery
* 👍***Broad Knowledge***: GPT-4 demonstrates a wide-ranging understanding of key concepts in drug discovery, including individual drugs, target proteins, general principles for small-molecule drugs, and the challenges faced in various stages of the drug discovery process. 
* 👍***Versatility in Key Tasks***: LLMs, such as GPT-4, can help in several essential tasks in drug discovery, including Molecule Manipulation, Drug-Target Binding Prediction, Molecule Property Prediction, Retrosynthesis Prediction and so on.
* 👍***Novel Molecule Generation***: GPT-4 can be used to generate novel molecules following text instruction. This de novo molecule generation capability can be a valuable tool for identifying new drug candidates with the potential to address unmet medical needs.
* 👍***Coding capability***: GPT-4 can provide help in coding for drug discovery, offering large benefits in data downloading, processing, and so on. The strong coding capability of GPT-4 can greatly ease human efforts in the future.
* 😵***SMILES Sequence Processing Challenges***: GPT-4 may struggle with directly processing SMILES sequences. To improve the model’s understanding and output, it is better to provide the names of drug molecules along with their descriptions, if possible.
* 😵***Limitations in Quantitative Tasks***: GPT-4 may face limitations when it comes to quantitative tasks, such as predicting numerical values for molecular properties and drug-target binding. Researchers are advised to take GPT-4’s output as a reference and perform verification using dedicated AI models or scientific computational tools to ensure reliable conclusions.
* 😵***Double-Check Generated Molecules***: When generating novel molecules with GPT-4, it is essential to verify the validity and chemical properties of the generated structures.


## Biology 
* 👍***Bioinformation Processing***: GPT-4 displays its understanding of information processing from specialized files in biological domains, such as MEME format, FASTQ format, and VCF format. Furthermore, it is adept at performing bioinformatic analysis with given tasks and data, exemplified by predicting the signaling peptides for a provided sequence.
* 👍***Biological Understanding***: GPT-4 demonstrates a broad understanding of various biological topics, encompassing consensus sequences, PPI, signaling pathways, and evolutionary concepts. 
* 👍***Biological Reasoning***: GPT-4 possesses the ability to reason about plausible mechanisms from biological observations using its built-in biological knowledge.
* 👍***Biological Assisting***: GPT-4 demonstrates its potential as a scientific assistant in the realm of protein design tasks, and in wet lab experiments by translating experimental protocols for automation purposes.
* 😵***FASTA Sequence Understanding***: A notable challenge for GPT-4 is the direct processing of FASTA sequences. It is preferable to supply the names of biomolecules in conjunction with their sequences when possible.
* 😵***Inconsistent Result***: GPT-4’s performance on tasks related to biological entities is influenced by the abundance of information pertaining to the entities. Analysis of under-studied entities, such as transcription factors, may yield inconsistent results.
* 😵***Arabic Number Understanding***: GPT-4 struggles to directly handle Arabic numerals; converting Arabic numerals to text is recommended.
* 😵***Quantitative Calculation***: While GPT-4 excels in biological language understanding and processing, it encounters limitations in quantitative tasks (Fig. 3.7). Manual verification or validation with alternative computational tools is advisable to obtain reliable conclusions.



## Computational Chemistry
* 👍***Literature Review***: GPT-4 possesses extensive knowledge of computational chemistry, covering topics such as density functional theory, Feynman diagrams, and fundamental concepts in electronic structure theory, molecular dynamics simulations, and molecular conformation generation. 
* 👍***Code Development***: GPT-4 is able to assist with the implementation of novel algorithms or functionality in existing computational chemistry and physics software packages.
* 👍***Method Selection***: GPT-4 is able to recommend suitable computational methods and software packages for specific research problems, taking into account factors such as system size, timescales, and level of theory.
* 👍***Simulation Setup***: GPT-4 is able to aid in preparing simple molecular-input structures, establishing and suggesting simulation parameters, including specific symmetry, density functional, time step, ensemble.
* 👍***Experimental, Computational, and Theoretical Guidance***: GPT-4 is able to assist researchers by providing experimental, computational, and theoretical guidance.
* 😵***Hallucinations***: GPT-4 may occasionally generate incorrect information. It may struggle with complex logic reasoning. Researchers need to independently verify and validate outputs and suggestions from GPT-4. 
* 😵***Raw Atomic Coordinates***: GPT-4 is not adept at generating or processing raw atomic coordinates of complex molecules or materials. However, with proper prompts that include molecular formula, name, or other supporting information, GPT-4 may still work for simple systems. 
* 😵***Precise Computation***: GPT-4 is not proficient in precise calculations in our evaluated benchmarks and usually ignores physical priors such as symmetry and equivariance/invariance. Currently, the quantitative numbers returned by GPT-4 may come from a literature search or few-shot examples. It is better to combine GPT-4 with specifically designed scientific computation packages or machine learning models, such as Graphormer and DiG.
* 😵***Hands-on Experience***: GPT-4 can only provide guidance and suggestions but cannot directly perform experiments or run simulations. Researchers will need to set up and execute simulations or experiments by themselves or leverage other frameworks based on GPT-4, such as AutoGPT , HuggingGPT, AutoGen and so on.


## Materials Design
* 👍***Information memorization***: Excels in memorizing information and suggesting design principles for inorganic crystals and polymers. Its understanding of basic rules for materials design in textual form is remarkable. For instance, when designing solid-state electrolyte materials, it can competently propose ways to increase ionic conductivity and provide accurate examples.
* 👍***Composition Creation***: Proficient in generating feasible chemical compositions for new inorganic materials.
* 👍***Synthesis Planning***: Exhibits satisfactory performance for synthesis planning of inorganic materials.
* 👍***Coding Assistance***: Provides generally helpful coding assistance for materials tasks. It can generate molecular dynamics and DFT inputs for numerous property calculations and can correctly utilize many computational packages and construct automatic processing pipelines. Iterative feedback and manual adjustments may be needed to fine-tune the generated code. 
* 😵***Representation***: Encounters challenges in representing and proposing organic polymers and MOFs. 
* 😵***Structure Generation***: Limited capability for structure generation, particularly when generating accurate atomic coordinates.
* 😵***Predictions***: Falls short in providing precise quantitative predictions in property prediction. For instance, when predicting whether a material is metallic or semi-conducting, its accuracy is only slightly better than a random guess.
* 😵***Synthesis Route***: Struggles to propose synthesis routes for organic polymeric materials not present in the training set without additional guidance.



## Partial Differential Equations
* 👍***PDE Concepts***: GPT-4 demonstrates its awareness of fundamental PDE concepts, thereby enabling researchers to gain a deeper understanding of the PDEs they are working with. It can serve as a helpful resource for teaching or mentoring students, enabling them to better understand and appreciate the importance of PDEs in their academic pursuits and research endeavors. 
* 👍***Concept Relationships***: The model is capable of discerning relationships between concepts, which may aid mathematicians in broadening their perspectives and intuitively grasping connections across different subfields. 
* 👍***Solution Recommendations***: GPT-4 can recommend appropriate analytical and numerical methods for addressing various types and complexities of PDEs. Depending on the specific problem, it can suggest suitable techniques for obtaining either exact or approximate solutions..
* 👍***Code Generation***: The model is capable of generating code in different programming languages, such as MATLAB and Python, for numerical solution of PDEs, thus facilitating the implementation of computational solutions.
* 😵***Output Verification***: While GPT-4 exhibits human-like capabilities in solving partial differential equations and providing explicit solutions, there might be instances of incorrect derivation. Researchers should exercise caution and verify the model’s output when using GPT-4 to solve PDEs. 
* 😵***Hallucinations Awareness***: GPT-4 may occasionally erroneously cite non-existent references. Researchers should cross-check citations and be aware of this limitation to ensure the accuracy and reliability of the information provided by the model. 


# Related Survey/Evaluation
* **What can Large Language Models do in chemistry? A comprehensive benchmark on eight tasks**  
Taicheng Guo, Kehan Guo, Bozhao Nan, Zhenwen Liang, Zhichun Guo, Nitesh V. Chawla, Olaf Wiest, Xiangliang Zhang  
*NeurIPS Datasets and Benchmarks Track, December 2023.*  
[![](https://img.shields.io/badge/neurips_workshop-5291C8?style=flat&logo=Read.cv&labelColor=555555)]([https://arxiv.org/abs/2305.18365](https://arxiv.org/abs/2305.18365))
![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F20d7965c0b282a0cd7f990e435d0f6bc9535bbc6%3Ffields%3DcitationCount&query=%24.citationCount&label=citation&style=social&labelColor=555555&color=ED8936)

* **SciBench: Evaluating College-Level Scientific Problem-Solving Abilities of Large Language Models**  
Xiaoxuan Wang, Ziniu Hu, Pan Lu, Yanqiao Zhu, Jieyu Zhang, Satyen Subramaniam, Arjun R. Loomba, Shichang Zhang, Yizhou Sun, Wei Wang  
*Arxiv, July 2023.*  
[![](https://img.shields.io/badge/arxiv-5291C8?style=flat&logo=Read.cv&labelColor=555555)]([https://arxiv.org/abs/2307.10635](https://arxiv.org/abs/2307.10635))
![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F4993258852711c4e3d0011325ac3db680eae84f4%3Ffields%3DcitationCount&query=%24.citationCount&label=citation&style=social&labelColor=555555&color=ED8936)

* **SciEval: A Multi-Level Large Language Model Evaluation Benchmark for Scientific Research**  
Liangtai Sun, Yang Han, Zihan Zhao, Da Ma, Zhennan Shen, Baocai Chen, Lu Chen, Kai Yu  
*Arxiv, August 2023.*  
[![](https://img.shields.io/badge/arxiv-5291C8?style=flat&logo=Read.cv&labelColor=555555)]([https://arxiv.org/abs/2308.13149](https://arxiv.org/abs/2308.13149))
![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Ff53a955ea1812fb0481504fdfd8febcb2a553a45%3Ffields%3DcitationCount&query=%24.citationCount&label=citation&style=social&labelColor=555555&color=ED8936)

* **Do Large Language Models Understand Chemistry? A Conversation with ChatGPT**  
Cayque Monteiro Castro Nascimento, André Silva Pimentel  
*J. Chem. Inf. Model, March 2023.*  
[![](https://img.shields.io/badge/JCIM-5291C8?style=flat&logo=Read.cv&labelColor=555555)]([https://pubs.acs.org/doi/10.1021/acs.jcim.3c00285](https://pubs.acs.org/doi/10.1021/acs.jcim.3c00285))
![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F23d01461a54505705649c1f5378f81dcd524d46c%3Ffields%3DcitationCount&query=%24.citationCount&label=citation&style=social&labelColor=555555&color=ED8936)

* **Language models in molecular discovery**  
Nikita Janakarajan, Tim Erdmann, Sarath Swaminathan, T. Laino, Jannis Born  
*Arxiv, September 2023.*  
[![](https://img.shields.io/badge/arxiv-5291C8?style=flat&logo=Read.cv&labelColor=555555)]([https://arxiv.org/abs/2309.16235](https://arxiv.org/abs/2309.16235))
![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F1fff185d1915ca76e8e2b621ed5bcc45ac2d559e%3Ffields%3DcitationCount&query=%24.citationCount&label=citation&style=social&labelColor=555555&color=ED8936)

* **ChemCrow: Augmenting large-language models with chemistry tools**  
Andrés M Bran, Sam Cox, Oliver Schilter, Carlo Baldassari, Andrew D. White, P. Schwaller  
*Arxiv, April 2023.*  
[![](https://img.shields.io/badge/arxiv-5291C8?style=flat&logo=Read.cv&labelColor=555555)]([https://arxiv.org/abs/2304.05376](https://arxiv.org/abs/2304.05376))
![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F354dcdebf3f8b5feeed5c62090e0bc1f0c28db06%3Ffields%3DcitationCount&query=%24.citationCount&label=citation&style=social&labelColor=555555&color=ED8936)

* **ChatGPT Chemistry Assistant for Text Mining and the Prediction of MOF Synthesis**  
Zhiling Zheng, Oufan Zhang, Christian Borgs, Jennifer T. Chayes, and Omar M. Yaghi  
*J. Am. Chem. Soc., August 2023.*  
[![](https://img.shields.io/badge/JACS-5291C8?style=flat&logo=Read.cv&labelColor=555555)]([https://pubs.acs.org/doi/10.1021/jacs.3c05819](https://pubs.acs.org/doi/10.1021/jacs.3c05819))
![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Fb33577b6624da43765d215d9954531e3c7e48e52%3Ffields%3DcitationCount&query=%24.citationCount&label=citation&style=social&labelColor=555555&color=ED8936)

* **A Comprehensive Evaluation of Large Language Models on Benchmark Biomedical Text Processing Tasks**  
Israt Jahan, Md Tahmid Rahman Laskar, Chun Peng, Jimmy Huang  
*Arxiv, October 2023.*  
[![](https://img.shields.io/badge/arxiv-5291C8?style=flat&logo=Read.cv&labelColor=555555)]([https://arxiv.org/ftp/arxiv/papers/2310/2310.04270.pdf](https://arxiv.org/ftp/arxiv/papers/2310/2310.04270.pdf))
![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F7b5b7aefc727bdf1e73efdd65af539d79628230a%3Ffields%3DcitationCount&query=%24.citationCount&label=citation&style=social&labelColor=555555&color=ED8936)

* **BioPlanner: Automatic Evaluation of LLMs on Protocol Planning in Biology**  
Odhran O'Donoghue, Aleksandar Shtedritski, John Ginger, Ralph Abboud, Ali Essa Ghareeb, Justin Booth, Samuel G Rodriques  
*EMNLP, October 2023.*  
[![](https://img.shields.io/badge/EMNLP-5291C8?style=flat&logo=Read.cv&labelColor=555555)]([https://aclanthology.org/2023.emnlp-main.162/](https://aclanthology.org/2023.emnlp-main.162/))
![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F1efb48995732f58dbf2e251bfdf8571545033db9%3Ffields%3DcitationCount&query=%24.citationCount&label=citation&style=social&labelColor=555555&color=ED8936)

* **14 examples of how LLMs can transform materials science and chemistry: a reflection on a large language model hackathon**  
K. Jablonka, Qianxiang Ai, Alexander H Al-Feghali, S. Badhwar, Joshua D. Bocarsly Andres M Bran, S. Bringuier, L. Brinson, K. Choudhary, Defne Çirci, Sam Cox, W. D. Jong, Matthew L. Evans, Nicolas Gastellu, Jérôme Genzling, M. Gil, Ankur Gupta, Zhi Hong, A. Imran, S. Kruschwitz, A. Labarre, Jakub L'ala, Tao Liu, Steven Ma, Sauradeep Majumdar, G. Merz, N. Moitessier, E. Moubarak, B. Mouriño, Brenden G. Pelkie, M. Pieler, Mayk C. Ramos, Bojana Rankovi'c, Samuel G. Rodriques, J. N. Sanders, P. Schwaller, Marcus Schwarting, Jia-Xin Shi, B. Smit, Benn Smith, J. V. Heck, C. Volker, Logan T. Ward, S. Warren, B. Weiser, Sylvester Zhang, Xiaoqi Zhang, Ghezal Ahmad Jan Zia, A. Scourtas, K. Schmidt, Ian T. Foster, Andrew D. White, B. Blaiszik.   
*Digital Discovery, June 2023.*  
[![](https://img.shields.io/badge/DigDis-5291C8?style=flat&logo=Read.cv&labelColor=555555)]([https://pubs.rsc.org/en/content/articlepdf/2023/dd/d3dd00113j](https://pubs.rsc.org/en/content/articlepdf/2023/dd/d3dd00113j))
![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F822f41fdb57c57db614a27936474644daf12b715%3Ffields%3DcitationCount&query=%24.citationCount&label=citation&style=social&labelColor=555555&color=ED8936)

# License
This repo is [MIT-licensed](https://github.com/microsoft/LLM4ScientificDiscovery/tree/main?tab=MIT-1-ov-file).

# Contact
If you have any questions or suggestions, look forward to your messages through the discussion channel or email [llm4sciencediscovery@microsoft.com](mailto:llm4sciencediscovery@microsoft.com).

Contact people: Tao Qin ([taoqin@microsoft.com](mailto:taoqin@microsoft.com)), Lijun Wu ([lijuwu@microsoft.com](mailto:lijuwu@microsoft.com)).
```
@misc{ai4science2023impact,
      title={The Impact of Large Language Models on Scientific Discovery: a Preliminary Study using GPT-4}, 
      author={Microsoft Research AI4Science and Microsoft Azure Quantum},
      year={2023},
      eprint={2311.07361},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```
