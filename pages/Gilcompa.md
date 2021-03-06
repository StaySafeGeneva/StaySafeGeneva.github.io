---
layout: page
title: Getting started
subtitle:
---

An exploratory analysis has been done in order to understand better and get a general overview of the Geneva accidents.


## When does the accidents happen?
All the news evoque to an increase of accidents during last years. The evolution of number of accidents from 2010 to 2016 in Geneva shows that from 2012 to 2014 there has been a **strong increase**, however it has been stabilized during the last two years.

> ### In 2015, there were 66 accidents per week

![Image](../img/acc_year.png)

The **months of the year with more accidents** are March, June, September and October. This coincide with the holidays start or the holidays ending. It can also be observed that in average, there are **more accidents at the end of the year**.

But when is the day of the week with more number of accidents in average? From Monday to Thursday we observe that there is the same amount of accidents in average. Let's check which day of the week there are more accidents:

![Image](../img/acc_weekday.png)
> ### **Be careful** on Friday!

<br>
<br>


## Is there the same risk during the morning and the evening?
It is known that the traffic is more dense in the morning or in the afternoon, when people go or come back home. We observe that it also correlated with the number of accidents.
> ### The time of the day you may be more aware is at 17h

![Image](../img/acc_hour.png)

<br>
<br>


## Which are the more recurrent type of accident and when?
> ### Drift, Traffic jam collision and Parking accidents are the accident group with more ocurrence.

![Image](../img/acc_gr.png)

The number of accidents during the day is larger than during the night. However, the number of **drifting accidents** is nearly the same during the day than during the night. In addition, it is observed on the data that **speed is one of the main causes of the accidents at night**.

#### Accidents per day hour
![Image](../img/hour_acc.png)
* Traffic jam collision useally happen at 17h.
* Drift accidents are uniformly distributed during the day.


#### Accidents per weekday
![Image](../img/day_acc.png)
* Most of drift accidents are during the weeknd!
* Traffic jam collison mostly happen on Friday.


#### Accidents per season
![Image](../img/season_acc.png)
* The number of accidents during the summer decrease a lot.
* There is a huge amount of drift accidents during winter due to the slippery conditions.

<br>
<br>

## Can be all the accidents classified equally?
Depending the consequence of the accident, it can be classified as **Mortal, Severe, Mild and Unknown**. Let's check how the split is done comparing the accident group and the consequences:
![Image](../img/acc_gr_con.png)
* **Drifting accidents** and **accidents involving pedestrian** are **the most mortal**.
* **Traffic jam's collision accidents** and **drifting accidents** are the ones with more severe consequenses.
* Tha amount of **accidents involving pedestrian** with severe consequences is considerable.

> ### From the conequences point of view, accidents involving pedestrians are also relevant

<br>
<br>


## What are the main causes of the three more important accidents?
![Image](../img/acc_gr_causeg.png)
* **Drifting accidents** are mainly caused by the driver state or distraction. In addition, the speed is the third cause for this kind of accidents.
* One of the main causes of the accidents involving pedestrian is the pedestrian attitude itself.
* For all the three accidents type, the driver or inattention of the driver is an important cause.

> ### The momentary innatention represents the 29% (40 accidents per month) of the total number of accidents of three main accident groups. Alcohol influence represents the 17% (23 accidents per month).

<br>
<br>

## Have the number of accidents due to the alchool influence increased during last years?
{% include num_consequences.html %}
> ### It is not observed an evolution on the accidents consequence during the last years, hence the increase of the number of accidents. 

<br>
<br>


## Which is the accident group with more ocurrences for each mean of transport?
The more populated vechicles are Tourism. So let's investigate it alone.
![Image](../img/tourism_transp.png)
> ### If you drive a car, it more probable to have a traffic jam collision than a drift accident. 


Then, the other trasnports are summerized in the following plot:
![Image](../img/other_transp.png)
* For heavy transports, the more recurrent accidents are: take over accidents and traffic jam collisions.
* For motorbikes, the more common accident is the drifting accidents. The second more recurrent accident is by leaving a road.

> ### The more recurrent accident for public transport is those involving pedestrians!
