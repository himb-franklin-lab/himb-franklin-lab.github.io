---
title: Contact
date: 2024-10-10
authors:
  - erik-franklin
type: landing

sections:
  - block: contact
    content:
      title: Contact
      text: |-
        To contact the lab, please send in an inquiry using the form below, or reach out to the email listed below! 
      email: himb.franklin.lab@gmail.com
      address:
        street: 46-007 Lilipuna Rd
        city: Kaneohe
        region: HI
        postcode: '96744'
        country: United States
        country_code: US
      coordinates:
        latitude: '21.433400466507358'
        longitude: '-157.788233967327'
      appointment_url: 'https://calendly.com'
      #contact_links:
      #  - icon: comments
      #    icon_pack: fas
      #    name: Discuss on Forum
      #    link: 'https://discourse.gohugo.io'
    
      # Automatically link email and phone or display as text?
      autolink: true
    
      # Email form provider
      form:
        provider: netlify
        formspree:
          id:
        netlify:
          # Enable CAPTCHA challenge to reduce spam?
          captcha: false
    design:
      columns: '1'

  - block: markdown
    content:
      title:
      subtitle: ''
      text:
    design:
      columns: '1'
      background:
        image: 
          filename: /images/Papio.jpg
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
