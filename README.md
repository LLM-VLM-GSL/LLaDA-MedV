# LLaDA-MedV: Exploring Large Language Diffusion Models for Biomedical Image Understanding

## New
- [2025-08-06] We have upload our paper to [arxiv](https://arxiv.org/abs/2508.01617v1) and release model weight.

## Introduction
Autoregressive models (ARMs) have long dominated the landscape of biomedical vision-language models (VLMs). Recently, masked diffusion models such as LLaDA have emerged as promising alternatives, yet their application in the biomedical domain remains largely underexplored. To bridge this gap, we introduce **LLaDA-MedV**, the first large language diffusion model tailored for biomedical image understanding through vision instruction tuning. LLaDA-MedV achieves relative performance gains of 7.855\% over LLaVA-Med and 1.867\% over LLaDA-V in the open-ended biomedical visual conversation task, and sets new state-of-the-art accuracy on the closed-form subset of three VQA benchmarks: 84.93\% on VQA-RAD, 92.31\% on SLAKE, and 95.15\% on PathVQA. Furthermore, a detailed comparison with LLaVA-Med suggests that LLaDA-MedV is capable of generating reasonably longer responses by explicitly controlling response length, which can lead to more informative outputs. We also conduct an in-depth analysis of both the training and inference stages, highlighting the critical roles of initialization weight selection, fine-tuning strategies, and the interplay between sampling steps and response repetition.

## Model Performance
### Open-end Biomedical conversation
We adopt the [Biomedical Visual Chatbot benchmark](https://arxiv.org/abs/2306.00890) to evaluate the performance of LLaDA-MedV in a realistic open-ended conversation setting. As shown below, LLaDA-MedV demonstrates superior performance compared to several baselines. We provide detailed generation results for improved visualization.
<table>
  <tr>
    <td><img src="https://github.com/LLM-VLM-GSL/LLaDA-MedV/blob/main/images/fig-radarmedicalnew.png" width="500"/></td>
    <td><img src="https://github.com/LLM-VLM-GSL/LLaDA-MedV/blob/main/images/bio-conversation.png" width="500"/></td>
  </tr>
</table>

### Downstream Biomedical VQA
We also evaluate model performance on three biomedical visual question answering (VQA) benchmarks after fine-tuning on the training sets of [VQA-RAD](https://pubmed.ncbi.nlm.nih.gov/30457565/), [SLAKE](https://arxiv.org/abs/2102.09542) and [PathVQA](https://arxiv.org/abs/2003.10286), following their official splits. The results are reported below.
![Results](https://github.com/LLM-VLM-GSL/LLaDA-MedV/blob/main/images/table.png)

## Model Details
### Training
We are currently finalizing the training code and will release it very soon.

### Evaluation 
We are currently finalizing the evaluation code and will release it very soon.

### Weight 
We release our model weights to support future research in the community. Specifically, [LLaDAMedV-2A4E](https://drive.google.com/drive/u/1/folders/1HwW4l-r9H3uyVPpysndP6ZOJXIQfkVB9) refers to our main model after semantic alignment and supervised fine-tuning (SFT). [VQA_RAD_2E](https://drive.google.com/drive/u/1/folders/1HwW4l-r9H3uyVPpysndP6ZOJXIQfkVB9), [SLAKE_10E](https://drive.google.com/drive/u/1/folders/1HwW4l-r9H3uyVPpysndP6ZOJXIQfkVB9) and [PathVQA_7E](https://drive.google.com/drive/u/1/folders/1HwW4l-r9H3uyVPpysndP6ZOJXIQfkVB9) refer to dataset-specific models after task-specific fine-tuning. For more details, please refer to our manuscript.

### Acknowledgements
We gratefully acknowledge the authors of the following open-source repositories, which served as valuable references during our implementation:

- [LLaDA](https://github.com/ML-GSAI/LLaDA)
- [LLaDA-V](https://github.com/ML-GSAI/LLaDA-V)
- [LLaVA-Med](https://github.com/microsoft/LLaVA-Med/tree/v1.0.0)

We deeply appreciate their contributions to the research community.

