---
# Leave the homepage title empty to use the site title
title: ""
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: "6rem"

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
      text: ""
      # Show a call-to-action button under your biography? (optional)
      button:
        text: Download CV
        url: uploads/Resume2025.pdf
    design:
      css_class: text-black
      css_style: |
        .bio-text {
          color: #000000 !important;
          font-size: 1.25rem !important;
          position: relative;
        }
        .bio-text h2 {
          color: #000000 !important;
          font-size: 2rem !important;
        }
        .bio-text p {
          color: #000000 !important;
          font-size: 1.25rem !important;
        }
        .bio-text::before {
          content: '';
          position: absolute;
          top: 0;
          left: 0;
          width: 100%;
          height: 100%;
          background: rgba(0, 0, 0, 0.85);
          border-radius: 12px;
          z-index: 0;
          display: none;
        }
        .bio-text > * {
          position: relative;
          z-index: 1;
        }
        .portrait-title {
          color: #000000 !important;
        }
        .portrait-title h3 {
          color: #000000 !important;
        }
        .portrait-title div {
          color: #000000 !important;
        }
        @media (prefers-color-scheme: dark) {
          .bio-text, .bio-text h2, .bio-text p, .portrait-title, .portrait-title h3, .portrait-title div {
            color: #fff !important;
            text-shadow: 0 4px 24px rgba(0,0,0,1);
          }
          .bio-text::before {
            display: block;
          }
        }
      background:
        color: white
        image:
          filename: stacked-peaks.svg
          filters:
            brightness: 1.0
          size: cover
          position: center
          parallax: false
  - block: markdown
    content:
      title: '📚 My Research'
      subtitle: ''
      text: |-
       ###  Large Language Models for Similarity and Contradiction Analysis in Cardiovascular Research
       Cardiovascular disease research generates thousands of papers each year, making it challenging to track which studies align or contradict each other. My project explored how *large language models (LLMs)* can analyze medical literature to identify dominant topics, detect similarities and contradictions, and extract key facts from abstracts.

       ##### What I Did:
       - Grouped research papers into topics using *LDA (Gensim)* and tracked topic evolution.  
       - Used *LLMs (Llama, Orca, Gemini)* and *sentence embeddings* to compare abstracts and detect contradictions.  
       - Extracted structured facts from abstracts with *prompt engineering*, improving consistency and reliability.  
       - Visualized similarity distributions using *histograms and boxplots* to reveal patterns across topics.
       
       ##### Key Insights:
       - Contradictions within topics were rare; papers often explore different angles of the same topic.  
       - Topic cohesion varies—“risk factors” were more aligned, “gene expression” more diverse.  
       - Larger models and carefully crafted prompts produce more accurate results.

       ##### Tools & Skills:
       Python (Pandas, NLTK, Matplotlib), Gensim, SentenceTransformers, LLMs, NLP preprocessing, data visualization, prompt engineering.


       ### 🌿 Exploring Biodiversity in the Peruvian Jungle with Machine Learning
       This project focused on analyzing the rich soundscape of the Peruvian Amazon using machine learning. By transforming hours of raw audio into high-dimensional vector embeddings with the Animal2Vec transformer model, we were able to cluster animal vocalizations without needing labeled data. The goal was to uncover hidden patterns in biodiversity, such as species behavior and daily activity rhythms, through unsupervised learning.
       
       ##### What I Did:
       I implemented and analyzed K-means clustering on the audio embeddings. My main contributions included:
       - Running clustering experiments and selecting the optimal number of clusters using the Elbow method.
       - Comparing regular K-means with Mini-Batch K-means to improve scalability and efficiency.
       - Visualizing results with UMAP projections, making it easier to interpret how clusters grouped similar sounds.- Analyzing time-of-day activity patterns across clusters to reveal ecological trends.

       ##### Key Insights:
       - K-means identified broad patterns: It grouped similar acoustic features into 20 well-separated clusters, effectively capturing recurring vocalization types across recordings.
       - Efficiency matters: Mini-batch K-means significantly reduced computation time while maintaining cluster quality, proving useful for large-scale datasets.
       - Behavioral patterns emerged: Some clusters revealed species-specific activity rhythms (e.g., midday vocalizations), while others grouped rare sounds such as snore-like or background noises.
       
       Compared to HDBSCAN, K-means was better at capturing general soundscape structures, while HDBSCAN excelled at identifying rare or localized events.
       
       ##### Tools & Skills:
       Python (scikit-learn, NumPy, pandas) – clustering and preprocessing
       UMAP & t-SNE – dimensionality reduction for visualization
       matplotlib & plotly – plots and cluster visualizations
       librosa & torchaudio – audio analysis and spectrograms
       Streamlit – for interactive exploration of clusters 

       Our Project Website:
       <a href="https://sites.google.com/sdsu.edu/soundscape-analysis/home" target="_blank" style="display:inline-block;padding:10px 20px;background:#007ACC;color:#fff;border-radius:8px;text-decoration:none;">
       🌱 Visit Soundscape Analysis Project
       </a>

    design:
      columns: '1'

  - block: collection
    content:
      title: "Featured Projects"
      text: "These are some of my favorite projects - where I combined data, code, and creativity to solve meaningful problems."
      filters:
        folders:
          - project
      count: 6
    design:
      view: article-grid
      fill_image: false
      columns: 3

  - block: markdown
    content:
      title: "Skills & Hobbies"
      text: |
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
          <div>
            <h3 class="font-bold text-lg mb-4">Technical Skills</h3>
            <ul class="list-none pl-0 space-y-2">
              <li class="flex items-center"><span class="mr-2">{{< icon name="brain-circuit" >}}</span> Machine Learning</li>
              <li class="flex items-center"><span class="mr-2">{{< icon name="microchip" >}}</span> Deep Learning</li>
              <li class="flex items-center"><span class="mr-2">{{< icon name="chart-line" >}}</span> Data Science</li>
              <li class="flex items-center"><span class="mr-2">{{< icon name="database" >}}</span> SQL</li>
              <li class="flex items-center"><span class="mr-2">{{< icon name="code" >}}</span> Python</li>
              <li class="flex items-center"><span class="mr-2">{{< icon name="chart-bar" >}}</span> Tableau</li>
            </ul>
          </div>
          <div>
            <h3 class="font-bold text-lg mb-4">Hobbies</h3>
            <ul class="list-none pl-0 space-y-2">
              <li class="flex items-center"><span class="mr-2">{{< icon name="custom/hiking" >}}</span> Hiking</li>
              <li class="flex items-center"><span class="mr-2">{{< icon name="custom/travelling" >}}</span> Travelling</li>
              <li class="flex items-center"><span class="mr-2">{{< icon name="custom/working-out" >}}</span> Working Out</li>
              <li class="flex items-center"><span class="mr-2">{{< icon name="custom/dancing" >}}</span> Dancing</li>
            </ul>
          </div>
        </div>
---
