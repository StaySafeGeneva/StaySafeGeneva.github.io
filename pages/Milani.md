---
layout: page
subtitle: Visualization of the accidents in the canton of Genève from 2010 to 2016
---

{% include main_causes_ALL.html %}

The dataset in our possess is
- not big (20K data point, of which 9K localized in the center of Genève)
- with a lot of features, all possibly worth of attention (daytime of the accident, cause, sub-cause, vehicle involved, consequences, etc.etc.)

While a choropleth map could be a possible option to visualize this dataset, we decided not to aggregate the data in such a way. Aggregating data in a choropleth map, even with really small regions, would have make the micro-patterns typical of this dataset disappear. By plotting each data point and letting the user the possibility to zoom in/out, we are able to fully exploit our data at every scale: from the analysis of the single crossroad to the analysis of the entire center of Geneva. Of course this is possible given the relatively small size of our dataset. On the other hand, to make clusters appear we need a certain amount of data; we opted then to consider all the accidents in pur dataset, from 2010 to 2016.

Let's have a look at our data!

First, let' visualize our datapoints

{% include  all_accidents_canton_datashade_small.html %}

We this first visualization we can already identify the roads with the most accidents: it easy to recognize that the most accidents happen in the following zones:
- close to the Railway station
- close to the main bridge of Geneve: Le Pont du Mont Blanc.

In the next analysis we'll tell the sad story of the Pont du Mont Blanc. Ready to start? Let's go!

{% include main_causes.html %}

Using the data from section --- we plotted the accidents relative to the 4 main causes of accidents  in the canton of Geneve:
- accidents par tamponament
- accidents par derapage ou perte de maitrise
- accidents impliquant des pietons
- accident en parquant
We already see different clusters of accidents here: while on the bridge the only cause is "accidents par tamponament", the crossroad north of the bridge is heavily carachterized by "accidents par derapage". Let's now zoom and hover with the mouse on such accidents: 

# INSERT PNG OF THE ZOOM

we'll discover that such accidents are:
- mainly caused by "vitesse" or "influence d'alcool"
- The accidents caused by alcool happened mainly during night time, especially during the weekend

Maybe the amministration could think of lowering the speed limit on this bridge, and increase the controls during the night!

Let's now visualize which accidents happened at night and which ones happened at day time:
{% include day_and_night.html %}
We again see the the accidents that happen north of the brigde du Mont Blanc happend mainly during night time; more in general, we can now recognize that the accidents at night are mailny concentrated on crossroads and on main streets;

Let's now try to focus our attention to only one category of accidents: the accidents involving pedestrians.

{% include pietons.html %}

Now our attention falls on the north-west part of the map: there's an unusual concentration of accidents involving pedestrians in that zone. With a simple zoom, we discover immediately that the center of such distribution could be identified with the train station of Geneve!Again by hovering onto the points, we can see how most of the accidents close to the train station are actually not cause by the drivers, but by the pedestrians themselves, not paying attention, not respecting the traffic lights, and not using the pedestrian crossing. This is understandable if only we think to the usual chaos of pedestrians close to such an important train station; however, another suggestion to the institutions could be sensibilize more the pedestrians close to the train station, and maybe prioritize pedestrian traffic more with special lanes or, in a maybe too optimistic future, special overpasses, to eliminate the problem at the root.

# Conclusions

Similar analysis have proven to be extremely effective: in these examples we were able to completey exploit the data in our possess to efficiently recognize patterns at different lenght-scales. Once discovered such patterns, it could be possible to deepen such analysis by adding more effective interactivity 


### main_causes_old

{% include luca_map_main_causes.html %}

### main_causes_ALL
{% include main_causes_ALL.html %}

### pluie

{% include PLUIE.html %}

### pietons
{% include pietons.html %}

### main_causes
{% include main_causes.html %}

### day_and_night
{% include day_and_night.html %}

### all_accidents_canton_datasade
{% include  all_accidents_canton_datashade.html %}

### all_accidents_canton_datasade_small
{% include  all_accidents_canton_datashade_small.html %}
