---
layout: project
type: project
image: img/clubhub.png
title: "Club Hub"
date: 2022
published: true
labels:
  - Web Development
  - React
  - Meteor
summary: "Club Hub is a place where students are able to view all of the clubs around the University Of Hawaii campus and stay up to date with club events by bookmarking their favorite clubs. Students are also able to post their own clubs as well as publish their own events reguarding their club."
---


For this project, the team practiced agile software development to complete our goal of a fully functioning club hub website. In order for our team to succeed, I implemented the dynamic population of the club lists page, and events page, as well as the full functionality of the manage your events page. For the club lists page, with each club in the club collection, I populated a card that read through some of the properties of each club. The events page also collected data from the ProfileClubs collection which is a collection made by each user that populates from the clubs that the user bookmarks. To make this function, I filtered out all of the events by the club name property given from the ProfileClubs collection. With this, I populated the page with event cards consisting of properties of the events. Finally, I created a manage your events page where you are able to see a full events page consisting of events that the user logged in owns. For example, the user, acmmanoa@hawaii.edu, is able to manage all of the events regarding acmmanoa@hawaii.edu. 

<div class="text-center p-4">
  <img width="200px" src="../img/clubhub-hp.png" class="img-thumbnail" >
  <img width="200px" src="../img/clubhub-b.png" class="img-thumbnail" >
  <img width="200px" src="../img/clubhub-e.png" class="img-thumbnail" >
  <img width="200px" src="../img/clubhub-mye.png" class="img-thumbnail" >
</div>
