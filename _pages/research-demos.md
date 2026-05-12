---
title: "Research Demos"
permalink: /research-demos/
layout: single
author_profile: true
---

This page presents static demonstrations of my recent vision-language model research for ecological and remote sensing applications. The examples show how fine-tuned multimodal models can interpret drone thermal imagery and camera trap imagery for structured ecological information extraction.

These are static portfolio demonstrations. They show representative inputs, prompts, and expected model-style outputs. Interactive image upload and live inference will require a separate backend service, such as Hugging Face Spaces, Gradio, FastAPI, or a GPU-enabled server.

---

## Demo 1: Thermal Drone VLM for Species Recognition and Habitat-Context Interpretation

<div class="demo-card">

<h3>Lightweight Multimodal Adaptation of Vision Language Models for Species Recognition and Habitat Context Interpretation in Drone Thermal Imagery</h3>

<p>
This demo illustrates a fine-tuned vision-language model adapted to drone thermal imagery. The model is designed to recognize wildlife species, estimate instance counts, and generate habitat-context descriptions from thermal remote sensing inputs.
</p>

<p><strong>Research focus:</strong> Thermal drone imagery, vision-language models, multimodal projector alignment, species recognition, instance counting, and habitat-context interpretation.</p>

<p><strong>Representative task:</strong></p>

<pre><code>Identify the species, count the individuals, and describe the habitat context in this drone thermal image.</code></pre>

<div class="demo-image-grid">

  <div>
    <img src="/assets/images/demo-thermal-input-1.jpg" alt="Drone thermal demo input image 1" class="demo-image">
    <p class="image-caption">Example input 1: drone thermal imagery for wildlife recognition.</p>
  </div>

  <div>
    <img src="/assets/images/demo-thermal-input-2.jpg" alt="Drone thermal demo input image 2" class="demo-image">
    <p class="image-caption">Example input 2: drone thermal imagery for species and count interpretation.</p>
  </div>

</div>

<p><strong>Example structured output:</strong></p>

<div class="model-output">
Species: Rhino<br>
Count: 1<br>
Habitat context: The animal appears as a high-contrast thermal target in an open or partially open landscape. The surrounding scene suggests detectable large-bodied wildlife in a drone-based thermal remote sensing view.<br>
Interpretation: The image provides evidence for species-level recognition and instance enumeration from thermal drone imagery.
</div>

<p><strong>Publication:</strong> Chen, H., Qiu, F., Dong, F., Yang, D., Bohnett, E., &amp; An, L. (2026). <em>Lightweight Multimodal Adaptation of Vision Language Models for Species Recognition and Habitat Context Interpretation in Drone Thermal Imagery.</em> arXiv preprint arXiv:2604.06124.</p>

<p>
  <a href="https://arxiv.org/abs/2604.06124" target="_blank" rel="noopener noreferrer">View paper</a>
</p>

</div>

---

## Demo 2: CameraTrap-Instruct for Structured Camera Trap Interpretation

<div class="demo-card">

<h3>CameraTrap-Instruct: A Vision-Language Model for Structured Extraction and Interpreting of Camera Trap Imagery</h3>

<p>
This demo illustrates CameraTrap-Instruct, a vision-language model designed for structured ecological interpretation of camera trap imagery. The model supports species identification, instance counting, behavior description, metadata extraction, visual question answering, and ecological reasoning.
</p>

<p><strong>Research focus:</strong> Camera trap imagery, ecological attribute extraction, behavior interpretation, OCR-based metadata extraction, and structured wildlife monitoring outputs.</p>

<p><strong>Representative task:</strong></p>

<pre><code>Analyze this camera trap image. Identify the species, count the animals, describe the behavior, and extract visible metadata if available.</code></pre>

<div class="demo-image-grid">

  <div>
    <img src="/assets/images/demo-cameratrap-input-1.jpg" alt="Camera trap demo input image 1" class="demo-image">
    <p class="image-caption">Example input 1: camera trap imagery for structured ecological interpretation.</p>
  </div>

  <div>
    <img src="/assets/images/demo-cameratrap-input-2.jpg" alt="Camera trap demo input image 2" class="demo-image">
    <p class="image-caption">Example input 2: camera trap imagery with species, behavior, and metadata cues.</p>
  </div>

</div>

<p><strong>Example structured output:</strong></p>

<div class="model-output">
Species: Deer<br>
Count: 2<br>
Behavior: Moving through the camera trap scene.<br>
Visible metadata: Date, time, and ambient temperature can be extracted when visible in the image frame.<br>
Ecological interpretation: The image provides structured evidence of wildlife presence, activity, and site-level ecological context.
</div>

<p><strong>Publication:</strong> Chen, H., Qiu, F., Dong, F., Yang, D., Bohnett, E., &amp; An, L. (2026). <em>CameraTrap-Instruct: A Vision-Language Model for Structured Extraction and Interpreting of Camera Trap Imagery.</em> Available at SSRN 6301278.</p>

<p>
  <a href="https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6301278" target="_blank" rel="noopener noreferrer">View paper</a>
</p>

</div>

---

## Notes on Interactive Deployment

GitHub Pages is a static hosting service, so this page cannot run fine-tuned VLM checkpoints directly. A fully interactive demo would require a model inference backend.

A practical deployment structure would be:

<div class="model-output">
GitHub Pages frontend<br>
↓<br>
Hugging Face Spaces / Gradio / FastAPI backend<br>
↓<br>
Fine-tuned VLM checkpoint<br>
↓<br>
Generated model output
</div>

For the current portfolio version, the static demo format is recommended because it is lightweight, professional, and does not require uploading model checkpoints.
