# ubuntu20.04でのros-noeticのインストール手順

## rosパッケージの公式リポジトリを追加
```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```

## 公開鍵をシステムに追加
```
sudo apt install curl
```
```
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
```

## パッケージをアップデート
```
sudo apt update
```

## rosのインストール
```
sudo apt install ros-noetic-desktop-full
```

## /opt/ros/noetic/setup.bashを.bashrcに追加
```
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
```
```
source ~/.bashrc
```

## rosの初期設定
```
sudo apt install python3-rosinstall python3-catkin-tools python3-rosdep
```

![](https://lh3.googleusercontent.com/pw/AP1GczNdyU1tmXMdB018FC5ivyyKOZIiyL1hF1gra82zC-ljykntMtv8shwk9W-Pp2cfCpqmFqX2e8eplBezhgyiiKhs_Xk1vfUnZf3yNEQ1F_lLi3WHY6AuHk5Eq3riJl9j1zc1IYuArXtbRxJnFgN3OFHt=w812-h645-s-no-gm)
```
sudo rosdep init
```
```
rosdep update
```
