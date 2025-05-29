# CSE 168 Final Project Proposal
[Link to Site](https://ethan-schwartzman.github.io/CSE168-Final-Project-Site/)
## Overview
For our CSE 168 final project, we have chosen to implement option 3.3, the Image-Based Rendering: Light Field Viewer. For this milestone, we implemented a basic version of the light field viewer with no optimizations or add-ons.

![Milestone](/docs/assets/images/milestone.png)

The resource that we referred to heavily was the 1996 light field rendering paper mentioned in lecture. Since the writeup states that the Stanford data had issues with its formatting, we also found a dataset from the University of Konstanz which contains 4D light field data. The dataset contains 23 scenes of 9x9x512x512x3 light fields.

## Resources
**Light Field Rendering** by Levoy and Hanrahan in SIGGRAPH 96
- Website: https://graphics.stanford.edu/papers/light/ 
- Paper: https://graphics.stanford.edu/papers/light/light-lores-corrected.pdf 
- Video: https://youtu.be/dMcZpeGOBPI?si=aFbabkKX1UFo8gy9 
- Slides: https://graphics.stanford.edu/~hanrahan/LightFieldTalk/

**4D Light Field Dataset** from University of Konstanz
- https://lightfield-analysis.uni-konstanz.de/ 

## Future Additions
There are several future additions we are considering for the final version of the project. One feature is prefiltering the light field using an aperture as in the original paper. This would help with antialiasing the light field and applying a blur to make the transitions more smooth. 

Another option is compression since the 4D data takes up a lot of memory on the GPU. The paper uses vector quantization (VQ) compression to compress with a 120:1 ratio. Even at such a high ratio, this has minimal visual effects, so this method of compression is something we will look into. Hardware texture mapping could also help to optimize efficiency of sampling from and transforming the light field data.
