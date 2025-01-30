---
# Leave the homepage title empty to use the site title
title:
date: 2022-10-24
type: landing

sections:
  - block: hero
    content:
      title: |
        Franklin Lab at HIMB
      text: |
        - Hawaii Institute of Marine Biology
        - School of Ocean and Earth Science and Technology
        - University of Hawaii at Manoa
      images: 
        - filename: /images/HIMB_Icon_White.png
        - filename: /images/SOEST_logo.jpg
        - filename: /images/manoaseal_logo.png
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
        position: relative;
        background-image: url('kaneohe-bay.jpg');
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
      } 
      .hero .images {
        display: flex;
        justify-content: center;
        gap: 20px; /* Space between images */
        margin-top: 20px; /* Space between text and images */
        position: relative;
        z-index: 2;
      }
      .hero .images img {
        max-width: 100px; /* Set max width for the images */
        height: auto;
        z-index: 3;
        position: relative;
      }

  - block: markdown
    content:
      title:
      subtitle:
      text: |
        <div class="cta-links">
          {{< cta cta_link="./about/" cta_text="About">}}
          {{< cta cta_link="./research/" cta_text="Research">}}
          {{< cta cta_link="./people/" cta_text="People">}}
          {{< cta cta_link="./publications/" cta_text="Publications">}}
          {{< cta cta_link="./resources/" cta_text="Resources">}}
          {{< cta cta_link="./want-to-join-us/" cta_text="Want to Join Us?">}}
        </div>
    style: |
      .cta-links {
        display: flex;
        flex-wrap: nowrap;
        justify-content: center; /* Centers the links horizontally */
        gap: 20px; /* Space between the links */
      }
      .cta-links .cta {
        display: inline-block;
        padding: 15px 25px;
        text-align: center;
        border-radius: 5px;
        text-decoration: none; /* No underline */
        color: #ffffff; /* Text color */
        font-size: 16px;
        flex: 0 1 auto; /* Ensure that each link takes up some space and is responsive */
        min-width: 150px;
        background-size: cover; /* Ensure background covers the whole element */
        background-position: center; /* Position background in the center */
      }
      /* Specific Background Images for Each CTA */
      .cta-links .cta:nth-child(1) {
        background-image: url('/images/Papio.jpeg'); 
      }
      .cta-links .cta:nth-child(2) {
        background-image: url('/images/Papio.jpeg');
      }
      .cta-links .cta:nth-child(3) {
        background-image: url('/images/Papio.jpeg');
      }
      .cta-links .cta:nth-child(4) {
        background-image: url('/images/Papio.jpeg');
      }
      .cta-links .cta:nth-child(5) {
        background-image: url('/images/Papio.jpeg');
      }
      .cta-links .cta:nth-child(6) {
        background-image: url('/images/Papio.jpeg');
      }
      .cta-links .cta:hover {
        opacity: 0.8;
      }
---