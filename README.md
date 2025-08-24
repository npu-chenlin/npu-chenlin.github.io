CoMA-SLAM: Collaborative Multi-Agent Gaussian SLAM With Geometric Consistency
Auther:
Lin Chen, Yongxin Su, Jvboxi Wang, Kun Li, Shuhui Bu, Guangming Wang, Pengcheng Han, Xia Zhenyu, Boni Hu, Shengqi Meng
Abstract:
Although Gaussian scene representation has achieved remarkable success in tracking and mapping, most existing methods are confined to single-agent systems. Current multi-agent solutions typically rely on centralized architectures, which struggle to account for communication bandwidth constraints. Furthermore, the inherent depth ambiguity of 3D Gaussian splatting poses notable challenges in maintaining geometric consistency. To address these challenges, we introduce CoMA-SLAM, the first distributed multi-agent Gaussian SLAM framework. By leveraging 2D Gaussian surfels and robust initialization strategy, CoMA-SLAM enhances tracking accuracy and geometry consistency. It efficiently manages communication bandwidth while dynamically scaling with the number of agents. Through the integration of intra- and inter-loop closure, distributed keyframe optimization and submap centric update, our framework ensures global consistency and robustly alignment. Synthetic and real-world experiments demonstrate that CoMA-SLAM outperforms state-of-the-art methods in pose accuracy, rendering fidelity, and geometric consistency while maintaining competitive efficiency across distributed multi-agent systems. Notably, by avoiding data transmission to a centralized server, our method reduces communication bandwidth by 99.8% compared to centralized approaches.
pub: AAAI Under review
date:2025
image/2025CoMA.png


GauS-SLAM: Dense RGB-D SLAM with Gaussian Surfels
Authers:
Yongxin Su, Lin Chen, Kaiting Zhang, Zhongliang Zhao, Chenfeng Hou, Ziping Yu
Abstract: 
We propose GauS-SLAM, a dense RGB-D SLAM system that leverages 2D Gaussian surfels to achieve robust tracking and high-fidelity mapping. Our investigations reveal that Gaussian-based scene representations exhibit geometry distortion under novel viewpoints, which significantly degrades the accuracy of Gaussian-based tracking methods. These geometry inconsistencies arise primarily from the depth modeling of Gaussian primitives and the mutual interference between surfaces during the depth blending. To address these, we propose a 2D Gaussian-based incremental reconstruction strategy coupled with a Surface-aware Depth Rendering mechanism, which significantly enhances geometry accuracy and multi-view consistency. Additionally, the proposed local map design dynamically isolates visible surfaces during tracking, mitigating misalignment caused by occluded regions in global maps while maintaining computational efficiency with increasing Gaussian density. Extensive experiments across multiple datasets demonstrate that GauS-SLAM outperforms comparable methods, delivering superior tracking precision and rendering fidelity.
pub: 	arXiv
date: 2025
paper url: https://doi.org/10.48550/arXiv.2505.01934
project page: https://gaus-slam.github.io/
image/2025GauS.png

Cluster-ALIV: Aerial LiDAR-Inertia-Visual Dense Reconstruction for Cluster UAV
Authers: Xiaohan Li; Jie Zhang; Shuhui Bu; Lin Chen; Kun Li; Zhenyu Xia
Abstract:
Uncrewed Aerial Vehicles (UAVs) equipped with LiDAR, camera, and Inertial Measurement Unit sensors are increasingly utilized for real-time dense reconstruction in large-scale rescue operations and environmental monitoring, among others. However, achieving algorithmic robustness remains challenging due to the UAVs' high-speed flight and rapid pose changes. Additionally, energy constraints on individual UAVs can be mitigated through multi-UAV collaboration, improving operational efficiency. Nevertheless, when faced with unknown environments or the loss of Global Navigation Satellite System signal, most multi-UAV dense reconstruction systems can't work, making it hard to construct a global consistent map. In this letter, we propose Cluster-ALIV, a real-time dense reconstruction system for multiple UAVs that effectively supports aerial, large-scale scenarios with lost global positioning and weak co-visibility of LiDAR or vision. The system integrates LiDAR-Inertial-Visual odometry through multi-sensor fusion to generate accurate, gravity-aligned, colorized LiDAR point clouds and visual information with scale. Overall, in the Cluster-ALIV, each UAV executes a LiDAR-Inertial-Visual odometry, transmitting point cloud and visual data to a ground server, where multi-UAV joint optimization is performed through LiDAR post-processing, visual post-processing, and normal distributions transform refinement. Extensive experiments demonstrate that our system can efficiently construct large-scale dense map in real time with high accuracy and robustness.
pub: IEEE Robotics and Automation Letters
date: 2025
paper url: https://doi.org/10.1109/lra.2025.3559839
image/2025ClusterALIV.png


