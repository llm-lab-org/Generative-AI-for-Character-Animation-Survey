# Generative AI for Character Animation: A Comprehensive Survey of Techniques, Applications, and Future Directions

[![arXiv](https://img.shields.io/badge/arXiv-Paper-<COLOR>.svg)](https://arxiv.org/abs/your_eprint_number)

This repository is designed to collect and categorize papers, datasets, and resources related to generative AI for character animation based on our survey. As advances in generative AI continue to transform animation from realistic facial synthesis to dynamic gesture and motion generation, this resource will be continuously updated to serve as a comprehensive guide for researchers and practitioners.

---

## 📑 List of Contents

- [📝 Abstract](#-abstract)
- [📚 Background](#-background)
  - [🤖 Models](#-models)
    - [🎨 Computer Graphics Models](#-computer-graphics-models)
    - [👀 Vision](#-vision)
    - [📝 Language Models](#-language-models)
    - [🕒 Temporal Sequence Modeling](#-temporal-sequence-modeling)
    - [🗣 Speech Models](#-speech-models)
    - [🎭 Additional Generative Models](#-additional-generative-models)
  - [📊 Metrics](#-metrics)
    - [✅ Quality and Realism of Generated Output](#-quality-and-realism-of-generated-output)
    - [🔄 Diversity and Multimodality](#-diversity-and-multimodality)
    - [🎯 Relevance and Accuracy](#-relevance-and-accuracy)
    - [🏃 Physical Plausibility and Interaction](#-physical-plausibility-and-interaction)
    - [⚡️ Efficiency and Computational Metrics](#-efficiency-and-computational)
- [👨 Face](#-face)
  - [🗂 Datasets](#-datasets)
  - [🤖 Models](##-models-1)
- [😃 Expression](#-expression)
  - [🗂 Datasets](#-datasets-1)
  - [🤖 Models](##-models-2)
- [🖼 Image](#-image)
  - [🗂 Datasets](#-datasets-2)
  - [🤖 Models](##-models-3)
- [👤 Avatar](#-avatar)
  - [🗂 Datasets](#-datasets-3)
  - [🤖 Models](##-models-4)
- [🤝 Gesture](#-gesture)
  - [🗂 Datasets](#-datasets-4)
  - [🤖 Models](##-models-5)
- [🎥 Motion](#-motion)
  - [🗂 Datasets](#-datasets-5)
  - [🤖 Models](##-models-6)
- [📦 Object](#-object)
  - [🗂 Datasets](#-datasets-6)
  - [🤖 Models](##-models-7)
- [🧵 Texture](#-texture)
  - [🗂 Datasets](#-datasets-7)
  - [🤖 Models](##-models-8)
<!-- - [🔗 Citations](#-citations)
- [📧 Contact](#-contact)
- [⭐️ Star History](#-star-history) -->

---

## 📝 Abstract 

Generative AI is transforming various fields, including art, gaming, and animation. One of its most significant applications lies in animation, where advances in artificial intelligence—such as foundation models and diffusion models—have driven remarkable progress, significantly reducing the time and cost of content creation. Characters are central components of animations involving elements such as motion, emotions, gestures, and facial expressions. Rapid and wide-ranging developments in AI-driven animation technologies have made it challenging to maintain an overarching view of progress in the field, highlighting the need for a comprehensive survey to integrate and contextualize these advancements.

This survey offers a comprehensive review of the state-of-the-art in generative AI applications for animated character design and behavior, integrating a wide range of aspects often examined in isolation (e.g., avatars, gestures, and facial expressions). Unlike previous studies, it provides a unified perspective covering all major applications of generative AI in character animation. The survey begins with foundational concepts and introduces evaluation metrics tailored to this domain, then explores key areas such as facial animation, image synthesis, avatar generation, gesture modeling, motion synthesis, expression rendering, and texture generation. Finally, it addresses the main challenges and outlines future research directions, offering a roadmap to advance AI-driven character animation technologies. This survey aims to serve as a resource for researchers and developers in generative AI for animation and related fields.

---

## 📚 Background

### 🤖 Models

#### 🎨 Computer Graphics Models
- **SMPL** [🔗](https://smpl.is.tue.mpg.de/)  
  *A popular parametric model representing 3D human body geometry using a low-dimensional representation for shape (β) and pose (θ).*
  - **SMPL+H**  
    *An extension of SMPL that incorporates detailed hand modeling by introducing hand joint parameters (θhands).*
  - **SMPL-X**  
    *Further extends SMPL+H by including facial expressions along with detailed hand and body modeling for full-body human representation.*
- **SMIL (Skinned Multi-Infant Linear Model)** [🔗](https://files.is.tue.mpg.de/black/papers/miccai18.pdf)  
  *A model developed specifically for infants, addressing challenges in capturing non-cooperative subjects with low-quality RGB-D data.*
- **SMAL (Skinned Multi-Animal Linear Model)** [🔗](https://smal.is.tue.mpg.de/)  
  *Designed for 3D modeling of animals, enabling the creation of a shape space from a few scans of diverse species.*

#### 👀 Vision
- **Convolutional Neural Networks (CNNs)** [🔗](https://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf)  
  *CNNs are specialized for image-related tasks by using convolution, pooling, and fully connected layers.*
- **3D CNNs** [🔗](https://www.cv-foundation.org/openaccess/content_iccv_2015/html/Tran_Learning_Spatiotemporal_Features_ICCV_2015_paper.html)  
  *Extend CNNs to process volumetric data (e.g., videos, MRI scans) by using 3D convolutional kernels.*
- **U-Net** [🔗](https://arxiv.org/abs/1505.04597)  
  *A U-shaped network architecture designed for biomedical image segmentation, known for its efficient denoising and skip connections.*
- **Inception** [🔗](https://arxiv.org/abs/1409.4842)  
  *Introduces multi-scale processing via parallel convolutions (1x1, 3x3, 5x5) for improved feature extraction.*
- **VGG** [🔗](https://arxiv.org/abs/1409.1556)  
  *Evaluates the impact of increasing CNN depth using very small (3x3) filters to capture complex visual features.*
- **ResNet** [🔗](https://arxiv.org/abs/1512.03385)  
  *Introduces residual learning with shortcut connections to enable training of very deep networks (up to 152 layers).*
- **Vision Transformers (ViTs)** [🔗](https://arxiv.org/abs/2010.11929)  
  *Applies the self-attention mechanism to image patches, offering competitive performance on image recognition tasks.*

#### 📝 Language Models
- **RNNs** [🔗](https://en.wikipedia.org/wiki/Recurrent_neural_network)  
  *General recurrent neural networks for sequence modeling.*
- **Bidirectional RNNs (BRNNs)** [🔗](https://ieeexplore.ieee.org/document/650093)  
  *Process sequences in both directions to leverage past and future context.*
- **Encoder-Decoder Frameworks** [🔗](https://arxiv.org/abs/1409.3215)  
  *Used for tasks like machine translation by compressing sequences into a fixed-length vector.*
- **LSTMs** [🔗](https://www.bioinf.jku.at/publications/older/2604.pdf)  
  *Introduces memory cells and gating mechanisms to capture long-term dependencies.*
- **GRUs** [🔗](https://arxiv.org/abs/1406.1078)  
  *A streamlined variant of LSTMs merging input and forget gates into an update gate.*
- **Attention Mechanisms** [🔗](https://arxiv.org/abs/1706.03762)  
  *Allows models to dynamically focus on different parts of the input sequence.*
- **Transformers** [🔗](https://arxiv.org/abs/1706.03762)  
  *Utilize self-attention to process sequences without recurrence.*
- **BERT** [🔗](https://arxiv.org/abs/1810.04805)  
  *Bidirectional Encoder Representations from Transformers for deep language understanding.*
- **GPT Series:**  
  - **GPT-1** [🔗](https://cdn.openai.com/research-covers/language-unsupervised/language_understanding_paper.pdf)  
  - **GPT-2** [🔗](https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf)  
  - **GPT-3** [🔗](https://arxiv.org/abs/2005.14165)  
  - **GPT-3.5 / ChatGPT**  
  - **InstructGPT** [🔗](https://arxiv.org/abs/2203.02155)  
  - **GPT-4** [🔗](https://arxiv.org/abs/2303.08774)  
  - **GPT-4-O** [🔗](https://arxiv.org/abs/2410.21276)  
- **PoseGPT** [🔗](https://arxiv.org/abs/2210.10542)  
  *Specialized for pose estimation in video generation.*
- **GestureGPT** [🔗](https://arxiv.org/abs/2310.12821)  
  *Extends the GPT framework to generate realistic human gestures based on text or audio input.*
- **MotionGPT** [🔗](https://arxiv.org/abs/2306.14795)  
  *Designed for generating motion sequences.*

#### 🕒 Temporal Sequence Modeling 
- **Temporal Convolutional Networks (TCNs)** [🔗](https://arxiv.org/abs/1803.01271)  
  *Use causal and dilated convolutions to model sequential data efficiently.*
- **Transformer-XL** [🔗](https://arxiv.org/abs/1901.02860)  
  *Extends Transformers with a segment-level recurrence mechanism to capture long-range dependencies.*
- **ConvLSTM** [🔗](https://arxiv.org/abs/1506.04214)  
  *Combines CNNs and LSTM units to capture both spatial and temporal dynamics in spatiotemporal data.*

#### 🗣 Speech Models
- **WaveNet** [🔗](https://arxiv.org/abs/1609.03499)  
  *An autoregressive model for raw audio synthesis using dilated causal convolutions.*
- **Tacotron** [🔗](https://arxiv.org/abs/1703.10135)  
  *A sequence-to-sequence TTS model that converts text to mel-spectrograms via attention.*
- **Tacotron 2** [🔗](https://arxiv.org/abs/1712.05884)  
  *Combines Tacotron with a WaveNet vocoder for end-to-end, high-fidelity speech synthesis.*
- **FastSpeech** [🔗](https://arxiv.org/abs/1905.09263)  
  *A non-autoregressive TTS model using transformers for parallel synthesis to reduce latency.*
- **FastSpeech 2** [🔗](https://arxiv.org/abs/2006.04558)  
  *Improves FastSpeech by introducing variance predictors for pitch, energy, and duration for more natural speech.*
- **Wave2Vec** [🔗](https://arxiv.org/abs/1904.05862)  
  *A self-supervised framework for learning robust speech representations directly from raw audio.*
- **Wave2Vec 2.0** [🔗](https://arxiv.org/abs/2006.11477)  
  *Enhances Wave2Vec with quantization and contextual embeddings to improve ASR performance.*
- **HuBERT** [🔗](https://arxiv.org/abs/2106.07447)  
  *Uses clustering-based pseudo-labeling and masked prediction to learn effective speech representations.*
- **Whisper** [🔗](https://arxiv.org/pdf/2212.04356)  
  *A transformer-based model for multilingual ASR, translation, and transcription with zero-shot capabilities.*
- **SeamlessM4T** [🔗](https://arxiv.org/abs/2308.11596)  
  *An end-to-end model for universal speech translation and generation that preserves speaker emotion via attention.*

#### 🎭 Additional Generative Models
- **GANs (Generative Adversarial Networks)** [🔗](https://arxiv.org/abs/1406.2661)  
  *An adversarial framework where a generator and discriminator engage in a minimax game to synthesize realistic data.*
- **CycleGAN** [🔗](https://arxiv.org/abs/1703.10593)  
  *Enables unpaired image-to-image translation by enforcing cycle consistency between two domains.*
- **Autoencoders**  
  *A general framework that compresses input data into a latent representation and reconstructs it for unsupervised learning.*
- **Variational Autoencoders (VAEs)** [🔗](https://arxiv.org/abs/1312.6114)  
  *Probabilistic autoencoders that regularize the latent space using KL divergence to generate new data samples.*
- **Vector Quantized VAEs (VQ-VAEs)** [🔗](https://arxiv.org/abs/1711.00937)  
  *Enhances VAEs by discretizing the latent space with a codebook for more structured representations.*
- **NeRF (Neural Radiance Fields)** [🔗](https://arxiv.org/abs/2003.08934)  
  *Learns an implicit 3D scene representation via volumetric rendering for novel view synthesis.*
- **3D Gaussian Splatting (3DGS)** [🔗](https://arxiv.org/abs/2308.04079)  
  *Represents 3D scenes with a collection of Gaussian functions for efficient real-time rendering.*
- **Denoising Diffusion Probabilistic Models (DDPMs)** [🔗](https://arxiv.org/abs/2006.11239)  
  *Generates high-quality outputs by iteratively denoising data from a latent space.*
- **ControlNet** [🔗](https://arxiv.org/abs/2302.05543)  
  *Augments diffusion models with auxiliary conditioning inputs for precise image generation.*
- **DALL-E** [🔗](https://arxiv.org/abs/2102.12092)  
  *An autoregressive transformer that generates images from text by jointly modeling text and image tokens.*

---

### 📊 Metrics 

#### ✅ Quality and Realism of Generated Output

These metrics assess how natural, realistic, and perceptually convincing the generated content appears.

| **Metric** | **Description** | **Formula** |
|------------|-----------------|-------------|
| **Fréchet Inception Distance (FID)** | Measures statistical distance between real and generated images. | $\text{FID} = \lVert \mu_r - \mu_g \rVert^2 + \text{tr}(\Sigma_r + \Sigma_g - 2(\Sigma_r\Sigma_g)^{1/2})$ |
| **CLIP Score** | Evaluates semantic similarity between generated images and textual descriptions. | $\text{CLIPScore} = \frac{\cos(t,i)}{\lVert t \rVert \cdot \lVert i \rVert}$ |
| **Mean Squared Error (MSE)** | Measures pixel-wise difference between generated and real images. | $\text{MSE} = \frac{1}{n}\sum{(x_i - y_i)^2}$ |
| **Learned Perceptual Image Patch Similarity (LPIPS)** | Assesses perceptual similarity using deep feature embeddings. | $\text{LPIPS}(x,y) = \sum_l \frac{1}{H_l W_l} \sum_{h,w}\lVert \phi_l(x)^{h,w}-\phi_l(y)^{h,w} \rVert_2^2$ |
| **Identity Consistency** | Ensures identity preservation in generated faces by computing cosine similarity. | $\text{IC} = \frac{1}{N}\sum \text{cosine-sim}(f(x_i), f(y_i))$ |
| **Fréchet Gesture Distance (FGD)** | Measures statistical differences between real and generated gesture distributions. | $\text{FGD} = \lVert \mu_{\text{gesture real}} - \mu_{\text{gesture gen}} \rVert^2 + \text{tr}(\Sigma_{\text{real}} + \Sigma_{\text{gen}} - 2(\Sigma_{\text{real}}\Sigma_{\text{gen}})^{1/2})$ |
| **CLIP Fréchet Inception Distance (CLIP FID)** | A CLIP-based extension of FID for assessing generated textures. | $\text{CLIPFID} = \lVert \mu_{\text{gesture real}} - \mu_{\text{gesture gen}} \rVert^2 + \text{tr}(\Sigma_{\text{real}} + \Sigma_{\text{gen}} - 2(\Sigma_{\text{real}}\Sigma_{\text{gen}})^{1/2})$ |



---

#### 🔄 Diversity and Multimodality

These metrics assess whether the generative model produces diverse and varied outputs.


| **Metric** | **Description** | **Formula** |
|------------|-----------------|-------------|
| **Diversity** | Quantifies variation between independently sampled subsets of generated outputs. | $\text{Diversity} = \frac{1}{N}\sum \lVert x_i - x'_i \rVert^2$ |
| **Multimodality** | Measures diversity of outputs within the same action class. | $\text{Multimodality} = \frac{1}{C \cdot N}\sum \lVert x_{c,n} - x'_{c,n} \rVert^2$ |
| **Average Pairwise Distance (APD)** | Evaluates diversity across generated samples. | $\text{APD} = \frac{1}{N(N-1)}\sum \lVert x_i - x_j \rVert$ |

---

#### 🎯 Relevance and Accuracy

These metrics assess how well the generated content aligns with ground truth data.


| **Metric** | **Description** | **Formula** |
|------------|-----------------|-------------|
| **Mean Absolute Joint Error (MAJE)** | Measures positional accuracy of generated motion. | $\text{MAJE} = \frac{1}{n}\sum \lvert x_i - y_i \rvert$ |
| **Probability of Correct Keypoints (PCK)** | Evaluates the percentage of correct keypoint predictions. | $\text{PCK} = \frac{\text{number of correct keypoints}}{\text{number of total keypoints}}$ |
| **Beat Consistency (BC)** | Measures alignment between motion and speech rhythms. | $\text{BC} = \frac{1}{T}\sum \cos(\text{motion-beats}(t), \text{speech-beats}(t))$ |
| **CLIP-Var** | Quantifies texture consistency across different views. | $\text{CLIP-Var} = \min(\cos(f_i, f_j)), \quad i \neq j$ |
| **Multimodal Distance (MM-Distance)** | Measures alignment between generated motion and textual descriptions. | $\text{MM-Distance} = \sqrt{\frac{1}{N}\sum\lVert f_{a,n}-f_{b,n} \rVert^2}$ |



---

#### 🏃 Physical Plausibility and Interaction

These metrics assess whether generated motion adheres to real‑world physical constraints.

| **Metric** | **Description** | **Formula** |
|------------|-----------------|-------------|
| **Foot Skating (FS)** | Detects unnatural foot movements in generated motion. | $\text{FS} = \frac{1}{T}\sum\lVert \text{foot-velocity}(t) - \text{expected-velocity}(t) \rVert$ |
| **Mean Acceleration Difference (MAD)** | Evaluates smoothness of generated motion by comparing acceleration. | $\text{MAD} = \frac{1}{n}\sum\lVert \text{acceleration}_i - \text{acceleration-pred}_i \rVert^2$ |


---

#### ⚡️ Efficiency and Computational Metrics

These metrics evaluate the computational cost of generative models.

| **Metric** | **Description** | **Formula** |
|------------|-----------------|-------------|
| **Execution Time** | Measures the time required to generate outputs. | $\text{Execution Time} = \text{End Time} - \text{Start Time}$ |
| **Kernel Inception Distance (KID)** | Measures output similarity using kernel functions. | $\text{KID} = \frac{1}{n(n-1)}\sum k(\phi(x_i),\phi(x_j)) + \frac{1}{m(m-1)}\sum k(\phi(y_i),\phi(y_j)) - \frac{2}{nm}\sum k(\phi(x_i),\phi(y_j))$ |

---

## 👨 Face
Focuses on realistic face generation, facial reenactment, and attribute editing using GANs, diffusion models, and specialized frameworks.

### 🗂 Datasets

# 📊 Facial Datasets Overview

This table provides an overview of various facial datasets, highlighting their key statistics, modalities, and links.

| 🏷️ **Name** | 📊 **Statistics** | 🎭 **Modalities** | 🔗 **Link** |
|-------------|------------------|------------------|-------------|
| **RaFD** | More than 8,000 images of 67 models displaying eight facial expressions from five different angles. | 🖼️ Images | [RaFD](https://rafd.socsci.ru.nl/) |
| **MPIE** | Over 750,000 images with variations in facial expressions, head poses, and lighting. | 🖼️ Images with metadata | [MPIE](https://www.cs.cmu.edu/afs/cs/project/PIE/MultiPie/Multi-Pie/Home.html) |
| **VoxCeleb1** | 100,000+ utterances from 1,251 celebrities. | 🎥 Audio-Video (facial images from video clips) | [VoxCeleb1](https://www.robots.ox.ac.uk/~vgg/data/voxceleb/) |
| **VoxCeleb2** | Over 1 million utterances from 6,112 celebrities. | 🎥 Audio-Video (facial images from video clips) | [VoxCeleb2](https://www.robots.ox.ac.uk/~vgg/data/voxceleb/) |
| **CelebA-HQ** | 30,000 images at 1024×1024 resolution. | 🖼️ Images | [CelebA-HQ](https://opendatalab.com/OpenDataLab/CelebA-HQ) |
| **FaceForensics** | Over 1,000 video sequences with face manipulations. | 🎥 Video | [FaceForensics](https://justusthies.github.io/posts/faceforensics/) |
| **300-VW** | 300+ videos of faces in diverse scenarios and lighting. | 🎥 Videos with facial landmarks | [300-VW](https://ibug.doc.ic.ac.uk/resources/300-VW/) |
| **FFHQ** | 70,000 images capturing diverse facial features and environments. | 🖼️ Facial Images | [FFHQ](https://www.computer.org/csdl/journal/tp/2021/12/08977347/1h2AHNHb9bW) |
| **AffectNet** | 1M+ images annotated for 11 facial expressions and emotions. | 😃 Image annotations for emotion | [AffectNet](http://mohammadmahoor.com/affectnet/) |
| **M³ CelebA** | 150K+ facial images with semantic segmentation, facial landmarks, and multilingual captions. | 🏷️ Face images with annotations | [M³ CelebA](https://huggingface.co/datasets/m3face/M3CelebA/viewer) |
| **CUB** | 11,000+ images of 200 bird species with detailed annotations. | 🐦 Bird images with attributes | [CUB](https://www.vision.caltech.edu/datasets/cub_200_2011/) |
| **CelebA-Dialog** | 202,599 face images annotated with 5 fine-grained attributes and captions. | 💬 Facial images with textual annotations | [CelebA-Dialog](https://mmlab.ie.cuhk.edu.hk/projects/CelebA/CelebA_Dialog.html) |
| **LS3D-W** | 230,000+ 3D facial landmarks dataset. | 🖼️ Facial Images | [LS3D-W](https://www.adrianbulat.com/face-alignment) |
| **MERL-RAV** | 19,000+ face images annotated with 68-point landmarks and head poses. | 🎥 Videos & audio with annotations | [MERL-RAV](https://github.com/abhi1kumar/MERL-RAV_dataset) |
| **AFLW2000-3D** | 2,000 images with 68-point 3D facial landmarks. | 🏷️ Facial images with 3D annotations | [AFLW2000-3D](https://github.com/tensorflow/datasets/blob/master/docs/catalog/aflw2k3d.md) |
| **FaceScape** | 18K+ high-resolution 3D facial scans from 938 subjects with 20 expressions each. | 📏 3D facial scans | [FaceScape](https://facescape.nju.edu.cn/) |


### 🤖 Models

## 😃 Expression
Covers emotion-driven synthesis, facial expression retargeting, and multimodal methods that capture nuanced nonverbal cues.

### 🗂 Datasets

| 🏷️ **Name** | 📊 **Statistics** | 🎭 **Modalities** | 🔗 **Link** |
|------------|------------------|------------------|------------|
| **BEAT (Body-Expression-Audio-Text)** | 76 hours of speech, 52D facial blend shape weights, 30 speakers, 8 emotional styles, 4 languages. | 🎵 Audio, 🎭 Facial Expressions, 😃 Emotion, 🏃 Gesture, 📝 Text | [BEAT](https://pantomatrix.github.io/BEAT/) |
| **MEAD (Multi-view Emotional Audio-visual Dataset)** | 60 actors in 8 emotions at 3 intensity levels, ~40 hours of 🎵 audio-visual clips per view. | 🎥 Video, 🎵 Audio, 😃 Emotion, 🎭 Facial Expressions | [MEAD](https://wywu.github.io/projects/MEAD/MEAD.html) |
| **TEAD (Text-Expression Aligned Dataset)** | 50,000 quadruples with text, emotion tags, Action Units, and blend shape weights. | 📝 Text, 😃 Emotion, 🎭 Facial Expressions | - |
| **JAFFE (Japanese Female Facial Expression)** | 213 images of 7 facial expressions posed by 10 Japanese female models, rated by 60 annotators. | 🖼️ Image, 🎭 Facial Expressions | [JAFFE](https://zenodo.org/records/3451524) |
| **MMI Facial Expression** | 2900+ videos and high-resolution still images from 75 subjects. | 🎥 Video, 🖼️ Image, 🎭 Facial Expressions, 😃 Emotion | [MMI](https://mmifacedb.eu/) |
| **Multiface** | High-quality face recordings of 13 identities with ~23,000 frames per subject, captured from 160 camera angles. | 🖼️ Image, 🎭 Facial Expressions, 🎵 Audio, 🏃 Pose | [Multiface](https://github.com/facebookresearch/multiface) |
| **ICT FaceKit** | 4000 high-resolution facial scans from 79 subjects (ages 18-67), plus 99 full head scans with 26 expressions. | 🎭 3D Geometry, Facial Expressions, 🎭 Texture | [ICT FaceKit](https://github.com/ICT-VGL/ICT-FaceKit) |
| **TikTok Dataset** | 300+ dance videos (10-15s each), ~100K extracted frames at 30fps with UV coordinates. | 🎥 Video, 🖼️ Image, 🏃 Pose | [TikTok Dataset](https://www.yasamin.page/hdnet_tiktok#h.jr9ifesshn7v) |
| **Everybody Dance Now** | Long single-dancer videos for training and evaluation, includes self-filmed and YouTube videos. | 🎥 Video, 🏃 Pose | [Everybody Dance Now](https://carolineec.github.io/everybody_dance_now/) |
| **Obama Weekly Footage** | 17 hours of footage (~2M frames) spanning 8 years. | 🎥 Video, 🎵 Audio | [Obama Weekly Footage](https://grail.cs.washington.edu/projects/AudioToObama/) |
| **VoxCeleb2** | 1M+ utterances from 6,000+ speakers, collected from YouTube videos (61% male speakers). | 🎵 Audio, 🎥 Video | [VoxCeleb2](https://www.robots.ox.ac.uk/~vgg/data/voxceleb/vox2.html) |
| **BIWI** | 15K+ images of 20 people recorded with Kinect while turning heads freely. | 🎭 3D Geometry, 🖼️ Image, 🏃 Pose, 😃 Emotion | [BIWI](https://paperswithcode.com/dataset/biwi-kinect-head-pose) |
| **VOCASET** | 29 minutes of high-fidelity 4D scans at 60fps, synchronized with 🎵 audio; 12 speakers, 40 sequences per subject. | 🎥 4D Scans, 🎵 Audio | [VOCASET](https://voca.is.tue.mpg.de/) |
| **SHOW (Synchronous Holistic Optimization in the Wild)** | SMPLX parameters for 4 persons reconstructed from videos; includes 88-frame motion clips. | 🎥 Video, 🎵 Audio, 🎭 Facial Expressions, 🏃 Pose | [SHOW](https://github.com/yhw-yhw/SHOW) |


### 🤖 Models

## 🖼 Image
Explores diffusion-based methods, VAEs, and other generative techniques to produce high-fidelity images and textures for animation backgrounds and elements.

### 🗂 Datasets

| 🏷️ **Name** | 📊 **Statistics** | 🎭 **Modalities** | 🔗 **Link** |
|------------|------------------|------------------|------------|
| **LAION-5B** | 5.85 billion CLIP-filtered image-text pairs | 🖼️ Image-Text Pairs | [LAION-5B](https://laion.ai/blog/laion-5b/) |
| **LAION-400M** | 400M English (image, text) pairs | 🖼️ Image-Text Pairs | [LAION-400M](https://laion.ai/blog/laion-400-open-dataset/) |
| **LAION-Aesthetics v2** | 1.2B images with aesthetics scores (various thresholds from 4.5 to 6.5) | 🖼️ Image-Text Pairs | [LAION-Aesthetics v2](https://laion.ai/blog/laion-aesthetics/) |
| **Open Images V7** | 9M images annotated with object labels, bounding boxes, segmentation masks, and visual relationships | 🖼️📏 Images with Annotations | [Open Images V7](https://storage.googleapis.com/openimages/web/index.html) |
| **COYO** | 747M image-text pairs | 🖼️ Image-Text Pairs | [COYO](https://github.com/kakaobrain/coyo-dataset) |
| **Conceptual Captions** | 3.3M images with descriptive captions | 🖼️ Image-Text Pairs | [Conceptual Captions](https://ai.google.com/research/ConceptualCaptions/) |
| **COCO** | 330K images (200K labeled), 1.5M object instances, 80 object categories, 91 stuff categories, 5 captions per image, 250K people with key points | 🏷️ Object Detection, 🖼️ Segmentation, ✍️ Captions | [COCO](https://cocodataset.org) |
| **ShareGPT** | 100K highly descriptive image-caption pairs | 🖼️ Image-Text Pairs | [ShareGPT](https://huggingface.co/datasets/Lin-Chen/ShareGPT4V) |
| **ADE20K** | 20,210 training images, 2,000 validation images, 3,000 test images | 🏙️ Scene Parsing, 🖼️ Images with Annotations | [ADE20K](https://groups.csail.mit.edu/vision/datasets/ADE20K/) |


### 🤖 Models

## 👤 Avatar
Reviews approaches for both 2D and 3D avatar creation, emphasizing lifelike digital representations with detailed facial expressions and body dynamics.

### 🗂 Datasets

| 🏷️ **Name** | 📊 **Statistics** | 🎭 **Modalities** | 🔗 **Link** |
|------------|------------------|------------------|------------|
| **WildAvatar** | 10,000+ human subjects extracted from YouTube; significantly richer than previous 3D avatar datasets. | 🎥 Video, 🏃 3D Body Motion, 🎵 Audio | [WildAvatar](https://wildavatar.github.io/) |
| **ZJU-MoCap** | Multi-camera system (20+ cameras); includes SMPL-X parameters for body, hand, and face motion capture. | 🎥 Video, 🏃 3D Body Motion, 🔷 SMPL-X Parameters | [ZJU-MoCap](https://chingswy.github.io/Dataset-Demo/) |
| **TalkSHOW** | 26.9 hours of in-the-wild talking videos (4 speakers); expressive 3D whole-body meshes at 30 fps, synchronized with 🎵 audio at 22 kHz. | 🎵 Audio, 🏃 3D Body Meshes | [TalkSHOW](https://talkshow.is.tue.mpg.de/) |
| **HuMMan** | 1,000 human subjects, 400K sequences, 60M frames; includes point clouds, SMPL parameters, and textured meshes. | 🎥 Video, 📏 Point Clouds, 🔷 SMPL Parameters, 🎭 Textured Meshes | [HuMMan](https://caizhongang.com/projects/HuMMan/) |
| **BUFF** | 6 subjects performing motions in two clothing styles; 13,632 3D scans with high-resolution minimally-clothed shapes. | 🏃 3D Body Scans, 🎭 Textured 3D Meshes | [BUFF](https://buff.is.tue.mpg.de/) |
| **AMASS** | 15 motion capture datasets merged; 42+ hours of motion data, 346 subjects, 11,451 motions, SMPL parameters. | 🏃 3D Body Motion, 🔷 SMPL Parameters | [AMASS](https://amass.is.tue.mpg.de/) |
| **3DPW** | 60 video sequences with 3D pose estimation using IMU sensors and video data; includes 18 re-poseable body models. | 🎥 Video, 🏃 2D/3D Poses, 📡 IMU Data, 🏃 3D Body Scans | [3DPW](https://virtualhumans.mpi-inf.mpg.de/3DPW/) |
| **AIST++** | 10M+ frames of 3D keypoints; 1,408 dance motion sequences spanning 10 genres, synchronized with 🎵 music. | 🎥 Video, 🎵 Audio, 🏃 3D Keypoints, 🔷 SMPL Parameters | [AIST++](https://google.github.io/aistplusplus_dataset/) |
| **RenderMe-360** | 243M head frames from 500 identities; includes FLAME parameters, UV maps, action units, and textured meshes. | 🎥 Video, 🎭 2D/3D Facial Landmarks, 🔷 FLAME Parameters | [RenderMe-360](https://renderme-360.github.io/) |
| **PuzzleIOI** | 41 subjects with nearly 1,000 Outfit-of-the-Day (OOTD) configurations; paired 3D body scans for partial images. | 🖼️ Image, 🏃 3D Body Models, 📝 Text Descriptions | [PuzzleIOI](https://puzzleavatar.is.tue.mpg.de/) |

### 🤖 Models

## 🤝 Gesture
Examines methods for generating human-like gestures and co-speech movements, critical for interactive and immersive animations.

### 🗂 Datasets

### 🤖 Models

## 🎥 Motion
Highlights text-constrained motion generation techniques, including MotionGPT and diffusion frameworks, for creating smooth and realistic animation sequences.

### 🗂 Datasets

### 🤖 Models

## 📦 Object
Discusses approaches for text-to-3D object generation, such as Neural Radiance Fields (NeRFs) and 3D Gaussian Splatting, to create realistic assets.

### 🗂 Datasets

### 🤖 Models

## 🧵 Texture
Focuses on methods for generating detailed surface textures that enhance the realism of 3D models, including text-guided synthesis and neural rendering techniques.

### 🗂 Datasets

### 🤖 Models

---

<!-- ## 🔗 Citations {-citations}

If you find our survey or repository useful, please consider citing our paper: -->

<!-- --------------------------------------------------------- -->

<!-- # Generative-AI-for-Character-Animation

# Background

| Name | Link |
|------|------|

# Metrics

| Name | Link |
|------|------|

# Face

## Dataset

| Name | Link |
|------|------|

## Works

| Name | Link |
|------|------|

# Expression

## Dataset

| Name | Link |
|------|------|

## Works

| Name | Link |
|------|------|

# Image

## Dataset

| Name | Link |
|------|------|

## Works

| Name | Link |
|------|------|

# Avatar

## Dataset

| Name | Link |
|------|------|

## Works

| Name | Link |
|------|------|

# Gesture

## Dataset

| Name | Link |
|------|------|

## Works

| Name | Link |
|------|------|

# Motion

## Dataset

| Name | Link |
|------|------|

## Works

| Name | Link |
|------|------|

# Object

## Dataset

| Name | Link |
|------|------|

## Works

| Name | Link |
|------|------|

# Texture

## Dataset

| Name | Link |
|------|------|

## Works

| Name | Link |
|------|------| -->
