# Indoor-Modelling-Robotic-Path-Planning-and-Navigation
Compilation of algorithms for modelling indoor environments from 2D LiDAR point clouds, RRT-based path planning, and Gazebo ROS simulation

## Introduction
The project combines various computing principles and programming languages to provide a proof of concept of the technologies and algorithms used in the field of indoor modelling, robotic path planning, and navigation.

## Project Goals and Challenges
The final versions of the projects must be able to achieve the following:

<li><b>Indoor Modelling:</b> <p>Given 2-dimensional LiDAR scans of an indoor space at various heights, the task is to convert the scans into a 3-dimensional model that approximately represents the indoor space. The task requires knowledge of Light Detection and Ranging and the types of LiDAR available in the market. One particular LiDAR that we have used in this project is the RPLIDAR developed by SLAMTEC, which is a low-cost, low-power sensor typically used for 2D applications, due to limited access to hardware and costs. Going through their official documentation was necessary in order to integrate the sensor with our operating systems to collect the readings and understand the exact working of their sensor.</p></li><br><br>

<li><b>Robotic Path Planning:</b> <p>Given a free configuration space, two end points for start and destination, coordinates of obstacles, the objective of the robot is to travel to the destination while avoiding all the obstacles in between, without any prior knowledge of the surroundings. The path should also be optimal. This project requires knowledge of path planning algorithms which are broadly classified into graph-based and sampling-based algorithms. Rapidly-Exploring Random Trees (RRT) are the most implemented and widely researched topic in this field, and the algorithm along with its variants are studied and implemented here. An extensive knowledge of the algorithm is necessary for this implementation, and to pin-point areas where high performance computing can be included to reduce some of the bottleneck in performance while generating the trees in the space.</p></li><br><br>

<li><b>Indoor Navigation:</b> <p>This project is done in the Gazebo ROS simulator to understand the concept of autonomous indoor navigation. Given a 3-dimensional model of an indoor space, the robot deployed in the environment must first map the entire world, and know its relative position using Simultaneous Localization and Mapping (SLAM). Once the layout of the map is constructed, the robot uses RRT to sample random nodes across and construct tree-links while avoiding obstacles. The robot now has all the route maps between any 2 points in the map and with that knowledge, the robot can now traverse the region. Since the entire simulation is done in Gazebo ROS, knowledge of Linux OS was necessary to follow the instructions for deploying ROS in the same. Since the approach uses SLAM, we need to first understand how the robot first maps the world and then uses path planning algorithm while mapping to construct occupancy grid of obstacles and route-maps to navigate within the map. </p></li>


## References

