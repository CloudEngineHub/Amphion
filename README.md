# Amphion: An Open-Source Audio, Music, and Speech Generation Toolkit

<div>
    <a href="https://arxiv.org/abs/2312.09911"><img src="https://img.shields.io/badge/arXiv-Paper-<COLOR>.svg"></a>
    <a href="https://huggingface.co/amphion"><img src="https://img.shields.io/badge/%F0%9F%A4%97%20HuggingFace-Amphion-pink"></a>
    <a href="https://modelscope.cn/organization/amphion"><img src="https://img.shields.io/badge/ModelScope-Amphion-cyan"></a>
    <a href="https://openxlab.org.cn/usercenter/Amphion"><img src="https://cdn-static.openxlab.org.cn/app-center/openxlab_app.svg"></a>
    <a href="https://discord.com/invite/drhW7ajqAG"><img src="https://img.shields.io/badge/Discord-Join%20chat-blue.svg"></a>
    <a href="egs/tts/README.md"><img src="https://img.shields.io/badge/README-TTS-blue"></a>
    <a href="models/vc/vevo/README.md"><img src="https://img.shields.io/badge/README-VC-blue"></a>
    <a href="models/vc/vevo/README.md"><img src="https://img.shields.io/badge/README-AC-blue"></a>
    <a href="egs/svc/README.md"><img src="https://img.shields.io/badge/README-SVC-blue"></a>
    <a href="egs/tta/README.md"><img src="https://img.shields.io/badge/README-TTA-blue"></a>
    <a href="egs/vocoder/README.md"><img src="https://img.shields.io/badge/README-Vocoder-purple"></a>
    <a href="egs/metrics/README.md"><img src="https://img.shields.io/badge/README-Evaluation-yellow"></a>
    <a href="LICENSE"><img src="https://img.shields.io/badge/LICENSE-MIT-red"></a>
    <a href="https://trendshift.io/repositories/5469" target="_blank"><img src="https://trendshift.io/api/badge/repositories/5469" alt="open-mmlab%2FAmphion | Trendshift" style="width: 150px; height: 33px;" width="150" height="33"/></a>
</div>
<br>

**Amphion (/æmˈfaɪən/) is a toolkit for Audio, Music, and Speech Generation.** Its purpose is to support reproducible research and help junior researchers and engineers get started in the field of audio, music, and speech generation research and development. Amphion offers a unique feature: **visualizations** of classic models or architectures. We believe that these visualizations are beneficial for junior researchers and engineers who wish to gain a better understanding of the model.

**The North-Star objective of Amphion is to offer a platform for studying the conversion of any inputs into audio.** Amphion is designed to support individual generation tasks, including but not limited to,

- **TTS**: Text to Speech (⛳ supported)
- **SVS**: Singing Voice Synthesis (👨‍💻 developing)
- **VC**: Voice Conversion (⛳ supported)
- **AC**: Accent Conversion (⛳ supported)
- **SVC**: Singing Voice Conversion (⛳ supported)
- **TTA**: Text to Audio (⛳ supported)
- **TTM**: Text to Music (👨‍💻 developing)
- more…

In addition to the specific generation tasks, Amphion includes several **vocoders** and **evaluation metrics**. A vocoder is an important module for producing high-quality audio signals, while evaluation metrics are critical for ensuring consistent metrics in generation tasks. Moreover, Amphion is dedicated to advancing audio generation in real-world applications, such as building **large-scale datasets** for speech synthesis.

