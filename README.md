<div align="center">

# [ICCAD'25] LMLitho: A Large Vision Model-Driven Lithography Simulation Framework

[![black](https://img.shields.io/badge/Code%20Style-Black-black.svg?labelColor=gray)](https://black.readthedocs.io/en/stable/)
[![license](https://img.shields.io/badge/License-MIT-green.svg?labelColor=gray)](https://github.com/ashleve/lightning-hydra-template#license)
[![PRs](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/ashleve/lightning-hydra-template/pulls)
[![contributors](https://img.shields.io/github/contributors/LMLitho/LMLitho.svg)](https://github.com/LMLitho/LMLitho/graphs/contributors)

</div>

## Dataset Description

The LMLitho dataset is partially available at https://github.com/LMLitho/LMLitho

### Source
We explore six representative source types: circular, annular, bull's eye, di-pole, quasar, and multi-pole. By varying internal parameters, such as inner radius, outer radius, open angle, and rotation angle, we generate 9,000 illumination source configurations. From these, 500 configurations are selected to construct optical models using the commercial tool.

### Layout
We take seven representative layout patterns used to characterize lithographic processes, resulting in 100,000 layout patterns at the 28nm technology node. Additionally, 28nm CPU M$1$ layer patterns are cropped using a sliding window approach, generating 25,000 more complex layouts to enhance the model’s robustness in handling intricate structures.

### Mask
Using the generated sources and layouts, we perform OPC using the commercial tool to generate 60,000 masks, combining 1,000 layouts with 60 distinct optical models. To increase diversity, we further generate masks by randomly pairing layouts and optical models, producing additional 40,000 masks. In total, we obtain over 0.1 million source-layout-mask pairs.

### Resist
From these 0.1 million source-layout-mask pairs, resist images (RIs) are simulated using the commercial lithography tool, yielding a large-scale dataset of 0.1 million source-layout-mask-resist pairs.

Note that both input masks and output RIs are represented with a pixel size of $1{nm}^2$, covering an area of $4\mu m^2$ per image. The source patterns are represented at a resolution of $201\times201$ pixels and padded to $256\times 256$ before training.

<!--
**LMLitho/LMLitho** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
