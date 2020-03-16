## Dance Pose Synthesis

The idea is to generate new dance pose given a audio clip

### Dataset Generation

**Step 1**

Download dance videos from YouTube/other sources 

**Step 2**

Extract frames from the video

_e.g. ffmpeg -i video-path -r 24 folder-path/image%04d.png_

This will extract and save images with 24 fps to the given folder path.

**Step 3**

#### Background elimination and human body part segmentation:

I have used [ CVPR'18 spotlight WSHP](https://github.com/crazy-bot/WSHP) for this. Repository is forked from [here](https://github.com/MVIG-SJTU/WSHP)

orginal frame:

![orginal frame](https://github.com/crazy-bot/Dance-Pose-Synthesis/blob/master/Images/frame0221.png) 

Segmented frame:

![Segmented](https://github.com/crazy-bot/Dance-Pose-Synthesis/blob/master/Images/image0221.png)

### New Dance Pose Synthesis

Till now I experimented with [Progressive GAN](https://github.com/tkarras/progressive_growing_of_gans) to generate noble pose trained with 11 dance videos having total 11,931 frames.

Output frames:

![output](https://github.com/crazy-bot/Dance-Pose-Synthesis/blob/master/Images/image2.png)

#### To be Continued...

**Audio guided pose generation**

**Sequential pose generation**

**Overall dance choreography**



