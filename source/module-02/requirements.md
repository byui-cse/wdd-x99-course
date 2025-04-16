---
title: Module 02 — Case Study Requirements
---

![AnyCompany Cafe]({{URLROOT}}/shared/img/dessert.jpg)
*[Photo by Michaela Baum on Unsplash](https://unsplash.com/@miksbaum)*

  

## Scenario

AnyCompany Café sells dessert and drink items through their website. They have cafés in multiple cities throughout the world. The company wants to gain insights into the business by using data about how people interact with the website. The company plans to analyze clickstream data trends to make smarter decisions about where to invest. AnyCompany Café has hired your consulting company to lead this effort. You are a data integration specialist and work with a team of data engineers, data analysts, and web developers.

The clickstream log data from the café website includes an entry for every click that a potential customer makes while browsing the website. Your task is to design and create a data analytics pipeline to capture the clickstream data. You will also create an analytics dashboard so that the café owner can quickly observe customer behavior. The team wants to gain insights on user behavior on the website and then use those insights to focus advertising efforts. The company might even use the data to decide where to open additional locations.

## Stakeholders

These are the individuals your team will be helping during the case study:

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/amy.jpg">
	<h5>Amy Sorensen, Owner of AnyCompany Cafe</h5>
	<blockquote><p>Good morning, everyone. Thank you for joining this meeting. As you know, we've been exploring ways to leverage data to better understand our business and make informed decisions. Today, we have our consulting team here to discuss the progress on building our data analytics pipeline.</p><p>So, let's dive in. How's the progress on designing and creating the data analytics pipeline?</p>
</blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/cloud-team.jpg">
	<h5>Taylor Zitlau, Cloud Support Engineer</h5>
	<blockquote><p>We've made significant strides in designing and cost-optimizing the solution. Before we proceed to build, we want to ensure that it aligns with your needs and is cost-effective.</p></blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/tyler.jpg">
	<h5>Tyler Pruitt, VP of Marketing</h5>
	<blockquote><p>That sounds great. Can you elaborate on how you plan to capture and analyze the clickstream data?</p></blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/cloud-team.jpg">
	<h5>Taylor Zitlau, Cloud Support Engineer</h5>
	<blockquote><p>Certainly. We'll be ingesting access_log data from the café web server. To ensure functionality and provide insights, we'll transform the data and use simulated log data for testing purposes.</p></blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/amy.jpg">
	<h5>Amy Sorensen, Owner of AnyCompany Cafe</h5>
	<blockquote><p>That's good to hear. I'm keen on gaining insights from this data. Can you give us an idea of what insights we can expect?</p>
</blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/cloud-team.jpg">
	<h5>Brooke Timber, Cloud Support Engineer</h5>
	<blockquote><p>Absolutely. By analyzing the clickstream data, we'll be able to understand user behavior on our website. This information will help us focus our advertising efforts effectively and even make decisions on where to open additional café locations.</p></blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/amy.jpg">
	<h5>Amy Sorensen, Owner of AnyCompany Cafe</h5>
	<blockquote><p>Impressive. Now, I know there are some additional requirements you've been working on. Could you share those with the group?</p>
</blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/cloud-team.jpg">
	<h5>Taylor Zitlau, Cloud Support Engineer</h5>
	<blockquote><p>Of course.</p><p>We've been asked to incorporate geolocation information for website visitors and develop a visual dashboard to gain insights. The dashboard will include various metrics such as the top cities and regions with the most website visitors, those who accessed the menu page, and those who made a purchase. Additionally, we'll provide the ability to store access logs in Amazon S3 and query them using SQL.</p></blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/tyler.jpg">
	<h5>Tyler Pruitt, VP of Marketing</h5>
	<blockquote><p>That sounds incredibly useful for our marketing efforts. Being able to pinpoint where our website visitors are coming from will greatly enhance our targeting strategies.</p></blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/amy.jpg">
	<h5>Amy Sorensen, Owner of AnyCompany Cafe</h5>
	<blockquote><p>Agreed. Overall, I'm impressed with the progress and the direction we're headed. Thank you all for your hard work.</p>
</blockquote>
</div>

!!! note "Stakeholder Focus Areas"
	The shareholders are particularly interested in the following areas:

	1.	Provide a cost estimate and architecture diagram.
	2.  Examine logs and get them in a format that is usable.
	3.  Start collecting clickstream data.
	4.	Use the data to build a dashboard to inform business decisions.

## Module 02 Requirements

The project must meet the following requirements:

1.	Design and cost-optimize the solution prior to building
2.	Ensure that the solution is functional
3.	Transform data
4.	Ingest access_log data from the café web server
5.	Use simulated log data
6.	Analyze and visualize data
7.	Generate insights


[^1]: [Dessert photo by Michaela Baum on Unsplash](https://unsplash.com/photos/VnM6_liIRJ0)

[^2]: [Owner photo by Amy Hirschi on Unsplash](https://unsplash.com/photos/b3AYk8HKCl0)

[^3]: [Cloud Team photo by Tyler NixChristina @ wocintechchat.com on Unsplash](https://unsplash.com/photos/swi1DGRCshQ)

[^4]: [VP of Marketing photo by Tyler Nix on Unsplash](https://unsplash.com/photos/ZGa9d1a_4tA)


