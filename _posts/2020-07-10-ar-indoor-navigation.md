---
layout: page
title:  "AR Indoor Navigation"
subtitle: "A service application when someone is indoors by using AR tech"
date:   2020-07-10 11:11:11 +0530
categories: ["project"]
---
<p align="middle"><iframe width="759" height="480" src="https://www.youtube.com/embed/NvaQYQSHGWI" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></p>

*총 두 가지의 영상이 차례로 재생됩니다.*  

*영상 1 : 좌측 상단의 메뉴 버튼의 Direction 버튼을 클릭하여 현재 내가 어디에 위치해 있는지 알 수 있습니다. 우측 상단의 목적지 버튼을 클릭하면 안내 받을 수 있는 영역이 빨간색으로 표시됩니다. 원하는 지역을 클릭하면 해당 목적지까지 화면을 통해 안내를 받을 수 있습니다. 사실감 있게 표현하기 위해 AR 물체가 벽에 가려졌을 경우 가려져서 보이지 않도록 Stencil Shader & Mask 기법을 적용하였습니다. Map을 더욱 정교히 구현하고 신호의 오차를 정교히 핸들링한다면 더욱 사실감 있는 AR 서비스를 구현할 수 있겠습니다.*  

*영상 2 : 현재의 위치는 카메라와 블루투스 신호를 통해 계산됩니다. 카메라를 가리고 Random한 위치로 움직입니다. 도착한 후 메뉴 버튼의 Scan 버튼을 통해 현재의 위치가 정상적으로 계산되는지, 기타 다양한 기능들이 정상적으로 작동하는지를 테스트하는 영상입니다.*  

<br>

최근 소비자들의 편리성을 증대시키기 위하여 실내 위치 측정에 관한 다양한 연구가 진행되고 있습니다. 단순히 무선 신호에 기반한 측위 시스템에서는 송수긴기 사이의 전파 경로가 물체들로 인하여 가려지거나, 다른 환경적인 요인들로 인한 신호의 정확성 문제가 발생하기 때문에 무선 신호만을 이용하여 정확한 실내 위치를 도출하는 것에는 한계가 존재합니다. 즉, **BLE(Bluetooth Low Energy) Beacon**만을 이용하여 실내 위치 측위를 하는 방법들은 대부분 정확성이 떨어지기에 실제로 사용함에 있어서 한계가 존재합니다. 본 프로젝트의 목적은 위에서 발생한 문제점들을 해결하기 위해 Beacon을 설치하여 RSSI(Received Signal Strength Indication, 신호강도)를 실시간으로 수신하여 **머신러닝** 분야와의 응용을 통해 실내 위치 측위 오차를 개선하는 것입니다. 또한, 최근들어 **증강현실** 기술이 비약적으로 발전하면서 사용자들에게 많은 서비스를 제공하고 있음에 따라 증강현실을 이용하여 실내에서의 다양한 서비스를 제공하는 응용 소프트웨어를 구현하였습니다.

[SourceCode][sourceCode] 👈 Click here

<img src="{{ '/assets/img/diagram.jpg' }}">

*위의 그림은 시스템의 전반적인 구성과 흐름을 Block Diagram 형태로 나타낸 것입니다.*  

<br>

<img src="{{ '/assets/img/equipment.jpg' }}">

*BLE Beacon을 제작하기 위해 HM-10 모듈만을 따로 구매하여 제작하였고 아두이노를 통하여 환경설정 하였습니다. 블루투스 신호를 수신하기 위하여 Android 기반의 Samsung Galaxy S7 Edge 모델을 사용하였습니다.*  

<br>

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

[sourcecode]: https://github.com/DCherish/G-Project
