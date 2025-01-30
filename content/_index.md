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
        
        Take a look through our website to learn more about us and what we have been up to!
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
        {{% cta cta_link="./research/" cta_text="See what we do →"%}}
    design:
      columns: '1'
      background:
        image: 
          filename: mushroom_coral.webp
          filters:
            brightness: 1
          size: banner
  
---

<style>
  .cta {
  color: #ffffff; /* Change this to your desired text color */
  background-color: #3bbcd9 /* Change this to your desired background color */
  padding: 20px 20px; /* Optional: adjust padding */
  border-radius: 5px; /* Optional: rounded corners */
  text-decoration: none; /* Optional: remove underline */
}

/* Optional: Change color on hover */
.cta:hover {
  background-color: #2a8ca3; /* Change to a darker shade for hover effect */
}
</style>