CODE: COllaborative Visual-UWB SLAM for Online Large-Scale Metric DEnse Mapping
Authers:
Lin Chen, Xuan Jia, Shuhui Bu*, Guangming Wang3*, Kun Li, Zhenyu Xia,Xiaohan Li, Pengcheng Han, Xuefeng Cao
Abstract:
This paper presents a novel collaborative online
dense mapping system for multiple Unmanned Aerial Vehicles(UAVs). The system confers two primary benefits: it facilitates simultaneous UAVs co-localization and real-time dense map reconstruction, and it recovers the metric scale even in GNSS-denied conditions. To achieve these advantages, Ultrawideband (UWB) measurements, monocular Visual Odometry (VO), and co-visibility observations are jointly employed to recover both relative positions and global UAV poses, thereby ensuring optimality at both local and global scales. In the proposed methodology, a two-stage optimization strategy is proposed to reduce optimization burden. Initially, relative Sim3 transformations among UAVs are swiftly estimated, with UWB measurements facilitating metric scale recovery in the absence of GNSS. Subsequently, a global pose optimization is performed to effectively mitigate cumulative drift. By integrating UWB, VO, and co-visibility data within this framework, both local geometric consistency and global pose accuracy are robustly maintained. Through comprehensive simulation and empirical real-world testing, we demonstrate that our system not only improves UAV positioning accuracy in challenging scenarios but also facilitates the high-quality, online integration of dense point clouds in large-scale areas. This research offers valuable contributions and practical techniques for precise, real-time map reconstruction using an autonomous UAV fleet, particularly in GNSS-denied environments
pub:  2025 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)
date: 2025
image/2025CODE.png



G2-Mapping: General Gaussian Mapping for Monocular, RGB-D, and LiDAR-Inertial-Visual Systems
Authers:
Lin Chen; Boni Hu; Jvboxi Wang; Shuhui Bu; Guangming Wang; Pengcheng Han
Abstract:
In this paper, we introduce G2-Mapping, a novel method to comprehensively support online monocular, RGB-D, and LiDAR-Inertial-Visual systems, employing 3D gaussian points as scene representation. There are several issues when applying 3d gaussian splatting (3DGS) techniques to simultaneous localization and mapping (SLAM) 1) for monocular, the lack of depth information makes scene initialization difficult and large baseline positioning challenging; 2) differentiable rendering with respect to depth and pose has not been implemented in 3DGS, making it difficult to directly apply to the SLAM system; 3) strategy for updating the scene with incoming online frames is not present, which may lead to memory overflow. In order to overcome problems mentioned above, we formulate a mathematical derivation and propose a differentiable rendering approach that leverages both depth and color to optimize the scene and pose. We introduce a simplified odometry that provides a metric depth estimation for monocular and enhance the low-overlap scene availability. A scale consistency and uncertainty weighted optimization is further proposed to eliminates the impact of inaccurate depth prediction. Our proposed scene updating strategy effectively prevents rapid memory growth. Tracking and mapping are performed alternatively to achieve precise localization and synchronous high-fidelity map reconstruction. Extensive experiments demonstrate that our G2-Mapping surpasses feature-based SLAM in localization precision and exceeds state-of-the-art neural SLAM methods in the fidelity of view synthesis. Note to Practitioners—This paper is dedicated to tackling the efficiency challenges in multi-source SLAM and map reconstruction, aiming to generate pose and high-fidelity maps synchronously. We introduce G2-Mapping, a novel framework that leverages the power of 3D Gaussian points for scene representation, offering a universal solution for monocular, RGB-D, and LiDAR-Inertial-Visual systems. By developing a comprehensive differentiable renderer and presenting a strategy for dynamic scene updating, G2-Mapping significantly advances the state-of-the-art in localization precision and view synthesis fidelity. Although the approach is highly promising, it currently relies on the accuracy of depth prediction networks and requires further optimization for handling sparse LiDAR data. Future research will focus on enhancing these aspects, aiming to seamlessly integrate G2-Mapping into practical applications within robotics, autonomous vehicles, and augmented reality, where robust and efficient SLAM solutions are paramount.
pub:  IEEE Transactions on Automation Science and Engineering
paper url: https://doi.org/10.1109/tase.2025.3541255
date: 2025
image/2025G2.png

