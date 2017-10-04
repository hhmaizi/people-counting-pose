# pose-tensorflow-video

Based on [pose-tensorflow](https://github.com/eldar/pose-tensorflow)

## Usage

Install [Docker](https://docker.com) and [Kitematic](https://kitematic.com/)

#### Installation / Setting
```
$ docker pull jgravity/tf-opencv-jupyter:pose-video
$ docker run jgravity/tf-opencv-jupyter:pose-video

# git clone https://github.com/PJunhyuk/pose-tensorflow-video

// If compile.sh permission ERROR
# chmod u+x compile.sh
# ./compile.sh

# cd models/coco
// If download_models.sh permission ERROR
# chmod u+x download_models.sh
# ./download_models.sh
# cd -
```

#### Multiperson pose detection in image
```
# TF_CUDNN_USE_AUTOTUNE=0 python3 demo/demo_multiperson.py test_multi_00
```

## Environments

Use Docker [jgravity/tf-opencv-jupyter](https://hub.docker.com/r/jgravity/tf-opencv-jupyter/),

or install

- python 3.5.3
- opencv 3.1.0
- jupyter 4.2.1
- git 2.1.4
- tensorflow 1.3.0
- some pip3 packages(scipy, scikit-image, matplotlib, pyyaml, easydict, cython, munkres)

## Reference

### Test dataset
- testset/video_1.mov: [Pedestrian overpass - original video (sample) - BriefCam Syndex](https://www.youtube.com/watch?v=aUdKzb4LGJI)

### Citation
    @inproceedings{insafutdinov2017cvpr,
	    title = {ArtTrack: Articulated Multi-person Tracking in the Wild},
	    booktitle = {CVPR'17},
	    url = {http://arxiv.org/abs/1612.01465},
	    author = {Eldar Insafutdinov and Mykhaylo Andriluka and Leonid Pishchulin and Siyu Tang and Evgeny Levinkov and Bjoern Andres and Bernt Schiele}
    }

    @article{insafutdinov2016eccv,
        title = {DeeperCut: A Deeper, Stronger, and Faster Multi-Person Pose Estimation Model},
	    booktitle = {ECCV'16},
        url = {http://arxiv.org/abs/1605.03170},
        author = {Eldar Insafutdinov and Leonid Pishchulin and Bjoern Andres and Mykhaylo Andriluka and Bernt Schiele}
    }
