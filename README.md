# ddd
Google Deepdream Dockerfile, forked from https://registry.hub.docker.com/u/mjibson/deepdream/ 

## Installation
- clone this repo
- install docker
- Build the image. `cd` in the just cloned repository folder and `docker build -t edap/ddd .`
- create a folder where to store the output images, `mkdir ~/dreams`

## Example
Supposing that you are in your home direcotry
  ```bash
  docker run --rm -v `pwd`/dreams:/images edap/ddd 'https://www.google.com/logos/2013/zamboni-1005006-hp.jpg' 'inception_3b/5x5_reduce' 15 8 1.9
  ```

## Parameters
- `'https://www.google.com/logos/2013/zamboni-1005006-hp.jpg'` Mandatory, an Url that points to a jpg
- `'inception_3b/5x5_reduce'` Optional, default is `inception_4c/output`
- `15` Optional, number of iteration, default is `10`
- `8` Optional, number of octave, default is `4`
- `1.9` Optional, number of octave_scale, default is `1.4`

In the Ipython [notebook](https://github.com/google/deepdream/blob/master/dream.ipynb) you can find more details about the parameters 
