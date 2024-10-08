---
permalink: /
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

My name is Tang Zichen (汤子宸), an MPhil student in Data Science and Analytics (DSA) at The Hong Kong University of Science and Technology (Guangzhou). Under the supervision of Prof. Xiaowen Chu, my research explores MLsys and Federated Learning.

Before that, I obtained a Bachelor's degree in Engineering in Computer Science (BEng in COMP) from the Hong Kong University of Science and Technology (HKUST) with a double major in Mathematics.

## Education {#education}
- **MPhil in Data Science and Analytics**, HKUST (Guangzhou), 2023.09 - present
- **BEng in Computer Science with a double major in Mathematics**, HKUST, 2019.09 - 2023.06

## CV {#cv}
### Education
- **2023.09 - present**: MPhil student in Data Science and Analytics (DSA) at The Hong Kong University of Science and Technology (Guangzhou)
- **2019.09 - 2023.06**: Bachelor's degree in Computer Science with a double major in Mathematics from the Hong Kong University of Science and Technology (HKUST)

### Skills
- **Programming**: Python, Java, C++
- **Machine Learning**: TensorFlow, PyTorch
- **Distributed Systems**: LocalSGD, Federated Learning

### Awards
- **Outstanding Youth League Member**, Shanghai University of Finance and Economics

### Publications {#publications}
{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{ site.author.googlescholar }}">my Google Scholar profile</a>.</div>
{% endif %}

<ul>
  {% for post in site.publications reversed %}
    <li>{{ post.authors }}. <em>{{ post.title }}</em>. 
    {% if post.status == "Published" %}
      In {{ post.venue }} ({{ post.status }}), {{ post.date | date: "%Y-%m-%d" }}.
    {% else %}
      {{ post.venue }} - {{ post.status }}.
    {% endif %}
    </li>
  {% endfor %}
</ul>
