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
        Hawaii Institute of Marine Biology<br>
        School of Ocean and Earth Science and Technology<br>
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
      
  - block: cta
    content:
      cta_buttons:
        - text: "Learn More"
          url: "/learn-more"
        - text: "Contact Us"
          url: "/contact-us"
    style: |
      .cta-section {
        background-color: #00bcd4; /* Blue background for CTA section */
        padding: 40px 20px; /* Add padding for top and bottom */
        text-align: center;
        color: white;
      }
      .cta-buttons {
        display: flex;
        justify-content: center;
        gap: 20px;
        margin-top: 20px;
      }
      .cta-buttons a {
        background-color: #ffffff; /* White button with blue text */
        color: #00bcd4; /* Blue text */
        text-decoration: none;
        padding: 15px 30px;
        font-size: 18px;
        border-radius: 30px;
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
        transition: background-color 0.3s ease, transform 0.3s ease;
      }
      .cta-buttons a:hover {
        background-color: #00bcd4; /* Blue background on hover */
        color: white; /* White text on hover */
        transform: translateY(-5px); /* Button lift effect */
      }
---
