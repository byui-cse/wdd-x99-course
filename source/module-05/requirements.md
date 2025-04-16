---
title: Module 05 — Case Study Requirements
---

![Southern LA Volleyball Association]({{URLROOT}}/shared/img/new-volleyball-logo.jpg)

## Scenario: Southern LA Volleyball Association

Southern LA Volleyball Association hosts volleyball tournaments year-round across hundreds of venues in Southern California. These tournaments attract players from various parts of the nation, creating a vibrant and dynamic environment. However, as the association adds more and more tournaments managing the logistics of these tournaments has become cumbersome and expensive. The association currently relies on printing large-format pool charts and tournament brackets for each venue, leading to logistical challenges and increased costs.

To address these issues, the association aims to develop a digital solution that simplifies the process and enhances the overall experience for players and parents. This case study will task student teams with designing and implementing a cloud-based application to streamline tournament management and improve communication among stakeholders.

### General Tournament Information

* Each tournament has between 8 and 32 teams. 
* Teams play in *pool play* and then based on their results in pool play, they are seeded into brackets.
* Seeding is based on pool ranking (1st, 2nd, etc), then wins, then points differential.
* Brackets are in groups of 4, 8, or 12 teams. (8 team brackets are most common)
* Each team is assigned to a 4 team pool and plays all teams in their pool. Each pool is assigned a single court.
* Each match consists of 2 sets in pool play, which means there could be ties in pool play. Each match in bracket play is best 2 out of 3.
	* If there are only 3 teams in a pool, they play the other 2 teams for 3 sets instead of 2.
* Each location has between 1 and 4 courts.
* Each location has a site director who is responsible for writing scores on the pool sheets and brackets.
* Once pool play is finished, teams travel to the location of the bracket they are playing in. e.g. Gold, Silver, Bronze, Diamond
* All teams in a bracket will be at one location.


## Stakeholders

These are the individuals your team will be helping during the case study:
<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/jena.jpg">
	<h5>Jena, Association President</h5>
	<blockquote><p>Good morning, everyone. Thank you for joining me today. As you know, we're facing some challenges with our current tournament management process, particularly in terms of communication and efficiency.</p></blockquote>
</div>
 
<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/stephanie.jpg">
	<h5>Stephanie Livi, Product Owner</h5>
	<blockquote><p>Absolutely, Jena.</p><p>We've been discussing how we can leverage technology to streamline our operations and enhance the overall experience for players, parents, and tournament organizers.</p></blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/courtney.jpg">
	<h5>Courtney Love, Senior Cloud Engineer</h5>
	<blockquote><p>I've been looking into potential cloud-based solutions that could address these issues. However, before we proceed, it would be helpful to understand the specific pain points you're encountering.</p></blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/jena.jpg">
	<h5>Jena, Association President</h5>
	<blockquote><p>Well, one major issue we're facing is the reliance on printed pool charts and tournament brackets. Not only is this expensive, but it also creates logistical challenges as we have to get them printed and delivered for each venue. This becomes a real problem as we have teams drop, add, or change just days before the tournaments.</p>
	<p>We also use dispersed gyms for our large tournaments, so communication between gyms to figure out overall rankings is a nightmare. Gathering the results from each of the gyms is a headache. On top of this, once teams finish their pool play, they must get to the gym that has their bracket. We've had teams go to the wrong gym, or sit around waiting to find out where to go, not realizing that results had been posted. These inefficiencies make tournaments last longer than is needed. Add this to travel times and a long day becomes almost unbearably long.</p>
	<p>We didn't have these issues when we were running smaller tournaments that fit in a single gym, but our new growth has caused some major growing pains.</p>
	</blockquote>
</div>

![Pool Chart]({{URLROOT}}/shared/img/pool-play.jpg)

![Pool Chart]({{URLROOT}}/shared/img/filled-pool.jpg)

![Bracket Chart]({{URLROOT}}/shared/img/bracket.jpg)


<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/stephanie.jpg">
	<h5>Stephanie Livi, Product Owner</h5>
	<blockquote><p>Jena, I've been watching how players and parents interact with the pools and brackets at the tournaments. Some players and parents take pictures of the pools when they enter the gym and then try to keep track by drawing on the images.</p><p>Additionally, I've noticed that other parents tend to walk out of the stands during matches to check the updated brackets. Or they crowd around the pool sheets as the site director is writing and updating the information. This is pretty intimidating for the site directors and this disrupts the flow of the tournament and detracts from the overall experience.</p></blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/courtney.jpg">
	<h5>Courtney Love, Senior Cloud Engineer</h5>
	<blockquote><p>That's certainly an important consideration. It sounds like we need a solution that provides real-time updates and ensures easy access to tournament information without requiring people to leave their seats.</p></blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/jena.jpg">
	<h5>Jena, Association President</h5>
	<blockquote><p>Exactly. Furthermore, we've been experiencing issues with players not showing up for their reffing assignments and line judge duties. Despite our efforts to communicate these responsibilities, it seems that some players aren't understanding the sheets or just forget when they are supposed to help. This makes the tournament slow down since the officials have to track down the coaches and teams before the next match can begin.</p></blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/stephanie.jpg">
	<h5>Stephanie Livi, Product Owner</h5>
	<blockquote><p>This emphasizes the importance of not only providing information but also ensuring that it's easily accessible and digestible. We need a solution that not only displays match schedules but also includes clear instructions and reminders for additional duties.</p></blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/courtney.jpg">
	<h5>Courtney Love, Senior Cloud Engineer</h5>
	<blockquote><p>I see. In that case, we'll need to design a user-friendly interface that prioritizes essential information and encourages active engagement from players, coaches, and parents. Additionally, we can implement something like push notifications or reminders to ensure that everyone is aware of their responsibilities.</p></blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/jena.jpg">
	<h5>Jena, Association President</h5>
	<blockquote><p>That sounds promising, but we don't gather all of the player's information. Maybe something just for the coaches, or a way for the players to request updates for their specific team? I'm not very techy, so I'm just throwing out ideas.</p></blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/stephanie.jpg">
	<h5>Stephanie Livi, Product Owner</h5>
	<blockquote><p>I'm confident that by leveraging cloud technology, we can create a centralized platform that consolidates all tournament-related information and updates in real-time. This would not only reduce costs but also improve communication and efficiency across the board.</p><p>Let's continue to collaborate closely to develop a solution that meets the needs of our association and enhances the overall tournament experience which will make for happier coaches, players, and parents. With your technical expertise, we can create something truly impactful for our community.</p></blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/courtney.jpg">
	<h5>Courtney Love, Senior Cloud Engineer</h5>
	<blockquote><p>Absolutely, I'm excited to work on this project and see how we can leverage cloud computing to address these challenges effectively. Together, I believe we can develop a solution that revolutionizes how we manage volleyball tournaments in Southern California.</p></blockquote>
</div>


## Module 05 Requirements

Based on the scenario and discussion above, your team will define the product requirements.


[^1]: [Association President photo by Jenny Ueberberg on Unsplash](https://unsplash.com/photos/9xXYjXzmsbk)

[^2]: [Product Owner by Stephanie Liverani on Unsplash](https://unsplash.com/photos/Zz5LQe-VSMY)

[^3]: [Senior Cloud Engineer photo by Courtney Cook on Unsplash](https://unsplash.com/photos/TSZo17r3m0s)


