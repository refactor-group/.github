# Welcome! 👋

Have you ever thought to yourself that you know you can become a better software developer (professionally or for fun) if you could get
someone with experience to provide you some help and guidance? Well that's exactly what this open source software community is for. We're
an international group of software craftspeople who love building free software and helping others learn how to do this better.

Currently we:

1. Build useful projects that solve real world problems with a current focus on ambient environment sensing applications like room
air conditions and visualizing highly localized paragliding climate conditions. The focus will expand over time to other applications
like specific ways to help solve climate change or truly better many lives in specific ways.
2. Are a place to learn and grow your comprehensive software development skillset with others who have all levels of experience (just getting started
to multiple decades of software building experience) from around the world

We hang out on a Slack instance called [Rust Never Sleeps](https://rustneversleepshq.slack.com/). [Please contact us if you'd like to
join the community conversation](mailto:jim@jimhodappcoaching.com).

We welcome new members into the community and will provide a more formal way of joining coming soon. In the meantime, feel free to
browse around the repositories, clone the code, see if you can get everything running, and even contribute bug fixes or new features.

***

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary><h2 style="display: inline-block">Table of Contents</h2></summary>
  <ol>
    <li><a href="#weekly_meetings">Weekly Meetings</a></li>
    <li><a href="#current_software_projects">Current Software Projects</a></li>
    <li><a href="#project_goals">Project Goals</a></li>
    <li><a href="#getting_involved">Getting Involved</a></li>
    <li><a href="#learning_resources">Learning Resources</a></li>
    <li><a href="#community_values_and_code_of_conduct">Community Values and Code of Conduct</a></li>
    <li><a href="#software_engineer_coaching">Software Engineer Coaching</a></li>
  </ol>
</details>

***

<!-- WEEKLY MEETINGS -->

## Weekly Meetings

We currently meet every Thursday at 7 PM central US time. Note that we're considering changing this time or adding another meeting to accommodate more timezones from around the world.

