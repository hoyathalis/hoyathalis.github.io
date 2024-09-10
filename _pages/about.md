---
permalink: /
title: "Welcome"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
news_and_updates:
  - date: "Feb 2023"
    organization: "Bluevoir Technologies"
    url: "https://bluevoir.com"
    logo: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR5G6V7WktZE2ATFZhEpXvzyiFY70CLzSPR2Q&s"
    description: "Joined Bluevoir Technologies in February 2023. Developed an ML-driven system with fine-tuned LLMs for real-time, context-aware clinical trial protocols. Reduced protocol creation time by 30% and enhanced protocol quality by 40%."
  
  - date: "Aug 2021"
    organization: "Goldman Sachs"
    url: "https://www.goldmansachs.com/"
    logo: "https://logowik.com/content/uploads/images/9675-goldman.webp"
    description: "Joined Goldman Sachs as an analyst in August 2021. Developed a machine learning fraud detection system for credit card transactions, enhancing financial security and operational efficiency. Automated case routing and triggered actions, resulting in significant savings and a 25% reduction in costs."
  
  - date: "July 2019"
    organization: "Pegasystems"
    url: "https://www.pegasystems.com/"
    logo: "https://www.pega.com/sites/default/files/styles/1024/public/media/images/2021-10/pega-logo-horiztonal-prevcard.png?itok=C5-EphPx"
    description: "Joined Pegasystems in July 2019. Addressed critical issues, preventing major downtime for key clients and avoiding significant revenue losses."
---

Hello! I’m Hoyath Ali, a Master’s student in Computer Science at the <a href="https://www.ucr.edu/">University of California, Riverside</a> 🎓, with 3 years of experience in machine learning. My career has involved developing systems to enhance financial security and optimize clinical trial protocols.

I’m passionate about machine learning and deep learning, focusing on fine-tuning large language models (LLMs) and exploring retrieval-augmented generation (RAG). My technical skill set includes Python, JavaScript, and frameworks such as <a href="https://pytorch.org/">PyTorch</a>, <a href="https://scikit-learn.org/">Scikit-learn</a>, and <a href="https://huggingface.co/transformers/">Transformers</a>. I also have hands-on experience with <a href="https://aws.amazon.com/">AWS</a>, <a href="https://www.docker.com/">Docker</a>, and <a href="https://kubernetes.io/">Kubernetes</a> for real-time model monitoring and deployment.

## News and Updates

<table style="border-collapse: collapse; width: 100%; border: none;">
  {% for update in page.news_and_updates %}
  <tr>
    <td style="border: none;">
      <a href="{{ update.url }}">
        <img src="{{ update.logo }}" alt="{{ update.organization }}" style="width:500px; height:auto;">
      </a>
    </td>
    <td>{{ update.date }}</td>
    <td style="border: none;">{{ update.description }}</td>
  </tr>
  {% endfor %}
</table>
