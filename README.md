# MFC-Bench
[https://arxiv.org/abs/2406.11288](https://arxiv.org/abs/2406.11288)

![architecture](images/architecture.png)

## Introduction
We introduce the MFC-Bench, a comprehensive Multimodal FactChecking testbed designed to evaluate LVLM in terms of identifying factual inconsistencies and
counterfactual scenarios.
MFC-Bench encompasses a wide range of visual and textual queries,
organized into three binary classification tasks: Manipulation Classification, Out-of-Context Classification, and Veracity Classification.  
1) The Manipulation Classification task targets various
alterations like face swapping, face attribute editing, background changing, image generation, entity
replacement, and style transfer. (Dataset:[manipulation-mfc-bench](https://huggingface.co/datasets/Anonymous-2024/manipulation-mfc-bench))
2) The Out-of-Context Classification task focuses on identifying the
false connection between the image and text that may be both true.(Dataset:[ooc-mfc-bench](https://huggingface.co/datasets/Anonymous-2024/ooc-mfc-bench))
3) The Veracity Classification task
is the multimodal counterpart to classifying the veracity of textual claims given the visual evidence, by
leveraging the inherent knowledge embedded in LVLMs.(Dataset:[veracity-mfc-bench](https://huggingface.co/datasets/Anonymous-2024/veracity-mfc-bench))

## Datasets Construction
![Datasets](/images/datasets.png)

## Methodology
To provide an exhaustive perspective on the current state of LVLMs within the context of multimodal
fact-checking, we conducted evaluations on 12 representative accessible LVLMs. For the open-source and accessible LVLMs, we adopt the representative models like [LLaVANeXT](https://github.com/haotian-liu/LLaVA/blob/main/docs/MODEL_ZOO.md#llava-v16) , [InstructBLIP](https://github.com/salesforce/LAVIS/tree/main/projects/instructblip) , [Qwen-VL](https://github.com/QwenLM/Qwen-VL) , [Yi-VL](https://github.com/01-ai/Yi), [InternVL](https://github.com/OpenGVLab/InternVL) , [CogVLM](https://github.com/THUDM/CogVLM) , [MiniCPM-V-2 ](https://github.com/OpenBMB/MiniCPM-V), [mPLUG-Owl](https://github.com/X-PLUG/mPLUG-Owl) , [Emu2](https://github.com/baaivision/Emu) and [MiniGPT-v2](https://minigpt-v2.github.io/) . As two of the most powerful closed-source LVLMs, both [GPT-4V](https://openai.com/index/gpt-4v-system-card/) and [Claude3-Haiku](https://www.anthropic.com/news/claude-3-haiku) are
also included in our testing scope.

To explore the effect of different prompt strategies like Chain-of-Thought
(CoT)  or In-Context Learning (ICL) prompting, we utilized the four following
prompt methods for the MFC-Bench: Zero-shot, Zero-shot with CoT , Few-shot,
and Few-shot with CoT.
![prompt-types](/images/prompt-types.png)
## Experiment Results
![Main Result](/images/main_result.png)
![Zero-shot CoT](/images/zero_shot_cot.png)


## BibTeX
@misc{wang2024mfcbenchbenchmarkingmultimodalfactchecking,
      title={MFC-Bench: Benchmarking Multimodal Fact-Checking with Large Vision-Language Models}, 
      author={Shengkang Wang and Hongzhan Lin and Ziyang Luo and Zhen Ye and Guang Chen and Jing Ma},
      year={2024}  
}








