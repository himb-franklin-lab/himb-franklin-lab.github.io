---
# This is the front matter for Hugo

title: "Welcome to The Franklin Lab!"
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
        color: #ffffff;
        height: 100vh;
        padding: 20px;
        background-image: url('kaneohe-bay.jpg'); /* Ensure this path is correct */
        background-size: cover;
        background-position: center;
      }
      .hero .images {
        display: flex;
        justify-content: center;
        gap: 20px;
        margin-top: 20px;
      }
      .hero .images img {
        max-width: 100px;
        height: auto;
      }

  - block: markdown
    content:
      title: 
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
        justify-content: center;
        gap: 20px;
        margin-top: 40px;
        flex-wrap: wrap;
      }
      .cta-links .cta {
        display: inline-block;
        padding: 15px 25px;
        text-align: center;
        border-radius: 5px;
        text-decoration: none;
        color: white;
        font-size: 16px;
        background-size: cover;
        background-position: center;
        width: 150px;
        height: 150px;
        box-sizing: border-box;
      }
      /* Optional: Add background images for each CTA button */
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
