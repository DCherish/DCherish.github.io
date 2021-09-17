---
layout: page
title:  "AR Indoor Navigation"
subtitle: "A service application when someone is indoors by using AR tech"
date:   2020-07-10 11:11:11 +0530
categories: ["project"]
comments: true
---

<br>

<p align="middle"><iframe width="759" height="480" src="https://www.youtube.com/embed/NvaQYQSHGWI" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></p>

*총 두 가지의 영상이 차례로 재생됩니다.*  

*영상 1 : 좌측 상단의 메뉴 버튼의 Direction 버튼을 클릭하여 현재 내가 어디에 위치해 있는지 알 수 있습니다. 우측 상단의 목적지 버튼을 클릭하면 안내 받을 수 있는 영역이 빨간색으로 표시됩니다. 원하는 지역을 클릭하면 해당 목적지까지 화면을 통해 안내를 받을 수 있습니다. 사실감 있게 표현하기 위해 AR 물체가 벽에 가려졌을 경우 가려져서 보이지 않도록 Stencil Shader & Mask 기법을 적용하였습니다. Map을 더욱 정교히 구현하고 신호의 오차를 정교히 핸들링한다면 더욱 사실감 있는 AR 서비스를 구현할 수 있겠습니다.*  

*영상 2 : 현재의 위치는 카메라와 블루투스 신호를 통해 계산됩니다. 카메라를 가리고 Random한 위치로 움직입니다. 도착한 후 메뉴 버튼의 Scan 버튼을 통해 현재의 위치가 정상적으로 계산되는지, 기타 다양한 기능들이 정상적으로 작동하는지를 테스트하는 영상입니다.*  

<br>
<br>

### INTRODUCTION 💬

최근 소비자들의 편리성을 증대시키기 위하여 실내 위치 측정에 관한 다양한 연구가 진행되고 있습니다. 단순히 무선 신호에 기반한 측위 시스템에서는 송수긴기 사이의 전파 경로가 물체들로 인하여 가려지거나, 다른 환경적인 요인들로 인한 신호의 정확성 문제가 발생하기 때문에 무선 신호만을 이용하여 정확한 실내 위치를 도출하는 것에는 한계가 존재합니다. 즉, **BLE(Bluetooth Low Energy) Beacon**만을 이용하여 실내 위치 측위를 하는 방법들은 대부분 정확성이 떨어지기에 실제로 사용함에 있어서 한계가 존재합니다. 본 프로젝트의 목적은 위에서 발생한 문제점들을 해결하기 위해 Beacon을 설치하여 RSSI(Received Signal Strength Indication, 신호강도)를 실시간으로 수신하여 **머신러닝(Machine Learning)** 분야와의 응용을 통해 실내 위치 측위 오차를 개선하는 것입니다. 또한, 최근들어 **증강현실(Augmented Reality, AR)** 기술이 비약적으로 발전하면서 사용자들에게 많은 서비스를 제공하고 있음에 따라 증강현실을 이용하여 실내에서의 다양한 서비스를 제공하는 응용 소프트웨어를 구현하였습니다.  

[SourceCode][sourceCode] 👈 Click here  
👉 Unity Project File + Server(java) File + AAR plugin + TensorFlow Model + Deep Learning(python) code  

<br>
<br>

### CONFIGURATION ⚡

<div style="text-align : center;">
<img src="{{ '/assets/img/diagram.jpg' }}" style="width: 800px; height: auto; margin-left: auto; margin-right: auto; display: block;">
</div>


위의 그림은 시스템의 전반적인 구성과 흐름을 **Block Diagram** 형태로 나타낸 것입니다.

<br>

<img src="{{ '/assets/img/equipment.jpg' }}" style="width: 800px; height: auto; margin-left: auto; margin-right: auto; display: block;">

BLE Beacon을 제작하기 위해 HM-10 모듈만을 따로 구매하여 제작하였고 아두이노를 통하여 환경설정을 하였습니다. 블루투스 신호를 수신하기 위하여 Android 기반의 Samsung Galaxy S7 Edge 모델을 사용하였습니다.

<br>

<img src="{{ '/assets/img/kalmanfilter.jpg' }}" style="width: 500px; height: auto; margin-left: auto; margin-right: auto; display: block;">

스마트폰에서 수신되는 블루투스의 신호 강도가 얼마나 불규칙적인지 알아보기 위하여 간단한 Application을 구현하여 테스트하였습니다. 신호를 **안정**시키기 위하여 대중적으로 사용되는 **칼만 필터(Kalman-Filter)**를 적용하여 대조한 결과입니다.

<br>

<img src="{{ '/assets/img/data.gif' }}" style="width: 600px; height: auto; margin-left: auto; margin-right: auto; display: block;">

