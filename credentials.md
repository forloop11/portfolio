---
layout: default
title: Credentials
tagline: Certifications, course certificates, and skill assessments
description: Todd Takala's certifications, course certificates, and skill assessments.
---

[Back to home](./)

## Certifications

| Name | Issued By |
| ---  | ---       |
| [AWS Certified Machine Learning - Specialty (MLS-C01)](https://www.credly.com/badges/65a3c7d5-1977-4c71-94d6-2d016ea1fe29) | Amazon Web Services |
| [Lean Six Sigma Black Belt](https://www.coursera.org/account/accomplishments/specialization/3EOLHJ57IMRP) | Kennesaw State University |
| [SAFe 6 Agilist](https://www.credly.com/badges/a4c2f671-694e-46f5-bdd1-a1025d0e3b00) | SAFe by Scaled Agile, Inc. |
| Applied Failure Analysis | Caterpillar Inc. |
| Certified Technical Communicator | Komatsu North America |
| [Fundamentals of Flight Mechanics](https://www.coursera.org/account/accomplishments/specialization/VYE4OV5XDPW8) | ISAE - Supaero |
| [Semiconductor Packaging](https://www.coursera.org/account/accomplishments/specialization/AAGBCPUY6CW2) | Arizona State University |
| [Probabilistic Graphical Models](https://www.coursera.org/account/accomplishments/specialization/H2GYUKL51ESK) | Stanford University |
| [AI for Mechanical Engineers](https://www.coursera.org/account/accomplishments/specialization/5ADKOPJUDPHV) | University of Michigan |
| [Applied Python Data Engineering](https://www.coursera.org/account/accomplishments/specialization/TTKGZKR2MW48) | Duke University |
| [Data Engineering for AI and ML Pipelines](https://coursera.org/verify/specialization/KCO0GWKYWF44) | Edureka |
| [Advanced Deep Learning Specialist](https://www.credly.com/badges/c0442903-5f35-4a0f-8fa9-ec034ee3c092) | IBM |
| [RAG and Agentic AI](https://www.coursera.org/account/accomplishments/professional-cert/1XWIEFNB5MPF) | IBM |
| [Deep Learning with PyTorch, Keras and Tensorflow](https://www.coursera.org/account/accomplishments/professional-cert/O12BBM4K4R9L) | IBM |
| [Building AI Agents and Agentic Workflows](https://www.coursera.org/account/accomplishments/specialization/ELTSTT0PO1GQ) | IBM |
| [The Science of Happiness at Work](https://credentials.edx.org/credentials/139917b546984a14980b2d10f9684455/) | University of California, Berkeley |

## Course and Trade Certificates

| Certificate | Issued By |
| ---         | ---       |
{%- assign files = site.static_files | sort: "path" -%}
{%- for file in files -%}
{%- if file.path contains "/accomplishments/00" and file.extname == ".pdf" -%}
{%- assign parts = file.basename | split: " - " -%}
{%- comment -%} "NNNNNN - Issuer - Title"; without the second dash, the first word is the issuer. {%- endcomment -%}
{%- if parts.size > 2 -%}
{%- assign issuer = parts[1] -%}
{%- assign title = parts[2] -%}
{%- else -%}
{%- assign words = parts[1] | split: " " -%}
{%- assign issuer = words[0] -%}
{%- assign title = parts[1] | remove_first: issuer | strip -%}
{%- endif %}
| [{{ title | replace: "_", " " }}]({{ file.path | uri_escape | relative_url }}) | {{ issuer }} |
{%- endif -%}
{%- endfor %}

## DataCamp Skill Assessments

<div class="badges">
{%- for file in files -%}
{%- if file.path contains "/resources/" and file.extname == ".png" -%}
{%- unless file.path contains "/resources/projects/" %}
<img src="{{ file.path | uri_escape | relative_url }}" alt="{{ file.basename | replace: "_", " " }}">
{%- endunless -%}
{%- endif -%}
{%- endfor %}
</div>
