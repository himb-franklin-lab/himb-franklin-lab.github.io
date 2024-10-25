---
# Display name
title: Dr. Erik C. Franklin
layout: "single"
slug: "erik-franklin"
avatar: /images/EF.jpg

# Full name (for SEO)
first_name: Erik
last_name: Franklin

#is this the primary user of the site?
superuser: true

# Role/position/tagline
role: Associate Research Professor

#Organizations
organizations:
    - name: Hawaii Institute of Marine Biology
      url: https://www.himb.hawaii.edu/
    - name: School of Ocean and Earth Science and Technology
      url: https://www.soest.hawaii.edu/soestwp/
    - name: University of Hawaii at Mānoa
      url: https://manoa.hawaii.edu/

# short bio
bio: Dr. Erik Franklin is an Associate Research Professor at the University of Hawai'i at Mānoa. His lab focuses on quantitative marine ecology, fisheries science, and ecological restoration, particularly within coral reef ecosystems. Collaborating with the NOAA Pacific Island Fisheries Science Center, the Franklin Lab conducts essential studies on marine population dynamics and habitats across the US Pacific, including the Hawaiian and Mariana archipelagos. His research also emphasizes applied ecological analysis to support sustainable marine resource management, leveraging empirical data and geospatial technologies. Dr. Franklin's collaborative efforts span local, state, and international partnerships, providing sound resource management solutions.

# Research interests
interests: 
   - Fisheries science
   - Quantitative ecology and ecoinformatics of coral reefs
   - Ecological restoration
   - Fish life history and population
   - Climate change

# Education
education:
  - area: Ph.D., Zoology, 2016
    institution: University of Hawaii at Mānoa
  - area: M.S., Marine Biology and Fisheries, 2004
    institution: University of Miami
  - area: B.S., Ecology, Behavior, and Evolution with a minor in Environmental Studies, 1996
    institution: University of California, San Diego

#Social
profiles:
  - icon: "fas fa-envelope" 
    url: 'mailto:erik.franklin@hawaii.edu'
    label: "Email"
  - icon: "fab fa-linkedin" 
    url: "https://www.linkedin.com/in/erikcfranklin"
    label: "LinkedIn"
  - icon: "ai ai-google-scholar" 
    url: "https://scholar.google.com/citations?user=aPMTCK8AAAAJ&hl=en"
    label: "Google Scholar"
  - icon: "ai ai-orcid" 
    url: "https://orcid.org/0000-0002-8660-3085"
    label: "ORCID"
  - icon: "ai ai-researchgate" 
    url: "https://www.researchgate.net/profile/Erik-Franklin"
    label: "ResearchGate"
  - icon: "ai ai-cv"  
    url: "/files/FranklinEC_cv_202410.pdf"
    label: "CV"
---
<!-- Include CSS for Font Awesome and Academicons -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/academicons@latest/css/academicons.min.css">

<ul class="network-icon" aria-hidden="true">
    {{ range .Params.profiles }}
    <li>
        <a href="{{ .url }}" target="_blank" rel="noopener" aria-label="{{ .label }}">
            <i class="{{ .icon }}"></i>
        </a>
    </li>
    {{ end }}
</ul>
