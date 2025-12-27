---
title: Coding Sky Web App
summary: University of Glasgow IT+ Project Web App - Coding Sky.
tags:
  - Open Source
date: '2021-12-15T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: 
  focal_point: Smart

links:
  - icon: aws
    icon_pack: fab
    name: Preview (Server Expired after December 2022)
    url: https://codingsky.online/
url_code: 'https://github.com/Siriusq/coding_sky'
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ''
---

# Introduction
A comprehensive educational platform designed to support novice programmers through a multi-modal learning experience. The system integrates a Django-based quiz application for conceptual reinforcement, an interactive serious game built in Unity to visualize abstract programming logic in 3D, and a web-based code editor utilizing the Ace editor for hands-on JavaScript practice. The project focuses on bridging the gap between theoretical syntax and practical application through immediate feedback and interactive engagement.


# Instructions to run
**Clone And Open Project**

    $ git clone git@github.com:Siriusq/coding_sky.git
    $ cd .\coding_sky\

**Create Virtual Environment**

    $ conda create -n coding_sky python=3.7.5 

**Activate Virtual Environment**

    $ conda activate coding_sky

**Install Required Packages**

    $ pip install -r requirements.txt

**Build Database**

    $ python manage.py makemigrations
    $ python manage.py migrate --run-syncdb

**Create Superuser**

    $ python manage.py createsuperuser

**Start The Server**

If used for production

    $ python manage.py runserver --insecure

If used for development
- Open '.\coding_sky\coding_sky\settings.py'
- Change 'DEBUG = False' To 'DEBUG = True'

        $ python manage.py runserver

# Test

    $ python manage.py test coding.tests

# Browser Compatibility
Since the game uses WebGL 2.0, according to the [Unity Official Documentation](https://docs.unity3d.com/2021.1/Documentation/Manual/webgl-browsercompatibility.html), the compatible browsers are as follows.

- Mozilla Firefox 51 and newer
- Google Chrome 56 and newer
- Microsoft Edge (based on Chromium)
- Apple Safari 15 and newer

# Reference
The quiz function and running Javascript code in the browser function refer to the following source code.

> [1]	S. Shindemeshram (2019), django-quiz-app: It is django based quiz app for multiple choice questions. [Source code]. Available: https://github.com/sswapnil2/django-quiz-app.

> [2]	L.-V. Le (2020), code-editor-tutorial. [Source code]. Available: https://github.com/luvuong-le/code-editor-tutorial.

# Gallery
{{< gallery album="coding_sky_web_app" >}}
