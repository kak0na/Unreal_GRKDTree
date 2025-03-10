KD-Tree Module Technical Imagesation

 Overview

This module implements a KD-Tree data structure based on 3D space, supporting efficient spatial query operations, including nearest neighbor search, range search, and frustum culling. It is suitable for point cloud data management, proximity queries, and other scenarios.

\------

Download the example project：https://github.com/kak0na/Unreal_GRKDTree/tree/main

Open Map: Map_KDTreeDemo，Modify different queryType values to see different effects

 Usage Example

1. Create an Actor based on GRKDTreeStruct

![image-20250309121858478](images/image-20250309121858478.png) 

2. Place the Actor in the scene

![image-20250309121933939](images/image-20250309121933939.png)

3. Create a Locations array

![image-20250309122110064](images/image-20250309122110064.png) 

4. Construct the data structure

![image-20250309122120321](images/image-20250309122120321.png) 

5. Set queryType and perform queries


queryType: 0: Query the nearest point

queryType: 1: Query the nearest N points

queryType: 2: Query points within a spherical range

queryType: 3: Query the nearest N points within the field of view

![image-20250309122330329](images/image-20250309122330329.png) 

Query the nearest point

![image-20250309123835042](images/image-20250309123835042.png) 

![image-20250309122230558](images/image-20250309122230558.png) 

![image-20250309122318970](images/image-20250309122318970.png) 

Query the nearest 10 points

![ ](images/image-20250309123857273.png) 

![image-20250309122404081](images/image-20250309122404081.png) 

![image-20250309122443646](images/image-20250309122443646.png) 

Query points within a spherical range

![image-20250309123905368](images/image-20250309123905368.png) 

![image-20250309122608941](images/image-20250309122608941.png) 



Query the nearest 10 points within the field of view

![image-20250309123911782](images/image-20250309123911782.png) 

![image-20250309123542562](images/image-20250309123542562.png) 

All Blueprint Content

![image-20250310182547132](images/image-20250310182547132.png)





------

 Performance Optimization

The performance is exceptionally superior.



| Number of Points | Construction Time |
| ---------------- | ----------------- |
| 1,000 points     | 0.0001s          |
| 10,000 points    | 0.002s           |
| 400,000 points   | 0.17s            |

**Recommendations**:

1. Regularly rebuild the tree structure for frequently updated scenes.