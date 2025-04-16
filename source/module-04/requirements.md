---
title: Module 04 — Case Study Requirements
---

![Hot Cocoa]({{URLROOT}}/shared/img/hot-cocoa.jpg)
*[Photo by Liam McGlynn on Unsplash](https://unsplash.com/@liamo27)*

  

## Scenario

The owners of a café corporation with many franchise locations have noticed how popular their gourmet hot cocoa offerings have become. 

Customers (the café franchise location managers) cannot seem to get enough of the high-quality cacao beans that are needed to create amazing hot cocoa in their cafés. 

Meanwhile, the employees in the café corporate office have been challenged to consistently source the highest-quality cacao beans. Recently, the leaders at the corporate office learned that one of their favorite cacao suppliers wants to sell her company. The café corporate managers jumped at the opportunity to buy the company. The acquired cacao supplier runs a cacao supplier listings application on an AWS account, as shown in the following image.

![Scenario]({{URLROOT}}/shared/img/scenario-one.jpg)

The cacao suppliers application currently runs as a monolithic application. It has reliability and performance issues. That is one of the reasons that you have recently been hired to work in the café corporate office. In this project, you perform tasks that are associated with software development engineer (SDE), app developer, and cloud support engineer roles.

You have been tasked to split the monolithic application into microservices, so that you can scale the services independently and allocate more compute resources to the services that experience the highest demand, with the goal of avoiding bottlenecks. A microservices design will also help avoid single points of failure, which could bring down the entire application in a monolithic design. With services isolated from one another, if one microservice becomes temporarily unavailable, the other microservices might remain available.

You have also been challenged to develop a CI/CD pipeline to automatically deploy updates to the production cluster that runs containers, using a blue/green deployment strategy. 

## Stakeholders

These are the individuals your team will be helping during the case study:

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/christian.jpg">
	<h5>Christian Jones, Software Development Team Lead</h5>
	<blockquote><p>Good morning, everyone. Thank you for joining this meeting. As you know, we've been tasked with splitting the monolithic cacao supplier application into microservices and implementing a CI/CD pipeline for automated deployment. Let's discuss our plan and how we'll collaborate with the cloud support team to achieve this.</p>
</blockquote>
</div>
 
<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/cloud-team.jpg">
	<h5>Taylor Zitlau, Cloud Support Engineer</h5>
	<blockquote><p>Morning, team. I've reviewed the requirements, and I think we can align our efforts effectively. First, we need to ensure the microservices architecture is well-suited for deployment on AWS. Have we drafted an architecture diagram?</p>
</blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/bruce.jpg">
	<h5>Bruce VanNoy, Senior Cloud Engineer</h5>
	<blockquote><p>Not yet, we've tasked our newest cloud support team member with creating an initial diagram outlining the microservices architecture.</p>
</blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/christian.jpg">
	<h5>Christian Jones, Software Development Team Lead</h5>
	<blockquote><p>This diagram should illustrate how we'll split the monolith into individual services: one for user authentication, another for managing cocoa listings, and a third for order processing. Each service will have its own database and API endpoints.</p>
</blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/cloud-team.jpg">
	<h5>Brooke Timber, Cloud Support Engineer</h5>
	<blockquote><p>Looks good. We'll need to consider factors like load balancing and fault tolerance for each microservice. How are we planning to handle scalability and resilience?</p>
</blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/bruce.jpg">
	<h5>Bruce VanNoy, Senior Cloud Engineer</h5>
	<blockquote><p>We'll use AWS Elastic Load Balancing to distribute incoming traffic across multiple instances of each microservice. Additionally, we'll implement auto-scaling groups to automatically adjust the number of instances based on demand.</p>
</blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/cloud-team.jpg">
	<h5>Taylor Zitlau, Cloud Support Engineer</h5>
	<blockquote><p>Excellent. And what about portability? We need to ensure the application remains agnostic to the underlying infrastructure.</p>
</blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/bruce.jpg">
	<h5>Bruce VanNoy, Senior Cloud Engineer</h5>
	<blockquote><p>We'll containerize each microservice using Docker, making them independent of the host environment. We will then orchestrate container deployment and management, providing portability across different cloud providers if needed.</p>
</blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/christian.jpg">
	<h5>Christian Jones, Software Development Team Lead</h5>
	<blockquote><p>Now, regarding the CI/CD pipeline, we'll use AWS CodePipeline for automation. Whenever changes are pushed to our Git repository, CodePipeline will trigger the pipeline, which includes building Docker images, running tests, and deploying to our Kubernetes cluster using a blue/green deployment strategy.</p>
</blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/cloud-team.jpg">
	<h5>Taylor Zitlau, Cloud Support Engineer</h5>
	<blockquote><p>Sounds like a robust plan. Have we estimated the cost implications of this solution?</p>
</blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/cloud-team.jpg">
	<h5>Brooke Timber, Cloud Support Engineer</h5>
	<blockquote><p>Yes, I've calculated the cost based on the anticipated usage and resource requirements. With proper utilization of AWS services like ECS for container orchestration and spot instances for non-critical workloads, we can optimize costs while ensuring scalability and reliability.</p>
</blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/christian.jpg">
	<h5>Christian Jones, Software Development Team Lead</h5>
	<blockquote><p>Great work, team. Let's ensure close collaboration throughout the implementation process to address any challenges that arise and to maintain alignment with the solution requirements.</p>
</blockquote>
</div>

<div class="dialogue">
	<img src="{{URLROOT}}/shared/img/cloud-team.jpg">
	<h5>Brooke Timber, Cloud Support Engineer</h5>
	<blockquote><p>Agreed. We'll provide ongoing support for infrastructure provisioning, monitoring, and optimization to ensure the solution operates efficiently in production.</p>
</blockquote>
</div>


!!!note "Stakeholder Focus Areas"
	The shareholders are particularly interested in the following areas:

	1.	Provide a cost estimate and architecture diagram.
	2.  Break monolithic services into containerized microservices.
	3.  Create the code CI/CD pipelines.
	4.	Deploy iterative improvements using a blue/green deployment strategy.

## Module 04 Requirements

The project must meet the following requirements:

1.	R1 – **Design** – The solution must have an architecture diagram
2.	R2 – **Cost Optimized** – The solution must include a cost estimate
3.	R3 – **Microservices-based architecture**: Ensure that the solution is functional and deploys a microservice-based architecture
4.	R4 – **Portability**: The solution must be portable so that the application code isn’t tied to running on a specific host machine.
5.	R5 – **Scalability/resilience**: The solution must provide the ability to increase the amount of compute resources that are dedicated to serving requests as usage patterns change, and the solution must use routing logic that is reliable and scalable.
6.	R6 – **Automated CI/CD**: The solution must provide a CI/CD pipeline that can be automatically invoked when code is updated and pushed to a version-controlled repository.



[^1]: [Hot Cocoa photo by Liam McGlynn on Unsplash](https://unsplash.com/photos/uW4F8DorLs8)

[^2]: [Software Development Team Lead photo by Christian Buehner on Unsplash](https://unsplash.com/photos/DItYlc26zVI)

[^3]: [Cloud Team photo by Tyler NixChristina @ wocintechchat.com on Unsplash](https://unsplash.com/photos/swi1DGRCshQ)

[^4]: [Senior Cloud Engineer photo by bruce mars on Unsplash](https://unsplash.com/photos/8YG31Xn4dSw)


