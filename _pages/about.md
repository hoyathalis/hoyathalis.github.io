---
permalink: /
title: "Welcome"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
news_and_updates:
  - date: "Sep 2024"
    organization: "Revent Solutions, Ashburn"
    url: "https://reventsolutions.com/"
    logo: "https://cdn.cmsfly.com/6601ca74197a880013d1b524/revent-solutions-logos-2-PD5-zQ.png"
    description: "Joined Revent Solutions as a Machine Learning Engineer Intern, focusing on building large-scale recommendation systems to enhance user experiences"

  - date: "Sep 2023"
    organization: "University Of California, Riverside"
    url: "https://ucr.edu"
    logo: "https://websites.ucr.edu/sites/default/files/styles/form_preview/public/logo-horizontal-on-white_0.png?itok=C8v1rbQR"
    description: "Pursuing a Master’s in Machine Learning to enhance my industry experience with advanced theoretical and practical knowledge."

  - date: "Feb 2023"
    organization: "Bluevoir Technologies"
    url: "https://bluevoir.com"
    logo: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR5G6V7WktZE2ATFZhEpXvzyiFY70CLzSPR2Q&s"
    description: "Joined Bluevoir Technologies as a Principal Engineer. Developed an ML-driven system with fine-tuned LLMs for real-time, context-aware clinical trial protocols. "
  
  - date: "Aug 2021"
    organization: "Goldman Sachs"
    url: "https://www.goldmansachs.com/"
    logo: "https://logowik.com/content/uploads/images/9675-goldman.webp"
    description: "Joined Goldman Sachs as an analyst. Contributed to the development of a machine learning system aimed at improving fraud detection and streamlining operations in financial transactions."
  
  - date: "July 2019"
    organization: "Pegasystems"
    url: "https://www.pegasystems.com/"
    logo: "https://www.pega.com/sites/default/files/styles/1024/public/media/images/2021-10/pega-logo-horiztonal-prevcard.png?itok=C5-EphPx"
    description: "Joined Pegasystems in July 2019. Addressed critical issues, preventing major downtime for key clients and avoiding significant revenue losses."

blogs:
  - date: ""
    title: "ML4LM-Content Based Recommendation Systems"
    url: "https://hoyath.medium.com/ml4lm-content-based-recommendation-systems-859c1c601ea1"
    logo: "https://miro.medium.com/v2/resize:fit:640/format:webp/1*rJVUd9vrk527wbcefVJAJw.png"
    description: "Explored content-based recommendation systems and demonstrated how embeddings and cosine similarity can be used to deliver personalized content recommendations."

  - date: ""
    title: "ML4LM- How does Lasso bring sparsity?"
    url: "https://hoyath.medium.com/ml4lm-how-does-lasso-bring-sparsity-29f3efe31ab3"
    logo: "https://miro.medium.com/v2/resize:fit:640/format:webp/1*1EfAhEVm8eW-tAgM8KW-eg.png"
    description: "Lasso regression: how its unique constraint shape brings sparsity by pushing coefficients to zero, simplifying models and fighting overfitting."

  - date: ""
    title: "ML4LM — RL — Making sense of Bellman EquationIntroduction"
    url: "https://hoyath.medium.com/making-sense-of-bellman-equation-rl-ml4lm-cd0e6fcc2098"
    logo: "https://miro.medium.com/v2/resize:fit:828/format:webp/1*LW-v8IKzwgIU-QKKaEfepw.png"
    description: "Unpacking the Bellman equations and their role in Reinforcement Learning"

---

**Hello! I’m Hoyath Ali**, a Master’s student in Computer Science at the [University of California, Riverside](https://www.ucr.edu/) 🎓, with over 3 years of experience in developing and deploying machine learning models. My work has spanned various domains, including optimizing operations and enhancing decision-making through data-driven solutions.

I specialize in building, fine-tuning, and deploying machine learning models, with a deep understanding of natural language processing (NLP), deep learning architectures, and real-time model monitoring. My expertise includes working with large language models (LLMs), optimizing algorithms for efficiency, and implementing scalable ML solutions using frameworks like [PyTorch](https://pytorch.org/), [Scikit-learn](https://scikit-learn.org/), and [Transformers](https://huggingface.co/transformers/). Additionally, I have hands-on experience deploying models in cloud environments with [AWS](https://aws.amazon.com/), [Docker](https://www.docker.com/), and [Kubernetes](https://kubernetes.io/), ensuring robust, production-grade performance.


## News and Updates

<table style="border-collapse: collapse; width: 100%; border: none;">
  {% for update in page.news_and_updates %}
  <tr>
    <td style="border: none;">
      <a href="{{ update.url }}">
        <img src="{{ update.logo }}" alt="{{ update.organization }}" style="width:150px; height:auto;">
      </a>
    </td>
    <td style="border: none;"> {{ update.date }} - {{ update.description }}</td>
  </tr>
  {% endfor %}
</table>

## Recent Blogs

<div style="width:100%; display: flex; flex-direction: column;">
  {% for update in page.blogs %}
  <div style="margin-bottom: 20px; border-bottom: 1px solid #ccc; padding: 10px 0;">
    <a href="{{ update.url }}" style="text-decoration: none; color: #000;">
      <div style="display: flex; align-items: center;">
        <img src="{{ update.logo }}" alt="{{ update.organization }}" style="width:100px; height:auto; margin-right: 20px;">
        <div>
          <h3>{{ update.date }}{{ update.title }}</h3>
          <p>{{ update.description }}</p>
        </div>
      </div>
    </a>
  </div>
  {% endfor %}
</div>

<a href= "https://hoyathalis.github.io/year-archive/"> click here for more</a>


