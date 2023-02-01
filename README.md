# VGMDataset

Dataset containing images of objects of various sizes for benchmarking optical size measurement methodologies

<h2>Dataset Details</h2>
The dataset comprises **221 RGB images** of **9** different parallelepiped objects of different dimensions. The
dimensions of
each object is stated at the name of the images and the folders that are contained in the form of [width x height].

For each object there is a corresponding **.json** file that contains information regarding the bounding boxes that were
used
to measure the object at each different image, the ground truth height and width of the object. Each key of the .json
file
has a list that contains information about each image. Each index of each list correspond to the same image.

You can download the dataset
from [here](https://drive.google.com/drive/folders/1l2r_q8BGJAXMlFjWzWWe6mMYSyPn3RJV?usp=sharing)!

<h2>Example of a .json file of an object</h2>

The .json file is of the form {"img": [filename_1, filename_2...], "bb": [[u1, v1, u2, v2], ...], "
distance": [z1, z2, ...], "object_height": [dY1, dY2, ...], "object_width": [dX1, dX2, ...]}.

<li>**img**: A list of the filenames of the images of an object</li>
<li>**bb**: List of coordinates of the object bounding box for each image</li>
<li>**bb**: List of coordinates of the object bounding box for each image</li>
<li>**distance**: List of distances between the image and the camera</li>
<li>**object_height**: Ground truth height of the object</li>
<li>**object_width**: Ground truth width of the object</li>

```
{"img": ["obj_0.12X0.25_0", "obj_0.12X0.25_1", "obj_0.12X0.25_2", "obj_0.12X0.25_3", "obj_0.12X0.25_4", "obj_0.12X0.25_5", "obj_0.12X0.25_6", "obj_0.12X0.25_7", "obj_0.12X0.25_8", "obj_0.12X0.25_9", "obj_0.12X0.25_10", "obj_0.12X0.25_11"], "bb": [[286, 135, 119, 261], [95, 139, 113, 274], [461, 152, 106, 275], [225, 205, 47, 399], [28, 222, 31, 442], [403, 222, 37, 414], [294, 107, 145, 207], [102, 115, 143, 220], [495, 123, 134, 221], [314, 90, 162, 172], [163, 94, 160, 183], [473, 99, 155, 178]], "distance": [0.5820000276435167, 0.554000026313588, 0.5440000258386135, 0.3840000182390213, 0.34200001624412835, 0.3660000173840672, 0.729000034625642, 0.6850000325357541, 0.687000032630749, 0.8740000415127724, 0.8450000401353464, 0.8510000404203311], "obj_height": [0.25, 0.25, 0.25, 0.25, 0.25, 0.25, 0.25, 0.25, 0.25, 0.25, 0.25, 0.25], "obj_width": [0.12, 0.12, 0.12, 0.12, 0.12, 0.12, 0.12, 0.12, 0.12, 0.12, 0.12, 0.12]}
```

<h2>Camera Details</h2>
The images were captured using the Intel RealSense D435. The intrinsic parmaeters of the camera tha correspond to the
capture session are stored in a camera_params.json.

```
{
  "fx": 613.712,
  "fy": 613.795,
  "ppx": 322.23,
  "ppy": 240.52,
  "image_width": 640,
  "image_height": 480,
  "camera_height": 0.12
}
```

<h2>Citation</h2>
This dataset is part of "Virtual Grid Mapping for Visual Size Measurements" so in case of use of this dataset please use
the following bibtex for citing:

```
//Paper citation to be added here when published//
```

<h2>To Do</h2>
<li>Provide code for loading the dataset</li>
