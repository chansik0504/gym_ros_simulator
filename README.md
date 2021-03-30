# gym_ros_simulator

docker 설치

    $ curl -fsSL https://get.docker.com/ | sudo sh

설치확인

    $ sudo docker run hello-world

Hello from Docker! 가 뜨면 정상설치

    $ sudo apt install ros-melodic-ackermann-*
    $ sudo apt install ros-melodic-map-server*
    $ sudo apt install ros-melodic-joy*


https://drive.google.com/drive/folders/10vGlJ7DFu_uM2USHLafMs9LOzKyEl6t_?usp=sharing

구글 드라이브에 들어가서 f1tenth_gym_ros, car_duri 다운로드

    $ mkdir f1tenth_ws
    $ cd f1tenth_ws
    $ mkdir src


f1tenth/src/ 폴더안에 드라이브에서 설치한 f1tenth_gym_ros, car_duri 넣기

    $ cd ~/f1tenth_ws
    $ catkin_make
    
    $ gedit ~/.bashrc
        맨밑줄에 추가
        source ~/f1tenth_ws/devel/setup.bash
        저장 후 종료   
    $ bash
    
docker파일 설치

    $ cd ~/f1tenth_ws/src/f1tenth_gym_ros
    $ chmod +x *
    $ cd script
    $ chmod +x *
    $ cd ..

    $ sudo ./build_docker.sh
    $ cd ~/f1tenth_ws/src/car_duri
    $ chmod +x *
    
실행

    $ sudo ./docker.sh
    
    새로운 터미널 실행
    $ roslaunch car_duri ICE_fgm_solo.launch
    
