---
layout: post
type: portfolio
title:  "Doodle Rocks Community"
date:   2018-02-25
start: 2018-01-19
end: 2018-02-25
image: /images/doodle/home.png
url: 'https://doodlerocks.com'
excerpt: "Doodle Rocks is a community of artists, rock finders, and sponsors sharing in the experience of rock painting."
tag:
- portfolio
- php 
- javascript
- algorithms
- facebook api
- mailchimp api
- mysql
- mdb bootstrap
- square connect api
---

<a href="{{ site.global.data.baseurl }}/images/doodle/home.png"><img src="{{ site.global.data.baseurl }}/images/doodle/home.png" class="thumbnail" alt="Home page of Doodle Rocks"></a>  
<center><b><a>Doodle Rocks</a></b> is a community of artists, rock finders, and sponsors sharing in the experience of rock painting.</center><br>

## Project Summary
Doodle Rocks is a new site that aims to bring together the global community of doodle rock painters, explorers, and sponsors. 

Rock painters register and are sent a PDF of generated codes to put on their painted rocks. An explorer finds the rock and enters its code on the Doodle Rocks site and uploads a picture of the rock where they found it. This picture, along with the profile information of the painter and sponsor, is posted to the Doodle Rocks Facebook page using Facebook's Graph API. The system looks for a local or global sponsor who might be sponsoring a giveaway for that rock. If the explorer wins the giveaway, they're sent the winnings via PayPal.

Sponsors can subscribe monthly to have their logo and a promo code show up on the profile of 40 rocks (either locally or globally, depending on their choice). Companies can also choose to sponsor giveaways, the winners being randomly chosen upon entering a rock's code.

I spent a lot of time completely reworking our system to perform all logic before sending a response header. Now, headers can be changed at any point by using a routing/middleware structure. All requests are filtered through a custom request middleware that looks for an action and includes the appropriate file based on the action. I also implemented a validation library (Respect Validation) to validate data server-side.

### Role:
---
 - Lead Developer

### Responsibilities:
--- 

1. Design database schema
1. Develop algorithm for determining giveaway winners
1. Redesign backend system
1. Integrate Mailchimp and Facebook APIs
1. Develop custom e-commerce/subscription services using Square API and cron jobs
1. Produce PDF with variable content

### Unique parts
* Giveaway winners and random sponsor assignments
* Entering a code searches for a rock and its sponsors
* Every entry is posted to Facebook

### What I learned
- Restructuring the system gave me a better understanding of how modern frameworks behave and why they are structured the way they are. A great deal of flexibility comes from separating logic from display.
- Using Facebook's graph API was pretty complicated, but in its implementation, I learned a lot about authentication protocols and redirects/webhooks

## Conclusion
In this project, I put into practice a lot of the major things I've learned throughout other recent projects. I used composer for dependency and library management, rewrote the backend for better request/response handling, and separated logic from display for better error handling. It was fun to use my knowledge of data structures, algorithms, and frameworks to improve the system and make things more efficient.

## Preview

{% capture images %}
	{{ site.global.data.baseurl }}/images/doodle/enter-code.png
 	{{ site.global.data.baseurl }}/images/doodle/rock-profile.png
{% endcapture %}
{% include gallery images=images caption="The fulcrum of the community is the entries of found rocks. An explorer finds a rock, enters its code, posts a photo, and sees the rock's profile." cols=2 %}

{% capture images %}
	{{ site.global.data.baseurl }}/images/doodle/become-a-painter.png
	{{ site.global.data.baseurl }}/images/doodle/painter-profile.png
	{{ site.global.data.baseurl }}/images/doodle/painter-settings.png
{% endcapture %}
{% include gallery images=images caption="Painters register and are given codes to put on their rocks. They can add their social media to spread their name to visitors of their rocks' profiles." cols=3 %}

{% capture images %}
	{{ site.global.data.baseurl }}/images/doodle/become-a-sponsor.png
	{{ site.global.data.baseurl }}/images/doodle/sponsor-billing.png
	{{ site.global.data.baseurl }}/images/doodle/sponsor-profile.png
{% endcapture %}
{% include gallery images=images caption="Sponsors register and can choose a number of options for sponsoring giveaways and rocks. They can see the effects of their subscriptions/giveaways by seeing winners and the number of codes they sponsor." cols=3 %}

{% capture images %}
	{{ site.global.data.baseurl }}/images/doodle/login.png
	{{ site.global.data.baseurl }}/images/doodle/login-error.png
{% endcapture %}
{% include gallery images=images caption="Painter and Sponsor account types log in using the same form. Error handling is done server-side and displayed in the form." cols=3 %}
