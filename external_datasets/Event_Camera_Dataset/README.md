# ABCE Open Data Project - the event camera dataset example

## Dataset introduction

[The event camera dataset](https://rpg.ifi.uzh.ch/davis_data.html) is one of real-world dataset samples where the ABCE Open Data team explore under [FAIR principles](https://www.go-fair.org/fair-principles/).
There are three file types of data in each dataset: Text(.zip), rosbag and Plots(.zip). From their [webpage](https://rpg.ifi.uzh.ch/davis_data.html), we can see format details as follows:

**Text Files**

- events.txt: One event per line (timestamp x y polarity)
- images.txt: One image reference per line (timestamp filename)
- images/00000001.png: Images referenced from images.txt
- imu.txt: One measurement per line (timestamp ax ay az gx gy gz)
- groundtruth.txt: One ground truth measurements per line (timestamp px py pz qx qy qz qw)
- calib.txt: Camera parameters (fx fy cx cy k1 k2 p1 p2 k3)

**Binary Files (rosbag)**

The rosbag files contain the events using [dvs_msgs/EventArray](https://github.com/uzh-rpg/rpg_dvs_ros/blob/master/dvs_msgs/msg/EventArray.msg) message types. 
The images, camera calibration, and IMU measurements use the standard [sensor_msgs/Image](http://docs.ros.org/api/sensor_msgs/html/msg/Image.html), [sensor_msgs/CameraInfo](http://docs.ros.org/api/sensor_msgs/html/msg/CameraInfo.html), and [sensor_msgs/Imu](http://docs.ros.org/api/sensor_msgs/html/msg/Imu.html) message types, respectively. 
Ground truth is provided as [geometry_msgs/PoseStamped](http://docs.ros.org/api/geometry_msgs/html/msg/PoseStamped.html) message type.

**Plots**
The plots are available inside a ZIP file for a quick inspection.

## What we are exploring

In their dataset, text files are the most flexible one since they can be loaded easily by Python or Matlab. However, the metadata is only on webpage, seperately stored from dataset if users download the dataset. This may result in inconvenience when reusing.

What we want to do is to create a metadata file to contain the necessary information from webpage and to provide a demonstration about reusage of metadata we create. 

## License

## Reference

## Tasks

## 

The purpose of this dataset is to …. 
The pictures are taken at a rate of …. e.g.  1 pic per 0.5 second,




### First stage

- [ ] write metadata.json (all .txt/.csv in one .json)
      - convert txt to csv?
      - write json
- [ ] code to reuse metadata
      - reuse metadata.json with dataset
      - csv validating
- [ ] upload zipfile of dataset sample. if we can use python to read zip from url, this step can be skiped.
      - consider about the data file format
      - notes: python library zipfile


### Second stage (optional)

If time and resourses are allowed, the second stage could be restructing the dataset using ['sensor observation model'](https://www.w3.org/TR/vocab-ssn/#Observations-overview).
