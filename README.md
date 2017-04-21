# NormFace
NormFace: $L_2$ HyperSphere Embedding for Face Verification

# Requirements

1. My Caffe (https://github.com/happynear/caffe-windows/tree/ms). If you want to use your own Caffe, please transplant the `inner_distance_layer`, `normalize_layer`, `general_contrastive_layer`, `flip_layer`, `softmax_layer` and `accuracy_layer` to your Caffe.
2. Matlab to draw some figures,
3. GPU with CUDA support,
4. MTCNN face and facial landmark detector(https://github.com/kpzhang93/MTCNN_face_detection_alignment).
5. Baseline model such as [center face](https://github.com/ydwen/caffe-face) or [Light CNN](https://github.com/AlfredXiangWu/face_verification_experiment).

# Train

1. The dataset used in this paper is [CASIA-Webface](http://www.cbsr.ia.ac.cn/english/CASIA-WebFace-Database.html). Note that there are 3 identities overlap between CASIA-Webface and LFW. They are `0166921`, `1056413` and `1193098`. For fair evaluation, it is recommended to remove them from CAISA-Webface. Align all face images using MTCNN. The script can be found in [my another github repository](https://github.com/happynear/FaceVerification/blob/master/dataset/general_align.m).