OriLoc: Unlimited-FoV and Orientation-Free Cross-View Geolocalization
Authers:
Boni Hu; Haowei Li; Shuhui Bu; Lin Chen; Pengcheng Han
Abstract:
Cross-view image-based geolocalization enables accurate, drift-free navigation without external positioning signals, crucial for UAV delivery and disaster relief. However, existing research primarily focuses on ground panoramic images with known orientations, while real-world scenarios involve unknown orientations and limited field of view (FoV), creating a research-application gap. We introduce OriLoc, an innovative cross-view geolocalization method integrating sophisticated orientation estimation for limited FoV and arbitrary orientation scenarios. Our approach employs a dual-weighted soft-margin triplet loss with hard sample mining to extract discriminative features. Additionally, we develop an orientation estimation module using convolution-based sliding windows to assess similarity between satellite-view and query embeddings. The method demonstrates superior performance on three challenging datasets spanning commercial, residential, urban, and suburban areas across two continents. Results show that hard sample mining combined with appropriate learning objectives significantly enhances geolocalization for limited FoV and orientation-free images. Our orientation estimation module achieves remarkable accuracy when integrated with attention embeddings prior to polar transformation. Code and trained models are available at https://github.com/bonihu/OriLoc.
pub: IEEE Journal of Selected Topics in Applied Earth Observations and Remote Sensing
date: 2025
paper url: https://doi.org/10.1109/jstars.2025.3579740
image/2025OriLoc.png

AutoFusion: Autonomous Visual Geolocation and Online Dense Reconstruction for UAV Cluster
Authers:
Yizhu Zhang, Shuhui Bu, Yifei Dong, Yu Zhang, Kun Li, Lin Chen
Abstract:
Real-time dense reconstruction using Unmanned Aerial Vehicle (UAV) is becoming increasingly popular in large-scale rescue and environmental monitoring tasks. However, due to the energy constraints of a single UAV, the efficiency can be greatly improved through the collaboration of multi-UAVs. Nevertheless, when faced with unknown environments or the loss of Global Navigation Satellite System (GNSS) signal, most multi-UAV SLAM systems can’t work, making it hard to construct a global consistent map. In this paper, we propose a real-time dense reconstruction system called AutoFusion for multiple UAVs, which robustly supports scenarios with lost global positioning and weak co-visibility. A method for Visual Geolocation and Matching Network (VGMN) is suggested by constructing a graph convolutional neural network as a feature extractor. It can acquire geographical location information solely through images. We also present a real-time dense reconstruction framework for multi-UAV with autonomous visual geolocation. UAV agents send images and relative positions to the ground server, which processes the data using VGMN for multi-agent geolocation optimization, including initialization, pose graph optimization, and map fusion. Extensive experiments demonstrate that our system can efficiently and stably construct large-scale dense maps in real-time with high accuracy and robustness.
pub: 2024 IEEE International Conference on Robotics and Automation (ICRA)
date: 2024
paper url: https://doi.org/10.1109/icra57147.2024.10611315
image/2024AutoFusion.png


