---
# Leave the homepage title empty to use the site title
title:
date: 2022-10-24
type: landing

sections:
  - block: hero
    content:
      title: |
        Welcome to the Franklin Lab!
      image:
        filename: team_selfie.JPG
      text: |
        <br>
        
        Take a look through our website to learn more about us and what we have been up to!

  - block: markdown
    content:
      title:
      subtitle:
      text: |
        {{% cta cta_link="./research/" cta_text="See what we do →" %}}
    design:
      columns: '1'
      background:
        image: 
          filename: mushroom_coral.webp
          filters:
            brightness: 1
          size: banner
  
  - block: collection
    content:
      title: Latest News
      subtitle:
      text:
      count: 5
      filters:
        folders: 
          - post
        author: ''
        category: ''
        exclude_featured: false
        publication_type: ''
        tag: ''
      offset: 0
      order: desc
      page_type: post
    design:
      view: card
      columns: '1'
  
  - block: markdown
    content:
      title:
      subtitle: ''
      text: |
          <div style="position: relative; display: inline-block;
               bottom: 5px; right: 5px; background-color: rgba(0,0,0,0.5); color: white; padding: 5px 8px; font-size: 12px; border-radius: 3px;">
                  Photo credit: [Andrew Shoemaker]
              </div>
          </div>
    design:
      columns: '1'
      background:
        image: 
          filename: kaneohe-bay.jpg
          filters:
            brightness: 1
          parallax: false
          position: center
          size: cover
          text_color_light: true
      spacing:
        padding: ['20px', '0', '20px', '0']
      css_class: fullscreen

---

<style>
  .cta {
  color: #ffffff; /* Change this to your desired text color */
  background-color: #008080; /* Change this to your desired background color */
  padding: 20px 20px; /* Optional: adjust padding */
  border-radius: 5px; /* Optional: rounded corners */
  text-decoration: none; /* Optional: remove underline */
}

/* Optional: Change color on hover */
.cta:hover {
  background-color: #1c8c99; /* Change to a darker shade for hover effect */
}
</style>