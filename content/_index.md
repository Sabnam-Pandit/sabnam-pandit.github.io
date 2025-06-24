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
       ####  Large Language Models for Similarity and Contradiction Analysis in Cardiovascular Research

        Utilized advanced language models like LLama 8B Instruct with in-context learning to extract facts, identify leading topics, and analyze similarities, contradictions, and connections across research abstracts. Applied cosine similarity analysis to identify coherence within leading topics in cardiovascular research.

       #### Animals audio Data Analysis 

       Transformed animals, insects and birds audio recordings into high-dimensional embeddings using Transformer models.  Investigating patterns in the embeddings with the help of unsupervised clustering algorithm to derive meaningful insights and trends based on analysis of cluster information and spectrogram of audio.
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
