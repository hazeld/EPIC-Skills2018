# EPIC-Skills2018

Annotations and links to videos for the EPIC-Skills 2018 Dataset from the CVPR 2018 paper [Who's Better? Who's Best? Pairwise Deep Ranking for Skill Determination](https://openaccess.thecvf.com/content_cvpr_2018/html/Doughty_Whos_Better_Whos_CVPR_2018_paper.html)

## Citing
When using this dataset, kindly reference:

Hazel Doughty, Dima Damen and Walterio Mayol-Cuevas (2018). Who's Better? Who's Best? Pairwise Deep Ranking for Skill Determination. In The IEEE Conference on Computer Vision and Pattern Recognition (CVPR).

## Annotation Folder Structure
`annotations` is further broken down into seven subdirectories, corresponding to the seven tasks used in the paper. 

Within each folder there is a <task>_gt.csv containing the ground truth annotations. This file consists of three columns:

* Vid1: the name of the first video in an annotated pair 
* Vid2: the name of the second video in the annotated pair
* Best: name of the video annotated as the better video in the pair.

Each folder also contains a 'splits' folder this contains 8 files named <task>_<split>_<split_num>/csv corresponding the the training and test split for each of the four splits used for 4-fold cross validation. These files contain two columns:

 * Better: the name of the video in the pair annotated as the best
 * Worse: the name of the worse video in the pair

## Obtaining the Videos
The videos for 'ChopstickUsing', 'HandDrawing' and 'SonicDrawing' can be downloaded [here](https://drive.google.com/file/d/1Ck-Dke5AcKMzKsedJfblRcTjSPBklo4P/view?usp=sharing). The folders for each task contain two further subdirectories 'Headmounted' and 'Stationary' which contain the video recordings of the tasks. In the original paper the 'Stationary' footage was used.

The Dough Rolling task was taken from the CMU-MMAC dataset (http://kitchen.cs.cmu.edu/) Pizza task.
The segments used from this task are detailed in `dough_rolling_segments.csv` which contains three fields: 

* Video: the filename of the headmounted recording when downloading the CMU-MMAC data
* StartFrame: the starting frame of our segmentation
* EndFrame: the final frame of our segmentation

The Surgery task used in our paper is available from https://cirl.lcsr.jhu.edu/research/hmm/datasets/jigsaws_release/. We use the right-hand recording in our dataset (<task>_<participant>_capture2.avi).

## Video Information
Videos are recorded in 1080p at 59.94 FPS on a GoPro Hero 5 with linear field of
view for the headmounted recordings and on a GoPro Hero 4 with a narrow field of view for the stationary recordings. 
