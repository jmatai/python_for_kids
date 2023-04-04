#Project Proposal Overview 

## Introduction and Goals:
The mentorship program is designed to introduce high school students to advanced technologies such as machine learning and computer vision, and teach them how to do research, propose research topics, do independent study, and conduct experiments and feasibility studies.
The main goal of the program is to expose students to advanced research and provide them with the skills and knowledge to pursue their own research interests in these fields.

## Python Programming:
In the first two months of the program, students will learn Python programming. The curriculum will cover the basics of data types, control structures, and functions, and gradually introduce more advanced topics such as object-oriented programming, data visualization, and machine learning libraries such as NumPy and Pandas.
The program will include exercises and mini-projects to help students practice their coding skills and reinforce their learning.

## Project Proposal:
At the end of the second month, students will propose a research topic that they would like to work on for the remainder of the program. The program mentor will provide a template or guidelines to follow when writing the proposal.
Students are encouraged to focus on projects that are feasible and realistic given their skills and resources. The mentor will provide feedback on the proposals and suggest modifications or alternative ideas if necessary.
Students are also encouraged to think about the potential impact of their projects and how they can contribute to the broader community of machine learning and computer vision researchers.

## Project Work:
Students will work on their research projects for the remaining months of the program, meeting weekly with the mentor to discuss progress, get feedback, and ask questions.
The mentor will offer resources such as datasets, code snippets, and research papers that the students can use as references for their projects.
The mentor will encourage collaboration and sharing of ideas among the students, but also emphasize the importance of independent work and original ideas.

## Project Completion:
At the end of the program, students will write a final report summarizing their project and its outcomes. They will also push all source code and a readme file to Github.
The mentor may organize a showcase or presentation event where the students can present their projects to an audience of peers, parents, and other researchers.
The mentor may also offer opportunities for the students to continue their research and participate in hackathons, conferences, or other events in the field of machine learning and computer vision.


# Candaite Projects  
Here are list of candiate projects (This list will be updated)  
## Candiated Projects: Computer Vision 

### Object Detection 
**Real-time object detection with YOLOv5:**

-Tutorial: https://github.com/ultralytics/yolov5/wiki/Train-Custom-Data
-GitHub repository: https://github.com/ultralytics/yolov5
-COCO dataset: http://cocodataset.org/#download

**Object detection for autonomous driving:**

-Tutorial: https://github.com/WongKinYiu/yolov5-rt-stack-tutorial
-KITTI dataset: http://www.cvlibs.net/datasets/kitti/eval_object.php?obj_benchmark=2d
-Cityscapes dataset: https://www.cityscapes-dataset.com/



### Object Segmentation 

**Medical image segmentation with DeepLab V3+:**

-Tutorial: https://medium.com/analytics-vidhya/semantic-segmentation-with-deeplab-v3-56f6303f4c6f
-GitHub repository: https://github.com/tensorflow/models/tree/master/research/deeplab
-ISIC 2018 dataset: https://challenge2018.isic-archive.com/segmentation/

### Image Classification
**Image classification with CNNs:**

Tutorial: https://machinelearningmastery.com/how-to-develop-a-cnn-from-scratch-for-cifar-10-photo-classification/
GitHub repository: https://github.com/DeepLearningSandbox/DeepLearningSandbox/tree/master/transfer_learning
CIFAR-10 dataset: https://www.cs.toronto.edu/~kriz/cifar.html

**Transfer learning for image classification with pre-trained models:**
-Tutorial: https://www.tensorflow.org/tutorials/images/transfer_learning
-GitHub repository: https://github.com/keras-team/keras-applications
-ImageNet dataset: http://www.image-net.org/

**Image classification with CNNs and data augmentation:**
-Tutorial: https://www.tensorflow.org/tutorials/images/classification
-GitHub repository: https://github.com/tensorflow/models/tree/master/official/vision/image_classification
-Flowers dataset: https://www.tensorflow.org/datasets/catalog/tf_flowers


### Depth Estimation for Autonomous Drivng 

**Monocular depth estimation:** Build a system that can estimate the depth of a scene from a single image using deep learning algorithms. This could involve training a convolutional neural network (CNN) on a dataset of labeled images and depth maps, and using the output of the network to estimate the depth of a new image. Here is a tutorial on monocular depth estimation using deep learning: https://towardsdatascience.com/monocular-depth-estimation-using-deep-learning-and-opencv-5bfc3ddc858

**Stereo depth estimation:** Build a system that can estimate the depth of a scene from a stereo pair of images using deep learning algorithms. This could involve training a CNN on a dataset of labeled stereo image pairs and corresponding depth maps, and using the output of the network to estimate the depth of a new stereo pair. Here is a tutorial on stereo depth estimation using deep learning: https://towardsdatascience.com/depth-perception-using-stereo-images-and-deep-learning-19c2d3815a74

### Advanced Computer Vision

**NeRF( Neural Radiance Field)** 

Given a set of images and corresponding camera poses, the NeRF network learns to predict the radiance value of a 3D point in the scene. The network is typically a multi-layer perceptron (MLP) that takes as input the 3D coordinate and the view direction (i.e. the direction from the camera to the point).

During training, the network is optimized to minimize the error between the predicted and ground-truth radiance values at each 3D point. This is typically done using a combination of supervised and unsupervised learning techniques.

Once the network is trained, it can be used to render novel views of the scene by ray marching through the 3D function and accumulating the radiance values along each ray.

Here are some example projects related to NeRF:

NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis (Original NeRF paper):
-Paper: https://arxiv.org/abs/2003.08934
-Code: https://github.com/bmild/nerf

Collaborative NeRF: A Joint Neural Radiance Fields Framework for Depth Completion and Deblurring:
-Paper: https://arxiv.org/abs/2102.09635
-Code: https://github.com/youyuge34/CollaborativeNeRF

InverseRenderNet: Learning Single Image Inverse Rendering:
-Paper: https://arxiv.org/abs/2102.12599
-Code: https://github.com/facebookresearch/InverseRenderNet
 
