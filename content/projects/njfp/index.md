+++
title = 'NJFP'
date = 2024-05-31T13:06:24+08:00
draft = false
tags = []
unique_id = "f08b453cf90cf447dd4a616016178108"
aliases = ["f08b453cf90cf447dd4a616016178108"]
weight = 30
# For Open Graph and Twitter Card
images = ["cover.png"]
cover_image = "cover.png"
header_image = "header.png"
summary = "NJFP is a side project aims to provide a hosting service for people easily managing their project experiences. Serving as a self-taught project, NJFP started from defining need and goals with persona, creating Figma prototype, hosting UI components on Storybook, to defining ER diagram and setting api documentation with Swagger UI."
project_info = true
project_title = "NJFP (Not Just Final Project)"
project_size = "1 members"
project_duration = "Postponed"
project_timeframe = "2022 December → 2023 April"
project_lang = "English"
project_type = "Side Project"
project_summary = "NJFP is a side project aims to provide a hosting service for people easily managing their project experiences. Serving as a self-taught project, NJFP started from defining need and goals with persona, creating Figma prototype, hosting UI components on Storybook, to defining ER diagram and setting api documentation with Swagger UI."
+++

# Background

This postponed side project is established for exploring different stages of a web app development across the software lifecycle. Its features are derived from my experiences of establishing student clubs and SDGs community at NTHU. The observation shows that while students had many extracurricular experiences, organzied the projects are usually challenged due to lack of time and energy. What is even more difficult is utilized the experiences in the future or making them accessible for others.

# Goal

### Project Goal

This project, NJFP, abbreviated of “Not Just Final Projects”, aims to provide a hosting service for people easily managing their project experiences . People could easily archive all their projects, including report, descriptions, or other files. And others could also browse the public projects for inspiration.

### Learning Goal

Taking an Top-down approach, this project is served as an exploration of software development stages, including define potential user needs, prototyping, and making UI components.

# Process

## 1. Define Persona and User Story

The features of this project is derived from my observation when establishing students club and community at NTHU. Thus, as first step, the observations get crystallized into three persona, with different goals and need. A summary of the goal of three persona are as follows,

1. **Exhausted Youth:** I would like to apply any program in a more efficient way, so that I could leave more time for myself.
2. **Diligent Student:** I would like to develop projects in a more reliable way, so that I could learn more and do better.
3. **Ambitious Visionary:** I would like to recruit people engaging with inspiring projects, so that we could make impacts together.

The persona of Exhausted Youth is shown in **Figure 1**, showing the goal, needs, and pain points.

{{< figure src="persona.png" alt="Persona of Exhausted Youth" caption="Figure 1: Persona of Exhausted Youth" >}}

After defined persona, a few of user stories are listed based on the needs and pain points mentioned by the persona. **Figure 2** shows part of the user story lists, including which persona the user story referring to, what they want, and how they could benefit from the features.

{{< figure src="user-story.png" alt="User Story" caption="Figure 2: User Story" >}}

## 2. Figma Prototyping

With defined user stories, a prototype is created with Figma. The UI components are first designed at the team library, with variants and components properties. Then the components get exported and introduced in the prototype. **Figure 3** shows part of the field component with different properties.

{{< figure src="field-component-figma.png" alt="Field component at the team library in Figma" caption="Figure 3: Field component at the team library in Figma" >}}

The Figma prototype shows the basic features for hosting projects, such as project cards, tags, and search. The Figma prototype could be check at {{< link_blank "https://www.figma.com/proto/jkgFIwmQ7aQ61Pcqwk85DF/Wireframe?node-id=40-448&p=f&t=TfpvFIP1ZRGRmcWN-1&scaling=scale-down&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=13%3A7" "this prototype file" >}}.

## 3. UI Components By Storybook

After prototyping, the UI components are created with Vue.js. For documentation, {{< link_blank "https://storybook.js.org/" "Storybook" >}} is used for hosting UI components. **Figure 4** shows how the Single Card component be hosted at Storybook, with variants and components properties. The storybook could be checked {{< link_blank "https://main--659a7a938e8e6117f79c5c7d.chromatic.com/?path=/docs/design-system-atom-singlecard--docs" "here" >}}.

{{< figure src="single-card.png" alt="The Single Card components hosted by storybook" caption="Figure 4: The Single Card components hosted by storybook" >}}

The storybook as well as the frontend could be checked at {{< link_blank "https://github.com/NJFProjects/njfps-frontend-platform/tree/main" "this Github repo" >}}.

## 4. Database Table and Entity Relationship Diagram (ER Diagram)

While creating UI components, a table list is used to draft the schema of NJFP, shown in **Figure 5**.

{{< figure src="table-list.png" alt="Table list of NJFP" caption="Figure 5: Table list of NJFP" >}}

For each table, a specification table is created for noting fields’ properties. **Figure 6** shows the specification table for Profiles Table. 

{{< figure src="specification-table.png" alt="Specification Table for Profiles Table" caption="Figure 6: Specification Table for Profiles Table" >}}

With the table list and specification tables, an ER diagram is composed as **Figure 7** showed.

{{< figure src="er-diagram-njfp.png" alt="ER Diagram of NJFP" caption="Figure 7: ER Diagram of NJFP" >}}

## 5. Backend API Documentation by Swagger UI

Before building apis, the documentation are created following the OpenAPI 3.0. Swagger UI is used for enhancing readability and interactivity, shown in **Figure 8.** The api documentation could be checked {{< link_blank "https://njfprojects.github.io/njfps-backend-api-doc/" "here" >}}.

{{< figure src="api-doc.png" alt="API Documentation with Swagger UI" caption="Figure 8: API Documentation with Swagger UI" >}}

The api documentation could be checked at {{< link_blank "https://github.com/NJFProjects/njfps-backend-api-doc/tree/main" "this Github repo" >}}.