## 🚀 News
- **2025/05/26**: We release [***DualCodec***](models/codec/dualcodec/README.md), a low-frame-rate (12.5Hz or 25Hz), semantically-enhanced (with SSL feature) Neural Audio Codec designed to extract discrete tokens for efficient speech generation.[![paper](https://img.shields.io/badge/arXiv-2505.13000-brightgreen.svg?style=flat-square)](http://arxiv.org/abs/2505.13000)[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1VvUhsDffLdY5TdNuaqlLnYzIoXhvI8MK#scrollTo=Lsos3BK4J-4E)[![demo page](https://img.shields.io/badge/GitHub.io-Demo_Page-blue?logo=Github&style=flat-square)](https://dualcodec.github.io/)[![code](https://img.shields.io/badge/README-Code-blue)](models/codec/dualcodec/README.md)
- **2025/04/12**: We release [***Vevo1.5***](models/svc/vevosing/README.md), which extends Vevo and focuses on unified and controllable generation for both speech and singing voice. Vevo1.5 can be applied into a series of speech and singing voice generation tasks, including VC, TTS, AC, SVS, SVC, Speech/Singing Voice Editing, Singing Style Conversion, and more. [![blog](https://img.shields.io/badge/README-Blog-blue.svg)](https://veiled-army-9c5.notion.site/Vevo1-5-1d2ce17b49a280b5b444d3fa2300c93a)
- **2025/02/26**: We release [***Metis***](https://github.com/open-mmlab/Amphion/tree/main/models/tts/metis), a foundation model for unified speech generation. The system supports zero-shot text-to-speech, voice conversion, target speaker extraction, speech enhancement, and lip-to-speech. [![arXiv](https://img.shields.io/badge/arXiv-Paper-COLOR.svg)](https://arxiv.org/pdf/2502.03128) [![hf](https://img.shields.io/badge/%F0%9F%A4%97%20HuggingFace-model-yellow)](https://huggingface.co/amphion/metis)
- **2025/02/26**: *The Emilia-Large dataset, featuring over 200,000 hours of data, is now available!!!* Emilia-Large combines the original 101k-hour Emilia dataset (licensed under `CC BY-NC 4.0`) with the brand-new 114k-hour **Emilia-YODAS dataset** (licensed under `CC BY 4.0`). Download at [![hf](https://img.shields.io/badge/%F0%9F%A4%97%20HuggingFace-Dataset-yellow)](https://huggingface.co/datasets/amphion/Emilia-Dataset). Check details at [![arXiv](https://img.shields.io/badge/arXiv-Paper-COLOR.svg)](https://arxiv.org/abs/2501.15907).
- **2025/01/30**: We release [Amphion v0.2 Technical Report](https://arxiv.org/abs/2501.15442), which provides a comprehensive overview of the Amphion updates in 2024. [![arXiv](https://img.shields.io/badge/arXiv-Paper-COLOR.svg)](https://arxiv.org/abs/2501.15442)
- **2025/01/23**: [MaskGCT](https://arxiv.org/abs/2409.00750) and [Vevo](https://openreview.net/pdf?id=anQDiQZhDP) got accepted by ICLR 2025! 🎉
- **2024/12/22**: We release the reproduction of **Vevo**, a zero-shot voice imitation framework with controllable timbre and style. Vevo can be applied into a series of speech generation tasks, including VC, TTS, AC, and more. The released pre-trained models are trained on [Emilia](https://huggingface.co/datasets/amphion/Emilia-Dataset) dataset and achieve SOTA zero-shot VC performance. [![arXiv](https://img.shields.io/badge/OpenReview-Paper-COLOR.svg)](https://openreview.net/pdf?id=anQDiQZhDP) [![hf](https://img.shields.io/badge/%F0%9F%A4%97%20HuggingFace-model-yellow)](https://huggingface.co/amphion/Vevo) [![WebPage](https://img.shields.io/badge/WebPage-Demo-red)](https://versavoice.github.io/) [![readme](https://img.shields.io/badge/README-Key%20Features-blue)](models/vc/vevo/README.md)
- **2024/10/19**: We release **MaskGCT**, a fully non-autoregressive TTS model that eliminates the need for explicit alignment information between text and speech supervision. MaskGCT is trained on [Emilia](https://huggingface.co/datasets/amphion/Emilia-Dataset) dataset and achieves SOTA zero-shot TTS performance.  [![arXiv](https://img.shields.io/badge/arXiv-Paper-COLOR.svg)](https://arxiv.org/abs/2409.00750) [![hf](https://img.shields.io/badge/%F0%9F%A4%97%20HuggingFace-model-yellow)](https://huggingface.co/amphion/maskgct) [![hf](https://img.shields.io/badge/%F0%9F%A4%97%20HuggingFace-demo-pink)](https://huggingface.co/spaces/amphion/maskgct) [![ModelScope](https://img.shields.io/badge/ModelScope-space-purple)](https://modelscope.cn/studios/amphion/maskgct) [![ModelScope](https://img.shields.io/badge/ModelScope-model-cyan)](https://modelscope.cn/models/amphion/MaskGCT) [![readme](https://img.shields.io/badge/README-Key%20Features-blue)](models/tts/maskgct/README.md)
- **2024/09/01**: [Amphion](https://arxiv.org/abs/2312.09911), [Emilia](https://arxiv.org/abs/2407.05361) and [DSFF-SVC](https://arxiv.org/abs/2310.11160) got accepted by IEEE SLT 2024! 🤗
- **2024/08/28**: Welcome to join Amphion's [Discord channel](https://discord.com/invite/drhW7ajqAG) to stay connected and engage with our community！
- **2024/08/20**: [SingVisio](https://arxiv.org/abs/2402.12660) got accepted by Computers & Graphics, [available here](https://www.sciencedirect.com/science/article/pii/S0097849324001936)! 🎉
- **2024/08/27**: *The Emilia dataset is now publicly available!* Discover the most extensive and diverse speech generation dataset with 101k hours of in-the-wild speech data now at [![hf](https://img.shields.io/badge/%F0%9F%A4%97%20HuggingFace-Dataset-yellow)](https://huggingface.co/datasets/amphion/Emilia-Dataset) or [![OpenDataLab](https://img.shields.io/badge/OpenDataLab-Dataset-blue)](https://opendatalab.com/Amphion/Emilia)! 👑👑👑
- **2024/07/01**: Amphion now releases **Emilia**, the first open-source multilingual in-the-wild dataset for speech generation with over 101k hours of speech data, and the **Emilia-Pipe**, the first open-source preprocessing pipeline designed to transform in-the-wild speech data into high-quality training data with annotations for speech generation! [![arXiv](https://img.shields.io/badge/arXiv-Paper-COLOR.svg)](https://arxiv.org/abs/2407.05361) [![hf](https://img.shields.io/badge/%F0%9F%A4%97%20HuggingFace-Dataset-yellow)](https://huggingface.co/datasets/amphion/Emilia) [![demo](https://img.shields.io/badge/WebPage-Demo-red)](https://emilia-dataset.github.io/Emilia-Demo-Page/) [![readme](https://img.shields.io/badge/README-Key%20Features-blue)](preprocessors/Emilia/README.md)
- **2024/03/12**: Amphion now support **NaturalSpeech3 FACodec** and release pretrained checkpoints. [![arXiv](https://img.shields.io/badge/arXiv-Paper-COLOR.svg)](https://arxiv.org/abs/2403.03100) [![hf](https://img.shields.io/badge/%F0%9F%A4%97%20HuggingFace-model-yellow)](https://huggingface.co/amphion/naturalspeech3_facodec) [![hf](https://img.shields.io/badge/%F0%9F%A4%97%20HuggingFace-demo-pink)](https://huggingface.co/spaces/amphion/naturalspeech3_facodec) [![readme](https://img.shields.io/badge/README-Key%20Features-blue)](models/codec/ns3_codec/README.md)
- **2024/02/22**: The first Amphion visualization tool, **SingVisio**, release. [![arXiv](https://img.shields.io/badge/arXiv-Paper-COLOR.svg)](https://arxiv.org/abs/2402.12660) [![openxlab](https://cdn-static.openxlab.org.cn/app-center/openxlab_app.svg)](https://openxlab.org.cn/apps/detail/Amphion/SingVisio) [![Video](https://img.shields.io/badge/Video-Demo-orange)](https://drive.google.com/file/d/15097SGhQh-SwUNbdWDYNyWEP--YGLba5/view) [![readme](https://img.shields.io/badge/README-Key%20Features-blue)](egs/visualization/SingVisio/README.md)
- **2023/12/18**: Amphion v0.1 release. [![arXiv](https://img.shields.io/badge/arXiv-Paper-<COLOR>.svg)](https://arxiv.org/abs/2312.09911) [![hf](https://img.shields.io/badge/%F0%9F%A4%97%20HuggingFace-Amphion-pink)](https://huggingface.co/amphion) [![youtube](https://img.shields.io/badge/YouTube-Demo-red)](https://www.youtube.com/watch?v=1aw0HhcggvQ) [![readme](https://img.shields.io/badge/README-Key%20Features-blue)](https://github.com/open-mmlab/Amphion/pull/39)
- **2023/11/28**: Amphion alpha release. [![readme](https://img.shields.io/badge/README-Key%20Features-blue)](https://github.com/open-mmlab/Amphion/pull/2)

## ⭐ Key Features

### TTS: Text to Speech

- Amphion achieves state-of-the-art performance compared to existing open-source repositories on text-to-speech (TTS) systems. It supports the following models or architectures:
    - [FastSpeech2](https://arxiv.org/abs/2006.04558): A non-autoregressive TTS architecture that utilizes feed-forward Transformer blocks. [![code](https://img.shields.io/badge/README-Code-blue)](egs/tts/FastSpeech2/README.md)
    - [VITS](https://arxiv.org/abs/2106.06103): An end-to-end TTS architecture that utilizes conditional variational autoencoder with adversarial learning [![code](https://img.shields.io/badge/README-Code-blue)](egs/tts/VITS/README.md)
    - [VALL-E](https://arxiv.org/abs/2301.02111): A zero-shot TTS architecture that uses a neural codec language model with discrete codes. [![code](https://img.shields.io/badge/README-Code-blue)](egs/tts/VALLE/README.md)
    - [NaturalSpeech2](https://arxiv.org/abs/2304.09116): An architecture for TTS that utilizes a latent diffusion model to generate natural-sounding voices. [![code](https://img.shields.io/badge/README-Code-blue)](egs/tts/NaturalSpeech2/README.md)
    - [Jets](Jets): An end-to-end TTS model that jointly trains FastSpeech2 and HiFi-GAN with an alignment module. [![code](https://img.shields.io/badge/README-Code-blue)](egs/tts/Jets/README.md)
    - [MaskGCT](https://arxiv.org/abs/2409.00750): A fully non-autoregressive TTS architecture that eliminates the need for explicit alignment information between text and speech supervision. [![code](https://img.shields.io/badge/README-Code-blue)](models/tts/maskgct/README.md)
    - [Vevo-TTS](https://openreview.net/pdf?id=anQDiQZhDP): A zero-shot TTS architecture with controllable timbre and style. It consists of an autoregressive transformer and a flow-matching transformer. [![code](https://img.shields.io/badge/README-Code-blue)](models/vc/vevo/README.md)
    - [DualCodec-VALLE](models/codec/dualcodec/README.md): A VALLE model trained on 12.5Hz DualCodec tokens for super fast generation.

### VC: Voice Conversion

Amphion supports the following voice conversion models:

- [Vevo](https://openreview.net/pdf?id=anQDiQZhDP): A zero-shot voice imitation framework with controllable timbre and style. **Vevo-Timbre** conducts the style-preserved voice conversion, and **Vevo-Voice** conducts the style-converted voice conversion. [![code](https://img.shields.io/badge/README-Code-blue)](models/vc/vevo/README.md)
- [FACodec](https://arxiv.org/abs/2403.03100): FACodec decomposes speech into subspaces representing different attributes like content, prosody, and timbre. It can achieve zero-shot voice conversion. [![code](https://img.shields.io/badge/README-Code-blue)](https://huggingface.co/amphion/naturalspeech3_facodec)
- [Noro](https://arxiv.org/abs/2411.19770): A **noise-robust** zero-shot voice conversion system. Noro introduces innovative components tailored for VC using noisy reference speeches, including a dual-branch reference encoding module and a noise-agnostic contrastive speaker loss. [![code](https://img.shields.io/badge/README-Code-blue)](egs/vc/Noro/README.md)

## Neural Audio Codec
- [DualCodec](models/codec/dualcodec/README.md), a low-frame-rate (12.5Hz or 25Hz), semantically-enhanced (with SSL feature) Neural Audio Codec designed to extract discrete tokens for efficient speech generation.[![paper](https://img.shields.io/badge/arXiv-2505.13000-brightgreen.svg?style=flat-square)](http://arxiv.org/abs/2505.13000)[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1VvUhsDffLdY5TdNuaqlLnYzIoXhvI8MK#scrollTo=Lsos3BK4J-4E)[![demo page](https://img.shields.io/badge/GitHub.io-Demo_Page-blue?logo=Github&style=flat-square)](https://dualcodec.github.io/)[![code](https://img.shields.io/badge/README-Code-blue)](models/codec/dualcodec/README.md)
- [FACodec](https://arxiv.org/abs/2403.03100): FACodec decomposes speech into subspaces representing different attributes like content, prosody, and timbre. [![code](https://img.shields.io/badge/README-Code-blue)](https://huggingface.co/amphion/naturalspeech3_facodec)

### AC: Accent Conversion

- Amphion supports AC with [Vevo-Style](models/vc/vevo/README.md). Particularly, it can conduct the accent conversion in a zero-shot manner. [![code](https://img.shields.io/badge/README-Code-blue)](models/vc/vevo/README.md)

### SVC: Singing Voice Conversion

- Ampion supports multiple content-based features from various pretrained models, including [WeNet](https://github.com/wenet-e2e/wenet), [Whisper](https://github.com/openai/whisper), and [ContentVec](https://github.com/auspicious3000/contentvec). Their specific roles in SVC has been investigated in our SLT 2024 paper. [![arXiv](https://img.shields.io/badge/arXiv-Paper-<COLOR>.svg)](https://arxiv.org/abs/2310.11160) [![code](https://img.shields.io/badge/README-Code-blue)](egs/svc/MultipleContentsSVC)
- Amphion implements several state-of-the-art model architectures, including diffusion-, transformer-, VAE- and flow-based models. The diffusion-based architecture uses [Bidirectional dilated CNN](https://openreview.net/pdf?id=a-xFK8Ymz5J) as a backend and supports several sampling algorithms such as [DDPM](https://arxiv.org/pdf/2006.11239.pdf), [DDIM](https://arxiv.org/pdf/2010.02502.pdf), and [PNDM](https://arxiv.org/pdf/2202.09778.pdf). Additionally, it supports single-step inference based on the [Consistency Model](https://openreview.net/pdf?id=FmqFfMTNnv). [![code](https://img.shields.io/badge/README-Code-blue)](egs/svc/DiffComoSVC/README.md)

### TTA: Text to Audio

- Amphion supports the TTA with a latent diffusion model. It is designed like [AudioLDM](https://arxiv.org/abs/2301.12503), [Make-an-Audio](https://arxiv.org/abs/2301.12661), and [AUDIT](https://arxiv.org/abs/2304.00830). It is also the official implementation of the text-to-audio generation part of our NeurIPS 2023 paper. [![arXiv](https://img.shields.io/badge/arXiv-Paper-<COLOR>.svg)](https://arxiv.org/abs/2304.00830) [![code](https://img.shields.io/badge/README-Code-blue)](egs/tta/RECIPE.md)

### Vocoder

- Amphion supports various widely-used neural vocoders, including:
    - GAN-based vocoders: [MelGAN](https://arxiv.org/abs/1910.06711), [HiFi-GAN](https://arxiv.org/abs/2010.05646), [NSF-HiFiGAN](https://github.com/nii-yamagishilab/project-NN-Pytorch-scripts), [BigVGAN](https://arxiv.org/abs/2206.04658), [APNet](https://arxiv.org/abs/2305.07952).
    - Flow-based vocoders: [WaveGlow](https://arxiv.org/abs/1811.00002).
    - Diffusion-based vocoders: [Diffwave](https://arxiv.org/abs/2009.09761).
    - Auto-regressive based vocoders: [WaveNet](https://arxiv.org/abs/1609.03499), [WaveRNN](https://arxiv.org/abs/1802.08435v1).
- Amphion provides the official implementation of [Multi-Scale Constant-Q Transform Discriminator](https://arxiv.org/abs/2311.14957) (our ICASSP 2024 paper). It can be used to enhance any architecture GAN-based vocoders during training, and keep the inference stage (such as memory or speed) unchanged. [![arXiv](https://img.shields.io/badge/arXiv-Paper-<COLOR>.svg)](https://arxiv.org/abs/2311.14957) [![code](https://img.shields.io/badge/README-Code-blue)](egs/vocoder/gan/tfr_enhanced_hifigan)

### Evaluation

Amphion provides a comprehensive objective evaluation of the generated audio. [![code](https://img.shields.io/badge/README-Code-blue)](egs/metrics/README.md) 

The supported evaluation metrics contain:

- **F0 Modeling**: F0 Pearson Coefficients, F0 Periodicity Root Mean Square Error, F0 Root Mean Square Error, Voiced/Unvoiced F1 Score, etc.
- **Energy Modeling**: Energy Root Mean Square Error, Energy Pearson Coefficients, etc.
- **Intelligibility**: Character/Word Error Rate, which can be calculated based on [Whisper](https://github.com/openai/whisper) and more.
- **Spectrogram Distortion**: Frechet Audio Distance (FAD), Mel Cepstral Distortion (MCD), Multi-Resolution STFT Distance (MSTFT), Perceptual Evaluation of Speech Quality (PESQ), Short Time Objective Intelligibility (STOI), etc.
- **Speaker Similarity**: Cosine similarity, which can be calculated based on [RawNet3](https://github.com/Jungjee/RawNet), [Resemblyzer](https://github.com/resemble-ai/Resemblyzer), [WeSpeaker](https://github.com/wenet-e2e/wespeaker), [WavLM](https://github.com/microsoft/unilm/tree/master/wavlm) and more.

### Datasets

- Amphion unifies the data preprocess of the open-source datasets including [AudioCaps](https://audiocaps.github.io/), [LibriTTS](https://www.openslr.org/60/), [LJSpeech](https://keithito.com/LJ-Speech-Dataset/), [M4Singer](https://github.com/M4Singer/M4Singer), [Opencpop](https://wenet.org.cn/opencpop/), [OpenSinger](https://github.com/Multi-Singer/Multi-Singer.github.io), [SVCC](http://vc-challenge.org/), [VCTK](https://datashare.ed.ac.uk/handle/10283/3443), and more. The supported dataset list can be seen [here](egs/datasets/README.md) (updating). 
- Amphion (exclusively) supports the [**Emilia**](preprocessors/Emilia/README.md) dataset and its preprocessing pipeline **Emilia-Pipe** for in-the-wild speech data!

### Visualization

Amphion provides visualization tools to interactively illustrate the internal processing mechanism of classic models. This provides an invaluable resource for educational purposes and for facilitating understandable research.

Currently, Amphion supports [SingVisio](egs/visualization/SingVisio/README.md), a visualization tool of the diffusion model for singing voice conversion. [![arXiv](https://img.shields.io/badge/arXiv-Paper-COLOR.svg)](https://arxiv.org/abs/2402.12660) [![openxlab](https://cdn-static.openxlab.org.cn/app-center/openxlab_app.svg)](https://openxlab.org.cn/apps/detail/Amphion/SingVisio) [![Video](https://img.shields.io/badge/Video-Demo-orange)](https://drive.google.com/file/d/15097SGhQh-SwUNbdWDYNyWEP--YGLba5/view)


## 📀 Installation

Amphion can be installed through either Setup Installer or Docker Image.

### Setup Installer

```bash
git clone https://github.com/open-mmlab/Amphion.git
cd Amphion

# Install Python Environment
conda create --name amphion python=3.9.15
conda activate amphion

# Install Python Packages Dependencies
sh env.sh
```

### Docker Image

1. Install [Docker](https://docs.docker.com/get-docker/), [NVIDIA Driver](https://www.nvidia.com/download/index.aspx), [NVIDIA Container Toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html), and [CUDA](https://developer.nvidia.com/cuda-downloads).

2. Run the following commands:
```bash
git clone https://github.com/open-mmlab/Amphion.git
cd Amphion

docker pull realamphion/amphion
docker run --runtime=nvidia --gpus all -it -v .:/app realamphion/amphion
```
Mount dataset by argument `-v` is necessary when using Docker. Please refer to [Mount dataset in Docker container](egs/datasets/docker.md) and [Docker Docs](https://docs.docker.com/engine/reference/commandline/container_run/#volume) for more details.


## 🐍 Usage in Python

We detail the instructions of different tasks in the following recipes:

- [Text to Speech (TTS)](egs/tts/README.md)
- [Voice Conversion (VC)](models/vc/vevo/README.md)
- [Accent Conversion (AC)](models/vc/vevo/README.md)
- [Singing Voice Conversion (SVC)](egs/svc/README.md)
- [Text to Audio (TTA)](egs/tta/README.md)
- [Vocoder](egs/vocoder/README.md)
- [Evaluation](egs/metrics/README.md)
- [Visualization](egs/visualization/README.md)

## 👨‍💻 Contributing
We appreciate all contributions to improve Amphion. Please refer to [CONTRIBUTING.md](.github/CONTRIBUTING.md) for the contributing guideline.

## 🙏 Acknowledgement


- [ming024's FastSpeech2](https://github.com/ming024/FastSpeech2) and [jaywalnut310's VITS](https://github.com/jaywalnut310/vits) for model architecture code.
- [lifeiteng's VALL-E](https://github.com/lifeiteng/vall-e) for training pipeline and model architecture design.
- [SpeechTokenizer](https://github.com/ZhangXInFD/SpeechTokenizer) for semantic-distilled tokenizer design.
- [WeNet](https://github.com/wenet-e2e/wenet), [Whisper](https://github.com/openai/whisper), [ContentVec](https://github.com/auspicious3000/contentvec), and [RawNet3](https://github.com/Jungjee/RawNet) for pretrained models and inference code.
- [HiFi-GAN](https://github.com/jik876/hifi-gan) for GAN-based Vocoder's architecture design and training strategy.
- [Encodec](https://github.com/facebookresearch/encodec) for well-organized GAN Discriminator's architecture and basic blocks.
- [Latent Diffusion](https://github.com/CompVis/latent-diffusion) for model architecture design.
- [TensorFlowTTS](https://github.com/TensorSpeech/TensorFlowTTS) for preparing the MFA tools.


## ©️ License

Amphion is under the [MIT License](LICENSE). It is free for both research and commercial use cases.

## 📚 Citations
Amphion v0.2:
```bibtex
@article{amphion_v0.2,
  title        = {Overview of the Amphion Toolkit (v0.2)},
  author       = {Jiaqi Li and Xueyao Zhang and Yuancheng Wang and Haorui He and Chaoren Wang and Li Wang and Huan Liao and Junyi Ao and Zeyu Xie and Yiqiao Huang and Junan Zhang and Zhizheng Wu},
  year         = {2025},
  journal      = {arXiv preprint arXiv:2501.15442},
}
```
Amphion v0.1: 
```bibtex
@inproceedings{amphion,
    author={Xueyao Zhang and Liumeng Xue and Yicheng Gu and Yuancheng Wang and Jiaqi Li and Haorui He and Chaoren Wang and Ting Song and Xi Chen and Zihao Fang and Haopeng Chen and Junan Zhang and Tze Ying Tang and Lexiao Zou and Mingxuan Wang and Jun Han and Kai Chen and Haizhou Li and Zhizheng Wu},
    title={Amphion: An Open-Source Audio, Music and Speech Generation Toolkit},
    booktitle={{IEEE} Spoken Language Technology Workshop, {SLT} 2024},
    year={2024}
}
```
