+++
title = 'Job Kuai Tie'
date = 2025-04-25T21:02:36+08:00
draft = false
tags = []
unique_id = "a65572d047463102fdbee92a545ea8ec"
aliases = ["a65572d047463102fdbee92a545ea8ec"]
images = ["cover.png"]
cover_image = "cover.png"
header_image = "header.png"
summary = "Derived from personal needs and implemented for demo purpose, Job KuaiTie is a project prototyped in four days, with backend FastAPI (Python), frontend Vue.js (Javascript), and the help from ChatGPT. Job KuaiTie aims to provide a table-like panel for job seekers to organize and prioritize their job application with easy notes."
project_info = true
project_title = "Job KuaiTie (求職快貼)"
project_size = "1 members"
project_duration = "Postpone"
project_timeframe = "2025 April 20 → 23 "
project_lang = "English"
project_type = "Side Project"
project_summary = "Derived from personal needs and implemented for demo purpose, Job KuaiTie is a project prototyped in four days, with backend FastAPI (Python), frontend Vue.js (Javascript), and the help from ChatGPT. Job KuaiTie aims to provide a table-like panel for job seekers to organize and prioritize their job application with easy notes."
+++
# Background

While most of the job search platforms provide listing features, there is no place to organized all posts together from different platforms. In addition, while progress tracking is a feature for many job search platform, **more advance features, like customized weighting job post for prioritization, labelling jobs with different attributes (like “Work-Life Balance", “Tech-oriented") are not observed so far.** It was a pain to organize interested job posts if more features expected. 

The idea was **first implemented by Notion page** for personal need, until a demo opportunity emerged during a interview preparation. J**ob KuaiTie, as a demo project prototyped in four days, drafted an web app showing how job posts could be managed.** While many features are not deployed yet, **Job KuaiTie implemented the skeleton of the idea with features like saving a Job Post, saving a Firm Link, and defining a Category.** More features could emerged with these basic schema setting and would be explored in the future.

# Goal

This project aims to support job seekers with a more smooth job searching process by providing a panel for users to host all of the job post at one place, prioritizing and labelling their job post, and calculating the weights for better job application planning.

# Process

At first, the project idea is served as a Notion Page for me as a Job Post Collection, then with more features required, a Firm Collection added, weighting criteria added, and more domain logic emerged as I actually utilizing it during my job searching process.

Then I get a chance for an tech interview, from which used FastAPI as the main web app backend framework. It shows that it could be a interesting opportunity to draft this project as a FastAPI demo project. Within four days, I explored the basic of the FastAPI, implemented the core API for this project, and assemble a workable (though quite fragile with many tech debt due to the time limitation) version of the MVP (Minimum Viable Product) with the frontend made by Vue.js. All develop process are supported, but not replaced, by ChatGPT, as the LLM empowers me to pickup the key idea of FastAPI, alone with the Pydantic and SQLModel, and draft the interface with PrimeVue.

While the MVP do shows a basic CRUD operation for the entity Job, Firm, and Category with a old-style authentication flow, more updated would be expected for the next iteration.

The overall system with important packages is shown in the Figure 1, following a 3-mins demo video embedded belowed.

{{< figure src="overall.png" alt="The overall system with important packages" caption="Figure 1: The overall system with important packages">}}

{{< youtube id=wNl5DeUaiyE >}}

## 1. Notion Page for personal usage

Figure 2. shows the notion page for the Job Post. The Job Post page served as the main source for me to source, prioritize, and track my job application. It connected with the Firm Page, which is the collection of companies where the job posts from.

{{< figure src="notion-job.png" alt="The notion page of Job Post" caption="Figure 2: The notion page of Job Post">}}

To better access the job posts, two formula were used (Job Post and Firm List). Each one is a total weight from 0 to 5, with each attribute could be sum from 1 to 5 and normalized afterward. Figure 3 shows the weight formula for Job Post.

{{< figure src="notion-formula.png" alt="The notion formula for Job Post" caption="Figure 3: The notion formula for Job Post">}}

## 2. API designed for the MVP

As a demo project for FastAPI, this project use FastAPI and its common friends, which are Pydantic (for data validation and serialization), and SQLModel (for database schema definition). Due to the time limitation, the schema is quite simple (as the Figure 4 shows), and the API is mainly authentication and CRUD for the entities.

{{< figure src="database-schema.png" alt="The database schema" caption="Figure 4: The database schema">}}

The API design is mainly followed the FastAPI guide, like defining a BaseModel with three derived models Model: ModelCreate (for POST method in RESTful API), ModelPublic (GET method), and ModelUpdate. (PATCH method) (as the Figure 5 shows)

The API doc could be accessed in ({{< link_blank "https://job-kuai-tie-api.river1440.work/docs" "this demo link" >}}), and here is ({{< link_blank "https://github.com/Job-KuaiTie/job-kuai-tie-api" "the github repo link" >}})

{{< figure src="api-doc.png" alt="The API doc for Job KuaiTie" caption="Figure 5: The API doc for Job KuaiTie">}}

## 3. Frontend for the MVP

The frontend is developed (more like assembled) in a hurry - only half day left before the demo. Its skeleton is mainly reused from another project of mine, the UI utilized the PrimeVue UI library, and the router, state management, and api call are firstly generated from ChatGPT, then revised to fit in the system. Figure 6 shows the Job Post page from the frontend, with ({{< link_blank "https://github.com/Job-KuaiTie/job-kuai-tie-frontend" "its github repo link here." >}})

{{< figure src="frontend.png" alt="The frontend for Job KuaiTie" caption="Figure 6: The frontend for Job KuaiTie">}}

## Sidenote

The name “Job KuaiTie" literally means “Paste a Job quickly." I am thinking about post-it, and how fast post-it could help organize complex ideas. Job KuaiTie aims to provide a flow that we could just post the idea about the jobs, easily label them and order them. List and note about the jobs should like a breeze, not like a suffering.