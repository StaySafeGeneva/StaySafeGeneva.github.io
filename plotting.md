---
layout: bar_chart
title: test plots
permalink: /plotting/
---

### This is a first test with interactive plots

It is basically just one line to include bokeh plots :)  
For example:

{% include multiple_script_1.html %}

* Red:  

<div class="bk-root">
  <div class="bk-plotdiv" id="3b11fd2c-5135-4b3f-b61f-b277a8176c23"></div>
</div>

* Blue:  
<div class="bk-root">
  <div class="bk-plotdiv" id="d226e774-d805-4ffb-8dcf-6c2e209273d2"></div>
</div>

* Green:  
<div class="bk-root">    
  <div class="bk-plotdiv" id="484cf474-dc5c-47ed-8d67-436856551d94"></div>
</div>

Turn out it is really easy with bokeh, so we will do a second one:

---

### Beautiful texas here I come:
* Texas:  
<div class="bk-root">
  <div class="bk-plotdiv" id="ae0b6e6c-a3fd-4d0c-b9e2-030dd7e7db7f"></div>
</div>



so if Martino find it feasible to redo the maps with bokeh, it will be easy to show them :D

---
The procedure to follow is the following:

1. plot with bokeh as usual (for example declaring figures with ) and have the plots saved variables, say $p_i$.  
For example:
> ``` python
  from bokeh.plotting import figure
  p1 = figure(x_range=xr1, y_range=yr1, plot_width=300, plot_height=300)
  p1.scatter(x1, y1, size=12, color="red", alpha=0.5)
  ```

2. Create a dict with the plots variables (chose yourself the names you like)
For example:
> ``` python
  plots = {'Red': p1, 'Blue': p2, 'Green': p3}
  ```

3. import _components_ : *from bokeh.embed import components*
4. Use components, e.g. :
> ``` python
  script, div = components(plots)
  ```

5. Now the *script* and the *div* are ready to be added in our HTML pages! :D


##### References:

- [bokeh plots on jekyll](https://briancaffey.github.io/2017/01/23/bokeh-plots-on-jekyll.html)  
- [bokeh doc used intensivly](http://bokeh.pydata.org/en/latest/docs/user_guide/embed.html#components)  
- [The Texas interactive plot from bokeh](https://bokeh.pydata.org/en/latest/docs/gallery/texas.html)  
