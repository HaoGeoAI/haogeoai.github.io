---
title: "Research Demos"
permalink: /research-demos/
layout: single
author_profile: true
---

This page presents static demonstrations of my recent vision-language model research for ecological and remote sensing applications. The examples below illustrate representative inputs, prompts, and structured outputs from fine-tuned multimodal models.

---

## Demo 1: Lightweight Multimodal Adaptation of Vision Language Models for Drone Thermal and RGB Imagery

<div class="demo-card">

<h3>Species Recognition, Counting, and Habitat Context Interpretation</h3>

<p>
This demo is based on my fine-tuned vision-language model for drone imagery. The framework supports two related tasks: species recognition and counting from thermal imagery, and habitat-context interpretation from RGB imagery.
</p>

---

<h4>Demo 1A: Thermal Imagery</h4>

<p><strong>Input image:</strong></p>

<img src="/assets/images/Demo1_thermal.jpg" alt="Drone thermal input image" class="demo-image-single">

<p class="image-caption">Thermal drone image used for species recognition and instance counting.</p>

<p><strong>Prompt:</strong></p>

<pre><code>Identify the species and count. Return ONLY in the format: Species; Count (example: Deer; 1).</code></pre>

<p><strong>Example model output:</strong></p>

<div class="model-output">
Rhino; 1
</div>

---

<h4>Demo 1B: RGB Imagery</h4>

<p><strong>Input image:</strong></p>

<img src="/assets/images/demo1_RGB.jpg" alt="Drone RGB input image" class="demo-image-single">

<p class="image-caption">RGB drone image used for environmental and habitat-context interpretation.</p>

<p><strong>Prompt:</strong></p>

<pre><code>Describe the most important environmental context in this drone image. Return 4 lines only:
Habitat/land cover:
Key landscape features (e.g., river, road, forest edge, grassland).
Human presence/disturbance (if any).
Brief habitat-context interpretation (1 sentence).</code></pre>

<p><strong>Example model output:</strong></p>

<div class="model-output">
Habitat/land cover: Open grassland with scattered shrubs.
Key landscape features: Grassland, forest edge, and a narrow dirt track.
Human presence/disturbance (if any): No visible human presence.
Brief habitat-context interpretation: The scene suggests suitable open habitat adjacent to edge vegetation, which may support wildlife movement and foraging.
</div>

<p><strong>Publication:</strong> Chen, H., Qiu, F., Dong, F., Yang, D., Bohnett, E., &amp; An, L. (2026). <em>Lightweight Multimodal Adaptation of Vision Language Models for Species Recognition and Habitat Context Interpretation in Drone Thermal Imagery.</em> arXiv preprint arXiv:2604.06124.</p>

<p>
  <a href="https://arxiv.org/abs/2604.06124" target="_blank" rel="noopener noreferrer">View paper</a>
</p>

</div>

---

## Demo 2: CameraTrap-Instruct for Structured Camera Trap Interpretation

<div class="demo-card">

<h3>Structured Ecological Extraction from Camera Trap Imagery</h3>

<p>
This demo is based on CameraTrap-Instruct, a vision-language model for structured interpretation of camera trap images. The model supports species identification, counting, metadata extraction, behavior classification, and caption generation.
</p>

<p><strong>Input image:</strong></p>

<img src="/assets/images/Demo2.jpg" alt="Camera trap input image" class="demo-image-single">

<p class="image-caption">Camera trap image used for structured ecological extraction and metadata-aware interpretation.</p>

<p><strong>Prompt:</strong></p>

<pre><code>"You are assisting a wildlife conservation study with camera-trap images.
Return One JSON object ONLY (no extra text).
Keys and value rules:
species (comma-separated; one or two species; common names allowed);
count (integer);
temperature (e.g., 87°F (31°C));
date (MM/DD/YYYY);
time (HH:MM:SS, 24-hour);
behavior (one single word);
caption (1 or 2 sentences. Describe the target’s action, count, and what can be seen in the background.
Do not mention temperature, date, or time.)"</code></pre>

<p><strong>Example model output:</strong></p>

<div class="model-output">
{
  "species": "cow, human",
  "count": 2,
  "temperature": "97°F (36°C)",
  "date": "04/28/2022",
  "time": "15:14:25",
  "behavior": "moving",
  "caption": "A woman in an orange dress walks barefoot past a brown cow in a forested area. She carries a black backpack."
}
</div>

<p><strong>Publication:</strong> Chen, H., Qiu, F., Dong, F., Yang, D., Bohnett, E., &amp; An, L. (2026). <em>CameraTrap-Instruct: A Vision-Language Model for Structured Extraction and Interpreting of Camera Trap Imagery.</em> Available at SSRN 6301278.</p>

<p>
  <a href="https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6301278" target="_blank" rel="noopener noreferrer">View paper</a>
</p>

</div>

---

## Notes

This page presents static examples for research communication purposes. Live inference and user-upload functionality would require a separate backend service, such as Hugging Face Spaces, Gradio, FastAPI, or another GPU-enabled deployment environment.
