This is a running log of our weekly community meeting conversations and covers what the community is currently focused on, currently held every Thursday evening at 7 PM US CST. The latest meeting notes should always be listed first (reverse chronological order).

## March 10, 2022

### Ambi (web)
 * Joe finishing a PR that allows Ambi to handle and respond to invalid POST requests [(Issue 6)](https://github.com/Jim-Hodapp-Coaching/ambi/issues/6)
 * Chris taking on design and implementation of a CI system for the Ambi repo [(Part of Issue 14)](https://github.com/Jim-Hodapp-Coaching/ambi/issues/14) -> [Pull request from Chris that adds `mix format` as a git pre-commit hook](https://github.com/Jim-Hodapp-Coaching/ambi/pull/15)

### Edge (IoT/Embedded)
 * Latest status on [WiFi PoC completion](https://github.com/Jim-Hodapp-Coaching/esp32-pico-wifi/issues/8)

***

## February 24, 2022

### General
 * Discuss new concept of picking a current singular growth focus for the community (e.g. what are high quality PR reviews?)

### Ambi (web)
 * Fixing outstanding Ambi bugs + next steps:
   * [Dashboard doesn't show on empty DB](https://github.com/Jim-Hodapp-Coaching/ambi/issues/3)
   * [Initial dashboard page load gets slow with 100k+ sensor readings in the DB](https://github.com/Jim-Hodapp-Coaching/ambi/issues/5)
   * [Ambi dashboard view is missing a truthy case for displaying air_purity](https://github.com/Jim-Hodapp-Coaching/ambi/issues/7)

### Edge (IoT/Embedded)
 * [Finishing off Edge / ESP32 PoC](https://github.com/Jim-Hodapp-Coaching/esp32-pico-wifi/issues/8) + next steps
 * What would it mean to communally design an [ESP32 WiFi API and Rust Crate](https://github.com/Jim-Hodapp-Coaching/edge-rs/issues/1)?

### Discussion
   * Caleb: suggestion to add a notice to our future community code-of-conduct that says each person who signs will allow the community to relicense the code if it ever becomes necessary to (e.g. BSD + Patent license becomes legally invalidated somehow)
   * Look at Ockam's community to see how they automatically use a first PR to sign their contributor code-of-conduct
   * [Jim, Joe, Caleb]: talked through Joe's current issue of injecting an HTTP 400 error code when a client makes a bad request ([related GH Issue](https://github.com/Jim-Hodapp-Coaching/ambi/issues/6))

***

## February 17, 2022

**Topics**
 * Off for this week

***

## February 10, 2022

**Topics**
 * ESP32 WiFi PoC project work session

***


## February 3, 2022

**Topics**
* Next steps for the project

### What’s next for Ambi (ambient room condition use case)
* Add command line parameter functionality to [ambi_mock_client](https://github.com/Jim-Hodapp-Coaching/ambi_mock_client)
* [Chris Rees] Set up automatic test runs in a CI pipeline on GitHub
  * These should run with each new commit pushed by anyone to the repo
  * These should block merging if the tests don’t pass
* Allow for the dashboard user to toggle between metric and imperial units (1 global user for now, not multi-user)
* Consider how many sensor values should be read before the oldest values are truncated
  * Implement new total sensor readings limit
* Show dynamic labels for the X axis on the average temp/humidity charts
  * These should show hour labels in reference to now
* [Caleb] Allow for multiple sensor groups (e.g. different sensor group for different rooms)
  * Refactor DB schema model
  * Redesign dashboard to display multiple sensor groups (e.g. select a room to display)
* Dockerize and make it easy to:
  * Push an instance to a cloud server to run publicly (Azure, AWS, GCP, etc)
  * Do local Docker development
  * Carry out an evaluation of the best and simplest way to do this ([Docker Compose](https://docs.docker.com/compose/), [Rancher](https://rancher.com/docs/), [Microk8s](https://microk8s.io/), [Heroku](https://www.heroku.com/), other…)
* Community design of a multi-user experience

### Paragliding Use Case
* Thinking through how offline sensor readings sync to the DB
* Start incorporating paragliding sensor data into the backend DB
* Experiment with different frontend visualizations