CurriculumLoc: Enhancing Cross-Domain Geolocalization Through Multistage Refinement
Authers:
Boni Hu, Shuhui Bu, Lin Chen, Pengcheng Han
Abstract:
Cross-domain geolocalization, which aims to estimate the geographical location of a query image based on a reference image from a different domain, is a challenging task due to the significant domain gap between the reference and query images. Existing methods typically focus on aligning the visual features of the two images, but overlook the domain-specific characteristics that can be exploited to enhance the geolocalization performance. In this paper, we propose CurriculumLoc, a multistage refinement framework for cross-domain geolocalization. Our method first aligns the visual features of the two images using a feature alignment network. Then, we introduce a curriculum learning strategy to progressively refine the geolocalization results. Specifically, we first train a coarse geolocalization model using a small dataset with limited domain gap. Subsequently, we fine-tune the model using a larger dataset with a larger domain gap. Finally, we perform a post-processing step to further improve the geolocalization accuracy. Extensive experiments demonstrate that our method achieves state-of-the-art performance on the challenging cross-domain geolocalization task.
pub: IEEE Transactions on Geoscience and Remote Sensing
date: 2024
paper url: https://doi.org/10.1109/tgrs.2024.3380191
image/2024CurriculumLoc.png


HybridFusion: LiDAR and Vision Cross-Source Point Cloud Fusion
Authers:
Yu Wang; Shuhui Bu; Lin Chen; Yifei Dong; Kun Li; Xuefeng Cao; Ke Li; Jie Jin
Abstract:
Recently, cross-source point cloud registration from different sensors has become a significant research focus. Although current methods have advanced homogenous point cloud registration, challenges persist in the cross-source domain due to varying point cloud densities from different sensors and missing points caused by different viewing angles, which have hindered its development. To address these issues, we propose HybridFusion, a novel algorithm designed specifically for cross-source point cloud registration in outdoor large-scale scenes, accommodating various sensors and viewing angles. Due to the unique characteristics of point clouds, it is not a singular module, but rather a coarse-to-fine process. To extract similarity information from cross-source point clouds, local patches of the point cloud are subjected to similarity matching. Subsequently, precise alignment is performed using their distinctive features, including 2D boundary points. Finally, the poses obtained from multiple patches are fused to achieve the final registration. Our proposed approach is extensively evaluated through both qualitative and quantitative experiments with existing methods. Additionally, a novel metric for point cloud completion is introduced. The results establish our method as the state-of-the-art solution for cross-source point cloud registration, with a remarkable 70% increase in accuracy compared to recent approaches.
pub: IEEE Robotics and Automation Letters
date: 2023
paper url: https://doi.org/10.1109/lra.2023.3342555
image/2023HybridFusion.png

RTSfM: Real-Time Structure From Motion for Mosaicing and DSM Mapping of Sequential Aerial Images With Low Overlap
Authers:
Yong Zhao; Lin Chen; Xishan Zhang; Shibiao Xu; Shuhui Bu; hongkai jiang; Pengcheng Han; Ke Li; Gang Wan
Inspired by simultaneous localization and mapping (SLAM) style workflow, this article presented an online sequential structure from motion (SfM) solution for high-frequency video and large baseline high-resolution aerial images with high efficiency and novel precision. First, as traditional SLAM systems are not good in processing low overlap images, based on our novel hierarchical feature matching paradigm with multihomography and BoW, we proposed a robust tracking method where the relative pose and its scale are estimated separately followed by a joint optimization by considering both perspective-n-point (PnP) and epipolar constraints. Second, to further optimize the camera poses for the sparse map and dense pointcloud reconstruction, we provided a graph-based optimization with reprojection and GPS constraints, which make the camera trajectory and map georeferenced. We also incrementally generated the dense point cloud in real time from keyframes after local mapping optimization. Finally, we use a publicly available aerial image dataset with sequences of different environments, to evaluate the effectiveness of the proposed method, meanwhile, the robust performance of our solution is demonstrated with applications of high-quality aerial images mosaic and digital surface model (DSM) reconstruction in real time. Compared with the state-of-the-art SLAM and traditional SfM methods, the presented system can output large-scale high-quality ortho-mosaic and DSM in real time with the low computational cost.
pub: IEEE Transactions on Geoscience and Remote Sensing
date: 2021
paper url: https://doi.org/10.1109/tgrs.2021.3090203
image/2021RTSfM.png

