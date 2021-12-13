---
layout: about
title: about
permalink: /
description: Postdoc reseacher in Department of Informatics in <a href="https://mlr.in.tum.de/members">Technical University of Munich</a>.

profile:
  align: right
  image: xingxingzuo.jpg

news: true  # includes a list of news items
selected_papers: false # includes a list of papers marked as "selected={true}"
social: true  # includes social icons at the bottom of the page

years: [2021, 2020, 2019, 2018]
---

I'm currently a Postdoc Researcher in [Smart Robotics Lab](https://mlr.in.tum.de) at the Department of Informatics, Technical University of Munich, working with [Prof. Stefan Leutenegger](https://www.professoren.tum.de/en/leutenegger-stefan). Previously, I was an academic guest (2019 - 2021) in [Computer Vision and Geometry Group](https://cvg.ethz.ch/) (CVG), ETH, Zurich, Switzerland, working with [Prof. Marc Pollefeys](http://people.inf.ethz.ch/pomarc/). I was also a visiting scholar (2018)in the [Robot Perception and Navigation Group](http://sites.udel.edu/robot) (RPNG) of [Guoquan (Paul) Huang](https://udel.edu/~ghuang/) at University of Delaware, Newark, USA, and a visiting scholar (2017) in the [UTS Robotics Institute](https://www.uts.edu.au/research/robotics-institute), University of Technology Sydney, Australia, working with [Prof. Teresa Vidal Calleja](https://profiles.uts.edu.au/Teresa.VidalCalleja). I got my doctoral degree from Department of Control Science and Engineering in [Zhejiang University](https://www.zju.edu.cn/english/), China, and graduated with honors in 2021. Before that, I graduated with honors and obtained my Bachelor's degree in mechanical engineering in [University of Electronic Science and Technology of China](https://en.uestc.edu.cn/) (UESTC), Chengdu, China, in 2016.


I'm always open to collaboration about cutting-edge research on robot perception and intelligence, feel free to reach out through email:[xingxing.zuo@tum.de](mailto:xingxing.zuo@tum.de)!

---

<div class="post">

  {% if page.news %}
    {% include news.html %}
  {% endif %}

</div>

---

## __research interests__

My research interests include robotic perception, 3D computer vision, probabilistic multi-sensor fusion, visual-inertial navigation, state estimation, and dense mapping.  I'm conducting researches on integrating the intelligence of deep neural networks and the traditional probabilistic methods for robot perception tasks.

---

{: #publications}
## __publications__

{% for y in page.years %}
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}
