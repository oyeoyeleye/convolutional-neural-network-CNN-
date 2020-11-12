# Identifying thoracic pathologies from Chest X{ray data

## Background

A frequent and cost effective medical imaging examination is the chest X{ray. However, a clinical diagnosis can
be more challenging than diagnosis via chest CT imaging. In fact, achieving clinically relevant computer-aided
detection and diagnosis (CAD) in real world medical sites on all data settings of chest X-rays is still very difficult,
if not impossible when only several thousands of images are employed for study.
The desire is to teach computers how to detect and diagnose disease. Ultimately, this artificial intelligence mechanism
can lead to clinicians making better and quicker diagnostic decisions for patients by using a computer which has
been taught to read and process extremely large amounts of scans, to confrm the results radiologists have found and
potentially identify other findings that may have been overlooked.
In addition, this may also be able to: (1) help identify slow changes occurring over the course of multiple chest
x-rays that might otherwise be overlooked; (2) benefit patients in developing countries that do not have access to
radiologists to read their chest x-rays; and (3) create a virtual radiology resident that can later be taught to read
more complex images like CT and MRI in the future.

## Goal

Our goal is to train a deep convolutional neural network that can reliably classify dierent thoracic pathologies from
human chest X{rays. This will allow for a faster and more accurate diagnoses of several diseases, which will lead to
a more effcient care of patients in hospitals around the world.

## Data

This NIH Chest X-ray dataset [5] is comprised of 112; 120 X-ray images with resolution 1024 by 1024 and disease labels
from 30; 805 unique patients. The 14 disease image labels (where each image can have multi-labels, see Fig. 1 & 2),
were mined from the associated radiological reports using Natural Language Processing (NLP). The 14 classes are
common thoracic pathologies: Atelectasis, Consolidation, Infitration, Pneumothorax, Edema, Emphysema, Fibrosis,
Effusion, Pneumonia, Pleural thickening, Cardiomegaly, Nodule, Mass, and Hernia. These text-mined disease labels
are expected to have accuracy > 90%. Meta data for all images includes: Image Index, Finding Labels, Follow-up ,
Patient ID, Patient Age, Patient Gender, View Position, Original Image Size and Original Image Pixel Spacing.

## Model and Method

We will train deep convolutional neural networks on this dataset to correctly identify the one or more pathologies
in each X{ray image. In order to do this, we will try to minimize the cross{entropy between the ground truth and
the classiffication results. We will make use of transfer learning and therefore use a variety of popular architectures
used in image recognition such as ResNet, AlexNet, VGG, etc.
