# ERP42_Autonomouse_driving-Lab_view-
[![outdoor](https://img.youtube.com/vi/eRkZ373Lplc/0.jpg)](https://youtu.be/eRkZ373Lplc)
[Youtube Link(Click)]
# Outdoor_Robot_Project

>## 프로젝트 목차

#### 1. 프로젝트 목적
#### 2. 프로젝트 계획표
#### 3. 사용된 장비
#### 4. 구현한 기능
#### 5. VI Interface



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
![ERP42](https://user-images.githubusercontent.com/29765871/102717186-05325380-4324-11eb-8609-9a978e561779.png)</br>
+ Velodyne LiDAR</br>
![밸로다인](https://user-images.githubusercontent.com/29765871/102717184-02376300-4324-11eb-8185-608093b20e80.png)</br>
+ ublox GPS</br>
![C030-U201-Image_06102017-2 png 250x250_q85](https://user-images.githubusercontent.com/29765871/102717197-2135f500-4324-11eb-992a-78325a14893c.png)</br>


> ## 4.구현한 기능</br>
+LiDAR(물체인식, 물체 테두리 출력)</br>
![image48](https://user-images.githubusercontent.com/29765871/102717465-d87f3b80-4325-11eb-8f15-be7685ca75b2.gif)
![image49](https://user-images.githubusercontent.com/29765871/102717468-da48ff00-4325-11eb-8db3-82130cf65f8c.gif)</br>
+GPS 수신 (맵생성-RDDF생성)</br>
![KakaoTalk_20201221_222724769](https://user-images.githubusercontent.com/29765871/102786875-8997db80-43e3-11eb-92e1-e33dbdbdccd1.gif)</br>
+Path Tracking </br>
![KakaoTalk_20201221_223653747](https://user-images.githubusercontent.com/29765871/102786876-8997db80-43e3-11eb-948c-ff502ca22a6a.gif)
![231](https://user-images.githubusercontent.com/29765871/102786874-87ce1800-43e3-11eb-8137-f3d7c6c4814d.gif)</br>

> ## 5.VI Interface</br>
+Path</br>
![one_of_all1](https://user-images.githubusercontent.com/29765871/102788056-65d59500-43e5-11eb-9207-90ca9c42f934.JPG)</br>
+GPS</br>
![one_of_all2](https://user-images.githubusercontent.com/29765871/102788050-640bd180-43e5-11eb-9614-e9015781970b.JPG)</br>
+LiDAR</br>
![one_of_all3](https://user-images.githubusercontent.com/29765871/102788055-653cfe80-43e5-11eb-92af-a0c277ea9944.JPG)</br>