실시간으로 신호의 세기가 받아지는 것을 확인할 수 있습니다. Unity에서 블루투스 접근 권한 등의 **Native 안드로이드 기능들**을 사용하기 위하여 안드로이드 스튜디오에서 **JAR**파일을 추출하여 Unity에서 **plugin** 형식으로 사용할 수 있도록 구현하였습니다.

<br>

<img src="{{ '/assets/img/dnn.jpg' }}" style="width: 700px; height: auto; margin-left: auto; margin-right: auto; display: block;">

**Deep Learning**은 **Machine Learning**의 한 분야로, **인공신경망(Neural Network)**을 기초로 하고 있습니다. 인공신경망은 사람의 신경망 원리와 구조를 모방하여 만든 **기계학습 알고리즘**입니다. 인공신경망은 기본적으로 **입력층(Input Layer)**, **은닉층(Hidden Layer)**, **출력층(Output Layer)**, 총 세 개의 계층으로 구성되어 있습니다. 그 중, 은닉층이 Deep하고 Wide하다는 특성을 하지고 있는 **Deep Neural Network(DNN)** 구조를 이용하였습니다. **수치예측**, 분류, 문자인식 혹은 이미지 트레이닝 같은 분야에서 **장점**이 있습니다. But, 신경망이 복잡할수록 학습 시 많은 시간이 소요되며, 결과 해석이 어렵다는 단점이 있습니다.  

**Code의 일부분 (DNN 관련)**
```python
import tensorflow as tf  
#중략···
W1 = tf.get_variable("W1", shape=[4, 128], initializer=tf.contrib.layers.variance_scaling_initializer())  
W2 = tf.get_variable("W2", shape=[128, 128], initializer=tf.contrib.layers.variance_scaling_initializer())  
W3 = tf.get_variable("W3", shape=[128, 128], initializer=tf.contrib.layers.variance_scaling_initializer())  
W4 = tf.get_variable("W4", shape=[128, 128], initializer=tf.contrib.layers.variance_scaling_initializer())  
#중략···
L1 = tf.nn.relu(tf.matmul(X, W1))  
L1 = tf.nn.dropout(L1, keep_prob)  
L2 = tf.nn.relu(tf.matmul(L1, W2))  
L2 = tf.nn.dropout(L2, keep_prob)
#중략···
```

<br>

<img src="{{ '/assets/img/socket.gif' }}" style="margin-left: auto; margin-right: auto; display: block;">

**Client**에서 수신된 신호 세기 값들을 **Server**로 전송하면 **Deep Learning**을 통하여 생성된 **학습 모델**을 통하여 좌표 값을 계산해 다시 **Server**에서 **Client**에게 Data를 전송하는 것을 확인할 수 있습니다.

<br>

<img src="{{ '/assets/img/grid.jpg' }}" style="width: 630px; height: auto; margin-left: auto; margin-right: auto; display: block;">

<br>

<img src="{{ '/assets/img/3dmodel.jpg' }}" style="width: 630px; height: auto; margin-left: auto; margin-right: auto; display: block;">

<br>

<img src="{{ '/assets/img/unity3d.jpg' }}" style="width: 630px; height: auto; margin-left: auto; margin-right: auto; display: block;">


건물을 **Grid**한 구역으로 나누고 셀마다 좌표를 설정하였습니다. **SketchUp** Tool을 사용하여 실제 환경과 최대한 동일하게 3D Model을 생성하였으며, **Unity**에서 해당 모델을 활용하였습니다.  

<br>
<br>

### DISCUSSION ✍

Deep Learning 학습 모델을 생성하기 위하여 많은 양의 Data가 필요하였습니다. 각 셀마다 약 60개의 블루투스 신호 세기들을 수집하였고 총 약 3만개의 데이터를 수집하였습니다. 중복되었거나 불안정한 데이터들을 처리하는 과정을 통하여 약 1만개 정도로 감소하였습니다.

더 정확한 위치 측위를 위해서는 몇 가지 개선점이 필요하다고 생각됩니다. 각 좌표마다 약 500개씩으로 데이터를 수집하였다면 기존의 데이터에 비해 약 5배의 데이터를 학습시킬 수 있으므로 더 정확한 결과 값이 나왔을 것으로 생각됩니다. 또한, 3D Model을 줄자와 같은 측정 도구를 통해 단위를 측정하며 생성하였다면 보다 양질의 AR 서비스를 이용할 수 있었을 것으로 생각합니다.

위의 프로젝트를 보완하여 사용한다면 비용이 저렴하고 설치가 용이한 Beacon을 이용하여 다양한 실내 위치 서비스를 AR 형식으로 제공하기 때문에 사용자들의 편의성을 극대화할 수 있을 것입니다.  

<br>
<br>
<br>

<script src="https://utteranc.es/client.js"
        repo="DCherish/DCherish.github.io"
        issue-term="pathname"
        theme="boxy-light"
        crossorigin="anonymous"
        async>
</script>

[sourcecode]: https://github.com/DCherish/G-Project