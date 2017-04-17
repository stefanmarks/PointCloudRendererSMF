# BA_PointCloud
PointCloud-BachelorThesis

Project files for my bachelor thesis on rendering point clouds in Unity.

Projects:
* Points1: A simple test project for trying to render simple point clouds. Open Assets/Scene1.unity!
  In this project there are three objects in the scene, of which only one should be enabled.
  Depending on what you want to try, you can enable different objects:
  * PointCloud_Plane: A plane-pointcloud is created by creating random points and rendering them as circles (using the Quads-Primitive). If you press the space button, the points are newly generated.
  * PointCloud_Lion_Quads: The Lion-Cloud is loaded and rendered with circles (using the Quads-Primitive)
  * PointCloud_Lion_Points: The Lion-Cloud is loaded and rendered with points (using the Points-Primitive. PointSize doesn't seem to work)
  
  The used PointCloud is an upscaled version of the Lion-PointCloud. It is also subsampled because the original cloud file was too big for github. So there are only ~880.000 points instead of 4 million.

* PointCloudRenderer: Main-Project. Open Assets/Scenes/LionScene.unity!
  This project is able to load a pointcloud in the Potree-format. The whole cloud is loaded and rendered.
  In this project there is an object "PointCloudLoader" in the scene. When selecting this you can set the path to the point cloud to load in the inspector.
  You can also choose a MeshConfiguration by clicking on the small circle beside the textfield. Three configurations are provided:
  * DefaultPointMeshConfiguration: Draws the points as single 1px-points.
  * RectQuadMeshConfiguration: Draws the points as squares. The size is changeable in the inspector of this object.
  * CircleQuadMeshConfiguration: Draws the points as circles. The size is changeable in the inspector of this object.