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

---

### 🤖 Models


#### 🔧 Fine-Tuning & Regularization

- **Spectral Shift Fine-Tuning** [🔗](https://arxiv.org/abs/2305.18670)   
  *Introduces a compact parameter space called “spectral shift” for diffusion model fine-tuning. It reduces overfitting and storage inefficiency while achieving comparable or superior results in both single- and multi-subject generation. The method also employs the Cut Mix-Unmix data augmentation technique for improved multi-subject quality and acts as a regularizer enabling applications like single-image editing.*

- **Control via Zero Convolutions (ControlNet)** [🔗](https://arxiv.org/abs/2302.05543)  
  *Addresses the limited spatial control of text-to-image models by locking large pre-trained diffusion models and reusing their deep encoding layers as a robust backbone. Connected via “zero convolutions” (zero-initialized convolution layers), this approach progressively grows parameters from zero to prevent harmful noise during fine-tuning, thereby facilitating diverse conditional controls.*


#### ✂ Image Editing & Disentanglement

- **Lightweight Disentanglement for Image Editing** [🔗](https://ieeexplore.ieee.org/document/10175586)  
  *Explores the inherent disentanglement properties of stable diffusion models. By partially replacing text embeddings from a style-neutral description with one that reflects the desired style, a lightweight algorithm (optimizing only 50 parameters) is introduced for improved style matching and content preservation—outperforming more complex fine-tuning baselines.*

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

| 🏷️ **Name** | 📊 **Statistics** | 🎭 **Modalities** | 🔗 **Link** |
|------------|------------------|------------------|------------|
| **IEMOCAP** | 151 dialogue videos (302 total), 9 annotated emotions, valence/arousal/dominance labels, ~12 hours of audiovisual data. | ✋ Gestures, 🎵 Audio, 📝 Text, 😃 Emotion | [IEMOCAP](https://sail.usc.edu/iemocap/) |
| **SaGA** | 25 dialogues (50 total), German language, 6 published speakers, 1,764 annotated gestures, 1-hour duration. | ✋ Gestures, 🎵 Audio, 🎭 Gesture Properties | [SaGA](https://www.phonetik.uni-muenchen.de/Bas/BasSaGAeng.html) |
| **Creative-IT** | 16 actors in dyadic affective interactions (2-10 min each), ~8 sessions released. | ✋ Gestures, 🎵 Audio, 📝 Text, 😃 Emotion | [Creative-IT](https://sail.usc.edu/CreativeIT/ImprovRelease.html) |
| **CMU Panoptic** | 3D facial landmarks from 65 sequences (5.5 hours), 1.5 million 3D skeletons. | ✋ Gestures, 🎵 Audio, 📝 Text | [CMU Panoptic](http://domedb.perception.cs.cmu.edu/) |
| **Speech-Gesture** | 144 hours of data with 10 speakers, automatic pose annotations. | ✋ Gestures, 🎵 Audio | [Speech-Gesture](https://people.eecs.berkeley.edu/~shiry/projects/speech2gesture/) |
| **Talking With Hands 16.2M** | 16.2 million frames (~50 hours) of face-to-face conversations, strong covariance in hand movements. | ✋ Gestures, 🎵 Audio | [Talking With Hands](https://github.com/facebookresearch/TalkingWithHands32M) |
| **PATS** | 25 speakers, 251 hours of data, ~84,000 gesture intervals (avg. 10.7s). | ✋ Gestures, 🎵 Audio, 📝 Text | [PATS](http://chahuja.com/pats/) |
| **Trinity Speech-Gesture II** | 244 minutes of motion capture and audio, 1 speaker, 69-joint skeleton model. | ✋ Gestures, 🎵 Audio, 🎭 Gesture Segmentation | [Trinity](https://trinityspeechgesture.scss.tcd.ie/) |
| **SaGA++** | 25 recordings, ~4 hours of data. | ✋ Gestures, 🎵 Audio, 📝 Text, 🎭 Gesture Properties | [SaGA++](https://svito-zar.github.io/speech2properties2gestures/) |
| **ZEGGS** | 67 monologue sequences in 19 motion styles, 1 female actor, ~134 minutes total. | ✋ Gestures, 🎵 Audio | [ZEGGS](https://github.com/ubisoft/ubisoft-laforge-ZeroEGGS) |
| **BEAT** | 76 hours of 3D motion capture, 30 speakers, 8 emotions, 4 languages, 32M frame annotations. | ✋ Gestures, 🎵 Audio, 📝 Text, 😃 Emotion, 🎭 Gesture Properties | [BEAT](https://pantomatrix.github.io/BEAT/) |
| **BEAT2** | 60 hours of mesh-level motion-captured gestures, SMPL-X & FLAME parameters for head/neck/fingers. | ✋ Gestures, 🎵 Audio, 🎭 Gesture Properties, 😃 Emotion | [BEAT2](https://pantomatrix.github.io/EMAGE/) |
| **GAMT (Gestures Accompanying Math Terms)** | 176 video clips of volunteers demonstrating 8 math gesture classes. | ✋ Gestures, 🎵 Audio, 📝 Text | [GAMT](https://openaccess.thecvf.com/content/CVPR2024W/MAR/html/Maidment_Using_Language-Aligned_Gesture_Embeddings_for_Understanding_Gestures_Accompanying_Math_Terms_CVPRW_2024_paper.html) |
| **SeG** | 208 semantic gesture types, 544 motion files, avg. 2.6 gesture variations per type. | ✋ Gestures, 🎭 Gesture Properties, 🎵 Audio | [SeG](https://pku-mocca.github.io/Semantic-Gesticulator-Page/) |
| **DND Group Gesture** | 6 hours of data from 5 players in a Dungeons & Dragons setting, includes beat/iconic/deictic/metaphoric gestures. | ✋ Gestures, 🎵 Audio, 🎭 Gesture Properties | [DND](https://github.com/m-hamza-mughal/convofusion) |


---

### 🤖 Models


### 🛠 Traditional & Parametric Approaches

- **Parameter-Based Procedural Animation** [🔗 [161]]  
  *Uses high-level control parameters (e.g., emotion, speech intensity, rhythm) to select and interpolate predefined keyframes, yielding smooth and coherent gesture sequences.*

- **Blendshape Models** [🔗 [148]]  
  *Generates detailed hand and finger gestures by blending a set of predefined base shapes using weighted interpolation, enabling fine-grained control and smooth transitions.*


### 🧠 Deep Learning-Based Models

- **GestureGAN** [🔗 [256]]  
  *Employs a GAN-based generator-discriminator framework to synthesize realistic gesture sequences conditioned on audio inputs, capturing dynamic hand gestures effectively.*

- **Speech2Gesture** [🔗 [78]]  
  *Generates co-speech gestures directly from speech features using LSTM/RNN architectures, effectively modeling temporal dependencies between speech and gesture.*

- **StyleGestures** [🔗 [7]]  
  *Utilizes an encoder-decoder architecture with style tokens and Transformers to capture individual speaker styles, enabling personalized gesture synthesis.*

- **Audio-Driven Adversarial Gesture Generation** [🔗 [326]]  
  *Combines GANs with Conditional Variational Autoencoders (CVAE) to align audio and motion features in a shared latent space, resulting in nuanced, audio-driven gestures.*

- **GestureDiffuCLIP** [🔗 [9]]  
  *Leverages a diffusion process guided by CLIP for semantic alignment to iteratively refine gesture sequences, producing highly expressive gestures.*

- **ZeroEGGS** [🔗 [76]]  
  *Implements a zero-shot paradigm for generating gestures based solely on speech, using example-based learning to generalize across unseen gestural styles.*

- **GestureMaster** [🔗 [323]]  
  *Utilizes a graph neural network (GNN) framework to model spatial and temporal dependencies in gesture sequences, enhancing naturalistic hand and body gesture synthesis.*

- **ExpressGesture** [🔗 [70]]  
  *Integrates emotion recognition with gesture generation pipelines, creating gestures that reflect both the content of speech and underlying sentiment.*

- **MocapNET** [🔗 [211]]  
  *Bridges traditional motion capture with neural synthesis by combining 2D pose estimation and 3D gesture reconstruction using multimodal motion capture datasets.*

- **CSMP** [🔗 [56]]  
  *A diffusion-based co-speech gesture generation model that leverages joint text and audio representations to capture intricate inter-modal relationships.*

- **ZS-MSTM** [🔗 [67]]  
  *Introduces a zero-shot style transfer method for gesture animation through adversarial disentanglement, separating style and content features for effective style transfer across speakers.*


### 🚀 Transformer-Based Models

- **Gesticulator** [🔗 [139]]  
  *Employs a multimodal Transformer architecture to generate contextually relevant gestures conditioned on both text and audio inputs, aligning with co-speech dynamics.*

- **Mix-StAGE** [🔗 [4]]  
  *Uses an attention-based encoder-decoder with a style encoder and mixed spatial-temporal attention mechanisms to capture dynamic, expressive gestures.*

- **SAGA (Style and Grammar-Aware Gesture Generation)** [🔗 [267]]  
  *Combines an LSTM-based encoder-decoder with a Transformer-based grammar encoder to align gestures accurately with linguistic content, integrating both style and grammatical cues.*

- **Cross-Modal Transformer** [🔗 [289]]  
  *Leverages cross-attention mechanisms to fuse diverse modalities (text, audio, video), enhancing the coherence and contextual alignment of generated gestures.*

- **DiM-Gesture** [🔗 [304]]  
  *Introduces an adaptive layer normalization mechanism (Mamba-2) to adjust to different speakers, focusing on generating realistic co-speech gestures from audio.*

- **AMUSE** [🔗 [46]]  
  *Utilizes a disentangled latent diffusion technique to separate emotional expressions from gestures, enabling control over emotional aspects via a multi-stage training pipeline.*

- **FreeTalker** [🔗 [291]]  
  *Employs a diffusion-based framework with classifier-free guidance and a generative prior (DoubleTake) to produce natural transitions between gesture clips, extending beyond co-speech gestures.*

- **CoCoGesture** [🔗 [212]]  
  *Addresses long-sequence gesture generation with a Transformer-based diffusion model that uses a large dataset (GES-X) and a mixture-of-experts framework to effectively align gestures with human speech.*

- **DiffuseStyleGestures** [🔗 [290]]  
  *Integrates audio, text, speaker IDs, and seed gestures within a diffusion-based approach to produce stylistically diverse co-speech gesture outputs.*

- **DiffuseStyleGesture+** [🔗 [292]]  
  *Builds upon DiffuseStyleGestures by further refining gesture synthesis through advanced multimodal integration and specialized attention mechanisms for personalized outputs.*

- **ViTPose** [🔗 [288]]  
  *Applies Vision Transformers to human pose estimation, providing a robust foundation for gesture synthesis by accurately capturing pose dynamics.*

- **Gesture Motion Graphs** [🔗 [319]]  
  *Utilizes graph-based modeling for few-shot gesture reenactment, effectively representing motion sequences and their dependencies.*

- **DiffSHEG** [🔗 [39]]  
  *Adopts a diffusion-based approach for real-time speech-driven 3D expression and gesture generation, leveraging joint text and audio representations for coherent outputs.*

- **C2G2** [🔗 [120]]  
  *Emphasizes controllability in co-speech gesture generation by using modular components to handle different aspects of gesture synthesis.*

- **DiffuGesture** [🔗 [318]]  
  *Focuses on generating gestures for two-person dialogues with specialized diffusion techniques tailored for interactive and conversational settings.*

---

## 🎥 Motion
Highlights text-constrained motion generation techniques, including MotionGPT and diffusion frameworks, for creating smooth and realistic animation sequences.

### 🗂 Datasets


| 🏷️ **Name** | 📊 **Statistics** | 🎭 **Modalities** | 🔗 **Link** |
|------------|------------------|------------------|------------|
| **KIT** | First openly available dataset with text-motion pairs, enabling text-to-motion research. | 📜 Text, 🏃 Motion | [KIT](https://motion-database.humanoids.kit.edu/) |
| **AMASS** | Large-scale motion dataset unifying sequences from multiple sources under the SMPL model. | 🏃 Motion (SMPL) | [AMASS](https://amass.is.tue.mpg.de/) |
| **HumanAct12** | Motion dataset with single-word action annotations; widely used in research. | 📜 Text (single-word labels), 🏃 Motion | [HumanAct12](https://paperswithcode.com/dataset/humanact12) |
| **BABEL** | Extends AMASS with sequence and subsequence-level textual annotations. | 📜 Text (sequence-level & subsequence labels), 🏃 Motion | [BABEL](https://babel.is.tue.mpg.de/) |
| **HumanML3D** | Large dataset with diverse activities, annotated with multiple detailed descriptions for training text-to-motion models. | 📜 Text (detailed descriptions), 🏃 Motion | [HumanML3D](https://github.com/EricGuo5513/HumanML3D) |
| **Motion-X** | Over 5x more motion clips than HumanML3D, significantly increasing dataset size for text-to-motion tasks. | 📜 Text (detailed descriptions), 🏃 Motion | [Motion-X](https://motion-x-dataset.github.io/) |


---

### 🤖 Models

---

## 📦 Object
Discusses approaches for text-to-3D object generation, such as Neural Radiance Fields (NeRFs) and 3D Gaussian Splatting, to create realistic assets.

### 🗂 Datasets


| 🏷️ **Name** | 📊 **Statistics** | 🎭 **Modalities** | 🔗 **Link** |
|------------|------------------|------------------|------------|
| **ShapeNet** | 3D models across multiple categories (furniture, vehicles, etc.). | 📝 Text, 🏗️ 3D Geometry, 🏗️ Shape Synthesis | [ShapeNet](http://shapenet.org/about) |
| **BuildingNet** | Architectural structures for shape completion tasks. | 🏗️ 3D Geometry, 📝 Text | [BuildingNet](https://github.com/BuildingNet/BuildingNet) |
| **Text2Shape** | Textual descriptions linked to ShapeNet categories. | 📝 Text-to-Shape Learning | [Text2Shape](https://text2shape.github.io/) |
| **ShapeGlot** | Textual utterances describing differences between shapes. | 📝 Text-to-Shape Evaluation | [ShapeGlot](https://github.com/alters-mit/ShapeGlot) |
| **Pix3D** | Chamfer Distance and F-Score evaluation for shape accuracy. | 🏗️ 3D Shape Accuracy Metrics | [Pix3D](https://github.com/xingyuansun/pix3d) |
| **LAION-5B** | Image-text pairs for conditional diffusion training. | 🖼️ Image Embeddings, 🏗️ Shape Synthesis | [LAION-5B](https://laion.ai/) |
| **COCO-Stuff** | Diverse textual descriptions for real-world 3D synthesis. | 📝 Text, 🖼️ Images | [COCO-Stuff](https://github.com/nightrome/cocostuff) |
| **Flickr30K** | Real-world object generation using diverse descriptions. | 📝 Text-to-3D Synthesis | [Flickr30K](https://github.com/ubmdmg/Flickr30kEntities) |
| **ModelNet40** | Evaluates 3D shape generation across 40 categories. | 📝 Text-to-Shape Benchmarks | [ModelNet40](https://modelnet.cs.princeton.edu/) |
| **ShapeNetCore** | Annotated 3D models for geometry and texture testing. | 🏗️ 3D Geometry, 📝 Text | [ShapeNetCore](http://shapenet.org/about) |
| **BlendSwap** | Realistic meshes with PBR materials. | 📝 Text-to-Mesh Synthesis | [BlendSwap](https://www.blendswap.com/) |
| **InstructPix2Pix** | Guides 2D-based edits for 3D objects. | 🖼️ Image & Instruction-Based Guidance | [InstructPix2Pix](https://github.com/timothybrooks/instruct-pix2pix) |
| **MagicBrush** | Refines texture and appearance in 3D content. | 🖼️ Image-Guided Appearance | [MagicBrush](https://github.com/OSU-NLP-Group/MagicBrush) |
| **NeRF-Synthetic** | Sparse 2D images for 3D reconstruction. | 🖼️ Image-to-3D Synthesis | [NeRF-Synthetic](https://github.com/bmild/nerf) |


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
