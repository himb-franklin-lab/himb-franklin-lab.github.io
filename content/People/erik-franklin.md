---
name: "Dr. Erik C. Franklin"
title: "Researcher"
image: "images/erik-franklin.jpg"  # Make sure to place the image in the correct path
description: "Expert in Marine Biology"
social:
  twitter: "https://twitter.com/erikcfranklin"
  linkedin: "https://www.linkedin.com/in/erikcfranklin"
draft: false
---
<div class="team-member">
    <img src="{{ .Params.image }}" alt="{{ .Params.name }}">
    <h3>{{ .Params.name }}</h3>
    <p>{{ .Params.description }}</p>
    <a href="{{ .Params.social.twitter }}" target="_blank">Twitter</a>
    <a href="{{ .Params.social.linkedin }}" target="_blank">LinkedIn</a>
    <p>Education:</p>
    <ul>
        <li><i class="graduation-cap-icon"></i> PhD in Marine Biology, University of XYZ</li>
        <li><i class="graduation-cap-icon"></i> MSc in Marine Science, University of ABC</li>
    </ul>
    <p>Research Interests:</p>
    <p>Marine conservation, ecosystem dynamics, and climate change impacts.</p>
</div>

