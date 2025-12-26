---
title: "Tap & Drill Question Generator (Python) (UNDER CONSTRUCTION)"
date: 2025-12-26
layout: single
header:
  overlay_image: /assets/images/dml-engine-cnc/DML_CNC_CornerAngle.JPG
  overlay_filter: 0.4
excerpt: "This project uses Python to automatically generate realistic practice problems for tap and drill charts—covering standard and metric fasteners, hole callouts, and depths—to help DML students better understand and practice threaded hole design concepts."
classes: wide
read_time: 3
exclude_code_from_readtime: true

gallery_DML_CNC_engine:
  - image_path: /assets/images/dml-engine-cnc/DML_CNC_CornerAngle.JPG
    title: "Air Engine Corner View"
    url: https://ryanoceros19.github.io/truong-website/assets/images/dml-engine-cnc/DML_CNC_CornerAngle.JPG
  - image_path: /assets/images/dml-engine-cnc/DML_CNC_FrontAngle.JPG
    title: "Air Engine Front View"
    url: https://ryanoceros19.github.io/truong-website/assets/images/dml-engine-cnc/DML_CNC_FrontAngle.JPG
  - image_path: /assets/images/dml-engine-cnc/DML_CNC_TopDown.JPG
    title: "Air Engine Top View"
    url: https://ryanoceros19.github.io/truong-website/assets/images/dml-engine-cnc/DML_CNC_TopDown.JPG
---

In Design & Manufacturing Lab (DML), students are taught how to use a tap and drill chart. The chart they use is given below.

***INSERT TAP AND DRILL CHART PDF HERE***

Depending on the material and fastener size, a different thread pitch and tap drill size is needed in order to make a tapped hole. Students are often tested on this topic but very few practice problems are provided to students.

I have spent the past couple months, on and off, developing code to automatically generate sample questions. I chose to program this in python due to its simple syntax and popularity amongst beginner coders. Even without a computer science background, it can be fairly easy to follow. Even with confusion, AI can easily understand the python logic and be used to help user who wish to explore the code logic.

I first input the standard tap and drill values into code. With the help of AI, I developed a format to store the values in a convenient manner. Then I began writing the logic for the first option which asked for a tap drill size for a given fastener and material. This was Version 1 and was sent out to students.

I then wrote the logic for the second option. This option asks for the entire hole callout given the fastener size, material, and number of holes. This version was not sent to students, but several fellow DML TAs had tested this functionality.

For Version 3, I input the metric tap and drill values into code, again using AI to help develop a useful format to store the values. Then I wrote the third and fourth options which were the same as option 1 & 2 but for the metric values. Halfway through, I realized that options 1 & 3 and 2 & 4 had very similar logic structures, so I wrote functions to remove the repeated logic. The use of functions made options 5 & 6 very easy to implement. Option 5 generates a tap drill question for a standard or metric fastener while option 6 generates a hole callout question for a standard or metric fastener.

Currently, the hole callout questions assume that the holes are through holes. For Version 4, I plan to randomly generate a hole depth so that students can practice identifying tap drill depths and tap depths. Many students make the mistake on exams of drilling to the same depth as the tap. I hope that Verson 4 can reinforce the rule of thumb taught in DML: the the tap drill depth should be the tap depth plus one fastener diameter. For example, if I wanted thread for a 1/4" fastener to be 0.5" deep, then the tap drill should be drilled 0.75" deep.
