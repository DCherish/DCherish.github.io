---
layout: page
title:  "AR Indoor Navigation"
subtitle: "A service application when someone is indoors by using AR tech"
date:   2020-07-10 11:11:11 +0530
categories: ["project"]
---
<p align="middle"><iframe width="759" height="480" src="https://www.youtube.com/embed/NvaQYQSHGWI" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></p>


최근 소비자들의 편리성을 증대시키기 위하여 실내 위치 측정에 관한 다양한 연구가 진행되고 있다. 단순히 무선 신호에 기반한 측위 시스템에서는 송수긴기 사이의 전파 경로가 물체들로 인하여 가려지거나, 다른 환경적인 요인들로 인한 신호의 정확성 문제가 발생하기 때문에 무선 신호만을 이용하여 정확한 실내 위치를 도출하는 것에는 한계가 존재한다. **BLE(Bluetooth Low Energy) Beacon**을 이용하여 실내 위치 측위를 하는 방법들은 대부분 정확성이 떨어지기에 실제로 사용함에 있어서 한계가 존재한다. 본 프로젝트의 목적은 위에서 발생한 문제점들을 해결하기 위해 Beacon을 설치하여 RSSI(Received Signal Strength Indication, 신호강도)를 실시간으로 수신하여 **머신러닝** 분야와의 응용을 통해 실내 위치 측위 오차를 개선하는 것이다. 또한, 최근들어 **증강현실** 기술이 비약적으로 발전하면서 사용자들에게 많은 서비스를 제공하고 있음에 따라 증강현실을 이용하여 실내에서의 다양한 서비스를 제공하는 응용 소프트웨어를 구현하였다.

[SourceCode][sourceCode]

<img src="{{ '/assets/img/diagram.jpg' }}">

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

[sourcecode]: https://github.com/DCherish/G-Project
