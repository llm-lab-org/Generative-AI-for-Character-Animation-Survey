# Generative AI for Character Animation: A Comprehensive Survey of Techniques, Applications, and Future Directions

[![arXiv](https://img.shields.io/badge/arXiv-Paper-<COLOR>.svg)](https://arxiv.org/abs/your_eprint_number)

This repository is designed to collect and categorize papers, datasets, and resources related to generative AI for character animation based on our survey. As advances in generative AI continue to transform animation from realistic facial synthesis to dynamic gesture and motion generation, this resource will be continuously updated to serve as a comprehensive guide for researchers and practitioners.

---

## 📑 List of Contents

- [📝 Abstract](#-abstract)
- [🗺 Overview](#-overview)
- [🌳 Taxonomy](#-taxonomy)
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
  - [🤖 Models](#-models-1)
- [😃 Expression](#-expression)
  - [🗂 Datasets](#-datasets-1)
  - [🤖 Models](#-models-2)
    - [🎙 Speech-Driven & Multimodal Expression Generation](#-speech-driven--multimodal-expression-generation)
    - [🔁 Expression Retargeting & Motion Transfer](#-expression-retargeting--motion-transfer)
- [🖼 Image](#-image)
  - [🗂 Datasets](#-datasets-2)
  - [🤖 Models](#-models-3)
    - [🔧 Fine-Tuning & Regularization](#-fine-tuning--regularization)
    - [✂ Image Editing & Disentanglement](#-image-editing--disentanglement)
    - [👽 Multimodal Conversations & Visual Understanding](#-multimodal-conversations--visual-understanding)
- [👤 Avatar](#-avatar)
  - [🗂 Datasets](#-datasets-3)
  - [🤖 Models](#-models-4)
    - [🔍 CLIP-Guided Models](#-clip-guided-models)
    - [🧩 Implicit Function-Based Models](#-implicit-function-based-models)
    - [🎥 NeRF-Based Methods](#-nerf-based-methods)
    - [🌈 Diffusion-Based Methods](#-diffusion-based-methods)
    - [🔀 Hybrid Methods](#-hybrid-methods)
- [🤝 Gesture](#-gesture)
  - [🗂 Datasets](#-datasets-4)
  - [🤖 Models](#-models-5)
    - [🛠 Traditional & Parametric Approaches](#-traditional--parametric-approaches)
    - [🧠 Deep Learning-Based Models](#-deep-learning-based-models)
    - [🚀 Transformer-Based Models](#-transformer-based-models)
- [🎥 Motion](#-motion)
  - [🗂 Datasets](#-datasets-5)
  - [🤖 Models](#-models-6)
    - [🔤 Language-to-Pose Models](#-language-to-pose-models)
    - [📦 Variational Auto-Encoder (VAE) Based Models](#-variational-auto-encoder-vae-based-models)
    - [🗝 VQ-VAE Based Models](#-vq-vae-based-models)
    - [🌈 Diffusion-Based Models](#-diffusion-based-models)
- [📦 Object](#-object)
  - [🗂 Datasets](#-datasets-6)
  - [🤖 Models](#-models-7)
- [🧵 Texture](#-texture)
  - [🗂 Datasets](#-datasets-7)
  - [🤖 Models](#-models-8)
<!-- - [🔗 Citations](#-citations)
- [📧 Contact](#-contact)
- [⭐️ Star History](#-star-history) -->

---

## 📝 Abstract 

Generative AI is transforming various fields, including art, gaming, and animation. One of its most significant applications lies in animation, where advances in artificial intelligence—such as foundation models and diffusion models—have driven remarkable progress, significantly reducing the time and cost of content creation. Characters are central components of animations involving elements such as motion, emotions, gestures, and facial expressions. Rapid and wide-ranging developments in AI-driven animation technologies have made it challenging to maintain an overarching view of progress in the field, highlighting the need for a comprehensive survey to integrate and contextualize these advancements.

This survey offers a comprehensive review of the state-of-the-art generative AI applications for animated character design and behavior, integrating a wide range of aspects often examined in isolation (e.g., avatars, gestures, and facial expressions). Unlike previous studies, it provides a unified perspective covering all major applications of generative AI in character animation. The survey begins with foundational concepts and introduces evaluation metrics tailored to this domain, then explores key areas such as facial animation, image synthesis, avatar generation, gesture modeling, motion synthesis, expression rendering, and texture generation. Finally, it addresses the main challenges and outlines future research directions, offering a roadmap to advance AI-driven character animation technologies. This survey aims to serve as a resource for researchers and developers in generative AI for animation and related fields.

---
## 🗺 Overview
---
## 🌳 Taxonomy
[![ Overview of different components in animated character generation. Each aspect, including face, expression, image, avatar, gesture, motion, object, and texture, plays a crucial role in enhancing realism and expressiveness within digital animation environments. Generative AI techniques, such as transformer-based and diffusion-based models, contribute to these components by improving quality, streamlining content creation, and enabling more sophisticated character animation. 
    Generative AI techniques, such as transformer-based and diffusion-based models, contribute to these components, significantly enhancing quality and streamlining content creation.](https://i.postimg.cc/GtNMTS6m/overview.png)](https://postimg.cc/rR1Gvg8B)
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
  *Evaluate the impact of increasing CNN depth using very small (3x3) filters to capture complex visual features.*
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
| **CLIP Score** | Evaluates semantic similarity between generated images and textual descriptions. | 	$\text{CLIPScore} = \frac{t \cdot i}{\lVert t \rVert \lVert i \rVert}$ |
| **Mean Squared Error (MSE)** | Measures pixel-wise difference between generated and real images. |	$\text{MSE} = \frac{1}{n}\sum_{i=1}^{n}(x_i - y_i)^2$ |
| **Learned Perceptual Image Patch Similarity (LPIPS)** | Assesses perceptual similarity using deep feature embeddings. | $\text{LPIPS}(x,y) = \sum_l \frac{1}{H_l W_l} \sum_{h=1}^{H_l}\sum_{w=1}^{W_l}\lVert \phi_l(x)^{h,w}-\phi_l(y)^{h,w} \rVert_2^2$ |
| **Identity Consistency** | Ensures identity preservation in generated faces by computing cosine similarity. | $\text{IC} = \frac{1}{N}\sum_{i=1}^{N} \text{cosine-sim}\Bigl(f(x_i), f(y_i)\Bigr)$                                                          |
| **Fréchet Gesture Distance (FGD)** | Measures statistical differences between real and generated gesture distributions. | 	$\text{FGD} = \lVert \mu_{\text{real}} - \mu_{\text{gen}} \rVert^2 + \text{tr}(\Sigma_{\text{real}} + \Sigma_{\text{gen}} - 2(\Sigma_{\text{real}}\Sigma_{\text{gen}})^{1/2})$ |
| **CLIP Fréchet Inception Distance (CLIP FID)** | A CLIP-based extension of FID for assessing generated textures. | 	$\text{CLIPFID} = \lVert \mu_{\text{CLIP,real}} - \mu_{\text{CLIP,gen}} \rVert^2 + \text{tr}(\Sigma_{\text{CLIP,real}} + \Sigma_{\text{CLIP,gen}} - 2(\Sigma_{\text{CLIP,real}} \Sigma_{\text{CLIP,gen}})^{1/2})$ |



---

#### 🔄 Diversity and Multimodality

These metrics assess whether the generative model produces diverse and varied outputs.


| **Metric** | **Description** | **Formula** |
|------------|-----------------|-------------|
| **Diversity** | Quantifies variation between independently sampled subsets of generated outputs. |	$\text{Diversity} = \frac{1}{N}\sum_{i=1}^{N}\lVert x_i - x'_i \rVert^2$ |
| **Multimodality** | Measures diversity of outputs within the same action class. | $\text{Multimodality} = \frac{1}{C \cdot N}\sum_{c=1}^{C}\sum_{n=1}^{N}\lVert x_{c,n} - x'_{c,n} \rVert^2$ |
| **Average Pairwise Distance (APD)** | Evaluates diversity across generated samples. | 	$\text{APD} = \frac{1}{N(N-1)}\sum_{i\neq j} \lVert x_i - x_j \rVert$ |

---

#### 🎯 Relevance and Accuracy

These metrics assess how well the generated content aligns with ground truth data.


| **Metric** | **Description** | **Formula** |
|------------|-----------------|-------------|
| **Mean Absolute Joint Error (MAJE)** | Measures positional accuracy of generated motion. | $\text{MAJE} = \frac{1}{n}\sum_{i=1}^{n}\lvert x_i - y_i \rvert$ |
| **Probability of Correct Keypoints (PCK)** | Evaluates the percentage of correct keypoint predictions. | $\text{PCK} = \frac{\text{number of correct keypoints}}{\text{number of total keypoints}}$ |
| **Beat Consistency (BC)** | Measures alignment between motion and speech rhythms. | $\text{BC} = \frac{1}{T}\sum_{t=1}^{T}\cos\bigl(\text{motion-beats}(t), \text{speech-beats}(t)\bigr)$ |
| **CLIP-Var** | Quantifies texture consistency across different views. |	$\text{CLIP-Var} = 1 - \min_{i \neq j}\frac{f_i \cdot f_j}{\lVert f_i \rVert \lVert f_j \rVert}$ |
| **Multimodal Distance (MM-Distance)** | Measures alignment between generated motion and textual descriptions. | $\text{MM-Distance} = \sqrt{\frac{1}{N}\sum_{n=1}^{N}\lVert f_{a,n} - f_{b,n} \rVert^2}$ |



---

#### 🏃 Physical Plausibility and Interaction

These metrics assess whether generated motion adheres to real‑world physical constraints.

| **Metric** | **Description** | **Formula** |
|------------|-----------------|-------------|
| **Foot Skating (FS)** | Detects unnatural foot movements in generated motion. | $\text{FS} = \frac{1}{T}\sum_{t=1}^{T}\lVert \text{foot-velocity}(t) - \text{expected-velocity}(t) \rVert$ |
| **Mean Acceleration Difference (MAD)** | Evaluates smoothness of generated motion by comparing acceleration. | $\text{MAD} = \frac{1}{n}\sum_{i=1}^{n}\lVert a_i^{\text{gen}} - a_i^{\text{gt}} \rVert^2$ |


---

#### ⚡️ Efficiency and Computational Metrics

These metrics evaluate the computational cost of generative models.

| **Metric** | **Description** | **Formula** |
|------------|-----------------|-------------|
| **Execution Time** | Measures the time required to generate outputs. | $\text{Execution Time} = \text{End Time} - \text{Start Time}$ |
| **Kernel Inception Distance (KID)** | Measures output similarity using kernel functions. | $\text{KID} = \frac{1}{n(n-1)} \sum_{i \neq j} k(x_i, x_j) + \frac{1}{m(m-1)} \sum_{i \neq j} k(y_i, y_j) - \frac{2}{nm} \sum_{i=1}^{n} \sum_{j=1}^{m} k(x_i, y_j)$
 |

---

## 👨 Face
Focuses on realistic face generation, facial reenactment, and attribute editing using GANs, diffusion models, and specialized frameworks.

### 🗂 Datasets

| 🏷️ Name | 📊 Statistics | 🔍 Modalities | 🔗 Link |
| --- | --- | --- | --- |
| RaFD | More than 8,000 images. Images of 67 models displaying eight facial expressions, photographed from five different angles. | 🖼️ Images | [RaFD](https://rafd.socsci.ru.nl/) |
| MPIE | Over 750,000 images with a broad range of variations in facial expressions, head poses, and lighting conditions. | 🖼️ Images | [MPIE](https://www.cs.cmu.edu/afs/cs/project/PIE/MultiPie/Multi-Pie/Home.html) |
| VoxCeleb1 | More than 100,000 utterances from 1,251 celebrities. | 🔊 Audio, 🎥 Video | [VoxCeleb1](https://www.robots.ox.ac.uk/~vgg/data/voxceleb/) |
| VoxCeleb2 | Over 1 million utterances from 6,112 celebrities. | 🔊 Audio, 🎥 Video | [VoxCeleb2](https://www.robots.ox.ac.uk/~vgg/data/voxceleb/) |
| CelebA-HQ | 30,000 images at a resolution of 1024×1024, providing detailed facial images of celebrities. | 🖼️ Images | [CelebA-HQ](https://opendatalab.com/OpenDataLab/CelebA-HQ) |
| FaceForensics | Over 1,000 video sequences with various face manipulations. | 🎥 Video | [FaceForensics](https://justusthies.github.io/posts/faceforensics/) |
| 300-VW | About 300 videos of faces in various scenarios and lighting conditions. | 🎥 Video | [300-VW](https://ibug.doc.ic.ac.uk/resources/300-VW/) |
| FFHQ | 70,000 images with extensive diversity, capturing various facial features, accessories, and environments. | 🖼️ Images | [FFHQ](https://www.computer.org/csdl/journal/tp/2021/12/08977347/1h2AHNHb9bW) |
| AffectNet | Over 1 million images collected from the internet, with annotations for 11 different facial expressions and emotions. | 🖼️ Images | [AffectNet](http://mohammadmahoor.com/affectnet/) |
| M³ CelebA | Over 150K facial images annotated with semantic segmentation, facial landmarks, and captions in multiple languages. | 🖼️ Images, 📝 Text | [M³ CelebA](https://huggingface.co/datasets/m3face/M3CelebA/viewer) |
| CUB | Over 11,000 images of 200 bird species, each annotated with various attributes like species, part locations, and bounding boxes. | 🖼️ Images | [CUB](https://www.vision.caltech.edu/datasets/cub_200_2011/) |
| CelebA-Dialog | 202,599 face images from 10,177 identities, annotated with 5 fine-grained attributes: Bangs, Eyeglasses, Beard, Smiling, Age, along with captions and user editing requests. | 🖼️ Images, 📝 Text | [CelebA-Dialog](https://mmlab.ie.cuhk.edu.hk/projects/CelebA/CelebA_Dialog.html) |
| LS3D-W | A dataset of 230,000 3D facial landmarks. | 🖼️ Images | [LS3D-W](https://www.adrianbulat.com/face-alignment) |
| MERL-RAV | Over 19,000 face images with diverse head pose, all annotated by 68 point landmarks and visibility status. | 🔊 Audio, 🎥 Video | [MERL-RAV](https://github.com/abhi1kumar/MERL-RAV_dataset) |
| AFLW2000-3D | Contains 2000 images with 68-point 3D facial landmarks, used to evaluate 3D facial landmark detection models with diverse head poses. | 🖼️ Images, 🔷 3D/Point Cloud Data | [AFLW2000-3D](https://github.com/tensorflow/datasets/blob/master/docs/catalog/aflw2k3d.md) |
| FaceScape | Over 18K textured 3D faces, captured from 938 subjects, each with 20 specific expressions. | 🔷 3D/Point Cloud Data | [FaceScape](https://facescape.nju.edu.cn/) |

---

### 🤖 Models

- **StyleGAN** [🔗](https://arxiv.org/abs/1812.04948)  
  *A generative adversarial network known for producing high-quality, photorealistic images. It serves as a backbone for many face generation and editing tasks.*

- **ResNet** [🔗](https://arxiv.org/abs/1512.03385)  
  *A convolutional neural network architecture that provides robust feature extraction, often used as a backbone in face generation pipelines.*

- **Dual-Generator (DG)** [🔗](https://openaccess.thecvf.com/content/CVPR2022/papers/Hsu_Dual-Generator_Face_Reenactment_CVPR_2022_paper.pdf)  
  *A large-pose face reenactment model composed of two modules: the ID-Preserving Shape Generator (IDSG), which uses 3D landmark detection to capture local shape variations, and the Reenacted Face Generator (RFG), based on StarGAN2, to produce the final output.*

- **Feature Disentanglement and Identity Transfer Model** [🔗](https://www.sciencedirect.com/science/article/abs/pii/S002002552200682X)  
  *An approach that bypasses the need for pre-trained structural priors by using a Feature Disentanglement module with Feature Displacement Fields (FDF) and an Identity Transfer (IdT) module based on self-attention to align source identity with target attributes.*

- **Unified Neural Face Reenactment Pipeline** [🔗](https://openaccess.thecvf.com/content/ACCV2020/papers/Le_Minh_Ngo_Unified_Application_of_Style_Transfer_for_Face_Swapping_and_Reenactment_ACCV_2020_paper.pdf)  
  *A pipeline that leverages a 3D shape model to obtain disentangled representations of pose, expression, and identity, mapping changes in these parameters to the latent space of a fine-tuned StyleGAN2 for accurate face reenactment.*

- **Controllable 3D Generative Adversarial Face Model** [🔗](https://arxiv.org/abs/2208.14263)  
  *A model that employs a Supervised Auto-Encoder (SAE) to disentangle identity and expression into separate latent spaces, using a Conditional GAN (cGAN) for smooth and controllable expression intensity.*

- **AlbedoGAN** [🔗](https://openaccess.thecvf.com/content/WACV2024/papers/Rai_Towards_Realistic_Generative_3D_Face_Models_WACV_2024_paper.pdf)  
  *A self-supervised 3D generative face model that synthesizes high-resolution albedo and detailed 3D geometry. It refines facial textures (e.g., wrinkles) via a mesh refinement displacement map integrated with the FLAME model, and leverages CLIP for text-guided editing.*

- **IricGAN (Information Retention and Intensity Control GAN)** [🔗](https://www.researchgate.net/publication/361317388_Face_editing_based_on_facial_recognition_features)  
  *A face editing method designed to preserve identity and semantic details while enabling controlled modifications of facial attributes. It features a Hierarchical Feature Combination (HFC) module and an Attribute Regression Module (ARM) for smooth intensity control.*

- **GSmoothFace** [🔗](https://arxiv.org/abs/2312.07385)  
  *A speech-driven talking face generation framework based on fine-grained 3D face modeling. It addresses lip synchronization and generalizability across speakers by introducing bias-based cross-attention and a Morphology Augmented Face Blending (MAFB) module.*

- **Adaptive Latent Editing Model** [🔗](https://arxiv.org/abs/2307.07790)  
  *A face editing approach that uses adaptive and nonlinear latent space transformations to flexibly learn transformations for complex, conditional edits while maintaining image quality and realism.*

- **StyleT2I** [🔗](https://arxiv.org/abs/2203.15799)  
  *A text-to-image synthesis model that improves compositionality and fidelity. It uses a CLIP-guided Contrastive Loss and a Text-to-Direction module to align StyleGAN’s latent codes with text descriptions, enhancing attribute control.*

- **Hybrid Neural-Graphics Face Generation Model** [🔗](https://dl.acm.org/doi/10.1145/3588432.3591563)  
  *A model that combines neural networks (using StyleGAN2 for texture and background synthesis) with fixed-function graphics components (such as a differentiable renderer and the FLAME 3D head model) to achieve interpretable control over facial attributes.*

- **M3Face** [🔗](https://arxiv.org/abs/2402.02369)  
  *A framework leveraging multimodal and multilingual inputs for both face generation and editing. It uses the Muse model to generate segmentation masks or landmarks from text and applies ControlNet architectures to refine the results, streamlining the process into a single step.*

- **GuidedStyle** [🔗](https://arxiv.org/abs/2012.11856)  
  *A framework for semantic face editing on StyleGAN that employs a pre-trained attribute classifier as a knowledge network and sparse attention to guide layer-specific modifications, ensuring that only targeted facial features are changed.*

- **AnyFace** [🔗](https://arxiv.org/abs/2203.15334)  
  *The first free-style text-to-face synthesis model capable of handling open-world text descriptions. It features a two-stream architecture that decouples text-to-face generation from face reconstruction, using CLIP-based cross-modal distillation and a Diverse Triplet Loss to enhance alignment and diversity.*

- **HiFace** [🔗](https://arxiv.org/abs/2303.11225)  
  *A 3D face reconstruction model that decouples static (e.g., skin texture) and dynamic (e.g., wrinkles) details using its SD-DeTail Module. It extracts shape and detail coefficients via ResNet-50 and uses MLPs with AdaIN to generate detailed displacement maps for realistic reconstructions and animations.*

---

## 😃 Expression
Covers emotion-driven synthesis, facial expression retargeting, and multimodal methods that capture nuanced nonverbal cues.

### 🗂 Datasets

| 🏷️ Name | 📊 Statistics | 🔍 Modalities | 🔗 Link |
| --- | --- | --- | --- |
| BEAT | 76 hours of speech data, paired with 52D facial blend shape weights; 30 speakers performing in 8 distinct emotional styles across 4 languages. | 🔊 Audio, 🖼️ Images, 🎥 Video, 📝 Text | [BEAT](https://pantomatrix.github.io/BEAT/) |
| MEAD | A talking-face video corpus featuring 60 actors and actresses talking with eight different emotions at three intensity levels; approximately 40 hours of audio-visual clips per person and view. | 🎥 Video, 🔊 Audio, 📝 Text, 🖼️ Images | [MEAD](https://wywu.github.io/projects/MEAD/MEAD.html) |
| TEAD | 50,000 quadruples, each including text, emotion tags, Action Units, blend shape weights, and situation sentences. | 📝 Text, 🖼️ Images | - |
| JAFFE | 213 images of 10 Japanese female models posing 7 facial expressions, annotated with average semantic ratings from 60 annotators. | 🖼️ Images | [JAFFE](https://zenodo.org/records/3451524) |
| MMI Facial Expression | Over 2900 videos and high-resolution still images of 75 subjects. | 🎥 Video, 🖼️ Images, 📝 Text | [MMI](https://mmifacedb.eu/) |
| Multiface | High-quality recordings of the faces of 13 identities. An average of 23,000 frames per subject; each frame includes roughly 160 different camera views. | 🖼️ Images, 🔊 Audio, 📋 Tabular Data | [Multiface](https://github.com/facebookresearch/multiface) |
| ICT FaceKit | 4,000 high-resolution facial scans of 79 subjects (34 female, 45 male) aged 18–67, plus 99 full-head scans and 26 expressions per subject. | 🔷 3D/Point Cloud Data, 🖼️ Images | [ICT FaceKit](https://github.com/ICT-VGL/ICT-FaceKit) |
| TikTok Dataset | Over 300 single-person dance videos (10–15 seconds each), extracted at 30fps, yielding 100K+ frames. Includes segmented images and computed UV coordinates. | 🎥 Video, 🖼️ Images, 📋 Tabular Data | [TikTok Dataset](https://www.yasamin.page/hdnet_tiktok#h.jr9ifesshn7v) |
| Everybody Dance Now | Long single-dancer videos for training and evaluation; includes both self-filmed videos and short YouTube videos. | 🎥 Video, 📋 Tabular Data | [Everybody Dance Now](https://carolineec.github.io/everybody_dance_now/) |
| Obama Weekly Footage | 17 hours of video footage, nearly two million frames, spanning eight years. | 🎥 Video, 🔊 Audio | [Obama Weekly Footage](https://grail.cs.washington.edu/projects/AudioToObama/) |
| VoxCeleb2 | Over 1 million utterances from over 6,000 speakers, collected from YouTube videos with 61% male speakers. | 🔊 Audio, 🎥 Video | [VoxCeleb2](https://www.robots.ox.ac.uk/~vgg/data/voxceleb/vox2.html) |
| BIWI | Over 15K images of 20 people recorded with a Kinect while turning their heads around freely. | 🔷 3D/Point Cloud Data, 🖼️ Images, 📋 Tabular Data, 📝 Text | [BIWI](https://paperswithcode.com/dataset/biwi-kinect-head-pose) |
| VOCASET | About 29 minutes of high-fidelity 4D scans captured at 60fps, synchronized with audio; features 12 speakers with 40 sequences per subject (each sequence consists of English sentences lasting 3–5 seconds). | 🔷 3D/Point Cloud Data, 🔊 Audio | [VOCASET](https://voca.is.tue.mpg.de/) |
| SHOW | Contains SMPLX parameters of 4 persons reconstructed from videos; includes 88-frame motion clips for training and validation. | 🎥 Video, 🔊 Audio, 🖼️ Images, 📋 Tabular Data | [SHOW](https://github.com/yhw-yhw/SHOW) |


---

### 🤖 Models

#### 🎙 Speech-Driven & Multimodal Expression Generation

- **Joint Audio-Text Model for 3D Facial Animation** [🔗](https://arxiv.org/abs/2112.02214)  
  *Integrates a GPT-2-based text encoder with a dilated convolution audio encoder to improve upper-face expressiveness and lip synchronization. Lacks head and gaze control.*

- **VOCA** [🔗](https://arxiv.org/abs/1905.03079)  
  *A speech-driven facial animation model used as a baseline for lip synchronization and expressiveness.*

- **MeshTalk** [🔗](https://arxiv.org/abs/2104.08223)  
  *A model for speech-driven 3D facial animation, serving as a comparison baseline for upper-face motion and expressiveness.*

- **CSTalk** [🔗](https://arxiv.org/abs/2404.18604)  
  *Employs a transformer-based encoder to capture correlations across facial regions, enhancing emotional speech-driven animation; limited to five discrete emotions.*

- **ExpCLIP** [🔗](https://arxiv.org/abs/2308.14448)  
  *Aligns text, image, and expression embeddings via CLIP encoders, enabling expressive speech-driven facial animation from text/image prompts by leveraging the TEAD dataset and Expression Prompt Augmentation.*

- **Style-Content Disentangled Expression Model** [🔗](https://arxiv.org/abs/2412.14496)  
  *Enhances personalization in facial animation by disentangling style and content representations, thereby improving identity retention and transition smoothness. (Compared to FaceFormer.)*

- **FaceFormer** [🔗](https://arxiv.org/abs/2112.05329)  
  *A speech-driven facial animation model noted for its audio-visual synchronization, used as a baseline for comparison.*

- **AdaMesh** [🔗](https://arxiv.org/abs/2310.07236) 
  *Introduces an Expression Adapter (MoLoRA-enhanced) and a Pose Adapter (retrieval-based) for personalized speech-driven facial animation, achieving improved expressiveness, diversity, and synchronization compared to models such as GeneFace and Imitator.*

- **FaceXHuBERT** [🔗](https://galib360.github.io/FaceXHuBERT/)  
  *Explores disentangling emotional expressiveness through multimodal representations as part of advanced speech-driven facial animation.*

- **FaceDiffuser** [🔗](https://arxiv.org/abs/2309.11306)  
  *Utilizes stochastic approaches to enhance motion variability and disentangle emotional expressiveness in facial animation.*


#### 🔁 Expression Retargeting & Motion Transfer

- **Neural Face Rigging (NFR)** [🔗](https://arxiv.org/abs/2305.08296)  
  *Automates 3D mesh rigging by encoding interpretable deformation parameters, enabling fine-grained facial expression transfer.*

- **MagicPose** [🔗](https://arxiv.org/abs/2311.12052)  
  *Leverages diffusion models for 2D facial expression retargeting, balancing identity preservation and motion control through Multi-Source Attention and Pose ControlNet.*

- **DiffSHEG** [🔗](https://arxiv.org/abs/2401.04747)  
  *Pioneers joint 3D facial expression and gesture synthesis with speech-driven alignment, employing Fast Out-Painting-based Partial Autoregressive Sampling (FOPPAS) for seamless, real-time motion generation.*

- **DreamPose** [🔗](https://grail.cs.washington.edu/projects/dreampose/)   
  *A baseline model for 2D facial expression retargeting used for comparison with MagicPose.*

- **Disco** [🔗](https://arxiv.org/abs/2307.00040)  
  *Serves as a comparison baseline in 2D facial expression retargeting, noted for its identity retention and generalization capabilities.*

- **TalkSHOW** [🔗](https://talkshow.is.tue.mpg.de/)  
  *A speech-driven facial animation model referenced as a baseline for comparison with DiffSHEG.*

- **LS3DCG** [🔗](https://openaccess.thecvf.com/content/CVPR2024/papers/Chen_DiffSHEG_A_Diffusion-Based_Approach_for_Real-Time_Speech-driven_Holistic_3D_Expression_CVPR_2024_paper.pdf)   
  *A model for 3D facial expression and gesture synthesis used as a baseline when comparing motion realism and synchronization.*

- **DiffuseStyleGesture** [🔗](https://arxiv.org/abs/2305.04919)  
  *Referenced as a baseline model for facial expression and gesture synthesis in comparison to DiffSHEG.*

---

## 🖼 Image
Explores diffusion-based methods, VAEs, and other generative techniques to produce high-fidelity images and textures for animation backgrounds and elements.

### 🗂 Datasets

| 🏷️ Name           | 📊 Statistics                                                                                                                                                                          | 🔍 Modalities            | 🔗 Link                                                                                          |
| ------------------| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------- | ------------------------------------------------------------------------------------------------ |
| LAION-5B          | 5,85 billion CLIP-filtered image-text pairs                                                                                                                                            | 🖼️ Images, 📝 Text        | [LAION-5B](https://laion.ai/blog/laion-5b/)                                                       |
| LAION-400M        | 400M English (image, text) pairs                                                                                                                                                        | 🖼️ Images, 📝 Text        | [LAION-400M](https://laion.ai/blog/laion-400-open-dataset/)                                       |
| LAION-Aesthetics v2 | 1,2B aesthetics scores of ≥4.5<br>939M aesthetics scores of ≥4.75<br>600M aesthetics scores of ≥5<br>12M aesthetics scores of ≥6<br>3M aesthetics scores of ≥6.25<br>625K aesthetics scores of ≥6.5 | 🖼️ Images, 📝 Text        | [LAION-Aesthetics v2](https://laion.ai/blog/laion-aesthetics/)                                     |
| Open Images V7    | 9M images annotated with image-level labels, object bounding boxes, object segmentation masks, visual relationships, and localized narratives                                         | 🖼️ Images                | [Open Images V7](https://storage.googleapis.com/openimages/web/index.html)                       |
| COYO              | 747M image-text pairs                                                                                                                                                                  | 🖼️ Images, 📝 Text        | [COYO](https://github.com/kakaobrain/coyo-dataset)                                               |
| Conceptual Captions | 3.3M images annotated with captions                                                                                                                                                   | 🖼️ Images, 📝 Text        | [Conceptual Captions](https://ai.google.com/research/ConceptualCaptions/)                          |
| COCO              | 330K images (>200K labeled)<br>1.5 million object instances<br>80 object categories<br>91 stuff categories<br>5 captions per image<br>250,000 people with key points                | 🖼️ Images, 📝 Text        | [COCO](https://cocodataset.org)                                                                  |
| ShareGPT          | 100k highly descriptive image-caption                                                                                                                                                 | 🖼️ Images, 📝 Text        | [ShareGPT](https://huggingface.co/datasets/Lin-Chen/ShareGPT4V)                                   |
| ADE20K            | 20,210 images in the training set<br>2,000 images in the validation set<br>3,000 images in the testing set                                                                                 | 🖼️ Images                | [ADE20K](https://groups.csail.mit.edu/vision/datasets/ADE20K/)                                   |


---

### 🤖 Models


#### 🔧 Fine-Tuning & Regularization

- **Spectral Shift Fine-Tuning** [🔗](https://arxiv.org/abs/2305.18670)   
  *Introduces a compact parameter space called “spectral shift” for diffusion model fine-tuning. It reduces overfitting and storage inefficiency while achieving comparable or superior results in both single- and multi-subject generation. The method also employs the Cut Mix-Unmix data augmentation technique for improved multi-subject quality and acts as a regularizer enabling applications like single-image editing.*

- **Control via Zero Convolutions (ControlNet)** [🔗](https://arxiv.org/abs/2302.05543)  
  *Addresses the limited spatial control of text-to-image models by locking large pre-trained diffusion models and reusing their deep encoding layers as a robust backbone. Connected via “zero convolutions” (zero-initialized convolution layers), this approach progressively grows parameters from zero to prevent harmful noise during fine-tuning, thereby facilitating diverse conditional controls.*


#### ✂ Image Editing & Disentanglement

- **Lightweight Disentanglement for Image Editing** [🔗](https://ieeexplore.ieee.org/document/10175586)  
  *Explores the inherent disentanglement properties of stable diffusion models. By partially replacing text embeddings from a style-neutral description with one that reflects the desired style, a lightweight algorithm (optimizing only 50 parameters) is introduced for improved style matching and content preservation, outperforming more complex fine-tuning baselines.*

- **SmartEdit** [🔗](https://openaccess.thecvf.com/content/CVPR2024/papers/Huang_SmartEdit_Exploring_Complex_Instruction-based_Image_Editing_with_Multimodal_Large_Language_CVPR_2024_paper.pdf)  
  *Frames image editing as a supervised learning problem by generating a paired training dataset of text editing instructions with before/after images. Built on the Stable Diffusion framework, it successfully handles challenging edits such as object replacement, seasonal changes, background modifications, and alterations of material attributes or artistic mediums.*

- **Classifier-Free Guidance** [🔗](https://arxiv.org/pdf/2207.12598)  
  *Employs a modified classifier-free guidance strategy in two ways: by introducing model-based classifier-free guidance and by planting a content “seed” early during denoising. Coupled with a patch-based fine-tuning strategy on latent diffusion models (LDMs), this approach enables generation at arbitrary resolutions while leveraging large pre-trained models.*

- **Null Embedding Optimization for High-Fidelity Reconstructions** [🔗](https://null-text-inversion.github.io/)    
  *Observes that DDIM inversion provides a good starting point but struggles with classifier-free guidance. By optimizing the unconditional null embedding used in classifier-free guidance, this method achieves high-fidelity reconstructions without additional tuning of the model or conditional embeddings, thereby preserving editing capabilities.*

- **Unified Diffusion Model Editing Algorithm** [🔗](https://unified.baulab.info/)    
  *Follows a three-stage approach: (i) optimizing text embeddings to match a given image, (ii) fine-tuning diffusion models for improved image alignment, and (iii) linearly interpolating between optimized and target text embeddings. This unified algorithm enables precise editing of diffusion models, aiming to make them more responsible and beneficial.*

- **Debiasing Text-to-Image Diffusion Models** [🔗](https://arxiv.org/html/2402.14577v1)   
  *Enables targeted debiasing, removal of potentially copyrighted content, and moderation of offensive concepts using only text descriptions. This editing methodology can be applied to any linear projection layer by replacing pre-trained weights while preserving key concepts.*

#### 👽 Multimodal Conversations & Visual Understanding

- **AlignGPT** [🔗](https://arxiv.org/abs/2405.14129)  
  *Comprises a multimodal large language model (MLLM) for enhanced multimodal perception. An accompanying AlignerNet bridges the MLLM to the diffusion U-Net image decoder, enabling coherent integration of textual and visual information.*

- **KOSMOS-G** [🔗](https://arxiv.org/abs/2310.02992)  
  *Offers seamless concept-level guidance from interleaved input to the image decoder. Serving as an alternative to CLIP, it facilitates effective image generation by guiding the diffusion process with interleaved multimodal cues.*

- **MM-REACT** [🔗](https://arxiv.org/abs/2303.11381)    
  *Presents a unified approach that synergizes multimodal reasoning and action to tackle complex visual understanding tasks. Extensive zero-shot experiments demonstrate its capabilities in multi-image reasoning, multi-hop document understanding, and open-world concept comprehension.*

---

## 👤 Avatar
Reviews approaches for both 2D and 3D avatar creation, emphasizing lifelike digital representations with detailed facial expressions and body dynamics.

### 🗂 Datasets

| 🏷️ Name       | 📊 Statistics                                                                                                                                                       | 🔍 Modalities                                          | 🔗 Link                                                              |
| ------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------ | -------------------------------------------------------------------- |
| WildAvatar    | Over 10,000 human subjects; extracted from YouTube; significantly richer than previous datasets for 3D human avatar creation                                            | 🎥 Video, 🔷 3D/Point Cloud Data, 🔊 Audio              | [WildAvatar](https://wildavatar.github.io/)                          |
| ZJU-MoCap     | Multi-camera system with 20+ synchronized cameras; includes SMPL-X parameters for detailed motion capture of body, hand, and face; complex actions such as twirling, Taichi, and punching | 🎥 Video, 🔷 3D/Point Cloud Data                        | [ZJU-MoCap](https://chingswy.github.io/Dataset-Demo/)                 |
| TalkSHOW      | 26.9 hours of in-the-wild talking videos from 4 speakers; expressive 3D whole-body meshes reconstructed at 30 fps, synchronized with audio at 22 kHz                      | 🔊 Audio, 🔷 3D/Point Cloud Data                        | [TalkSHOW](https://talkshow.is.tue.mpg.de/)                           |
| HuMMan        | 1,000 human subjects, 400k sequences, 60M frames; include point clouds, SMPL parameters, and textured meshes for multimodal sensing                                   | 🎥 Video, 🔷 3D/Point Cloud Data                        | [HuMMan](https://caizhongang.com/projects/HuMMan/)                     |
| BUFF          | 6 subjects performing motions in two clothing styles; 13,632 3D scans with high-resolution ground-truth minimally-clothed shapes                                        | 🔷 3D/Point Cloud Data                                 | [BUFF](https://buff.is.tue.mpg.de/)                                    |
| AMASS         | Combines 15 motion capture datasets into a unified framework with over 42 hours of motion data; 346 subjects and 11,451 motions with SMPL pose parameters, 3D shape parameters, and soft-tissue coefficients | 🔷 3D/Point Cloud Data                                 | [AMASS](https://amass.is.tue.mpg.de/)                                  |
| 3DPW          | 60 video sequences with accurate 3D poses using video and IMU data; 18 re-poseable 3D body models with different clothing variations                                  | 🎥 Video, ⏱️ Time-Series Data, 🔷 3D/Point Cloud Data     | [3DPW](https://virtualhumans.mpi-inf.mpg.de/3DPW/)                     |
| AIST++        | 10,108,015 frames of 3D key points with corresponding images; 1,408 dance motion sequences spanning 10 dance genres with synchronized music                             | 🎥 Video, 🔊 Audio, 🔷 3D/Point Cloud Data               | [AIST++](https://google.github.io/aistplusplus_dataset/)              |
| RenderMe-360  | Over 243 million head frames from 500 identities; includes FLAME parameters, UV maps, action units, textured meshes, and diverse annotations                             | 🎥 Video, 🔷 3D/Point Cloud Data                        | [RenderMe-360](https://renderme-360.github.io/)                        |
| PuzzleIOI     | 41 subjects with nearly 1,000 Outfit-of-the-Day (OOTD) configurations; includes paired ground-truth 3D body scans for challenging partial photos                           | 🖼️ Images, 🔷 3D/Point Cloud Data, 📝 Text              | [PuzzleIOI](https://puzzleavatar.is.tue.mpg.de/)                       |


---

### 🤖 Models


#### 🔍 CLIP-Guided Models

- **AvatarCLIP** [🔗](https://hongfz16.github.io/projects/AvatarCLIP.html)   
  *A zero-shot framework for generating and animating 3D avatars from natural language descriptions. It uses a shape VAE for initial geometry generation guided by CLIP and integrates NeuS for high-quality geometry and photorealistic rendering. In the motion phase, candidate poses are selected via CLIP and a motion VAE synthesizes smooth motions.*

- **DreamField** [🔗](https://ajayj.com/dreamfields)  
  *Adapts NeRF for text-driven 3D object generation. While it facilitates text-to-3D synthesis, it struggles with capturing detailed geometry.*

- **Text2Mesh** [🔗](https://threedle.github.io/text2mesh/)    
  *Stylizes existing meshes using CLIP guidance. It aims for text-driven mesh modifications but faces challenges with stability and flexibility when handling diverse text descriptions.*


#### 🧩 Implicit Function-Based Models

- **PIFu (Pixel-Aligned Implicit Function)** [🔗](https://shunsukesaito.github.io/PIFu/)  
  *Reconstructs detailed 3D surfaces from single-view 2D images by projecting 3D points into 2D space to extract pixel-aligned features via CNNs, which are then processed by an MLP for high-resolution surface reconstructions.*

- **PIFuHD** [🔗](https://shunsukesaito.github.io/PIFuHD/)   
  *Enhances PIFu by incorporating multi-scale feature extraction, leading to improved global shape understanding and finer surface details.*

- **ARCH (Animatable Reconstruction of Clothed Humans)** [🔗](https://arxiv.org/abs/2004.04572)  
  *Reconstructs detailed 3D models of clothed individuals from single RGB images. It transforms poses into a canonical space using a parametric body model and employs an implicit surface representation to capture fine details such as clothing folds.*

- **ARCH++** [🔗](https://arxiv.org/abs/2108.07845)    
  *An enhanced version of ARCH that refines geometry encoding and boosts clothing details to produce photorealistic, animatable avatars.*

- **PaMIR (Parametric Model-Conditioned Implicit Representation)** [🔗](https://arxiv.org/abs/2007.03858)    
  *Combines a parametric SMPL body model with an implicit surface representation to reconstruct 3D humans from single RGB images. It uses a depth-ambiguity-aware loss and refines SMPL parameters during inference for better alignment.*

- **TADA (Text to Animatable Dynamic Avatar)** [🔗](https://tada.is.tue.mpg.de/)   
  *Generates high-fidelity, animatable 3D avatars directly from text prompts. It leverages an upsampled SMPL-X model and learnable displacements, optimizing geometry and texture via Score Distillation Sampling losses, with additional detail enhancement through partial mesh subdivision.*

- **GETAvatar (Generative Textured Meshes for Animatable Human Avatars)** [🔗](https://openaccess.thecvf.com/content/ICCV2023/papers/Zhang_GETAvatar_Generative_Textured_Meshes_for_Animatable_Human_Avatars_ICCV_2023_paper.pdf)    
  *Directly produces high-fidelity, explicitly textured 3D meshes. It represents human bodies using an articulated 3D mesh and generates a signed distance field (SDF) in canonical space, which is deformed to match the target shape and pose via SMPL-based transformations. A normal field trained on 3D scans enhances fine geometric details.*

- **RodinHD** [🔗](https://rodinhd.github.io/)    
  *Creates 3D avatars from a single portrait image by constructing a detailed 3D blueprint (triplane) that captures the avatar’s shape, textures, and fine details. A shared neural decoder then converts this blueprint into an image, with a cascaded diffusion model generating new triplanes based on the portrait.*

#### 🎥 NeRF-Based Methods

- **HumanNeRF** [🔗](https://grail.cs.washington.edu/projects/humannerf/)  
  *Pioneers the use of deformation fields for dynamic human models from monocular images, enabling the mapping of points from observation to canonical space.*

- **Neural Body** [🔗](https://zju3dv.github.io/neuralbody/)   
  *Introduces structured latent codes anchored to SMPL model vertices, processed via SparseConvNet, to regularize dynamic human modeling.*

- **Neural Human Performer** [🔗](https://youngjoongunc.github.io/nhp/)    
  *Captures dynamic human information directly in the observation space using a skeletal feature bank and transformer modules.*

- **Vid2Avatar** [🔗](https://moygcc.github.io/vid2avatar/)   
  *Jointly models human subjects and scene backgrounds using two separate neural radiance fields, enhancing realism in avatar generation.*

- **DreamHuman** [🔗](https://dream-human.github.io/)    
  *Generates animatable 3D human avatars from textual descriptions by combining NeRF with the imGHUM body model. It uses human body shape statistics for anatomical correctness and incorporates semantic zooming for detailed regions such as faces and hands.*


#### 🌈 Diffusion-Based Methods

- **Personalized Avatar Scene (PAS)** [🔗]  
  *Generates customized 3D avatars in various poses and scenes based on text descriptions. It employs a diffusion-based transformer to generate 3D body poses conditioned on text.*

- **3D Head Avatar via 3DMM & Diffusion** [🔗](https://arxiv.org/abs/2307.04859)    
  *Combines a parametric 3D Morphable Model of the head (using FLAME [153]) with diffusion models to jointly optimize geometry and texture for generating 3D head avatars from text prompts.*

- **Make-Your-Anchor** [🔗](https://arxiv.org/abs/2403.16510)    
  *Introduces a novel approach for generating 2D anchor-style avatars capable of realistic full-body motion and expression. It utilizes a Structure-Guided Diffusion Model (SGDM) to ensure coherent and expressive avatar generation.*


#### 🔀 Hybrid Methods

- **DreamAvatar** [🔗](https://yukangcao.github.io/DreamAvatar/)   
  *Integrates shape priors, diffusion models, and NeRF architecture within a dual-observation-space (DOS) framework. Leveraging SMPL for anatomical guidance and employing joint optimization with specialized head-focused VSD loss (using ControlNet [310]), it ensures structurally consistent avatars with controllable shape modifications. While it outperforms methods like DreamWaltz [111] in geometric accuracy, it currently lacks animation capabilities and may inherit biases from pretrained diffusion models.*

- **DreamWaltz** [🔗](https://idea-research.github.io/DreamWaltz/)   
  *Referenced as a comparative baseline, this model illustrates limitations in animation capabilities and inherited biases when compared to hybrid approaches like DreamAvatar.*

---

## 🤝 Gesture
Examines methods for generating human-like gestures and co-speech movements, critical for interactive and immersive animations.

### 🗂 Datasets

| 🏷️ Name                   | 📊 Statistics                                                                                                                                                                                                                                                                                             | 🔍 Modalities                                      | 🔗 Link                                                                                                                                                          |
| ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| IEMOCAP                   | 151 recorded dialogue videos, with 2 speakers per session, totaling 302 videos. Annotated for 9 emotions and valence, arousal, and dominance. Contains approximately 12 hours of audiovisual data.                                                                                                    | 🎥 Video, 🔊 Audio, 📝 Text, 📋 Tabular Data          | [IEMOCAP](https://sail.usc.edu/iemocap/)                                                                                                                         |
| SaGA                      | 25 dialogues between interlocutors (50 total). Language: German. Published speakers: 6, unpublished speakers: 19. Annotated gestures: 1,764 (total corpus). Total video duration: 1 hour.                                                                                                              | 🎥 Video, 🔊 Audio, 📋 Tabular Data                  | [SaGA](https://www.phonetik.uni-muenchen.de/Bas/BasSaGAeng.html)                                                                                                 |
| Creative-IT               | Data from 16 actors (male and female). Affective dyadic interactions range from 2 to 10 minutes each. Approximately 8 sessions of audiovisual data were released.                                                                                                                                    | 🎥 Video, 🔊 Audio, 📝 Text, 📋 Tabular Data          | [CreativeIT](https://sail.usc.edu/CreativeIT/ImprovRelease.html)                                                                                                 |
| CMU Panoptic              | 3D facial landmarks from 65 sequences (5.5 hours). Contains 1.5 million 3D skeletons.                                                                                                                                                                                                                   | 🎥 Video, 🔊 Audio, 📝 Text                          | [CMU Panoptic](http://domedb.perception.cs.cmu.edu/)                                                                                                             |
| Speech-Gesture            | A 144-hour dataset featuring 10 speakers. Includes frame-by-frame, automatically detected pose annotations.                                                                                                                                                                                             | 🎥 Video, 🔊 Audio                                  | [Speech-Gesture](https://people.eecs.berkeley.edu/~shiry/projects/speech2gesture/)                                                                                |
| Talking With Hands 16.2M  | 16.2 million frames (50 hours) of two-person, face-to-face spontaneous conversations. Strong covariance in arm and hand features.                                                                                                                                                                          | 🎥 Video, 🔊 Audio                                  | [Talking With Hands](https://github.com/facebookresearch/TalkingWithHands32M)                                                                                    |
| PATS                      | 25 speakers, 251 hours of data, approximately 84,000 intervals. Mean interval length: 10.7 seconds.                                                                                                                                                                                                     | 🎥 Video, 🔊 Audio, 📝 Text                          | [PATS](http://chahuja.com/pats/)                                                                                                                                 |
| Trinity Speech-Gesture II | 244 minutes of motion capture and audio (23 takes). Includes one male native English speaker. The skeleton consists of 69 joints.                                                                                                                                                                         | 🎥 Video, 🔊 Audio, 📋 Tabular Data                  | [Trinity](https://trinityspeechgesture.scss.tcd.ie/)                                                                                                             |
| SaGA++                    | 25 recordings, totaling 4 hours of data.                                                                                                                                                                                                                                                                  | 🎥 Video, 🔊 Audio, 📝 Text, 📋 Tabular Data          | [SaGA++](https://svito-zar.github.io/speech2properties2gestures/)                                                                                                 |
| ZEGGS                     | 67 monologue sequences with 19 different motion styles. Performed by a female actor speaking in English. Total duration: 134.65 minutes.                                                                                                                                                                | 🎥 Video, 🔊 Audio                                  | [ZEGGS](https://github.com/ubisoft/ubisoft-laforge-ZeroEGGS)                                                                                                     |
| BEAT                      | 76 hours of 3D motion capture data from 30 speakers. Covers 8 emotions and 4 languages. Includes 32 million frame-level emotion and semantic relevance annotations.                                                                    | 🎥 Video, 🔊 Audio, 📝 Text, 📋 Tabular Data          | [BEAT](https://pantomatrix.github.io/BEAT/)                                                                                                                      |
| BEAT2                     | 60 hours of mesh-level, motion-captured co-speech gesture data. Integrates SMPL-X body and FLAME head parameters. Enhances modeling of head, neck, and finger movements.                                                                | 🎥 Video, 🔊 Audio, 📋 Tabular Data                  | [BEAT2](https://pantomatrix.github.io/EMAGE/)                                                                                                                    |
| GAMT                      | 176 video clips of volunteers using math terms and gestures. Covers 8 classes of mathematical terms and gestures.                                                                                                                       | 🎥 Video, 🔊 Audio, 📝 Text                          | [GAMT](https://openaccess.thecvf.com/content/CVPR2024W/MAR/html/Maidment_Using_Language-Aligned_Gesture_Embeddings_for_Understanding_Gestures_Accompanying_Math_Terms_CVPRW_2024_paper.html) |
| SeG                       | 208 types of global semantic gestures. 544 motion files recorded from a male performer. Each gesture is represented in 2.6 variations on average.                                                                                      | 🎥 Video, 🔊 Audio, 📋 Tabular Data                  | [SeG](https://pku-mocca.github.io/Semantic-Gesticulator-Page/)                                                                                                   |
| DND Group Gesture         | 6 hours of gesture data from 5 individuals playing Dungeons & Dragons. Recorded over 4 sessions (total duration: 6 hours). Includes beat, iconic, deictic, and metaphoric gestures.                                               | 🎥 Video, 🔊 Audio, 📋 Tabular Data                  | [DND](https://github.com/m-hamza-mughal/convofusion)                                                                                                             |



---

### 🤖 Models


#### 🛠 Traditional & Parametric Approaches

- **Parameter-Based Procedural Animation** [🔗](https://www4.nccu.edu.tw/~tyli/pdf/iva2009.pdf)   
  *Uses high-level control parameters (e.g., emotion, speech intensity, rhythm) to select and interpolate predefined keyframes, yielding smooth and coherent gesture sequences.*

- **Blendshape Models** [🔗](https://graphics.cs.uh.edu/wp-content/papers/2014/2014-EG-blendshape_STAR.pdf)  
  *Generates detailed hand and finger gestures by blending a set of predefined base shapes using weighted interpolation, enabling fine-grained control and smooth transitions.*


#### 🧠 Deep Learning-Based Models

- **GestureGAN** [🔗](https://arxiv.org/abs/1808.04859)   
  *Employs a GAN-based generator-discriminator framework to synthesize realistic gesture sequences conditioned on audio inputs, capturing dynamic hand gestures effectively.*

- **Speech2Gesture** [🔗](https://shiry.ttic.edu/projects/speech2gesture/)  
  *Generates co-speech gestures directly from speech features using LSTM/RNN architectures, effectively modeling temporal dependencies between speech and gesture.*

- **StyleGestures** [🔗](https://diglib.eg.org/items/04569b85-1067-4ad0-9b32-46646ecdba66)  
  *Utilizes an encoder-decoder architecture with style tokens and Transformers to capture individual speaker styles, enabling personalized gesture synthesis.*

- **Audio-Driven Adversarial Gesture Generation** [🔗](https://arxiv.org/abs/2303.09119)  
  *Combines GANs with Conditional Variational Autoencoders (CVAE) to align audio and motion features in a shared latent space, resulting in nuanced, audio-driven gestures.*

- **GestureDiffuCLIP** [🔗](https://pku-mocca.github.io/GestureDiffuCLIP-Page/)   
  *Leverages a diffusion process guided by CLIP for semantic alignment to iteratively refine gesture sequences, producing highly expressive gestures.*

- **ZeroEGGS** [🔗](https://arxiv.org/abs/2209.07556)    
  *Implements a zero-shot paradigm for generating gestures based solely on speech, using example-based learning to generalize across unseen gestural styles.*

- **GestureMaster** [🔗](https://dl.acm.org/doi/10.1145/3536221.3558063)    
  *Utilizes a graph neural network (GNN) framework to model spatial and temporal dependencies in gesture sequences, enhancing naturalistic hand and body gesture synthesis.*

- **ExpressGesture** [🔗](https://onlinelibrary.wiley.com/doi/10.1002/cav.2016)   
  *Integrates emotion recognition with gesture generation pipelines, creating gestures that reflect both the content of speech and underlying sentiment.*

- **MocapNET** [🔗](https://github.com/FORTH-ModelBasedTracker/MocapNET)   
  *Bridges traditional motion capture with neural synthesis by combining 2D pose estimation and 3D gesture reconstruction using multimodal motion capture datasets.*

- **CSMP** [🔗](https://camp-nerf.github.io/)    
  *A diffusion-based co-speech gesture generation model that leverages joint text and audio representations to capture intricate inter-modal relationships.*

- **ZS-MSTM** [🔗](https://arxiv.org/abs/2305.12887)    
  *Introduces a zero-shot style transfer method for gesture animation through adversarial disentanglement, separating style and content features for effective style transfer across speakers.*


#### 🚀 Transformer-Based Models

- **Gesticulator** [🔗](https://svito-zar.github.io/gesticulator/)    
  *Employs a multimodal Transformer architecture to generate contextually relevant gestures conditioned on both text and audio inputs, aligning with co-speech dynamics.*

- **Mix-StAGE** [🔗](https://chahuja.com/mix-stage/)    
  *Uses an attention-based encoder-decoder with a style encoder and mixed spatial-temporal attention mechanisms to capture dynamic, expressive gestures.*

- **SAGA (Style and Grammar-Aware Gesture Generation)** [🔗](https://arxiv.org/abs/2307.09597)    
  *Combines an LSTM-based encoder-decoder with a Transformer-based grammar encoder to align gestures accurately with linguistic content, integrating both style and grammatical cues.*

- **Cross-Modal Transformer** [🔗](https://arxiv.org/abs/2301.01283)    
  *Leverages cross-attention mechanisms to fuse diverse modalities (text, audio, video), enhancing the coherence and contextual alignment of generated gestures.*

- **DiM-Gesture** [🔗](https://arxiv.org/abs/2408.00370)    
  *Introduces an adaptive layer normalization mechanism (Mamba-2) to adjust to different speakers, focusing on generating realistic co-speech gestures from audio.*

- **AMUSE** [🔗](https://amuse.is.tue.mpg.de/)    
  *Utilizes a disentangled latent diffusion technique to separate emotional expressions from gestures, enabling control over emotional aspects via a multi-stage training pipeline.*

- **FreeTalker** [🔗](https://youngseng.github.io/FreeTalker/)    
  *Employs a diffusion-based framework with classifier-free guidance and a generative prior (DoubleTake) to produce natural transitions between gesture clips, extending beyond co-speech gestures.*

- **CoCoGesture** [🔗](https://mattie-e.github.io/GES-X/)    
  *Addresses long-sequence gesture generation with a Transformer-based diffusion model that uses a large dataset (GES-X) and a mixture-of-experts framework to effectively align gestures with human speech.*

- **DiffuseStyleGestures** [🔗](https://arxiv.org/abs/2305.04919)    
  *Integrates audio, text, speaker IDs, and seed gestures within a diffusion-based approach to produce stylistically diverse co-speech gesture outputs.*

- **DiffuseStyleGesture+** [🔗](https://arxiv.org/abs/2308.13879)    
  *Builds upon DiffuseStyleGestures by further refining gesture synthesis through advanced multimodal integration and specialized attention mechanisms for personalized outputs.*

- **ViTPose** [🔗](https://arxiv.org/abs/2204.12484)   
  *Applies Vision Transformers to human pose estimation, providing a robust foundation for gesture synthesis by accurately capturing pose dynamics.*

- **Gesture Motion Graphs** [🔗](https://dl.acm.org/doi/10.1145/3577190.3616118)   
  *Utilizes graph-based modeling for few-shot gesture reenactment, effectively representing motion sequences and their dependencies.*

- **DiffSHEG** [🔗](https://jeremycjm.github.io/proj/DiffSHEG/)   
  *Adopts a diffusion-based approach for real-time speech-driven 3D expression and gesture generation, leveraging joint text and audio representations for coherent outputs.*

- **C2G2** [🔗](https://arxiv.org/abs/2308.15016)    
  *Emphasizes controllability in co-speech gesture generation by using modular components to handle different aspects of gesture synthesis.*

- **DiffuGesture** [🔗](https://dl.acm.org/doi/10.1145/3610661.3616552)    
  *Focuses on generating gestures for two-person dialogues with specialized diffusion techniques tailored for interactive and conversational settings.*

---

## 🎥 Motion
Highlights text-constrained motion generation techniques, including MotionGPT and diffusion frameworks, for creating smooth and realistic animation sequences.

### 🗂 Datasets


| 🏷️ Name                   | 📊 Statistics                                                                                                                                                                                                                                                  | 🔍 Modalities                                        | 🔗 Link                                                                                           |
| ------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| Motion-X++                | 19.5 million 3D poses across 120,500 sequences, synchronized with 80,800 RGB videos and 45,300 audio tracks. Annotated with free-form text descriptions.                                                                                                  | 🔷 3D/Point Cloud Data, 📝 Text, 🔊 Audio, 🎥 Video     | [Motion-X++](https://github.com/IDEA-Research/Motion-X)                                           |
| HumanMM (ms-Motion)       | 120 long-sequence 3D motions reconstructed from 500 in-the-wild multi-shot videos, totaling 60 hours of data. Includes rare interactions.                                                                                                                  | 🔷 3D/Point Cloud Data, 🎥 Video                      | [HumanMM](https://github.com/zhangyuhong01/HumanMM-code)                                          |
| Multimodal Anatomical Motion | 51,051 annotated poses with 53 anatomical landmarks, captured across 48 virtual camera views per pose. Includes 2,000+ pathological motion variations.                                                                                                    | 🔷 3D/Point Cloud Data, 📝 Text                        | -                                                                                                 |
| AMASS                     | 11,265 motion clips aggregated from 15 mocap datasets (e.g., CMU, KIT), totaling 43 hours of motion data in SMPL format. Covers 100+ action categories.                                                                                                   | 🔷 3D/Point Cloud Data                               | [AMASS](https://amass.is.tue.mpg.de/)                                                             |
| HumanML3D                 | 14,616 motion sequences (28.6 hours) paired with 44,970 free-form text descriptions spanning 200+ action categories.                                                                                                                                        | 🔷 3D/Point Cloud Data, 📝 Text                        | [HumanML3D](https://github.com/EricGuo5513/HumanML3D)                                             |
| BABEL                     | 43 hours of motion data from AMASS, annotated with 250+ verb-centric action classes across 13,220 sequences. Includes temporal action boundaries.                                                                                                         | 🔷 3D/Point Cloud Data, 📝 Text                        | [BABEL](https://babel.is.tue.mpg.de/)                                                             |
| AIST++                    | 1,408 dance sequences (10.1 million frames) captured from 9 camera views, totaling 15 hours of multi-view RGB video data.                                                                                                                                      | 🔷 3D/Point Cloud Data, 🎥 Video                      | [AIST++](https://google.github.io/aistplusplus_dataset/)                                          |
| 3DPW                      | 60 sequences (51,000 frames) captured in diverse indoor/outdoor environments, featuring challenging poses and natural object interactions.                                                                                                                  | 🔷 3D/Point Cloud Data, 🎥 Video                      | [3DPW](https://virtualhumans.mpi-inf.mpg.de/3DPW/)                                               |
| PROX                      | 20 subjects performing 12 interactive scenarios in 3D scenes, including 180 annotated RGB frames for scene-aware motion analysis.                                                                                                                             | 🔷 3D/Point Cloud Data, 🖼️ Images                     | [PROX](https://prox.is.tue.mpg.de/index.html)                                                     |
| KIT-ML                    | 3,911 motion clips (11.23 hours) with 6,278 natural language annotations containing 52,903 words, stored in BVH/FBX formats.                                                                                                                                  | 🔷 3D/Point Cloud Data, 📝 Text                        | [KIT-ML](https://git.h2t.iar.kit.edu/sw/motion-annotation)                                        |



---

### 🤖 Models


#### 🔤 Language-to-Pose Models

- **Language2Pose** [🔗](https://chahuja.com/language2pose/)    
  *Generates 3D human poses directly from natural language. It employs two encoders (for text and 3D motion) that map inputs into a joint embedding space, and a decoder that produces a fixed-length motion sequence by minimizing the distance between corresponding text and motion embeddings.*

- **MotionClip** [🔗](https://guytevet.github.io/motionclip-page/)   
  *An end-to-end pipeline for motion generation based on an encoder-decoder transformer. The model extracts a high-level motion representation and uses multiple loss functions—comparing joint orientations, velocities, and image-text groundings via CLIP—to enhance motion quality.*


#### 📦 Variational Auto-Encoder (VAE) Based Models

- **ACTOR** [🔗](https://arxiv.org/abs/2104.05670)   
  *Generates diverse and realistic 3D human motions conditioned on action labels. This approach uses a transformer-based VAE to encode actions and poses into a Gaussian latent space, allowing sampling of varied motions for the same action prompt.*

- **TEMOS (Text-To-Motions)** [🔗](https://arxiv.org/abs/2204.14109)   
  *A text-conditioned generative model that uses a transformer-based VAE architecture with two symmetric encoders (for motion and text). It learns a diverse latent space by aligning text and pose embeddings to generate meaningful SMPL body motions.*

- **Teach** [🔗](https://arxiv.org/abs/2209.04066)    
  *Transforms sequences of text descriptions into SMPL body motions. The model operates non-autoregressively within individual actions and autoregressively across action sequences by leveraging a past-conditioned text encoder that combines historical motion features with current text input.*

- **Generating Diverse and Natural 3D Human Motions from Text** [🔗](https://ericguo5513.github.io/text-to-motion/)    
  *Generates 3D human motions from textual descriptions by first pre-training an auto-encoder (using convolutional and deconvolutional layers) and then utilizing a temporal VAE with three recurrent networks (prior, posterior, and generator) to produce motion snippets.*

- **TMR** [🔗](https://mathis.petrovich.fr/tmr/)    
  *Enhances transformer-based text-to-motion generation by mapping motion and text embeddings into a joint space. Dual transformer encoders are used for each modality, and cosine similarity between embeddings is maximized for positive pairs while filtering out negatives via MPNet similarity.*


#### 🗝 VQ-VAE Based Models

- **T2M GPT** [🔗](https://mael-zys.github.io/T2M-GPT/)    
  *The first model to apply VQ-VAE for motion generation. It learns a discrete representation (codebook) of motion and formulates motion generation as an autoregressive token prediction task, conditioned on text encoded by CLIP.*

- **DiverseMotion** [🔗](https://arxiv.org/abs/2309.01372)    
  *Builds upon T2M GPT by discarding the autoregressive generation in favor of a diffusion process to diversify motion outputs. It employs CLIP for text encoding and Hierarchy Semantic Aggregation (HSA) to generate a richer holistic text embedding.*

- **MoMask** [🔗](https://ericguo5513.github.io/momask/)    
  *Uses a hierarchical VQ-VAE to quantize motion sequences into discrete tokens over multiple layers. A masked transformer predicts missing tokens (similar to BERT), and a residual transformer refines these predictions to incorporate fine motion details.*

- **T2LM Long-Term 3D Human Motion** [🔗](https://arxiv.org/abs/2406.00636)    
  *Transforms sequences of text descriptions into 3D motion sequences using a 1D-convolutional VQ-VAE and a transformer-based text encoder. This method generates smooth transitions between actions, outperforming earlier techniques like TEACH.*

- **MotionGPT** [🔗](https://motion-gpt.github.io/)    
  *Generates human motion from text by leveraging a pre-trained motion VQ-VAE alongside a large language model (LLM). The LLM is fine-tuned with LoRA to generate motion tokens that the VQ-VAE decoder transforms into motion sequences, significantly speeding up training.*


#### 🌈 Diffusion-Based Models

- **Flame** [🔗](https://kakaobrain.github.io/flame/)    
  *Employs a transformer-based motion decoder within a diffusion framework. It conditions on text using cross-attention (with text embeddings from RoBERTA) and incorporates special tokens for motion length and diffusion time steps. The model is optimized with a hybrid loss combining diffusion noise loss and a variational lower bound loss, with classifier-free guidance during inference.*

- **MotionDiffuse** [🔗](https://mingyuan-zhang.github.io/projects/MotionDiffuse.html)    
  *Similar to Flame but with slight architectural variations: it selects a random diffusion time step and divides the motion sequence into sub-intervals for time-varying conditioning. It utilizes efficient attention modules and optimizes using mean squared error on the noise prediction.*

- **HMDM** [🔗](https://www.researchgate.net/publication/389662135_IT-HMDM_Invertible_Transformer_for_Human_Motion_Diffusion_Model)    
  *A diffusion-based model with a fixed motion sequence length that leverages CLIP’s text encoder. It introduces additional loss functions (e.g., position, foot, and velocity losses) defined on the reconstructed motion signal, rather than just the noise, to improve temporal consistency and motion fidelity.*

- **Make-An-Animation** [🔗](https://azadis.github.io/make-an-animation/)    
  *Proposes a two-stage diffusion framework for text-to-3D motion generation. The model pre-trains on a large-scale static pose dataset using a UNet backbone and T5 text encoder, then fine-tunes on motion datasets, generating the entire motion sequence concurrently for improved smoothness.*

- **GMD (Guided Motion Diffusion)** [🔗](https://korrawe.github.io/gmd-project/)    
  *Focuses on incorporating spatial (trajectory) constraints into the diffusion process. The method uses a two-stage pipeline that first emphasizes ground location guidance and then propagates sparse guidance gradients across neighboring frames to enhance overall motion consistency.*

- **OmniControl** [🔗](https://neu-vi.github.io/omnicontrol/)    
  *Extends spatial guidance by cumulatively summing relative pelvis locations to infer global positions. It also introduces realism guidance, propagating control signals from keyframes and the pelvis to other joints for coherent, natural motion generation.*

---

## 📦 Object
Discusses approaches for text-to-3D object generation, such as Neural Radiance Fields (NeRFs) and 3D Gaussian Splatting, to create realistic assets.

### 🗂 Datasets


| 🏷️ Name        | 📊 Statistics                                                                          | 🔍 Modalities                                      | 🔗 Link                                                                                 |
| -------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------- | --------------------------------------------------------------------------------------- |
| ShapeNet       | 3D models in categories like furniture and vehicles.                                 | 🔷 3D/Point Cloud Data, 📝 Text                      | [ShapeNet](http://shapenet.org/about)                                                    |
| BuildingNet    | Architectural structures for shape completion tasks.                                  | 🔷 3D/Point Cloud Data, 📝 Text                      | [BuildingNet](https://github.com/BuildingNet/BuildingNet)                                |
| Text2Shape     | Textual descriptions linked to ShapeNet categories.                                  | 📝 Text, 🔷 3D/Point Cloud Data                      | [Text2Shape](https://text2shape.github.io/)                                                |
| ShapeGlot      | Textual utterances describing differences between shapes.                            | 📝 Text, 🔷 3D/Point Cloud Data                      | [ShapeGlot](https://github.com/alters-mit/ShapeGlot)                                       |
| Pix3D          | 3D models aligned with real-world images for evaluation.                             | 🖼️ Images, 🔷 3D/Point Cloud Data                    | [Pix3D](https://github.com/xingyuansun/pix3d)                                              |
| LAION-5B       | Large-scale dataset with 5 billion image-text pairs.                                 | 🖼️ Images, 📝 Text                                  | [LAION-5B](https://laion.ai/)                                                              |
| COCO-Stuff     | Annotated images for real-world 3D synthesis.                                          | 🖼️ Images, 📝 Text                                  | [COCO-Stuff](https://github.com/nightrome/cocostuff)                                       |
| Flickr30K      | Image dataset with diverse textual descriptions.                                     | 🖼️ Images, 📝 Text                                  | [Flickr30K](https://github.com/ubmdmg/Flickr30kEntities)                                   |
| ModelNet40     | 3D CAD models across 40 object categories.                                             | 🔷 3D/Point Cloud Data                             | [ModelNet40](https://modelnet.cs.princeton.edu/)                                           |
| ShapeNetCore   | Subset of ShapeNet with detailed object models.                                      | 🔷 3D/Point Cloud Data, 📝 Text                      | [ShapeNetCore](http://shapenet.org/about)                                                  |
| BlendSwap      | Realistic 3D models with physically based rendering (PBR).                           | 🔷 3D/Point Cloud Data, 🖼️ Images                   | [BlendSwap](https://www.blendswap.com/)                                                    |
| InstructPix2Pix| Dataset for instruction-driven image modifications.                                  | 🖼️ Images, 📝 Text                                  | [InstructPix2Pix](https://github.com/timothybrooks/instruct-pix2pix)                         |
| MagicBrush     | Dataset for refining texture and appearance in 3D.                                     | 🖼️ Images                                          | [MagicBrush](https://github.com/OSU-NLP-Group/MagicBrush)                                  |
| NeRF-Synthetic | 2D images rendered from synthetic 3D scenes.                                           | 🖼️ Images                                          | [NeRF-Synthetic](https://github.com/bmild/nerf)                                             |
| ScanNet        | 2.5M RGB-D views with semantic segmentations and camera poses.                         | 🖼️ Images, 📝 Text                                  | [ScanNet](http://www.scan-net.org/)                                                        |
| Matterport3D   | 10,800 panoramic views from 90 building-scale scenes.                                  | 🖼️ Images, 🔷 3D/Point Cloud Data, 📝 Text            | [Matterport3D](https://github.com/niessner/Matterport)                                       |


---

### 🤖 Models

---

## 🧵 Texture
Focuses on methods for generating detailed surface textures that enhance the realism of 3D models, including text-guided synthesis and neural rendering techniques.

### 🗂 Datasets

---

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
