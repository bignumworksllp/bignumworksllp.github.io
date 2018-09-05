---
layout: post
title: Template title
author: Harish Garg
date:   2018-08-01 13:32:30 +0530
categories: template
tags: [tag1]
published: true
---
{% if post.tags.size > 0 %}
  Tag{% if post.tags.size > 1 %}s{% endif %}:
  {{ post.tags | sort | join: ", " }}
{% endif %}
