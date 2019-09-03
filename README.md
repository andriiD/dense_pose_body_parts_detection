### DensePoseDetection | Human activity understanding | Activity detection dataset | Hand detection dataset
Conversion of densepose annotations for the body parts detection and segmentation.
 
 Densepose masks are converted into coco format for
 body part detection. 14 Body parts + "Person" class are provided (with segmentation masks).
  If you would like to extract other data from densepose dataset then follow the steps described in the jupyter notebooks.
 They were tested with the original DensePose Docker image installed as described in the 
 [[`INSTALL.md`](https://github.com/facebookresearch/DensePose/blob/master/INSTALL.md)] .
 Set up the COCO dataset and copy the notebooks to /densepose/notebooks or mount this repository to the docker image.
 
 * Download annotations for body parts detection from \
  [[`Google drive`](https://drive.google.com/drive/folders/1JXz_luM5pZDNJjyTotPmOlOL9acV3I7Y?usp=sharing)]
 * Generate your own annotations with "DensePose_coco_body_parts_annotations.ipynb"
 * Check the new annotations with "visual_check_of_obtained_annotations.ipynb"
 
 ##### Available body parts annotations

    "Torso": 0,
    "RightHand": 1,
    "LeftHand": 2,
    "LeftFoot": 3,
    "RightFoot": 4,
    "UpperLegRight": 5,
    "UpperLegLeft": 6,
    "LowerLegRight": 7,
    "LowerLegLeft": 8,
    "UpperArmLeft": 9,
    "UpperArmRight": 10,
    "LowerArmLeft": 11,
    "LowerArmRight": 12,
    "Head": 13,
    "Person": 14
    
 ##### Example of the obtained annotations
  Notice that not every person has detailed body parts annotations in the original dataset, if it is absent then 
  additional field "has_dp_masks" is set to "False". Please, check the jupyter notebooks for more details.
  
  (Only 'Torso', "Head", "LowerArmLeft", "Person", "RightHand" are displayed here for clarity).
  ![`Picture`](body_parts.png)
 
 
 You can use my code for commercial projects but the dataset is created with research-only license.  
 
 Citations:
 
 [[`Facebook DensePose`](https://github.com/facebookresearch/DensePose)]
  ```
  @InProceedings{Guler2018DensePose,
  title={DensePose: Dense Human Pose Estimation In The Wild},
  author={R\{i}za Alp G\"uler, Natalia Neverova, Iasonas Kokkinos},
  journal={The IEEE Conference on Computer Vision and Pattern Recognition (CVPR)},
  year={2018}
  }
```