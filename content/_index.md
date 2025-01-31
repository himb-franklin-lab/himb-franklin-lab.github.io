---
# Leave the homepage title empty to use the site title
title:
date: 2022-10-24
type: landing

sections:
  - block: hero
    content:
      title: 
      text: |
        <div class="centered-text">
          <h1>Welcome to The Franklin Lab!</h1>
          <p>
            Hawaii Institute of Marine Biology<br>
            School of Ocean and Earth Science and Technology<br>
            University of Hawaii at Manoa
          </p>
        </div>
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
        color: #ffffff; /* White text color for contrast */
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
      css_class: cta-buttons-row

style: |
  .centered-text {
    text-align: center; /* Center the text horizontally */
    color: #ffffff; /* Ensure the text is white */
  } 

  h1 {
    font-size: 2.5rem; /* Adjust title size */
    margin-bottom: 1rem; /* Space below the title */
  }

  p {
    font-size: 1.2rem; /* Adjust the size of the paragraph */
    line-height: 1.5; /* Line height for readability */
  }

  .cta-buttons-row {
    display: flex;
    justify-content: space-between; /* Distribute buttons evenly */
    gap: 1rem; /* Add space between buttons */
    flex-wrap: wrap; /* Allow wrapping on smaller screens */
    background-color: rgb(43, 139, 57);
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