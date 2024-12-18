# Dataset Preprocessing

This project utilizes the **TUMTraf V2X Cooperative Perception Dataset**, created for cooperative 3D object detection and tracking tasks.

## Selected Scenarios

We have selected **9 scenarios**, each containing **50 frames**, for tasks such as **scene reconstruction** and **novel view synthesis**. The selected scenarios are as follows:

| Scene Name                      |
|---------------------------------|
| Ego Vehicle Occlusion           |
| Cyclist in Blind Spot           |
| Pedestrians Crossing            |
| U-Turn Maneuver                 |
| RSU Occlusion                   |
| Far Distance Pedestrian         |
| Dense VRU Crossing              |
| Dense VRU with RSU Occlusion    |
| Night Scene                     |

## Sensors and Field of View

The dataset includes data from **2 road-side unit (RSU) cameras**, **1 camera in the ego vehicle**, and **LiDARs** whose fields of view (FOV) collectively cover the intersection. Below is the mapping of sensor and LiDAR names to their simplified identifiers:

| Sensor Name                                     | Identifier |
|-------------------------------------------------|------------|
| `s110_camera_basler_south2_8mm`                 | `cam01`    |
| `vehicle_camera_basler_16mm`                    | `cam02`    |
| `s110_camera_basler_south1_8mm`                 | `cam03`    |
| `s110_lidar_ouster_south_and_vehicle_lidar_robosense_registered` | `lidar`    |

---

## Preprocessing the Dataset

To preprocess the dataset as described above, run the following command:

```bash
python3 data_preprocessor.py --dataset "path_to_dataset"
