---
layout: post
title: ContextMenuType| SfSchedule | Wpf | Syncfusion
description: This section explain about how to use contextmenutype of Syncfusion WPF Scheduler control and more details. 
platform: wpf
control: SfSchedule
documentation: ug
---

# ContextMenuType of WPF SfSchedule

The collection of MenuItem elements can be organized by ContextMenuType property.
{% tabs %}
{% highlight html %}



	<Schedule:SfSchedule x:Name="schedule"   ScheduleType="Week" ContextMenuType="RadialMenu">

	</Schedule:SfSchedule>

{% endhighlight  %}


{% highlight c# %}



SfSchedule schedule = new SfSchedule();

schedule.ScheduleType = ScheduleType.Week;

schedule.EnableTouch = true;  

this.grid.Children.Add(schedule);



{% endhighlight  %}
{% endtabs %}

![ContextMenuTypeimg1](ContextMenuType_images/ContextMenuType_img1.png)



![ContextMenuTypeimg2](ContextMenuType_images/ContextMenuType_img2.png)





