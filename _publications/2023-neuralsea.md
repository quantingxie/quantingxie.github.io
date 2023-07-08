---
id:             2023-neuralsea
title:          "Beyond NeRF Underwater: Learning Neural Reflectance Fields for True Color Correction of Marine Imagery"
authors:
    - Me
    - MJR
venue:          In Submission.
year:           "2023-05"
thumbnail:      assets/publications/2023-neuralsea/neuralsea.png
links:
    paper:      https://arxiv.org/abs/2304.03384
    code:       https://github.com/tyz1030/neuralsea
    bibtex:     assets/publications/2023-neuralsea/ref.txt

layout: project
short_title: Learning Neural Reflectance Fields for True Color Correction of Underwater Imagery
abstract: "Underwater imagery often exhibits distorted coloration as a result of light-water interactions, which complicates the study of benthic environments in marine biology and geography. In this research, we propose an algorithm to restore the true color (albedo) in underwater imagery by jointly learning the effects of the medium and neural scene representations. Our approach models water effects as a combination of light attenuation with distance and backscattered light. The proposed neural scene representation is based on a neural reflectance field model, which learns albedos, normals, and volume densities of the underwater environment. We introduce a logistic regression model to separate water from the scene and apply distinct light physics during training. Our method avoids the need to estimate complex backscatter effects in water by employing several approximations, enhancing sampling efficiency and numerical stability during training. The proposed technique integrates underwater light effects into a volume rendering framework with end-to-end differentiability. Experimental results on both synthetic and real-world data demonstrate that our method effectively restores true color from underwater imagery, outperforming existing approaches in terms of color consistency."
---