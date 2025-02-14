+++
title = 'Tangjuan'
date = 2025-01-07T21:19:19+08:00
draft = false
tags = []
unique_id = "6e2eb856831b8637ac0885370e6d2c3a"
aliases = ["6e2eb856831b8637ac0885370e6d2c3a"]
weight = 20
# For Open Graph and Twitter Card
images = ["cover.png"]
cover_image = "cover.png"
header_image = "header.png"
summary = "As a on-going side project derived from a gossip about personal finance, Tang Juan took a bottom-up approach to implement a web app for empowering user making well-informed personal financial decision. This project is built with Python (Backend/Flask) and Javascript. (Frontend/Vue.js)"
project_info = true
project_title = "Tang Juan (躺卷)"
project_size = "1 members"
project_duration = "Ongoing"
project_timeframe = "2024 November → Current"
project_lang = "English"
project_type = "Side Project"
project_summary = "As a on-going side project derived from a gossip about personal finance, Tang Juan took a bottom-up approach to implement a web app for empowering user making well-informed personal financial decision. This project is built with Python (Backend/Flask) and Javascript. (Frontend/Vue.js)"
+++
# Background

This project is a side project derived from a gossip with friends about buying house and retirement. During the discussion, we gradually realized that a sense-making personal financial decision relied on multiple financial facts and estimation, which could not easily achieved by just thinking.

# Goal

This project aims to provide an application for users to evaluate important financial decisions based on their own financial facts, such as salary, living cost, and housing.

# Process

As a side project, Tangjuan is implemented through a **bottom-up approach.** Starting from a spreadsheet demo, essential data fields and formula get defined. Then a monolith web app get scaffolded, written in Python with {{< link_blank "https://flask.palletsprojects.com/en/stable/" "Flask" >}} framework, to re-implement the spreadsheet demo to improve the usability.

To accomplish further requirement, a front-end / backend web app get adapted with the monolith revised as backend. The frontend is developed with {{< link_blank "https://vuejs.org/" "vue.js" >}} framework, {{< link_blank "https://primevue.org/" "PrimeVue" >}} as UI library, and {{< link_blank "https://tailwindcss.com/" "Tailwind" >}} for utility class. After the implementation of the basic features demo by the spreadsheet, the further design is on going with a more detailed consideration and diverse features.

## 1. Spreadsheet demo

In the spreadsheet demo, important financial facts are considered, such as salary, living cost, and increase range of salary by year. Essential financial decisions, such as when buying a house, when start raising a child, and when to retire, are also included. **Figure 1** shows the asset accumulation, salary and living cost across ages estimated by the spreadsheet demo. ({{< link_blank "https://docs.google.com/spreadsheets/d/18yllhfdH4REEmy09jSiJQExAmy_hKN4mBsWSefzgpUQ/edit?usp=sharing" "Click to check the spreadsheet demo" >}})


{{< figure src="spreadsheet-demo.png" alt="Spreadsheet Demo" caption="Figure 1: Result of Spreadsheet Demo" >}}

## 2. Monolith implemented by Python/Flask
To provide a better user interface and encapsulated the formula, a monolith is implemented by Python with Flask framework. A javascript library {{< link_blank "https://www.chartjs.org/" "Chart.js" >}} is used for plotting on browser side. The **Figure 2** shows the landing page of the monolith. ({{< link_blank "https://useful-bev-f4lazylifes-d32aaf74.koyeb.app/" "Click to check the monolith web app demo" >}})

The source code could be check in this {{< link_blank "https://github.com/tangjuan-finance/tangjuan-backend" "Github repo" >}}.


{{< figure src="the-monolith.png" alt="The landing page of the monolith" caption="Figure 2: The landing page of the monolith" >}}

## 3. Frontend by Vue.js

While monolith could serves the basic features, such as rendering data from database to webpages, or calculating results based on input, more complicated UI interaction would required complicated javascript. Thus, a vue.js based frontend is introduced to provide robust support for UI interaction. UI library PrimeVue and css framework tailwind is used for coherent design style. **Figure 3** shows the landing page of the frontend app.

({{< link_blank "https://tangjuan.river1440.work/" "Click to check the front-end web app demo" >}})

The source code could be check in this {{< link_blank "https://github.com/tangjuan-finance/tangjuan-frontend" "Github repo" >}}.


{{< figure src="landing-page-front-end.png" alt="The landing page of the front-end app" caption="Figure 3: The landing page of the front-end app" >}}

## 4. System Design

By so far Tangjuan is served as a tool for estimating personal financial facts without signup. While it would be safe as no personal information left, and all the information would vanished once the page closed, the user scenario is limited to one-time estimation. Advanced needs, such as financial planning (save the result for checking in the future) or comparing (saving different plans for comparing) would not be possible without connecting with a database.

As an iterative and ongoing project, an Entity-Relationship Diagram (ER Diagram) is designed for supporting advanced features, shown in **Figure 4.** The deployment of the ER Diagram and advanced features is still in progressed.


{{< figure src="er-diagram-tangjuan.png" alt="Entity-Relationship Diagram of Tangjuan" caption="Figure 4: The Entity-Relationship Diagram of Tangjuan" >}}

## Sidenote

The project name “Tang Juan” is derived from two slangs in Mandarin, “{{< link_blank "https://en.wikipedia.org/wiki/Tang_ping" "Tang ping" >}}” (躺平) and "{{< link_blank "https://en.wikipedia.org/wiki/Neijuan" "Neijuan" >}}.” (内卷) “Tang ping” literally means “lie down flat”, which is considered as a rejection to the over-competitive work environment in China after 2020s. And “Neijuan”, emerged at similar time, literally means “inside roll”, meaning an overworked life under extreme competition.

Thus, “Tang Juan”, as a financial facts estimation tools, aims to empower users balancing work and life. With “Tang Juan”, a clear personal finance landscape would be shown, suggesting how much salary and assets would be needed to accomplish personal financial goals.

{{< figure src="logo-tangjuan.png" alt="Logo of Tangjuan" caption="Figure 5: Logo of Tangjuan" >}}