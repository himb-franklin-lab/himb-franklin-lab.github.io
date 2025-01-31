---
# Leave the homepage title empty to use the site title
title: 
date: 2022-10-24
type: landing

sections:
  - block: hero
    content:
      title: |
        Welcome to The Franklin Lab!
      text: |
        Hawaii Institute of Marine Biology
        School of Ocean and Earth Science and Technology
        University of Hawaii at Manoa
      images: 
        - filename: images/HIMB_Icon_White.png
        - filename: images/SOEST_logo.jpg
        - filename: images/manoaseal_logo.png
    style: |
      .hero {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-align: center;
        color: #ffffff; /* White text color for contrast */
        height: 100vh;
        padding: 20px;
      } 
      .hero .images {
        display: flex;
        justify-content: center;
        gap: 20px; /* Space between images */
        margin-top: 20px; /* Space between text and images */
      }
      .hero .images img {
        max-width: 100px; /* Set max width for the images */
        height: auto;
      }
    design: 
      background:
        image:
          filename: kaneohe-bay.jpg
          filters:
            brightness: 0.5
          size: cover
          position: center
          parallax: false
      css_class: fullscreen
---
