---
layout: about
title: about
permalink: /
subtitle: PhD in Mathematics · Analysis · PDE · Probability

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>Department of Mathematics</p>
    <p>University / Institute Name</p>
    <p>Email: your_email@domain.edu</p>

selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: true # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: true
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

I am a PhD researcher in mathematics, working on analysis, PDEs, and probability-inspired methods. My interests include regularity theory, geometric flows, and stochastic techniques in nonlinear equations.

My current projects focus on:

- nonlinear diffusion and entropy methods;
- variational formulations for PDE models;
- asymptotic behavior and stability in dissipative systems.

You can find publications on the [publications page](/publications/). The page is rendered from BibTeX in `_bibliography/papers.bib`.

This site supports LaTeX math directly in Markdown. For example:

<!-- Deployment note: this page intentionally includes MathJax examples. -->

$$
\partial_t u - \Delta u = f,\qquad u(0,x)=u_0(x),
$$

and an energy estimate:

$$
\frac{d}{dt}\int_{\Omega}\frac{|u|^2}{2}\,dx + \int_{\Omega}|\nabla u|^2\,dx
= \int_{\Omega}fu\,dx.
$$
