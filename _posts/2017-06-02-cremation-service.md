---
layout: post
type: portfolio
title:  "Cremation Services of Florida"
date:   2017-06-02
start: 2016-04-05
end: 2017-07-03
image: /images/cremation/user_profile.png
url: https://cremationservices.com/
excerpt: "Cremation Service of Florida is a pre- and at-need cremation arrangement service for families."
tag:
- portfolio
- php 
- ajax
- javascript
- database design
- mysql
- zurb foundation
---

<a href="{{ site.global.data.baseurl }}/images/cremation/user_profile.png"><img src="{{ site.global.data.baseurl }}/images/cremation/user_profile.png" class="thumbnail" alt="Home Page of RenewNow CEU"></a>  
<center><b><a>Cremation Service of Florida</a></b> is a pre- and at-need cremation arrangement service for families.</center><br>

## Project Summary
Cremation Service of Florida is a pre- and at-need cremation arrangement service for families. A member can arrange a cremation for for themselves or someone else for a death that has already occurred or beforehand. Each arrangement is assigned to an agent as a case and they are responsible for communications and verification of identities, etc.

There are four user types in this web app:
1. Admin is super-user and has access to all cases, staff, and user accounts for management purposes.
1. Managers have access to staff and cases.
1. Agents and assistants have access to the cases they're assigned.
1. Users can create and manage arrangements they create, as well as be invited to other arrangements for viewing important information and making payments on pre-arranged services.

I was the sole developer for this project and was responsible for every aspect of front- and back-end functionality. I chose to use Zurb's Foundation for theming, as the project had many reusable components and uses for modals, form validation, menus, and other standard components. I crafted nearly every function and database table from scratch for this project, improving on our older projects by implementing higher standards and best practices. 

### Role:
---
 - Lead Developer

### Responsibilities:
--- 

1. Design database schema
1. Design logic for determining stages of arrangements
1. Develop round robin algorithm for assigning cases to agents
- Agents are skipped if they are taking time off
- If a user already belongs to an arrangement and creates a new one, the agent for the first is assigned the new case
1. Create admin portal to manage users, staff, cases, orders, etc.

#### Above & beyond
In addition to what I was required to do, I...
* Implemented Bcrypt for password encryption
* Used AJAX for many features (inviting family members, adding notes, saving records, updating statuses, etc.) to improve user experience
* Used modals for improved user experience

### Unique parts
* Pre-need arrangements, which can be paid for over time
* Round-robin case assignment
* Statuses of arrangement

### What I learned
- I now understand how array_map works :D
- Data is complex
- Working alone is hard

## Conclusion
This project was very complex and quite difficult. I enjoyed the many challenges that required me to research and learn new practices, but I wish I had been able to work on a team for this. Working with vanilla, functional PHP instead of a framework or OOP made this project increasingly difficult as the project grew in size, so I had to be creative and intentional in abstracting reusable components, assets, and functions.
 
Overall, I'm happy with the results, as I was able to focus a great deal of time and effort on this project. It wasn't easy, but it was fun.

## Preview

{% capture images %}
	{{ site.global.data.baseurl }}/images/cremation/arrange_1.png
	{{ site.global.data.baseurl }}/images/cremation/arrange_2.png
	{{ site.global.data.baseurl }}/images/cremation/gpl_agreement.png
{% endcapture %}
{% include gallery images=images caption="Users are guided through a series of questions to determine the type of arrangement" cols=3 %}

{% capture images %}
	{{ site.global.data.baseurl }}/images/cremation/user_dashboard.png
	{{ site.global.data.baseurl }}/images/cremation/user_profile.png
{% endcapture %}
{% include gallery images=images caption="Users have a dashboard displaying each arrangement they're a part of and can view the arrangement details" cols=2 %}

{% capture images %}
	{{ site.global.data.baseurl }}/images/cremation/obituaries.png
	{{ site.global.data.baseurl }}/images/cremation/obituary_new.png
	{{ site.global.data.baseurl }}/images/cremation/obituary_comment.png
{% endcapture %}
{% include gallery images=images caption="Obituaries can be viewed and edited (by users with permissions), and anybody can comment (comments are reviewed by agents before publishing)" cols=3 %}

{% capture images %}
	{{ site.global.data.baseurl }}/images/cremation/agent_dashboard.png
	{{ site.global.data.baseurl }}/images/cremation/agent_user_profile.png
	{{ site.global.data.baseurl }}/images/cremation/agent_update_status.png
{% endcapture %}
{% include gallery images=images caption="Agents can view and edit the cases they're assigned, as well as set statuses, make notes, and upload documents" cols=3 %}