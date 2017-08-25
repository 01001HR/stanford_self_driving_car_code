### overview

i guess this package is a original velodyne driver from stanford or somewhere?


├── CMakeLists.txt    
├── include   
│   ├── defaultcal.h  //lookup table for laser ring  
│   ├── Driver.h  //handle udp data from velodyne, puts a packet in ROS message format and publish "/driving/velodyne/packet"  
│   ├── Points.h  
│   ├── Project3D.h  //subscribe "/driving/velodyne/packet" and project a packet data to 3D,  then publish /driving/velodyne/projected", "/driving/velodyne/rawpoints"  
│   ├── velodyneConfig.h  
│   ├── velodyne.h  //do all things in one class  
│   └── velo_support.h   
├── launch   
│   ├── Nodetest.launch   
│   ├── Playback.launch   
│   ├── velodyne.launch   
│   ├── VelodyneParam.launch  
│   ├── velodyne_view.vcg   
│   └── view.launch   
├── mainpage.dox   
├── Makefile   
├── manifest.xml   
├── msg    
│   ├── Block.msg    
│   ├── BlockRaw.msg  
│   ├── Packet.msg  
│   ├── Projected.msg  
│   ├── Return.msg  
│   ├── ScanPoint.msg  
│   └── Stat.msg  
├── nodelet_velodyne.xml  
└── src  
    ├── Driver.cpp  
    ├── Points.cpp  
    ├── Project3D.cpp  
    ├── velodyneConfig.cpp  
    ├── velodyne.cpp  
    ├── velodyne_dump.cpp  
    ├── velodyne_logger.cpp  
    ├── velodyne_main.cpp  
    ├── velodyne_stat.cc  
    ├── velo_support.cpp  
    ├── vlf_cut.cpp  
    └── vlf_index.cpp  


difference between "/driving/velodyne/projected" and "/driving/velodyne/rawpoints"
velodyne::Projected vs pcl::PointCloud<pcl::PointXYZI>
sorted pointcloud vs unsorted
