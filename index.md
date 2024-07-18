---
layout: default
---
# A Plugin-based Paradigm for Practical Vehicle Road Cooperative Perception

## Abstract

<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    .content {
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    .content img {
      width: 200%;
      max-width: 500px;
      height: auto;
      margin-bottom: 10px; /* Adjust the margin as needed */
    }
    .content p {
      margin-top: 0; /* Remove the top margin to reduce the gap */
      text-align: justify; /* Justify the text */
    }
  </style>
</head>
<body>
  <div class="content">
    <img src="pic/paper/figure1.png" alt="111">
    <p>
      Perception is vital for autonomous driving, and vehicle road cooperation systems based on augmented intelligence of things (AIoT) offer new development opportunities. Vehicle road cooperative perception can significantly enhance the perception capabilities of vehicles through information aggregation. However, existing methods use an end-to-end paradigm, which suffers from complex models and high training costs, and is difficult to implement due to the involvement of different vendors. Therefore, we explore a plugin-based cooperative paradigm that inserts cooperation modules into vehicle perception models, reducing trainable parameters and easing implementation. Based on the Plugin-based paradigm, we develop a Cooperative 3D Object Detection framework called PC3DOD, using object queries as transmitted features. The road model employs a temporal transformer decoder to enhance modeling, while the ego-vehicle uses a domain-aware fusion module to merge queries effectively. They both contribute to achieving high performance. To address communication latency, we introduce a tracking-prediction module to align delayed roadside queries with vehicle ones. Experiments on V2X-Seq and V2X-Sim demonstrate that the plugin-based paradigm enables cooperation. PC3DOD achieves leading performance on V2X-Seq with a few trainable parameters compared to existing methods. Thanks to the domain-aware fusion module, PC3DOD can cooperate with various roadside models, showcasing its flexibility. Results under different communication settings confirm the framework's robustness to latency. Results on V2X-Sim indicate that PC3DOD can also be used for vehicle-to-vehicle cooperative perception.
    </p>
  </div>
</body>
</html>
<!--
<div style="display: flex; justify-content: center; align-items: center; height: 500px;">
  <img src="pic/paper/figure1.png" alt="111" style="width: 200%; max-width: 500px; height: auto;"/>
</div>
  Infrastructure sensors installed at elevated positions offer a broader perception range and encounter fewer occlusions. Integrating both infrastructure and ego-vehicle data through V2X communication, known as vehicle-infrastructure cooperation, has shown considerable advantages in enhancing perception capabilities and addressing corner cases encountered in single-vehicle autonomous driving.
However, cooperative perception still faces numerous challenges, including limited communication bandwidth and practical communication interruptions.
In this paper, we propose CTCE, a novel framework for cooperative 3D object detection. This framework transmits queries with temporal contexts enhancement, effectively balancing transmission efficiency and performance to accommodate real-world communication conditions.
Additionally, we propose a temporal-guided fusion module to further improve performance. The roadside temporal enhancement and vehicle-side spatial-temporal fusion together constitute a multi-level temporal contexts integration mechanism, fully leveraging temporal information to enhance performance.
Furthermore, a motion-aware reconstruction module is introduced to recover lost roadside queries due to communication interruptions.
Experimental results on V2X-Seq and V2X-Sim datasets demonstrate that CTCE outperforms the baseline QUEST, achieving improvements of $3.8\%$ and $1.3\%$ in mAP, respectively. Experiments under communication interruption conditions validate CTCE's robustness to communication interruptions.
-->

## Method

  ![img](pic/paper/figure2.png)

## Results
coming soon...

<!--
# 3. Experiments

## 1) Experiments details

<div style="display: flex; justify-content: center; align-items: center; height: 500px;">
  <img src="pic/paper/5.png" alt="555" style="width: 200%; max-width: 500px; height: auto;"/>
</div>


## 2) Baseline Compare

<div style="display: flex; flex-direction: row; justify-content: center;">
  <figure style="display: flex; flex-direction: column; align-items: center; margin-bottom: 20px; height: 400px;">
    <img src="pic/baseline/cv.gif" alt="1" style="width: 350px; height: auto;"/>
    <figcaption>Physical-based</figcaption>
  </figure>
  <figure style="display: flex; flex-direction: column; align-items: center; margin-bottom: 20px; height: 400px;">
    <img src="pic/baseline/grip.gif" alt="2" style="width: 350px; height: auto;"/>
    <figcaption>GRIP++</figcaption>
  </figure>
  <figure style="display: flex; flex-direction: column; align-items: center; margin-bottom: 20px; height: 400px;">
    <img src="pic/baseline/walenet.gif" alt="3" style="width: 350px; height: auto;"/>
    <figcaption>WaleNet</figcaption>
  </figure>
</div>

<div style="display: flex; flex-direction: row; justify-content: center;">
  <figure style="display: flex; flex-direction: column; align-items: center; margin-bottom: 20px; height: 400px;">
    <img src="pic/baseline/t.gif" alt="1" style="width: 350px; height: auto;"/>
    <figcaption>Trajectron++</figcaption>
  </figure>
  <figure style="display: flex; flex-direction: column; align-items: center; margin-bottom: 20px; height: 400px;">
    <img src="pic/baseline/tp.gif" alt="2" style="width: 350px; height: auto;"/>
    <figcaption>POP</figcaption>
  </figure>
</div>




## 2) Planning performance

### a) Non-reactive

<div style="display: flex; flex-direction: row; justify-content: center;">
  <figure style="display: flex; flex-direction: column; align-items: center; margin: 0 20px 20px 0; height: 400px;">
    <img src="pic/case/bgr.gif" alt="1" style="width: auto; max-width: 100%; height: auto; margin-bottom: 10px;"/>
    <figcaption></figcaption>
  </figure>
  <figure style="display: flex; flex-direction: column; align-items: center; margin: 0 20px 20px 0; height: 400px;">
    <img src="pic/case/d.gif" alt="2" style="width: auto; max-width: 100%; height: auto; margin-bottom: 10px;"/>
    <figcaption></figcaption>
  </figure>
  <figure style="display: flex; flex-direction: column; align-items: center; margin: 0 0 20px 0; height: 400px;">
    <img src="pic/case/sind.gif" alt="3" style="width: auto; max-width: 100%; height: auto; margin-bottom: 10px;"/>
    <figcaption></figcaption>
  </figure>
</div>

<div style="display: flex; flex-direction: row; justify-content: center;">
  <figure style="display: flex; flex-direction: column; align-items: center; margin-bottom: 20px; height: 400px;">
    <img src="pic/case/usa.gif" alt="1" style="width: 350px; height: auto;"/>
    <figcaption></figcaption>
  </figure>
  <figure style="display: flex; flex-direction: column; align-items: center; margin-bottom: 20px; height: 400px;">
    <img src="pic/case/zam-t.gif" alt="2" style="width: 350px; height: auto;"/>
    <figcaption></figcaption>
  </figure>
  <figure style="display: flex; flex-direction: column; align-items: center; margin-bottom: 20px; height: 400px;">
    <img src="pic/case/zam-zip.gif" alt="3" style="width: 350px; height: auto;"/>
    <figcaption></figcaption>
  </figure>
</div>


### b) Reactive

<div style="display: flex; flex-direction: row; justify-content: center;">
  <figure style="display: flex; flex-direction: column; align-items: center; margin-bottom: 20px;">
    <img src="pic/case/usa-int.gif" alt="1" style="width: 350px; height: auto;"/>
    <figcaption></figcaption>
  </figure>
</div>


-->
