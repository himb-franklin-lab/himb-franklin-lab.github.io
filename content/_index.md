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
        <br>
        Hawaii Institute of Marine Biology<br>
        School of Ocean and Earth Science and Technology<br>
        University of Hawaii at Manoa
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
    style: |
      .hero {
        height: 100vh; /* Makes the hero block full height */
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        color: white; /* White text color for contrast */
      }  

  - block: markdown
    content:
      title:
      subtitle:
      text: |
        {{% cta cta_link="./about/" cta_text="About"%}}
        {{% cta cta_link="./research/" cta_text="Research"%}}
        {{% cta cta_link="./people/" cta_text="People"%}}
        {{% cta cta_link="./publications/" cta_text="Publications"%}}
        {{% cta cta_link="./resources/" cta_text="Resources"%}}
        {{% cta cta_link="./want-to-join-us/" cta_text="Want to join us?"%}}
    design:
      columns: '6'
      background:
          background-color:rgb(43, 139, 57)
          filters:
            brightness: 1
          size: banner
      css_class: cta-buttons-row

style: |
  .cta-buttons-row {
    display: flex;
    justify-content: space-between; /* Distribute buttons evenly */
    gap: 1rem; /* Add space between buttons */
    flex-wrap: wrap; /* Allow wrapping on smaller screens */
  }

  .cta-buttons-row .cta {
    flex: 1 1 calc(16.666% - 1rem); /* Ensure each button takes up equal space in the row */
    text-align: center; /* Center text in each button */
    margin-bottom: 1rem; /* Add spacing below buttons */
  }

  @media (max-width: 768px) {
    .cta-buttons-row .cta {
      flex: 1 1 100%; /* Stack buttons on smaller screens */
    }
  }
  
---