[1] Gunduz, M., Isikdag, U., & Basaraner, M. (2016). A REVIEW OF RECENT RESEARCH IN INDOOR MODELLING & MAPPING. International Archives of the Photogrammetry, Remote Sensing & Spatial Information Sciences, 41.<br>
[2] Han, J., Rong, M., Jiang, H., Liu, H., & Shen, S. (2021). Vectorized indoor surface reconstruction from 3D point cloud with multistep 2D optimization. ISPRS Journal of Photogrammetry and Remote Sensing, 177, 57-74.<br>
[3] Berger, M., Tagliasacchi, A., Seversky, L., Alliez, P., Levine, J., Sharf, A., & Silva, C. (2014, April). State of the art in surface reconstruction from point clouds. In Eurographics 2014-State of the Art Reports (Vol. 1, No. 1, pp. 161-185).<br>
[4] Pajaziti, A. (2014). Slam–map building and navigation via ros. International Journal of Intelligent Systems and Applications in Engineering, 2(4), 71-75.<br>
[5] Maiseli, B., Gu, Y., & Gao, H. (2017). Recent developments and trends in point set registration methods. Journal of Visual Communication and Image Representation, 46, 95-106.<br>
[6] Zhang, Z. (1994). Iterative point matching for registration of free-form curves and surfaces. International journal of computer vision, 13(2), 119-152.<br>
[7] dos Santos, R. C., Galo, M., & Carrilho, A. C. (2019). Extraction of building roof boundaries from LiDAR data using an adaptive alpha-shape algorithm. IEEE Geoscience and Remote Sensing Letters, 16(8), 1289-1293.<br>
[8] Guo, B., Menon, J., & Willette, B. (1997, October). Surface reconstruction using alpha shapes. In Computer graphics forum (Vol. 16, No. 4, pp. 177-190). Oxford, UK and Boston, USA: Blackwell Publishers.<br>
[9] Gardiner, J. D., Behnsen, J., & Brassey, C. A. (2018). Alpha shapes: determining 3D shape complexity across morphologically diverse structures. BMC Evolutionary Biology, 18(1), 1-16.<br>
[10] Bernardini, F., Mittleman, J., Rushmeier, H., Silva, C., & Taubin, G. (1999). The ball-pivoting algorithm for surface reconstruction. IEEE transactions on visualization and computer graphics, 5(4), 349-359.<br>
[11] Guo, B., Wang, J., Jiang, X., Li, C., Su, B., Cui, Z., ... & Yang, C. (2020). A 3D Surface Reconstruction Method for Large-Scale Point Cloud Data. Mathematical Problems in Engineering, 2020.<br>
[12] Kazhdan, M., Bolitho, M., & Hoppe, H. (2006, June). Poisson surface reconstruction. In Proceedings of the fourth Eurographics symposium on Geometry processing (Vol. 7).<br>
[13] Vizzo, I., Chen, X., Chebrolu, N., Behley, J., & Stachniss, C. (2021, May). Poisson surface reconstruction for LiDAR odometry and mapping. In 2021 IEEE International Conference on Robotics and Automation (ICRA) (pp. 5624-5630). IEEE.<br>
[14] LaValle, S. M. (1998). Rapidly-exploring random trees: A new tool for path planning.<br>
[15] Karaman, S., & Frazzoli, E. (2011). Sampling-based algorithms for optimal motion planning. The international journal of robotics research, 30(7), 846-894.<br>
[16] Mashayekhi, R., Idris, M. Y. I., Anisi, M. H., Ahmedy, I., & Ali, I. (2020). Informed RRT*-connect: An asymptotically optimal single-query path planning method. IEEE Access, 8, 19842-19852.<br>
[17] Palmieri, L., & Arras, K. O. (2014, September). A novel RRT extend function for efficient and smooth mobile robot motion planning. In 2014 IEEE/RSJ International Conference on Intelligent Robots and Systems (pp. 205-211). IEEE.<br>
[18] Bialkowski, J., Karaman, S., & Frazzoli, E. (2011, September). Massively parallelizing the RRT and the RRT. In 2011 IEEE/RSJ International Conference on Intelligent Robots and Systems (pp. 3513-3518). IEEE.<br>
[19] Pajaziti, A. (2014). Slam–map building and navigation via ros. International Journal of Intelligent Systems and Applications in Engineering, 2(4), 71-75.<br>
[20] An, Z., Hao, L., Liu, Y., & Dai, L. (2016). Development of mobile robot SLAM based on ROS. International Journal of Mechanical Engineering and Robotics Research, 5(1), 47-51.<br>
[21] Garrote, L., Premebida, C., Silva, M., & Nunes, U. (2014, July). An RRT-based navigation approach for mobile robots and automated vehicles. In 2014 12th IEEE International Conference on Industrial Informatics (INDIN) (pp. 326-331). IEEE.<br>
[22] Durrant-Whyte, H., & Bailey, T. (2006). Simultaneous localization and mapping: part I. IEEE robotics & automation magazine, 13(2), 99-110.<br>
[23] Bailey, T., & Durrant-Whyte, H. (2006). Simultaneous localization and mapping (SLAM): Part II. IEEE robotics & automation magazine, 13(3), 108-117.<br>
[24] SLAMTEC RPLIDAR URL https://www.slamtec.com/en/Lidar/A1<br>
[25] Open3D URL http://www.open3d.org/docs/release/<br>