Fast Tree Detection and Counting on UAVs for Sequential Aerial Images with Generating Orthophoto Mosaicing
Authers:
Pengcheng Han; Cunbao Ma; Jian Chen; Lin Chen; Shuhui Bu; Shibiao Xu; Yong Zhao; Chenhua Zhang; Tatsuya Hagino
Abstract:
Individual tree counting (ITC) is a popular topic in the remote sensing application field. The number and planting density of trees are significant for estimating the yield and for futher planing, etc. Although existing studies have already achieved great performance on tree detection with satellite imagery, the quality is often negatively affected by clouds and heavy fog, which limits the application of high-frequency inventory. Nowadays, with ultra high spatial resolution and convenient usage, Unmanned Aerial Vehicles (UAVs) have become promising tools for obtaining statistics from plantations. However, for large scale areas, a UAV cannot capture the whole region of interest in one photo session. In this paper, a real-time orthophoto mosaicing-based tree counting framework is proposed to detect trees using sequential aerial images, which is very effective for fast detection of large areas. Firstly, to guarantee the speed and accuracy, a multi-planar assumption constrained graph optimization algorithm is proposed to estimate the camera pose and generate orthophoto mosaicing simultaneously. Secondly, to avoid time-consuming box or mask annotations, a point supervised method is designed for tree counting task, which greatly speeds up the entire workflow. We demonstrate the effectiveness of our method by performing extensive experiments on oil-palm and acacia trees. To avoid the delay between data acquisition and processing, the proposed framework algorithm is embedded into the UAV for completing tree counting tasks, which also reduces the quantity of data transmission from the UAV system to the ground station. We evaluate the proposed pipeline using sequential UAV images captured in Indonesia. The proposed pipeline achieves an F1-score of 98.2% for acacia tree detection and 96.3% for oil-palm tree detection with online orthophoto mosaicing generation.
pub: Remote Sensing
date: 2023
paper url: http://dx.doi.org/10.3390/rs14164113
image/2023FastTree.png


Svar: A Tiny C++ Header Brings Unified Interface for Multiple programming Languages
Yong Zhao; Pengcheng Zhao; Shibiao Xu; Lin Chen; Pengcheng Han; Shuhui Bu; Hongkai Jiang
There are numerous types of programming languages developed in the last decades, and most of them provide interface to call C++ or C for high efficiency implementation. The motivation of Svar is to design an efficient, light-weighted and general middle-ware for multiple languages, meanwhile, brings the dynamism features from script language to C++ in a straightforward way. Firstly, a Svar class with JSON like data structure is designed to hold everything exists in C++, including basic values, functions or user defined classes and objects. Secondly, arguments are auto cast to and from Svar efficiently with compile time pointers, references and shared\_ptr detection. Thirdly, classes and functions are binded with string names to support reflection, this means all functions and classes in a shared library can be exported to a Svar object, which also calls a Svar module. The Svar modules can be accessed by different languages and this paper demonstrates how to import and use a Svar module in Python and Node.js. Moreover, the Svar modules or even a python module can also be imported by C++ at runtime, which makes C++ easier to compile and use since headers are not required anymore. We compare the performance of Svar with two state-of-the-art binding tool for Python and Node.js, and the result demonstrates that Svar is efficient, elegant and general. The core of this project is one single tiny modern C++ header with less than 5000 lines code without extra dependency. To help developers using Svar, all the source codes related are public available on http://github.com/zdzhaoyong/Svar, including documentations and benchmarks.
pub: arXiv
date: 2021
paper url: https://arxiv.org/abs/2108.08464
image/2021Svar.png


DenseFusion: Large-Scale Online Dense Pointcloud and DSM Mapping for UAVs
Authers:
Lin Chen; Yong Zhao; Shibiao Xu; Shuhui Bu; Pengcheng Han; Gang Wan
Abstract:
Large-scale online dense point cloud and digital surface model (DSM) mapping is a challenging task for unmanned aerial vehicles (UAVs). Existing methods either focus on single-view reconstruction or require a large number of images, which are not suitable for UAVs with limited onboard storage and computational resources. In this paper, we propose a large-scale online dense point cloud and DSM mapping method for UAVs. Our method is based on the DenseFusion framework, which is a state-of-the-art method for large-scale online dense point cloud and DSM mapping. Our method is evaluated on the public dataset, and the results show that our method is able to achieve a high-quality mapping result with a small number of images.
pub: 2020 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)
date: 2020
paper url: https://doi.org/10.1109/iros45743.2020.9341413
image/2020DenseFusion.png