You may find our meetings notes and current community focus for each project (Edge + Ambi) here:
 * [Ambi Project meeting notes](https://github.com/Jim-Hodapp-Coaching/ambi/wiki/Community-Meeting-Notes)
 * [Edge Project meeting notes](https://github.com/Jim-Hodapp-Coaching/edge-rs/wiki/Community-Meeting-Notes)


<!-- CURRENT SOFTWARE PROJECTS -->

# Current Software Projects

## Overview
The Edge / Ambi Projects currently exist to explore two main goals:

1. Creating a simple, highly performant IoT framework to collect and control hardware/software agents at the edge that:
    * Are almost always connected to the internet
    * Are intermittently connected to the internet
2. The use of the exciting new highly performant, safe and scalable Rust lang both for embedded and cloud implementations as well
  as use of Elixir for cloud implementations

The __Edge Project__ refers to the embedded/IoT aspects of the system including the hardware sensors, embedded board (Raspberry Pi Pico)
and embedded Rust source code.

[Browse the Edge GitHub Project board](https://github.com/orgs/Jim-Hodapp-Coaching/projects/3/views/1) that has all current
Edge feature/bug work

The __Ambi Project__ refers to the web backend and frontend components of this system acting as a local or cloud-hosted system that
processes, morphs and gives meaning to the data collected by the Edge pieces of the system.

[Browse the Ambi GitHub Project board](https://github.com/orgs/Jim-Hodapp-Coaching/projects/1/views/1?layout=board) that
has all current Ambi feature/bug work

<!-- PROJECT GOALS -->

## Project Goals

1. __Paragliding use-case:__ A primary application is sensing the environmental conditions in real-time around a paraglider, storing
the data locally and later pushing the data to an Edge cloud backend for further processing/visualization.
Ambient room conditions use-case: Another primary application is sensing the ambient room conditions, continually pushing the data
to an Edge cloud backend for further processing/visualization.
2. __A meaningful OSS project:__ Create a meaningful open source software project and community for coaching clients, friends and
trusted acquaintances to practice and build up skills for fun and future career success from a group with diverse experience. This
includes opportunities to design and contribute to embedded systems and cloud-based backends and frontends. It also provides multiple
opportunities to have your name attached to a real project for your career experience portfolio, useful for future job interviews and
job roles.
3. __Raspberry Pi Pico:__ Utilize and contribute back to the very accessible Raspberry Pi Pico software ecosystem specifically for Rust.
4. __Rust/Elixir:__ Utilize Rust for all embedded development and a combination of Rust/Elixir for cloud backend implementations.
Contributing publications: Communicating about the project and things that we’re learning about and building are important to do. This
involves writing overviews and guides for the Relational Technologist newsletter and creating mature project documentation.
5. __Growth + Fun:__ Fun projects solving real-world problems for anyone to become a better software developer, all done in community
with others from around the world. [Read more on why it's critically important to join an open source community to practice your software
development skills](https://reltech.substack.com/p/the-importance-of-open-source-software?utm_source=url).

<!-- GETTING INVOLVED -->

## Getting Involved

You can get involved in a number of ways:

### Embedded Development on Pico (currently using Rust)

1. Design and maintain Pico and sensors dev kit bill of materials (BOM)
2. Architect and design embedded software subsystems and APIs
3. Development of the main embedded Edge application in Rust (edge-rs)
4. Development of a device → cloud backend communications subsystem and API (e.g. RESTful + JSON)
5. ESP32 WiFi driver development in Rust for the Pimoroni Wireless Pack for Pico
6. Other sensor driver development in Rust (TBD)
7. Architect and implement a CI/CD strategy
8. Architect and implement an automated testing strategy
9. Design and maintain Pico and sensor wiring guide documentation
10. Writing overviews and guides of what we’re learning/building for the [Relational Technologist newsletter](https://reltech.substack.com/)
11. Writing mature project documentation (README and other)

Edge software repos and hardware:
 * [Edge](https://github.com/Jim-Hodapp-Coaching/edge-rs): our main embedded/IoT application written in 100% Rust targetting
 [Raspberry Pi Pico](https://www.raspberrypi.com/products/raspberry-pi-pico/)
 * [ESP32 WiFi Driver](https://github.com/Jim-Hodapp-Coaching/esp32-pico-wifi): our PoC code creating a Rust-based Pico WiFi driver
 that uses an [ESP32 companion board from Pimoroni](https://shop.pimoroni.com/products/pico-wireless-pack)

### Cloud Backend (currently using Elixir + Rust)

1. Architect and design cloud backend software subsystems and APIs
2. Development of a real time cloud backend API for receiving pushed data from multiple Pico or virtual nodes in parallel
3. Development of an asynchronous cloud backend API for receiving non-real time data from a Pico node
4. Development of data processing cloud backend subsystems
5. Architect and implement a CI/CD strategy
6. Architect and implement an automated testing strategy
7. Writing overviews and guides of what we’re learning/building for the Relational Technologist newsletter
8. Writing mature project documentation (README and other)

Ambi backend software repos:
 * [Ambi](https://github.com/Jim-Hodapp-Coaching/ambi): our main web application backend written in Elixir (and soon, some Rust)
 * [Ambi Mock Client](https://github.com/Jim-Hodapp-Coaching/ambi_mock_client): an increasingly comprehensive test double (mock)
 of an Edge hardware sensor target that sends simulated sensor data to an Ambi backend instance

### Cloud Frontend (currently using Phoenix LiveView + JavaScript)

1. Architect and design cloud frontend software subsystems and APIs
2. Development of a frontend → backend API
3. Development of an asynchronous cloud backend API for receiving non-real time data from a Pico node
4. Development of data processing cloud backend subsystems
5. Architect and implement a CI/CD strategy
6. Architect and implement an automated testing strategy
7. Writing overviews and guides of what we’re learning/building for the Relational Technologist newsletter
8. Writing mature project documentation (README and other)

Ambi frontend software repos:
 * [Ambi](https://github.com/Jim-Hodapp-Coaching/ambi): our main web application frontend written in Elixir + JavaScript

### Non-technical ways of contributing & software engineer practice

1. Facilitate community conversation in the Rust Never Sleeps Slack server
2. Facilitate regular project meetings keeping project members in sync and clear on next steps
3. Contribute to defining embedded project features and requirements
4. Contribute to defining cloud backend project features and requirements
5. Contribute to defining cloud frontend project features and requirements
+ many more...

If you’d like to join the project, please reach out to [Jim Hodapp](mailto:jim@jimhodappcoaching.com) and let him know
that you're interested in practicing and contributing to the project.

<!-- LEARNING RESOURCES -->

## Learning Resources

__Rust__
 * [Rust Book](https://doc.rust-lang.org/book/): Free, start here when learning Rust for the first time as well as for
 core language reference
 * [Rust by Example](https://doc.rust-lang.org/rust-by-example/): Free, hands-on and guided homework on almost every major
 area of Rust
 * [Rust in Action](https://www.manning.com/books/rust-in-action): A great intro book for new Rust developers (assumes zero
 prior language experience)
 * [Rust for Rustaceans](https://nostarch.com/rust-rustaceans): When you want to go much deeper in Rust

__Elixir__
 * [Elixir Getting Started Guide](https://elixir-lang.org/getting-started/introduction.html): Free, start here in learning Elixir
 * [Elixir in Action](https://www.manning.com/books/elixir-in-action-second-edition): A great intro book for new Elixir
 developers (assumes zero prior language experience)
 * [Phoenix Web Framework](https://hexdocs.pm/phoenix/overview.html): Free, hands-on guides covering the Elixir-based web
 framework used by Ambi
 * [Phoenix LiveView frontend](https://hexdocs.pm/phoenix_live_view/Phoenix.LiveView.html): frontend framework used by Ambi
 providing "real-time user experiences with server-rendered HTML."

<!-- COMMUNITY VALUES AND CODE OF CONDUCT -->

# Community Values and Code of Conduct

Please make sure to review our [community's overarching set of values and the code of conduct](./CODE_OF_CONDUCT).

__Note: all members of this community are expected to review, agree to, and sign the code of conduct before being invited into participating in the community.__

***

<!-- SOFTWARE ENGINEER COACHING -->

# Software Engineer Coaching

The community exists as part of [professional software engineer coaching](https://www.jimhodappcoaching.com/) and is available to help you master all technical, communication, organizational and relational aspects of being a master software engineer. It's also how the bills get paid which allows for this community to exist which includes covering living expenses for Jim Hodapp.

Even though the community exists under the coaching business umbrella, you do not need to participate in coaching if that's not what you're currently needing. Learning from and participating in this community exists as a compliment to Jim's coaching services, but you will certainly benefit from just starting with community participation. Feel free to jump in, ask questions and propose changes to any
of the software that the community is working on. You'll get quality feedback on your pull requests which is already something very valuable in helping you become a better software engineer.

If you would like to learn more about professional software engineer coaching, please
[read more about it here](https://reltech.substack.com/p/professional-engineering-coaching?utm_source=url) and [schedule a completely free
session with Jim](https://calendly.com/jim-hodapp-coaching).

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
