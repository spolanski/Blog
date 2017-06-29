---
layout: post
title: "A word about skateboarding [Part 1/3]"
categories: Daily Physics
tags: [FEA, simulation]
comments: true
categories: Personal
image:
  feature: skate.jpg
  teaser: skate-teaser.jpg
  credit:
  creditlink:
---

Skateboarding was one of my favourite sports when I was younger. It has changed my life so much that I even wrote a Bachelors Thesis about it. In this thesis, I tried to analyse what is happening with a skateboard deck when a skater lands on it. Looking back in time, I feel that picking this particular topic was a really good move. I was at the very beginning of the simulation learning curve and each tiny step towards my goal took ages. However, having practical experience in skateboarding helped me more than I would have imagined. First of all, I knew where the skateboard usually breaks so it was easier to understand the results. Secondly, I felt like I was contributing somehow to the development of skateboarding and that gave me a lot of satisfaction.

The simulation of skateboard is such a nice example of situation when hobby meets engineering that I decided to present it in my first blog. Unfortunately, I cannot use the model I built for Bachelors Thesis purposes as it was created in software that I currently don't have access to. I created new one in Abaqus Student version which is available free of charge to students, educators, and researchers for personal and educational use - I believe the educational blog fits well to these requirements.

## Rectangular specimen experiment
When I started to build the numerical model for thesis purposes, I knew that skateboard deck is a lamina made from Canadian Maple (usually 7-9 plies). The fact that it is a type of material I had not analyse before made my situation a bit problematic. For that reason, I decided to build a model of rectangular specimen at first to see how it behaves. Luckily, I found an old skateboard at home - that allows me to make an experiment on real piece of lamina. The photo was taken during the test performed in professional laboratory built from a home gym set :-) .

{% capture imagesrc %}00_skate/testing_station.jpg{% endcapture %}
{% capture imagetitle %}Testing station{% endcapture %}
<a href="{{site.url}}{{site.baseurl}}/assets/images/{{ imagesrc }}">{% picture post_landscape {{ imagesrc }} alt="{{ imagetitle }}" title="{{ imagetitle }}" %}</a>
{: .center-image }

The main idea of the experiment was to check the displacement under the given loading. I performed the measurements using a ruler, so the obtained data were probably not as accurate as it should. However, the rough results were enough to know if my numerical model, which I was about to build, would be near to acceptable.
Before I moved to model creation process, I had to find material properties which are crucial in Finite Element Analysis. At that stage, I found a very useful Wood Handbook with Canadian Maple material data (it can be found here https://www.fpl.fs.fed.us/documnts/fplgtr/fpl_gtr190.pdf). Using the data from this resource, I built a shell specimen in Abaqus and I applied the lamina material model to it. After that, I put appropriate restrains and loads to imitate real behaviour of the sample. The results from experiments are presented below.

{% capture imagesrc %}00_skate/Result_F_U.png{% endcapture %}
{% capture imagetitle %}Abaqus results{% endcapture %}
<a href="{{site.url}}{{site.baseurl}}/assets/images/{{ imagesrc }}">{% picture post_landscape {{ imagesrc }} alt="{{ imagetitle }}" title="{{ imagetitle }}" %}</a>
{: .center-image }

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

{% capture imagesrc %}00_skate/TestComparison.png{% endcapture %}
{% capture imagetitle %}Results comparison{% endcapture %}
<a href="{{site.url}}{{site.baseurl}}/assets/images/{{ imagesrc }}">{% picture post_landscape {{ imagesrc }} alt="{{ imagetitle }}" title="{{ imagetitle }}" %}</a>
{: .center-image }

