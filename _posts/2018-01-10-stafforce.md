---
layout: post
type: portfolio
title:  "Stafforce Staffing Portal"
date:   2018-01-10
start: 2017-07-11
end: 2017-11-14
image: /images/stafforce/dashboard.png
url: ''
excerpt: "Stafforce Staffing Portal is a workorder and employee management app for a staffing agency."
tag:
- portfolio
- php 
- ajax
- javascript
- database design
- mysql
- mdb bootstrap
---

<a href="{{ site.global.data.baseurl }}/images/stafforce/dashboard.png"><img src="{{ site.global.data.baseurl }}/images/stafforce/dashboard.png" class="thumbnail" alt="Dashboard of Stafforce Staffing Portal"></a>  
<center><b><a>Stafforce Staffing Portal</a></b> is a workorder and employee management app for a staffing agency.</center><br>

## Project Summary
Stafforce is a Jacksonville, FL based staffing company. This project provides an online system for creating and managing workorders, employees, and companies. Agents can create workorders for a company and the system algorithmically suggests suitable employees based on common skills, distance to the worksite, the employee's rating, and whether the employee has worked for the company before. 

I was the sole developer for this project and was responsible for every aspect of front- and back-end functionality. I chose to use Material Design Bootstrap for theming, as the project had many reusable components and uses for modals, form validation, menus, and other standard components. 

Every form is saved using Ajax and a log is kept of every change made to a record and which agent made the change. 

### Role:
---
 - Lead Developer

### Responsibilities:
--- 

1. Design database schema
1. Develop algorithm for evaluations to rate employees
1. Develop algorithm for suggesting employees for workorders
- Employees can be added to a 'do not return' list, which prohibits them from being suggested for a workorder
1. Export data as Excel sheets for various reports

### Unique parts
* Searching between multiple tables and highlighting results
* Suggested employees

### What I learned
- Composer for dependency management
- Greater familiarity with the Google Maps API
- Use a language's built-in functions whenever possible to improve performance and security. In this project, I learned about PHP's functions for differencing data. When a change is made to a record, I used array_diff to compare the old and new records and only store the differences

## Conclusion
This project helped me learn and understand a lot about efficient data interaction and data structures. I'm excited to continue developing my knowledge of algorithms and data structure theory.

## Preview

{% capture images %}
	{{ site.global.data.baseurl }}/images/stafforce/workorders.png
 	{{ site.global.data.baseurl }}/images/stafforce/workorder.png
	{{ site.global.data.baseurl }}/images/stafforce/evaluation.png
{% endcapture %}
{% include gallery images=images caption="The workorder overview, details, and employee removal evaluation (the answers become factors in suggesting the employee for future workorders). Skills listed on the workorder are used for employee recommendations." cols=3 %}

{% capture images %}
	{{ site.global.data.baseurl }}/images/stafforce/employees.png
	{{ site.global.data.baseurl }}/images/stafforce/employee.png
{% endcapture %}
{% include gallery images=images caption="Employees overview and details page. Skills listed for employees are used for suggesting employees for a workorder." cols=2 %}

{% capture images %}
	{{ site.global.data.baseurl }}/images/stafforce/company.png
	{{ site.global.data.baseurl }}/images/stafforce/search.png
{% endcapture %}
{% include gallery images=images caption="The company details page, which logs past employees and current and past workorders, as well as employees not to return. The search highlights matching terms or partial terms." cols=2 %}
