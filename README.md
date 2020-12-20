# ERP42_Autonomouse_driving-Lab_view-
[![outdoor](https://img.youtube.com/vi/eRkZ373Lplc/0.jpg)](https://youtu.be/eRkZ373Lplc)
[Youtube Link(Click)]
# Outdoor_Robot_Project

>## 프로젝트 목차

#### 1. 프로젝트 목적
#### 2. 프로젝트 계획표
#### 3. 사용된 장비
#### 4. 설치(installing)
#### 5. 실행(operating)
#### 6. 참고자료


> ## 1. 프로젝트 목적

자율주행 플랫폼인 ERP42를 활용한 실외자율주행 테스트. 밸로다인의 LiDAR와 ublox의 GPS를 사용해서 물체인식과 위치추적을 한다.

> ## 2. 프로젝트 계획표
교육 기간 : 매일 09:00 ~ 18:00

교육 장소 : 언맨드솔루션 



|                            **월**                            |                        **화**                         |                          **수**                          |                          **목**                          |                       **금**                       |
| :----------------------------------------------------------: | :---------------------------------------------------: | :------------------------------------------------------: | :------------------------------------------------------: | :------------------------------------------------: |
|                          09월 28일                           |                       09월 29일                       |                        09월 30일                         |                        10월 01일                         |                     10월 02일                      |
| Kick Off  자율주행 차량 개발 현황  센서 기술 동향 랩뷰 설치  |                   대표님 강연  자습                   |                           추석                           |                                                          |                                                    |
|                          10월 05일                           |                       10월 06일                       |                        10월 07일                         |                        10월 08일                         |                     10월 09일                      |
| Linux / Shell Script  Linux 명령어 쉘 스크립트 실습 ROS 용어 설명 |   Sensor Application  Velodyne Logitech WebCam GPS    | ERP42 Platform   Ackermann 구조 ERP42 ROS NODE 작성 실습 | ERP42 Platform  시리얼 통신 엔코더 기반 오도메트리 실습  |                       한글날                       |
|                          10월 12일                           |                       10월 13일                       |                        10월 14일                         |                        10월 15일                         |                     10월 16일                      |
|          발표  개인별 발표   ROS 기반 ERP 동작 실습          |          Labview Basic1  기본 기능 설명 실습          |           Labview Basic2  프로그래밍 기초 실습           | Labview Basic3  H/W 인터페이스 파일 생성 및 입/출력 실습 |  GPS Basic1  GPS 기초이론 ublox-f9p Parser  실습   |
|                          10월 19일                           |                       10월 20일                       |                        10월 21일                         |                        10월 22일                         |                     10월 23일                      |
|  발표  오전 학생발표준비 오후 개인별 발표 및 검토 이후 실습  |      GPS Basic2  좌표계 변환 RTK 이론 설명 실습       |       GPS Application1  Data Logging Plotting 실습       |       GPS Application2  RDDF 파일 보간법 설명 실습       | GPS Application3  Waypoint 생성 Path Planning 실습 |
|                          10월 26일                           |                       10월 27일                       |                        10월 28일                         |                        10월 29일                         |                     10월 30일                      |
|  발표  오전 학생발표준비 오후 개인별 발표 및 검토 이후 실습  |           LiDAR Basic  LiDAR 센서 이론 실습           |      LiDAR Application1  Point Cloud 좌표변환 실습       |   LiDAR Application2  객체 인식 장애물 회피 경로 실습    |  Waypoint Driving  조향각 생성 Waypoint 주행 실습  |
|                          11월 02일                           |                       11월 03일                       |                        11월 04일                         |                        11월 05일                         |                     11월 06일                      |
|  발표  오전 학생발표준비 오후 개인별 발표 및 검토 이후 실습  |   Camera Application1  영상처리 기초 차선인식 실습    | Camera Application2  Hough Transform Bird Eye View 실습  |         Camera Application3  Bird Eye View 실습          |      Tensorflow Basic1  Tensorflow 활용 실습       |
|                          11월 09일                           |                       11월 10일                       |                        11월 11일                         |                        11월 12일                         |                     11월 13일                      |
|           Tensorflow Basic2  Tensorflow 활용 실습            | Mission 1  자율주행 기능 통합 알고리즘 구현 확인 실습 |  Mission 2  자율주행 기능 통합 알고리즘 구현 확인 실습   |                      최종 발표 준비                      |                   최종 발표 준비                   |
|                  **결과 보고회(11월 16일)**                  |                                                       |                                                          |                                                          |                                                    |


> ## 3.사용된 장비
+ ERP42(자율주행 플랫폼 + 산업용PC 연결)</br>
![ERP42](https://user-images.githubusercontent.com/29765871/102717186-05325380-4324-11eb-8609-9a978e561779.png))</br>
+ Velodyne LiDAR</br>
![밸로다인](https://user-images.githubusercontent.com/29765871/102717184-02376300-4324-11eb-8185-608093b20e80.png))</br>
+ ublox GPS</br>
![C030-U201-Image_06102017-2 png 250x250_q85](https://user-images.githubusercontent.com/29765871/102717197-2135f500-4324-11eb-992a-78325a14893c.png)</br>


> ## 4.설치(installing)
![image48](https://user-images.githubusercontent.com/29765871/102717465-d87f3b80-4325-11eb-8f15-be7685ca75b2.gif)
![image49](https://user-images.githubusercontent.com/29765871/102717468-da48ff00-4325-11eb-8db3-82130cf65f8c.gif)</br>


+ remote PC</br>
    + ROS 1 설치[Link](http://wiki.ros.org/melodic/Installation/Ubuntu)를 통해 설치한다.

    + 필요한 Depandancy 설치</br>
    <pre>
        <code>
            sudo apt-get install ros-melodic-joy ros-melodic-teleop-twist-joy ros-melodic-teleop-twist-keyboard ros-melodic-laser-proc ros-melodic-rgbd-launch ros-melodic-depthimage-to-laserscan ros-melodic-rosserial-arduino ros-melodic-rosserial-python ros-melodic-rosserial-server ros-melodic-rosserial-client ros-melodic-rosserial-msgs ros-melodic-amcl ros-melodic-map-server ros-melodic-move-base ros-melodic-urdf ros-melodic-xacro ros-melodic-compressed-image-transport ros-melodic-rqt-image-view ros-melodic-gmapping ros-melodic-navigation ros-melodic-interactive-markers
        </code>
    </pre>
    + Turtlebot3 패키지 설치(melodic version)</br>
    <pre>
        <code>
            cd ~/catkin_ws/src/
            git clone https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git
            git clone -b melodic-devel https://github.com/ROBOTIS-GIT/turtlebot3.git
            cd ~/catkin_ws && catkin_make
        </code>
    </pre>
    + Turtlebot3 application 패키지 설치(melodic version)</br>
    <pre>
        <code>
            cd ~/catkin_ws/src
            git clone https://github.com/ros-perception/ar_track_alvar.git
            git clone https://github.com/ROBOTIS-GIT/turtlebot3_applications.git
            git clone https://github.com/ROBOTIS-GIT/turtlebot3_applications_msgs.git
            cd ~/catkin_ws && catkin_make
        </code>
    </pre>
    + 통합 launch 파일 패키지 설치</br>
    <pre>
        <code>
            cd ~/catkin_ws/src
            git clone https://github.com/DonGikS/behavior_controller.git
            cd behavior_controller/turtlebot3_navigation/launch
            mv move_base.launch ../../../turtlebot3/turtlebot3_navigation/launch
            cd ~/catkin_ws/src/behavior_controller/turtlebot3_description/urdf
            mv turtlebot3_burger.urdf.xacro ../../../turtlebot3/turtlebot3_description/urdf
            cd ~/catkin_ws && catkin_make
        </code>
    </pre>
    + ROBOT(turtlebot3에서)</br>
        터틀봇 라즈베리파이 활성화[Link](https://emanual.robotis.com/docs/en/platform/turtlebot3/appendix_raspi_cam/)참고
        + turtlebot3_bringup/launch/turtlebot3_rpicamera.launch 파일 수정
        <launch>
            <node type="raspicam_node" pkg="raspicam_node" name="raspicam_node" output="screen">
                
                <param name="framerate" type="int" value="30" />
                <param name="exposure_mode" value="antishake" />
                <param name="shutter_speed" value="0" />
                <param name="quality" type="int" value="10" />
                <param name="width" type="int" value="320" />
                <param name="height" type="int" value="240" />
                <!--뒤집혀있으면 넣는다
                <param name="hFlip" type="int" value="true" />
                <param name="vFlip" type="int" value="true" />
                -->

                <param name="camera_frame_id" value="camera" />
                <!--이거 있으면 카메라전송 속도가 빨라짐-->
                <param name="/raspicam_node/quality"  value="9"/>
            </node>
        </launch>

    + Calibration with raspicam_node</br>
        + Remote PC에서</br>
        <pre>
            <code>
                roscore
            </code>
        </pre>
        + ROBOT(turtlebot3에서)</br>
        <pre>
            <code>
                roslaunch turtlebot3_bringup turtlebot3_rpicamera.launch
            </code>
        </pre>

        + Remote PC에서</br>
        <pre>
            <code>
                rosrun image_transport republish compressed in:=/raspicam_node/image raw out:=/raspicam_node/image
                rosrun camera_calibration cameracalibrator.py --size 8x6 --square 0.024 image:=/raspicam_node/image camera:=/raspicam_node
            </code>
        </pre>
        ![camera_calibration](https://user-images.githubusercontent.com/29765871/94400915-d2554500-01a4-11eb-90a8-b994f92cf59f.png)</br>
        + calibration 저장하고나서
        <pre>
            <code>
                cd /tmp
                tar -xvzf calibrationdata.tar.gz 
                mv ost.txt ost.ini
                rosrun camera_calibration_parsers convert ost.ini camera.yaml
                mv camera.yaml ~/.ros/camera_info/
            </code>
        </pre>

    + AR 마커 트래커</br>
        + Remote PC에서</br>
        <pre>
            <code>
                roscore
            </code>
        </pre>
        + ROBOT(turtlebot3에서)</br>
        <pre>
            <code>
                roslaunch turtlebot3_bringup turtlebot3_rpicamera.launch
            </code>
        </pre>
        + Remote PC에서</br>
        <pre>
            <code>
                roslaunch ar_track_alvar pr2_indiv_no_kinetic.launch
                rviz rviz
            </code>
        </pre>
        fixed frame을 카메라 이름으로 한다.
    ![ar_marker_tracking](https://user-images.githubusercontent.com/29765871/94400914-d1241800-01a4-11eb-930b-5832de80b8a0.png)</br>

    + 맵 제작</br>
        + Remote PC에서</br>
            <pre>
                <code>
                    roscore
                </code>
            </pre>
        + ROBOT(turtlebot3에서)</br>
            <pre>
            <code>
                roslaunch turtlebot3_bringup turtlebot3_robot.launch
                
            </code>
        + Remote PC에서</br>
            <pre>
                <code>
                    roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=cartographer
                </code>
            </pre>
            (mapping...)</br>
            ![map_design](https://user-images.githubusercontent.com/29765871/94400919-d2eddb80-01a4-11eb-9ce0-6abc67c6fc47.jpg)</br>
            <pre>
                <code>
                    rosrun map_server map_saver -f ~/map_my_kiro
                </code>
            </pre>
            ![Screenshot from 2020-09-29 01-47-44](https://user-images.githubusercontent.com/29765871/94462017-d9f10a00-01f5-11eb-8f34-c68dc19b0f67.png)


    
> ## 5.실행(operating)
+ Remote PC에서</br>
    <pre>
        <code>
            roscore
        </code>
    </pre>
+ ROBOT(turtlebot3에서)</br>
    <pre>
    <code>
        roslaunch turtlebot3_bringup turtlebot3_robot.launch
        roslaunch turtlebot3_bringup turtlebot3_rpicamera.launch
    </code>
+ Remote PC에서</br>
    <pre>
        <code>
            roslaunch behavior_controller execute.launch
        </code>
    </pre>
> ## 6.참고자료
>   >[raspberry_pi_camera_with_turtlebot3](https://emanual.robotis.com/docs/en/platform/turtlebot3/appendix_raspi_cam/)
>   >[ar_track_alvar](http://wiki.ros.org/ar_track_alvar)</br>
>   >[teb_local_planner_tutorials](http://wiki.ros.org/teb_local_planner_tutorials)</br>
>   >[turtlebot3_application_auto_parking_vision](https://emanual.robotis.com/docs/en/platform/turtlebot3/applications/)</br>
>   >[turtlebot3_slam](https://emanual.robotis.com/docs/en/platform/turtlebot3/navigation/#run-navigation-nodes)</br>
>   >[ros_melodic_cartographer](https://aur.archlinux.org/packages/ros-melodic-cartographer-ros/)</br>
>   >[raspicam_node_too_slow](https://answers.ros.org/question/289300/very-low-image-publish-rate-from-raspicam_node-over-wifi/)</br>
roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=cartographer configuration_basename:=turtlebot3_lds_2d_gazebo.lua
