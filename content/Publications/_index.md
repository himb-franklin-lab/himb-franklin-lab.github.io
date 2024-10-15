---
title: Publications
authors:
  - erik-franklin

# Optional banner image (relative to `assets/media/` folder).
#banner:
  #caption: ''
  #image: ''
---
(* = Franklin lab student, + = other student)
<!-- Inline CSS for modal -->
<style>
    .modal {
        display: none; /* Hidden by default */
        position: fixed; /* Stay in place */
        z-index: 1; /* Sit on top */
        left: 0;
        top: 0;
        width: 100%; /* Full width */
        height: 100%; /* Full height */
        overflow: auto; /* Enable scroll if needed */
        transition: ease;
        background-color: rgb(0, 0, 0); /* Fallback color */
        background-color: rgba(0, 0, 0, 0.4); /* Black w/ opacity */
    }

    .modal-content {
       background-color: #fefefe;
       margin: 15% auto; /* 15% from the top and centered */
       padding: 20px;
       border: 1px solid #888;
       width: 80%; /* Could be more or less, depending on screen size */
       display: flex; /* Use flexbox for alignment */
       flex-direction: column; /* Align items in a column */
}

   .modal-buttons {
       display: flex; /* Use flexbox to align buttons */
       justify-content: space-between; /* Space between buttons */
       margin-top: 10px; /* Space above buttons */
}

    .close {
        color: #aaa;
        float: right;
        font-size: 28px;
        font-weight: bold;
    }

    .close:hover,
    .close:focus {
        color: black;
        text-decoration: none;
        cursor: pointer;
    }

    /* New button styles */
    .button-outline {
        background-color: transparent; /* Clear background */
        border: 2px solid teal; /* Blue outline */
        color: teal; /* Text color */
        padding: 8px 12px; /* Padding for the button */
        border-radius: 4px; /* Rounded corners */
        cursor: pointer; /* Pointer cursor on hover */
        transition: background-color 0.3s, color 0.3s; /* Transition effect */
        text-decoration: none; /* Remove underline */
        display: inline-block; /* Ensure proper alignment */
        margin-right: 10px;
    }

    .button-outline:hover {
        background-color: teal; /* Background color on hover */
        color: white; /* Text color on hover */
    }
</style>

<!-- Search bars and filters -->
<div style="display: flex; align-items: center; margin-bottom: 20px;">
    <!-- Search Bar -->
    <input type="text" id="searchBar" placeholder="Search..." onkeyup="searchCitations()" style="padding: 10px; width: 100%; max-width: 300px; margin-right: 20px; border: 1px solid #ccc; border-radius: 5px; height: 50px; font-size: 16px;">

   <!-- Drop down filter for type -->
   <select id="filter" onchange="filterPublications()" style="padding: 10px; width: 100%; max-width: 200px; margin-right: 20px; border: 1px solid #ccc; border-radius: 5px; height: 50px; font-size: 16px;">
        <option value="all">Type</option>
        <option value="journal">Journal Articles</option>
        <option value="book">Book Sections</option>
        <option value="report">Technical Reports</option>
        <option value="conference">Conferences</option>
    </select>

   <!-- Drop down filter for year -->
   <select id="yearFilter" onchange="filterPublications()" style="padding: 10px; width: 100%; max-width: 150px; border: 1px solid #ccc; border-radius: 5px; height: 50px; font-size: 16px;">
        <option value="all">Year</option>
        <option value="2023">2023</option>
        <option value="2022">2022</option>
        <option value="2021">2021</option>
        <option value="2020">2020</option>
        <option value="2019">2019</option>
        <option value="2018">2018</option>
        <option value="2017">2017</option>
        <option value="2016">2016</option>
        <option value="2015">2015</option>
        <option value="2014">2014</option>
        <option value="2013">2013</option>
        <option value="2012">2012</option>
        <option value="2011">2011</option>
        <option value="2010">2010</option>
        <option value="2009">2009</option>
        <option value="2008">2008</option>
        <option value="2007">2007</option>
        <option value="2006">2006</option>
        <option value="2005">2005</option>
        <option value="2004">2004</option>
        <option value="2003">2003</option>
        <option value="2002">2002</option>
        <option value="2001">2001</option>
        <!-- Add more years as needed -->
    </select>
</div>

<!-- Single Modal Template -->
<div id="citationModal" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre id="citationText"></pre>
        <button class="button-outline" onclick="copyToClipboard('citationText')">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation('citationText')">
            <img src="path/to/download-icon.png" alt="Download" style="vertical-align: middle; width: 16px; height: 16px;">
            Download Citation
        </button>
    </div>
</div>




<!-- Citations -->
<div class="publication-entry journal 2023">
    Franklin EC, Platt MT*, Andrade P (accepted). Increased occurrence of the rare golden color morph of Pacific chub Kyphosus sandwicensis in a no-take marine reserve. <em>Journal of Fish Biology</em>. <a href="https://doi.org/10.1111/jfb.15644">doi:10.1111/jfb.15644</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('franklin2023')">Cite</a>
  <a href="https://doi.org/10.1111/jfb.15644" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="franklin2023" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{franklin_2023,
  author = {Franklin, E.C. and Platt, M.T. and Andrade, P.},
  title = {Increased occurrence of the rare golden color morph of Pacific chub Kyphosus sandwicensis in a no-take marine reserve},
  journal = {Journal of Fish Biology},
  year = {accepted},
  doi = {10.1111/jfb.15644},
  url = {https://doi.org/10.1111/jfb.15644}
}
       </pre>
       <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
       <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2023">
    Winans WR+, Chen Q, Qiang Y, Franklin EC (2023). Large-area automatic detection of shoreline stranded marine debris using deep learning. <em>International Journal of Applied Earth Observation and Geoinformation</em>. <a href="https://doi.org/10.1016/j.jag.2023.103515">doi:10.1016/j.jag.2023.103515</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('winans2023')">Cite</a>
  <a href="https://doi.org/10.1016/j.jag.2023.103515" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="winans2023" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{winans_2023,
  author = {Winans, W.R. and Chen, Q. and Qiang, Y. and Franklin, E.C.},
  title = {Large-area automatic detection of shoreline stranded marine debris using deep learning},
  journal = {International Journal of Applied Earth Observation and Geoinformation},
  year = {2023},
  doi = {10.1016/j.jag.2023.103515},
  url = {https://doi.org/10.1016/j.jag.2023.103515}
}
      </pre>
      <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
      <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2023">
    Purwanto, Franklin EC, Mardiani SR, White AT (2023). Multiple-goal bioeconomic programming to address conflicting management objectives in Indonesian small pelagic fisheries. <em>Marine Policy</em> 150: 105519. <a href="https://doi.org/10.1016/j.marpol.2023.105519">doi:10.1016/j.marpol.2023.105519</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('purwanto2023')">Cite</a>
  <a href="https://doi.org/10.1016/j.marpol.2023.105519" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="purwanto2023" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{purwanto_2023,
  author = {Purwanto and Franklin, E.C. and Mardiani, S.R. and White, A.T.},
  title = {Multiple-goal bioeconomic programming to address conflicting management objectives in Indonesian small pelagic fisheries},
  journal = {Marine Policy},
  volume = {150},
  pages = {105519},
  year = {2023},
  doi = {10.1016/j.marpol.2023.105519},
  url = {https://doi.org/10.1016/j.marpol.2023.105519}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2022">
    Carlson KM, Mora C, Xu J+, Setter RO+, Harangody M+, Franklin EC, Kantar MB, Lucas M, Menzo ZM+, Spirandelli D, Schanzenbach D, Warr CC, Wong AE+, Businger S (2022). Global rainbow distribution under current and future climates. <em>Global Environmental Change</em> 77: 102604. <a href="https://doi.org/10.1016/j.gloenvcha.2022.102604">doi:10.1016/j.gloenvcha.2022.102604</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('carlson2022')">Cite</a>
  <a href="https://doi.org/10.1016/j.gloenvcha.2022.102604" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="carlson2022" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{carlson_2022,
  author = {Carlson, K.M. and Mora, C. and Xu, J. and Setter, R.O. and Harangody, M. and Franklin, E.C. and Kantar, M.B. and Lucas, M. and Menzo, Z.M. and Spirandelli, D. and Schanzenbach, D. and Warr, C.C. and Wong, A.E. and Businger, S.},
  title = {Global rainbow distribution under current and future climates},
  journal = {Global Environmental Change},
  volume = {77},
  pages = {102604},
  year = {2022},
  doi = {10.1016/j.gloenvcha.2022.102604},
  url = {https://doi.org/10.1016/j.gloenvcha.2022.102604}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2022">
    Setter RO+, Franklin EC, Mora C (2022). Co-occurring anthropogenic stressors reduce the timeframe of environmental viability for the world’s coral reefs. <em>PLoS Biology</em> 20: e3001821. <a href="https://doi.org/10.1371/journal.pbio.3001821">doi:10.1371/journal.pbio.3001821</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('setter2022')">Cite</a>
  <a href="https://doi.org/10.1371/journal.pbio.3001821" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="setter2022" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{setter_2022,
  author = {Setter, R.O. and Franklin, E.C. and Mora, C.},
  title = {Co-occurring anthropogenic stressors reduce the timeframe of environmental viability for the world’s coral reefs},
  journal = {PLoS Biology},
  volume = {20},
  pages = {e3001821},
  year = {2022},
  doi = {10.1371/journal.pbio.3001821},
  url = {https://doi.org/10.1371/journal.pbio.3001821}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2022">
    Barkley YM*, Sakai T, Oleson EM, Franklin EC (2022). Examining distribution patterns of foraging and non-foraging sperm whales in Hawaiian waters using visual and passive acoustic data. <em>Frontiers in Remote Sensing</em> 3: 940186. <a href="https://doi.org/10.3389/frsen.2022.940186">doi:10.3389/frsen.2022.940186</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('barkley2022')">Cite</a>
  <a href="https://doi.org/10.3389/frsen.2022.940186" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="barkley2022" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{barkley_2022,
  author = {Barkley, Y.M. and Sakai, T. and Oleson, E.M. and Franklin, E.C.},
  title = {Examining distribution patterns of foraging and non-foraging sperm whales in Hawaiian waters using visual and passive acoustic data},
  journal = {Frontiers in Remote Sensing},
  volume = {3},
  pages = {940186},
  year = {2022},
  doi = {10.3389/frsen.2022.940186},
  url = {https://doi.org/10.3389/frsen.2022.940186}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2022">
    Akiona AK*, Popp BN, Toonen RJ, Siple MC, Kotubetey K, Kawelo H, Franklin EC (2022). Predatory fish diets shift toward an invasive mullet in a traditional Hawaiian aquaculture system. <em>Aquaculture, Fish and Fisheries</em>. <a href="https://doi.org/10.1002/aff2.68">doi:10.1002/aff2.68</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('akiona2022')">Cite</a>
  <a href="https://doi.org/10.1002/aff2.68" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="akiona2022" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{akiona_2022,
  author = {Akiona, A.K. and Popp, B.N. and Toonen, R.J. and Siple, M.C. and Kotubetey, K. and Kawelo, H. and Franklin, E.C.},
  title = {Predatory fish diets shift toward an invasive mullet in a traditional Hawaiian aquaculture system},
  journal = {Aquaculture, Fish and Fisheries},
  year = {2022},
  doi = {10.1002/aff2.68},
  url = {https://doi.org/10.1002/aff2.68}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2022">
    Mora C, McKenzie T, Gaw IM+, Dean JM+, von Hammerstein H+, Knudson TA+, Setter RO+, Smith CZ+, Webster KM+, Patz JA, Franklin EC (2022). Over half of known human pathogenic diseases can be aggravated by climate change. <em>Nature Climate Change</em> 12: 869-875. <a href="https://doi.org/10.1038/s41558-022-01426-1">doi:10.1038/s41558-022-01426-1</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('mora2022')">Cite</a>
  <a href="https://doi.org/10.1038/s41558-022-01426-1" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="mora2022" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{mora_2022,
  author = {Mora, C. and McKenzie, T. and Gaw, I.M. and Dean, J.M. and von Hammerstein, H. and Knudson, T.A. and Setter, R.O. and Smith, C.Z. and Webster, K.M. and Patz, J.A. and Franklin, E.C.},
  title = {Over half of known human pathogenic diseases can be aggravated by climate change},
  journal = {Nature Climate Change},
  volume = {12},
  pages = {869--875},
  year = {2022},
  doi = {10.1038/s41558-022-01426-1},
  url = {https://doi.org/10.1038/s41558-022-01426-1}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2022">
    Nichols RS*, DeMartini EE, Franklin EC (2022). No butts about it: using urogenital disparity in a deep water snapper, <em>Etelis carbunculus</em> (Lutjanidae), for field based sexual identification. <em>Journal of Fish Biology</em>. <a href="https://doi.org/10.1111/jfb.15166">doi:10.1111/jfb.15166</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('nichols2022')">Cite</a>
  <a href="https://doi.org/10.1111/jfb.15166" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="nichols2022" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{nichols_2022,
  author = {Nichols, R.S. and DeMartini, E.E. and Franklin, E.C.},
  title = {No butts about it: using urogenital disparity in a deep water snapper, Etelis carbunculus (Lutjanidae), for field based sexual identification},
  journal = {Journal of Fish Biology},
  year = {2022},
  doi = {10.1111/jfb.15166},
  url = {https://doi.org/10.1111/jfb.15166}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2022">
    Andrade P, Morishige K, Mau A, Kapono L, Franklin EC (2022). Re-imagining contemporary conservation to support ʻĀina Momona: Productive and thriving communities of people, place, and natural resources. <em>Parks Stewardship Forum</em> 38: 186–198. <a href="https://doi.org/10.5070/P538257511">doi: 10.5070/P538257511</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('andrade2022')">Cite</a>
  <a href="https://doi.org/10.5070/P538257511" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="andrade2022" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{andrade_2022,
  author = {Andrade, P. and Morishige, K. and Mau, A. and Kapono, L. and Franklin, E.C.},
  title = {Re-imagining contemporary conservation to support ʻĀina Momona: Productive and thriving communities of people, place, and natural resources},
  journal = {Parks Stewardship Forum},
  volume = {38},
  pages = {186--198},
  year = {2022},
  doi = {10.5070/P538257511},
  url = {https://doi.org/10.5070/P538257511}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2022">
    Purwanto, Franklin EC, Mardiani SR, White AT (2022). Stock assessment and overexploitation risk of small pelagic fish in Fisheries Management Area 715 of Indonesia. <em>Asian Fisheries Science</em> 35: 76-89. <a href="https://doi.org/10.33997/j.afs.2022.35.1.007">doi:10.33997/j.afs.2022.35.1.007</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('purwanto2022')">Cite</a>
  <a href="https://doi.org/10.33997/j.afs.2022.35.1.007" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="purwanto2022" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{purwanto_2022,
  author = {Purwanto and Franklin, E.C. and Mardiani, S.R. and White, A.T.},
  title = {Stock assessment and overexploitation risk of small pelagic fish in Fisheries Management Area 715 of Indonesia},
  journal = {Asian Fisheries Science},
  volume = {35},
  pages = {76--89},
  year = {2022},
  doi = {10.33997/j.afs.2022.35.1.007},
  url = {https://doi.org/10.33997/j.afs.2022.35.1.007}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2022">
    Jaya I, Satria F, Wudianto, Nugroho D, Sadiyah L, Buchary EA, White AT, Franklin EC, Courtney CA, Green G, Green S (2022). Are the working principles of fisheries management at work in Indonesia? <em>Marine Policy</em> 140: 105047. <a href="https://doi.org/10.1016/j.marpol.2022.105047">doi:10.1016/j.marpol.2022.105047</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('jaya2022')">Cite</a>
  <a href="https://doi.org/10.1016/j.marpol.2022.105047" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="jaya2022" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{jaya_2022,
  author = {Jaya, I. and Satria, F. and Wudianto and Nugroho, D. and Sadiyah, L. and Buchary, E.A. and White, A.T. and Franklin, E.C. and Courtney, C.A. and Green, G. and Green, S.},
  title = {Are the working principles of fisheries management at work in Indonesia?},
  journal = {Marine Policy},
  volume = {140},
  pages = {105047},
  year = {2022},
  doi = {10.1016/j.marpol.2022.105047},
  url = {https://doi.org/10.1016/j.marpol.2022.105047}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2022">
    Longenecker K, Franklin EC, Hill-Lewenilovo R+, Lalavanua W, Langston R, Mangubhai, Piovano S (2022). Many immature individuals and largest size classes lacked females from three coral reef fishes (Actinopterygii) in Fiji market surveys: Implications for fishery management. <em>Acta Ichthyologica et Piscatoria</em> 52: 53-65. <a href="https://doi.org/10.3897/aiep.52.80586">doi:10.3897/aiep.52.80586</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('longenecker2022')">Cite</a>
  <a href="https://doi.org/10.3897/aiep.52.80586" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="longenecker2022" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{longenecker_2022,
  author = {Longenecker, K. and Franklin, E.C. and Hill-Lewenilovo, R. and Lalavanua, W. and Langston, R. and Mangubhai and Piovano, S.},
  title = {Many immature individuals and largest size classes lacked females from three coral reef fishes (Actinopterygii) in Fiji market surveys: Implications for fishery management},
  journal = {Acta Ichthyologica et Piscatoria},
  volume = {52},
  pages = {53--65},
  year = {2022},
  doi = {10.3897/aiep.52.80586},
  url = {https://doi.org/10.3897/aiep.52.80586}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2022">
    Johannsen T+, Franklin EC, Hunter CL (2022). A short-term winner? Dramatic increases in the population of mushroom coral <em>Lobactis scutaria</em> (Anthozoa: Fungiidae) in Kaneohe Bay, Hawaii from 2000 to 2018. <em>Pacific Science</em> 76: 79-93. <a href="https://doi.org/10.2984/76.1.7">doi:10.2984/76.1.7</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('johannsen2022')">Cite</a>
  <a href="https://doi.org/10.2984/76.1.7" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="johansen2022" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{johannsen_2022,
  author = {Johannsen, T. and Franklin, E.C. and Hunter, C.L.},
  title = {A short-term winner? Dramatic increases in the population of mushroom coral Lobactis scutaria (Anthozoa: Fungiidae) in Kaneohe Bay, Hawaii from 2000 to 2018},
  journal = {Pacific Science},
  volume = {76},
  pages = {79--93},
  year = {2022},
  doi = {10.2984/76.1.7},
  url = {https://doi.org/10.2984/76.1.7}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2022">
    Counsell CWW+, Coleman RR+, Lal SS+, Bowen BW, Franklin EC, Neuheimer AB, Powell BS, Toonen RJ, Donahue MJ, Hixon MA, McManus MA (2022). Interdisciplinary analysis of larval dispersal for a coral reef fish: opening the black box. <em>Marine Ecology Progress Series</em> 684: 117-132. <a href="https://doi.org/10.3354/meps13971">doi: 10.3354/meps13971</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('counsell2022')">Cite</a>
  <a href="https://doi.org/10.3354/meps13971" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="counsell2022" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{counsell_2022,
  author = {Counsell, C.W.W. and Coleman, R.R. and Lal, S.S. and Bowen, B.W. and Franklin, E.C. and Neuheimer, A.B. and Powell, B.S. and Toonen, R.J. and Donahue, M.J. and Hixon, M.A. and McManus, M.A.},
  title = {Interdisciplinary analysis of larval dispersal for a coral reef fish: opening the black box},
  journal = {Marine Ecology Progress Series},
  volume = {684},
  pages = {117--132},
  year = {2022},
  doi = {10.3354/meps13971},
  url = {https://doi.org/10.3354/meps13971}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2022">
    Limmon GV, Longenecker KL, Langston R, Franklin EC (2022). Capacity development in reproductive life history studies of tropical fishes in Ambon, Maluku, Indonesia for data-limited fisheries. <em>Marine Policy</em> 136: 104948. <a href="https://doi.org/10.1016/j.marpol.2021/104948">doi: 10.1016/j.marpol.2021/104948</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('limmon2022')">Cite</a>
  <a href="https://doi.org/10.1016/j.marpol.2021/104948" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="limmon2022" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{limmon_2022,
  author = {Limmon, G.V. and Longenecker, K.L. and Langston, R. and Franklin, E.C.},
  title = {Capacity development in reproductive life history studies of tropical fishes in Ambon, Maluku, Indonesia for data-limited fisheries},
  journal = {Marine Policy},
  volume = {136},
  pages = {104948},
  year = {2022},
  doi = {10.1016/j.marpol.2021/104948},
  url = {https://doi.org/10.1016/j.marpol.2021/104948}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry 2022">
    Hixon MA, Bowen BW, Coleman RR+, Counsell CW+, Donahue MJ, Franklin EC, Kittinger JN, McManus MA, Toonen RJ (2022). Fish flow: following fisheries from spawning to supper. <em>Frontiers in Ecology and the Environment</em> 20: 247-254. <a href="https://doi.org/10.1002/fee.2449">doi: 10.1002/fee.2449</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('hixon2022')">Cite</a>
  <a href="https://doi.org/10.1002/fee.2449" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="hixon2022" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{hixon_2022,
  author = {Hixon, M.A. and Bowen, B.W. and Coleman, R.R. and Counsell, C.W. and Donahue, M.J. and Franklin, E.C. and Kittinger, J.N. and McManus, M.A. and Toonen, R.J.},
  title = {Fish flow: following fisheries from spawning to supper},
  journal = {Frontiers in Ecology and the Environment},
  volume = {20},
  pages = {247--254},
  year = {2022},
  doi = {10.1002/fee.2449},
  url = {https://doi.org/10.1002/fee.2449}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2021">
    Mau A+, Franklin EC, Huss GR, Nagashima K, Nicodemus P, Valdez A, Bingham J-P (2021). Near-daily reconstruction of tropical intertidal SST from limpet shells to infer their growth rates. <em>Nature Communications Earth & Environment</em> 2, 171. <a href="https://doi.org/10.1038/s43247-021-00251-2">doi: 10.1038/s43247-021-00251-2</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('mau2021')">Cite</a>
  <a href="https://doi.org/10.1038/s43247-021-00251-2" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="mau2021" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{mau_2021,
  author = {Mau, A. and Franklin, E.C. and Huss, G.R. and Nagashima, K. and Nicodemus, P. and Valdez, A. and Bingham, J.-P.},
  title = {Near-daily reconstruction of tropical intertidal SST from limpet shells to infer their growth rates},
  journal = {Nature Communications Earth & Environment},
  volume = {2},
  pages = {171},
  year = {2021},
  doi = {10.1038/s43247-021-00251-2},
  url = {https://doi.org/10.1038/s43247-021-00251-2}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2021">
    Carlson B, Awai M, Saunders WB, Franklin EC (2021). Nautilus belauensis population demographics and trap yields in Palau were similar between surveys in 1982 and 2015. <em>Marine Ecology Progress Series</em> 670: 239-245. <a href="https://doi.org/10.3354/meps13773">doi: 10.3354/meps13773</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('carlson2021')">Cite</a>
  <a href="https://doi.org/10.3354/meps13773" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="carlson2021" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{carlson_2021,
  author = {Carlson, B. and Awai, M. and Saunders, W.B. and Franklin, E.C.},
  title = {Nautilus belauensis population demographics and trap yields in Palau were similar between surveys in 1982 and 2015},
  journal = {Marine Ecology Progress Series},
  volume = {670},
  pages = {239--245},
  year = {2021},
  doi = {10.3354/meps13773},
  url = {https://doi.org/10.3354/meps13773}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2021">
    Gill A+, Franklin EC, Donaldson TJ (2021). Fore reef location influences spawning success and egg predation in lek-like mating territories of the bird wrasse Gomphosus varius. <em>Journal of Fish Biology</em>. <a href="https://doi.org/10.1007/s10641-021-01084-w">doi: 10.1007/s10641-021-01084-w</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('gill2021')">Cite</a>
  <a href="https://doi.org/10.1007/s10641-021-01084-w" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="gill2021" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{gill_2021,
  author = {Gill, A. and Franklin, E.C. and Donaldson, T.J.},
  title = {Fore reef location influences spawning success and egg predation in lek-like mating territories of the bird wrasse Gomphosus varius},
  journal = {Journal of Fish Biology},
  year = {2021},
  doi = {10.1007/s10641-021-01084-w},
  url = {https://doi.org/10.1007/s10641-021-01084-w}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2021">
    Altman-Kurosaki NT*, Smith CM, Franklin EC (2021). Oahu's marine protected areas have limited success in protecting coral reef herbivore functional assemblages. <em>Coral Reefs</em>. <a href="https://doi.org/10.1007/s00338-021-02054-5">doi: 10.1007/s00338-021-02054-5</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('altman2021')">Cite</a>
  <a href="https://doi.org/10.1007/s00338-021-02054-5" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="altman2021" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{altman_2021,
  author = {Altman-Kurosaki, N.T. and Smith, C.M. and Franklin, E.C.},
  title = {Oahu's marine protected areas have limited success in protecting coral reef herbivore functional assemblages},
  journal = {Coral Reefs},
  year = {2021},
  doi = {10.1007/s00338-021-02054-5},
  url = {https://doi.org/10.1007/s00338-021-02054-5}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2021">
    Scherrer SR+, Kobayashi DR, Weng KC, Okamoto HY, Oishi FG, Franklin EC (2021). Estimation of growth parameters integrating tag-recapture, length-frequency, and direct aging data using likelihood and Bayesian methods for the tropical deepwater snapper *Pristipomoides filamentous* in Hawaii. <em>Fisheries Research</em> 233: 105753. <a href="https://doi.org/10.1016/j.fishres.2020.105753">doi: 10.1016/j.fishres.2020.105753</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('scherrer2021')">Cite</a>
  <a href="https://doi.org/10.1016/j.fishres.2020.105753" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="scherrer2021" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{scherrer_2021,
  author = {Scherrer, S.R. and Kobayashi, D.R. and Weng, K.C. and Okamoto, H.Y. and Oishi, F.G. and Franklin, E.C.},
  title = {Estimation of growth parameters integrating tag-recapture, length-frequency, and direct aging data using likelihood and Bayesian methods for the tropical deepwater snapper *Pristipomoides filamentous* in Hawaii},
  journal = {Fisheries Research},
  volume = {233},
  pages = {105753},
  year = {2021},
  doi = {10.1016/j.fishres.2020.105753},
  url = {https://doi.org/10.1016/j.fishres.2020.105753}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2020">
    Longenecker K, Langston R, Gill A+, Kelokelo M+, Donaldson TJ, Franklin EC (2020). Rapid reproductive analysis and weight-length relation of the humpnose big-eye bream <em>Monotaxis grandoculis</em> (Actinopterygii: Perciformes: Lethrinidae) from Micronesia with implications for fisheries. <em>Acta Ichthyologica et Piscatoria</em> 50(4): 493–500. <a href="https://doi.org/10.3750/AIEP/02965">doi: 10.3750/AIEP/02965</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('longenecker2020')">Cite</a>
  <a href="https://doi.org/10.3750/AIEP/02965" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="longenecker2020" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{longenecker_2020,
  author = {Longenecker, K. and Langston, R. and Gill, A. and Kelokelo, M. and Donaldson, T.J. and Franklin, E.C.},
  title = {Rapid reproductive analysis and weight-length relation of the humpnose big-eye bream \emph{Monotaxis grandoculis} (Actinopterygii: Perciformes: Lethrinidae) from Micronesia with implications for fisheries},
  journal = {Acta Ichthyologica et Piscatoria},
  volume = {50},
  number = {4},
  pages = {493--500},
  year = {2020},
  doi = {10.3750/AIEP/02965},
  url = {https://doi.org/10.3750/AIEP/02965}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2020">
    Winter KB, Rii YM, Reppun FAWL, Hintzen KD, Alegado R, Bowen BW, Bremer LL, Coffman M, Deenik JL, Donahue MJ, Falinski FA, Frank K, Franklin EC, Kurashima N, Lincoln NK, Madin E, McManus MA, Nelson CE, Okano R, Olegario A, Pascua P, Oleson KLL, Price MR, Rivera MAJ, Rodgers KS, Ticktin T, Sabine C, Smith CM, Hewett A, Kaluhiwa R, Cypher M, Thomas B, Leong J, Kekuewa K, Tanimoto J, Kukea-Shultz K, Kawelo H, Kotubetey K, Neilson B, Lee T, Toonen RJ (2020). Collaborative research to inform adaptive co-management: A framework for the Heʻeia National Estuarine Research Reserve. <em>Ecology and Society</em> 25(4): 15. <a href="https://doi.org/10.5751/ES-11895-27750415">doi: 10.5751/ES-11895-27750415</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('winter2020')">Cite</a>
  <a href="https://doi.org/10.5751/ES-11895-27750415" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="winter2020" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{winter_2020,
  author = {Winter, K.B. and Rii, Y.M. and Reppun, F.A.W.L. and Hintzen, K.D. and Alegado, R. and Bowen, B.W. and Bremer, L.L. and Coffman, M. and Deenik, J.L. and Donahue, M.J. and Falinski, F.A. and Frank, K. and Franklin, E.C. and Kurashima, N. and Lincoln, N.K. and Madin, E. and McManus, M.A. and Nelson, C.E. and Okano, R. and Olegario, A. and Pascua, P. and Oleson, K.L.L. and Price, M.R. and Rivera, M.A.J. and Rodgers, K.S. and Ticktin, T. and Sabine, C. and Smith, C.M. and Hewett, A. and Kaluhiwa, R. and Cypher, M. and Thomas, B. and Leong, J. and Kekuewa, K. and Tanimoto, J. and Kukea-Shultz, K. and Kawelo, H. and Kotubetey, K. and Neilson, B. and Lee, T. and Toonen, R.J.},
  title = {Collaborative research to inform adaptive co-management: A framework for the Heʻeia National Estuarine Research Reserve},
  journal = {Ecology and Society},
  volume = {25},
  number = {4},
  pages = {15},
  year = {2020},
  doi = {10.5751/ES-11895-27750415},
  url = {https://doi.org/10.5751/ES-11895-27750415}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2020">
    Winter KB, Lincoln NK, Berkes F, Kawelo H, Kotubetey K, Kukea-Shultz K, Alegado R, Kurashima N, Frank K, Pascua P, Rii Y, Reppun F, Knapp I, McClatchey W, Ticktin T, Smith C, Franklin EC, Oleson K, Price M, McManus M, Donahue M, Rodgers K, Bowen B, Nelson C, Beilson B, Thomas B, Leong J-A, Madin E, Rivera MA, Falinski K, Bremer L, Deenik J, Gon III S, Okano R, Olegario A, Toonen R (2020). Eco-mimicry in indigenous resource management: optimizing ecosystem services to achieve resource abundance in Hawai'i. <em>Ecology and Society</em> 25: 26. <a href="https://doi.org/10.5751/ES-11539-250226">doi: 10.5751/ES-11539-250226</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('winter2020b')">Cite</a>
  <a href="https://doi.org/10.5751/ES-11539-250226" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="winter2020b" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{winter_2020,
  author = {Winter, K.B. and Lincoln, N.K. and Berkes, F. and Kawelo, H. and Kotubetey, K. and Kukea-Shultz, K. and Alegado, R. and Kurashima, N. and Frank, K. and Pascua, P. and Rii, Y. and Reppun, F. and Knapp, I. and McClatchey, W. and Ticktin, T. and Smith, C. and Franklin, E.C. and Oleson, K. and Price, M. and McManus, M. and Donahue, M. and Rodgers, K. and Bowen, B. and Nelson, C. and Beilson, B. and Thomas, B. and Leong, J.A. and Madin, E. and Rivera, M.A. and Falinski, K. and Bremer, L. and Deenik, J. and Gon III, S. and Okano, R. and Olegario, A. and Toonen, R.},
  title = {Eco-mimicry in indigenous resource management: optimizing ecosystem services to achieve resource abundance in Hawai'i},
  journal = {Ecology and Society},
  volume = {25},
  pages = {26},
  year = {2020},
  doi = {10.5751/ES-11539-250226},
  url = {https://doi.org/10.5751/ES-11539-250226}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2020">
    Oyafuso ZS*, Leung PS, Franklin EC (2020). Evaluating biological and socioeconomic tradeoffs of marine reserve planning via a flexible integer linear programming approach. <em>Biological Conservation</em> 241: 108319. <a href="https://doi.org/10.1016/j.biocon.2019.108319">doi: 10.1016/j.biocon.2019.108319</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('oyafuso2020')">Cite</a>
  <a href="https://doi.org/10.1016/j.biocon.2019.108319" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="oyafuso2020" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{oyafuso_2020,
  author = {Oyafuso, Z.S. and Leung, P.S. and Franklin, E.C.},
  title = {Evaluating biological and socioeconomic tradeoffs of marine reserve planning via a flexible integer linear programming approach},
  journal = {Biological Conservation},
  volume = {241},
  pages = {108319},
  year = {2020},
  doi = {10.1016/j.biocon.2019.108319},
  url = {https://doi.org/10.1016/j.biocon.2019.108319}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2019">
    Franklin EC, Gray AE, Mundy BC (2019). Three new records of coastal fishes in the Hawaiian Islands. <em>Journal of the Ocean Science Foundation</em> 33: 99–106. <a href="https://doi.org/10.5281/zenodo.3572888">doi: 10.5281/zenodo.3572888</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('franklin2019')">Cite</a>
  <a href="https://doi.org/10.5281/zenodo.3572888" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="franklin2019" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{franklin_2019,
  author = {Franklin, E.C. and Gray, A.E. and Mundy, B.C.},
  title = {Three new records of coastal fishes in the Hawaiian Islands},
  journal = {Journal of the Ocean Science Foundation},
  volume = {33},
  pages = {99--106},
  year = {2019},
  doi = {10.5281/zenodo.3572888},
  url = {https://doi.org/10.5281/zenodo.3572888}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>

<div class="publication-entry journal 2019">
    Barkley YM*, Oleson EM, Oswald JN, Franklin EC (2019). Whistle classification of sympatric false killer whale populations in Hawaiian waters yields low accuracy rates. <em>Frontiers in Marine Science</em> 6: 645. <a href="https://doi.org/10.3389/fmars.2019.00645">doi: 10.3389/fmars.2019.00645</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('barkley2019')">Cite</a>
  <a href="https://doi.org/10.3389/fmars.2019.00645" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="barkley2019" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{barkley_2019,
  author = {Barkley, Y.M. and Oleson, E.M. and Oswald, J.N. and Franklin, E.C.},
  title = {Whistle classification of sympatric false killer whale populations in Hawaiian waters yields low accuracy rates},
  journal = {Frontiers in Marine Science},
  volume = {6},
  pages = {645},
  year = {2019},
  doi = {10.3389/fmars.2019.00645},
  url = {https://doi.org/10.3389/fmars.2019.00645}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2019">
    Mora C, Rollins R+, Taladay K+, Kantar M, Chock M+, Shimada M+, Franklin EC (2019). Mora et al. reply. <em>Nature Climate Change</em> 9: 658-659. <a href="https://doi.org/10.1038/s41558-019-0538-1">doi: 10.1038/s41558-019-0538-1</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('mora2019')">Cite</a>
  <a href="https://doi.org/10.1038/s41558-019-0538-1" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="mora2019" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{mora_2019,
  author = {Mora, C. and Rollins, R. and Taladay, K. and Kantar, M. and Chock, M. and Shimada, M. and Franklin, E.C.},
  title = {Mora et al. reply},
  journal = {Nature Climate Change},
  volume = {9},
  pages = {658-659},
  year = {2019},
  doi = {10.1038/s41558-019-0538-1},
  url = {https://doi.org/10.1038/s41558-019-0538-1}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2019">
    Darling ES, McClanahan TR, Maina J, Gurney G, Graham NAJ, Januchowski-Hartley F, Cinner JE, Mora C, Hicks CC, Maire E, Puotinen M, Skirving WJ, Adjeroud M, Ahmadia G, Arthur R, Bauman AG, Beger M, Berumen ML, Bigot L, Bouwmeester, Brenier, Bridge T, Brown E, Campbell SJ, Cannon S, Cauvin B, Chen AC, Claudet J, Denis V, Donner S, Estradivari, Fadli N, Feary DA, Fenner D, Fox H, Franklin EC, Friedlander A, Gilmour J, Goiran C, Guest J, Hobbs, J-PA, Hoey AS, Houk P, Johnson S, Jupiter S, Kayal M, Kuo C-Y, Lamb J, Lee MAC, Low J, Muthiga N, Muttaqin, Nand Y, Nash KL, Nedlic O, Pandolfi JM, Pardede S, Patankar V, Penin L, Ribas-Deulofeu L, Richards Z, Roberts TE, Rodgers KS, Safuari CDM, Sala E, Shedrawi G, Sin TM, Smallhorn-West P, Smith JE, Sommer B, Steinberg PD, Sutthacheep M, Tan CHJ, Williams GJ, Wilson S, Yeemin T, Bruno JF, Fortin MJ, Krkosek M, Mouillot D (2019). Social-environmental drivers inform strategic management of coral reefs in the Anthropocene. <em>Nature Ecology and Evolution</em> 3: 1341–1350. <a href="https://doi.org/10.1038/s41559-019-0953-8">doi: 10.1038/s41559-019-0953-8</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('darling2019')">Cite</a>
  <a href="https://doi.org/10.1038/s41559-019-0953-8" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="darling2019" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{darling_2019,
  author = {Darling, E.S. and McClanahan, T.R. and Maina, J. and Gurney, G. and Graham, N.A.J. and Januchowski-Hartley, F. and Cinner, J.E. and Mora, C. and Hicks, C.C. and Maire, E. and Puotinen, M. and Skirving, W.J. and Adjeroud, M. and Ahmadia, G. and Arthur, R. and Bauman, A.G. and Beger, M. and Berumen, M.L. and Bigot, L. and Bouwmeester and Brenier and Bridge, T. and Brown, E. and Campbell, S.J. and Cannon, S. and Cauvin, B. and Chen, A.C. and Claudet, J. and Denis, V. and Donner, S. and Estradivari and Fadli, N. and Feary, D.A. and Fenner, D. and Fox, H. and Franklin, E.C. and Friedlander, A. and Gilmour, J. and Goiran, C. and Guest, J. and Hobbs, J-PA and Hoey, A.S. and Houk, P. and Johnson, S. and Jupiter, S. and Kayal, M. and Kuo, C-Y and Lamb, J. and Lee, M.A.C. and Low, J. and Muthiga, N. and Muttaqin and Nand, Y. and Nash, K.L. and Nedlic, O. and Pandolfi, J.M. and Pardede, S. and Patankar, V. and Penin, L. and Ribas-Deulofeu, L. and Richards, Z. and Roberts, T.E. and Rodgers, K.S. and Safuari, C.D.M. and Sala, E. and Shedrawi, G. and Sin, T.M. and Smallhorn-West, P. and Smith, J.E. and Sommer, B. and Steinberg, P.D. and Sutthacheep, M. and Tan, C.H.J. and Williams, G.J. and Wilson, S. and Yeemin, T. and Bruno, J.F. and Fortin, M.J. and Krkosek, M. and Mouillot, D.},
  title = {Social-environmental drivers inform strategic management of coral reefs in the Anthropocene},
  journal = {Nature Ecology and Evolution},
  volume = {3},
  pages = {1341–1350},
  year = {2019},
  doi = {10.1038/s41559-019-0953-8},
  url = {https://doi.org/10.1038/s41559-019-0953-8}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2019">
    Randall JE, Gray A, Franklin EC, Mundy BC, McCosker JE (2019). Five new records of fishes for the Hawaiian Islands. <em>Journal of Ocean Science Foundation</em> 33: 28-43. <a href="http://dx.doi.org/10.5281/zenodo.3255089">doi: 10.5281/zenodo.3255089</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('randall2019')">Cite</a>
  <a href="http://dx.doi.org/10.5281/zenodo.3255089" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="randall2019" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{randall_2019,
  author = {Randall, J.E. and Gray, A. and Franklin, E.C. and Mundy, B.C. and McCosker, J.E.},
  title = {Five new records of fishes for the Hawaiian Islands},
  journal = {Journal of Ocean Science Foundation},
  volume = {33},
  pages = {28-43},
  year = {2019},
  doi = {10.5281/zenodo.3255089},
  url = {http://dx.doi.org/10.5281/zenodo.3255089}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2019">
    Johnson GB+, Taylor BM, Robbins WD, Franklin EC, Toonen R, Bowen BW, Choat JH (2019). Diversity and structure of parrotfish assemblages across the northern Great Barrier Reef. <em>Diversity</em> 11(1):14. <a href="doi.org/10.3390/d11010014">doi: 10.3390/d11010014</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('johnson2019')">Cite</a>
  <a href="doi.org/10.3390/d11010014" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="johnson2019" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{johnson_2019,
  author = {Johnson, G.B. and Taylor, B.M. and Robbins, W.D. and Franklin, E.C. and Toonen, R. and Bowen, B.W. and Choat, J.H.},
  title = {Diversity and structure of parrotfish assemblages across the northern Great Barrier Reef},
  journal = {Diversity},
  volume = {11},
  number = {1},
  pages = {14},
  year = {2019},
  doi = {10.3390/d11010014},
  url = {doi.org/10.3390/d11010014}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2018">
    Oyafuso ZS*, Leung PS, Franklin EC (2018). Evaluating bioeconomic tradeoffs of fishing reserves via spatial optimization. <em>Marine Policy</em>. <a href="doi.org/10.1016/j.marpol.2018.11.016">doi: 10.1016/j.marpol.2018.11.016</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('oyafuso2018')">Cite</a>
  <a href="doi.org/10.1016/j.marpol.2018.11.016" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="oyafuso2018" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{oyafuso_2018,
  author = {Oyafuso, Z.S. and Leung, P.S. and Franklin, E.C.},
  title = {Evaluating bioeconomic tradeoffs of fishing reserves via spatial optimization},
  journal = {Marine Policy},
  year = {2018},
  doi = {10.1016/j.marpol.2018.11.016},
  url = {doi.org/10.1016/j.marpol.2018.11.016}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2018">
    Mora C, Spirandelli D, Franklin EC, Lynham J, Kantar MB, Miles W, Smith CZ+, Freel K, Moy J+, Louis LV+, Barba EW+, Bettinger K, Frazier AG, Colburn IX JF+, Hanasaki N, Hawkins E, Hirabayashi Y, Knorr W, Little CM, Emanuel K, Sheffield J, Patz JA, Hunter CL (2018). Broad threat to humanity from cumulative climate hazards intensified by greenhouse gas emissions. <em>Nature Climate Change</em> 8: 1062-1071. <a href="https://doi.org/10.1038/s41558-018-0315-6">doi: 10.1038/s41558-018-0315-6</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('mora2018')">Cite</a>
  <a href="https://doi.org/10.1038/s41558-018-0315-6" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="mora2018" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{mora_2018,
  author = {Mora, C. and Spirandelli, D. and Franklin, E.C. and Lynham, J. and Kantar, M.B. and Miles, W. and Smith, C.Z. and Freel, K. and Moy, J. and Louis, L.V. and Barba, E.W. and Bettinger, K. and Frazier, A.G. and Colburn, I.X. J.F. and Hanasaki, N. and Hawkins, E. and Hirabayashi, Y. and Knorr, W. and Little, C.M. and Emanuel, K. and Sheffield, J. and Patz, J.A. and Hunter, C.L.},
  title = {Broad threat to humanity from cumulative climate hazards intensified by greenhouse gas emissions},
  journal = {Nature Climate Change},
  year = {2018},
  volume = {8},
  pages = {1062-1071},
  doi = {10.1038/s41558-018-0315-6},
  url = {https://doi.org/10.1038/s41558-018-0315-6}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2018">
    Mora C, Rollins R+, Taladay K+, Kantar MB, Chock MK+, Shimada M+, Franklin EC (2018). Bitcoin emissions alone could push global warming above 2°C. <em>Nature Climate Change</em> 8: 931-933. <a href="https://doi.org/10.1038/s41558-018-0321-8">doi: 10.1038/s41558-018-0321-8</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('mora2018b')">Cite</a>
  <a href="https://doi.org/10.1038/s41558-018-0321-8" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="mora2018b" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{mora_2018_b,
  author = {Mora, C. and Rollins, R. and Taladay, K. and Kantar, M.B. and Chock, M.K. and Shimada, M. and Franklin, E.C.},
  title = {Bitcoin emissions alone could push global warming above 2°C},
  journal = {Nature Climate Change},
  year = {2018},
  volume = {8},
  pages = {931-933},
  doi = {10.1038/s41558-018-0321-8},
  url = {https://doi.org/10.1038/s41558-018-0321-8}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2018">
    Geronimo, R+, Franklin EC, Brainard RE, Elvidge CD, Santos MD, Venegas R, Mora C (2018). Mapping fishing activities and suitable fishing grounds using nighttime satellite images and maximum entropy modelling. <em>Remote Sensing</em> 10: 1604. <a href="https://doi.org/10.3390/rs10101064">doi: 10.3390/rs10101064</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('geronimo2018')">Cite</a>
  <a href="https://doi.org/10.3390/rs10101064" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="geronimo2018" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{geronimo_2018,
  author = {Geronimo, R. and Franklin, E.C. and Brainard, R.E. and Elvidge, C.D. and Santos, M.D. and Venegas, R. and Mora, C.},
  title = {Mapping fishing activities and suitable fishing grounds using nighttime satellite images and maximum entropy modelling},
  journal = {Remote Sensing},
  year = {2018},
  volume = {10},
  pages = {1604},
  doi = {10.3390/rs10101064},
  url = {https://doi.org/10.3390/rs10101064}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2018">
    Forsman ZH, Maurin P, Parry M, Chung A+, Sartor C, Hixon MA, Hughes K, Rodgers K, Knapp I, Gulko DA, Franklin EC, Del Rio Torres L, Chan NT, Wolke CS, Gates RD, Toonen RJ (2018). The First Hawai‘i Workshop For Coral Restoration & Nurseries. <em>Marine Policy</em> 96: 133-135. <a href="https://doi.org/10.1016/j.marpol.2018.08.009">doi: 10.1016/j.marpol.2018.08.009</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('forsman2018')">Cite</a>
  <a href="https://doi.org/10.1016/j.marpol.2018.08.009" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="forsman2018" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{forsman_2018,
  author = {Forsman, Z.H. and Maurin, P. and Parry, M. and Chung, A. and Sartor, C. and Hixon, M.A. and Hughes, K. and Rodgers, K. and Knapp, I. and Gulko, D.A. and Franklin, E.C. and Del Rio Torres, L. and Chan, N.T. and Wolke, C.S. and Gates, R.D. and Toonen, R.J.},
  title = {The First Hawai‘i Workshop For Coral Restoration & Nurseries},
  journal = {Marine Policy},
  year = {2018},
  volume = {96},
  pages = {133-135},
  doi = {10.1016/j.marpol.2018.08.009},
  url = {https://doi.org/10.1016/j.marpol.2018.08.009}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2018">
    Counsell CWW+, Donahue MJ, Edwards K, Franklin EC, Hixon MA (2018). Variation in coral-associated cryptofaunal communities along spatial scales and environmental gradients. <em>Coral Reefs</em> 37: 827-840. <a href="https://doi.org/10.1007/s00338-018-1709-7">doi: 10.1007/s00338-018-1709-7</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('counsell2018')">Cite</a>
  <a href="https://doi.org/10.1007/s00338-018-1709-7" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="counsell2018" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{counsell_2018,
  author = {Counsell, C.W.W. and Donahue, M.J. and Edwards, K. and Franklin, E.C. and Hixon, M.A.},
  title = {Variation in coral-associated cryptofaunal communities along spatial scales and environmental gradients},
  journal = {Coral Reefs},
  year = {2018},
  volume = {37},
  pages = {827-840},
  doi = {10.1007/s00338-018-1709-7},
  url = {https://doi.org/10.1007/s00338-018-1709-7}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2018">
    Levy J+, Hunter C, Lukaczyk, Franklin EC (2018). Assessing the spatial distribution of coral bleaching using small unmanned aerial systems. <em>Coral Reefs</em> 37: 373-387. <a href="https://doi.org/10.1007/s00338-018-1662-5">doi: 10.1007/s00338-018-1662-5</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('levy2018')">Cite</a>
  <a href="https://doi.org/10.1007/s00338-018-1662-5" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="levy2018" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{levy_2018,
  author = {Levy, J. and Hunter, C. and Lukaczyk and Franklin, E.C.},
  title = {Assessing the spatial distribution of coral bleaching using small unmanned aerial systems},
  journal = {Coral Reefs},
  year = {2018},
  volume = {37},
  pages = {373-387},
  doi = {10.1007/s00338-018-1662-5},
  url = {https://doi.org/10.1007/s00338-018-1662-5}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2017">
    Franklin EC (2017). Vagrancy in paradise: documentation of the chevron butterflyfish *Chaetodon trifascialis* in Kaneohe Bay, Oahu, Hawaiian Islands. <em>Marine Biodiversity Records</em> 10:22. <a href="https://doi.org/10.1186/s41200-017-0124-z">doi: 10.1186/s41200-017-0124-z</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('franklin2017')">Cite</a>
  <a href="https://doi.org/10.1186/s41200-017-0124-z" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="franklin2017" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{franklin_2017,
  author = {Franklin, E.C.},
  title = {Vagrancy in paradise: documentation of the chevron butterflyfish Chaetodon trifascialis in Kaneohe Bay, Oahu, Hawaiian Islands},
  journal = {Marine Biodiversity Records},
  year = {2017},
  volume = {10},
  pages = {22},
  doi = {10.1186/s41200-017-0124-z},
  url = {https://doi.org/10.1186/s41200-017-0124-z}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2017">
    Longenecker K, Langston R, Bolick H, Crane M, Donaldson TJ, Franklin EC, Kelokelo M, Kondio U, Potuku T (2017). Rapid reproductive analysis and length–weight relations for five species of coral-reef fishes from Papua New Guinea: *Nemipterus isacanthus*, *Parupeneus barberinus*, *Kyphosus cinerascens*, *Ctenochaetus striatus*, and *Balistapus undulatus*. <em>Acta Ichthyologica et Piscatoria</em> 47:107-124. <a href="https://doi.org/10.3750/AIEP/02146">doi: 10.3750/AIEP/02146</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('longenecker2017')">Cite</a>
  <a href="https://doi.org/10.3750/AIEP/02146" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="longenecker2017" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{longenecker_2017,
  author = {Longenecker, K. and Langston, R. and Bolick, H. and Crane, M. and Donaldson, T.J. and Franklin, E.C. and Kelokelo, M. and Kondio, U. and Potuku, T.},
  title = {Rapid reproductive analysis and length–weight relations for five species of coral-reef fishes from Papua New Guinea: Nemipterus isacanthus, Parupeneus barberinus, Kyphosus cinerascens, Ctenochaetus striatus, and Balistapus undulatus},
  journal = {Acta Ichthyologica et Piscatoria},
  year = {2017},
  volume = {47},
  pages = {107-124},
  doi = {10.3750/AIEP/02146},
  url = {https://doi.org/10.3750/AIEP/02146}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2017">
    Oyafuso ZS*, Drazen JC, Moore CH, Franklin EC (2017). Habitat-based species distribution modelling of the Hawaiian deepwater snapper-grouper complex. <em>Fisheries Research</em> 195: 19-27. <a href="https://doi.org/10.1016/j.fishres.2017.06.011">doi: 10.1016/j.fishres.2017.06.011</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('oyafuso2017')">Cite</a>
  <a href="https://doi.org/10.1016/j.fishres.2017.06.011" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="oyafuso2017" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{oyafuso_2017,
  author = {Oyafuso, Z.S. and Drazen, J.C. and Moore, C.H. and Franklin, E.C.},
  title = {Habitat-based species distribution modelling of the Hawaiian deepwater snapper-grouper complex},
  journal = {Fisheries Research},
  year = {2017},
  volume = {195},
  pages = {19-27},
  doi = {10.1016/j.fishres.2017.06.011},
  url = {https://doi.org/10.1016/j.fishres.2017.06.011}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2017">
    Winston MS*, Taylor B, Franklin EC (2017). Intraspecific variability in the life history of endemic coral reef fishes between photic and mesophotic populations. <em>Coral Reefs</em> 36: 663-674. <a href="https://doi.org/10.1007/s00338-017-1559-8">doi: 10.1007/s00338-017-1559-8</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('winston2017')">Cite</a>
  <a href="https://doi.org/10.1007/s00338-017-1559-8" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="winston2017" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{winston_2017,
  author = {Winston, M.S. and Taylor, B. and Franklin, E.C.},
  title = {Intraspecific variability in the life history of endemic coral reef fishes between photic and mesophotic populations},
  journal = {Coral Reefs},
  year = {2017},
  volume = {36},
  pages = {663-674},
  doi = {10.1007/s00338-017-1559-8},
  url = {https://doi.org/10.1007/s00338-017-1559-8}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2017">
    Kapur MR*, Franklin EC (2017). Predicting climate impacts on tropical fisheries: are contemporary spatial management strategies sufficient? <em>Canadian Journal of Fisheries and Aquatic Sciences</em>. <a href="https://doi.org/10.1139/cjfas-2016-0200">doi: 10.1139/cjfas-2016-0200</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('kapur2017')">Cite</a>
  <a href="https://doi.org/10.1139/cjfas-2016-0200" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="kapur2017" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{kapur_2017,
  author = {Kapur, M.R. and Franklin, E.C.},
  title = {Predicting climate impacts on tropical fisheries: are contemporary spatial management strategies sufficient?},
  journal = {Canadian Journal of Fisheries and Aquatic Sciences},
  year = {2017},
  doi = {10.1139/cjfas-2016-0200},
  url = {https://doi.org/10.1139/cjfas-2016-0200}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2016">
    Veazey LM+, Franklin EC, Kelley C, Rooney J, Frazer NL, Toonen RJ (2016). The implementation of rare events logistic regression to predict the distribution of mesophotic hard corals across the main Hawaiian Islands. <em>PeerJ</em> 4:e2189. <a href="https://doi.org/10.7717/peerj.2189">doi: 10.7717/peerj.2189</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('veazey2016')">Cite</a>
  <a href="https://doi.org/10.7717/peerj.2189" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="veazey2016" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{veazey_2016,
  author = {Veazey, L.M. and Franklin, E.C. and Kelley, C. and Rooney, J. and Frazer, N.L. and Toonen, R.J.},
  title = {The implementation of rare events logistic regression to predict the distribution of mesophotic hard corals across the main Hawaiian Islands},
  journal = {PeerJ},
  year = {2016},
  volume = {4},
  article_number = {e2189},
  doi = {10.7717/peerj.2189},
  url = {https://doi.org/10.7717/peerj.2189}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2016">
    Selkoe KA, Gaggiotti OE, Donovan MK+, Treml EA, Wren JLK+, Hawai‘i Reef Connectivity Consortium†, Toonen RJ (2016). The DNA of coral reef biodiversity – predicting and protecting genetic diversity of reef assemblages. <em>Proceedings of the Royal Society B</em> 283: 20160354. <a href="https://doi.org/10.1098/rspb.2016.0354">doi: 10.1098/rspb.2016.0354</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('selkoe2016')">Cite</a>
  <a href="https://doi.org/10.1098/rspb.2016.0354" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="selkoe2016" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{selkoe_2016,
  author = {Selkoe, K.A. and Gaggiotti, O.E. and Donovan, M.K. and Treml, E.A. and Wren, J.L.K. and Hawai‘i Reef Connectivity Consortium and Toonen, R.J.},
  title = {The DNA of coral reef biodiversity – predicting and protecting genetic diversity of reef assemblages},
  journal = {Proceedings of the Royal Society B},
  year = {2016},
  volume = {283},
  article_number = {20160354},
  doi = {10.1098/rspb.2016.0354},
  url = {https://doi.org/10.1098/rspb.2016.0354}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2016">
    Oyafuso ZS*, Toonen RJ, Franklin EC (2016). Temporal and spatial trends in prey diversity of wahoo (<em>Acanthocybium solandri</em>): A diet analysis from the central North Pacific using visual and DNA bar-coding techniques. <em>Journal of Fish Biology</em> 88:1501-1523. <a href="https://doi.org/10.1111/jfb.12928">doi:10.1111/jfb.12928</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('oyafuso2016')">Cite</a>
  <a href="https://doi.org/10.1111/jfb.12928" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="oyafuso2016" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{oyafuso_2016,
  author = {Oyafuso, Z.S. and Toonen, R.J. and Franklin, E.C.},
  title = {Temporal and spatial trends in prey diversity of wahoo (Acanthocybium solandri): A diet analysis from the central North Pacific using visual and DNA bar-coding techniques},
  journal = {Journal of Fish Biology},
  year = {2016},
  volume = {88},
  pages = {1501-1523},
  doi = {10.1111/jfb.12928},
  url = {https://doi.org/10.1111/jfb.12928}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2016">
    Madin JS, Andreasen M, Bridge T, Connolly SR, Darling E, Diaz M, Falster D, Franklin EC, Gates RD, Hoogenboom MO, Huang D, Keith SA, Kuo CY, Lovelock CE, Luiz O, Martinelli J, Mizere T, Pandolfi JM, Pochon X, Putnam HM, Roberts TE, Stat M, Baird AH (2016). The Coral Trait Database. <em>Nature Scientific Data</em> 3:160017. <a href="https://doi.org/10.1038/sdata.2016.17">doi:10.1038/sdata.2016.17</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('madin2016')">Cite</a>
  <a href="https://doi.org/10.1038/sdata.2016.17" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="madin2016" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{madin_2016,
  author = {Madin, J.S. and Andreasen, M. and Bridge, T. and Connolly, S.R. and Darling, E. and Diaz, M. and Falster, D. and Franklin, E.C. and Gates, R.D. and Hoogenboom, M.O. and Huang, D. and Keith, S.A. and Kuo, C.Y. and Lovelock, C.E. and Luiz, O. and Martinelli, J. and Mizere, T. and Pandolfi, J.M. and Pochon, X. and Putnam, H.M. and Roberts, T.E. and Stat, M. and Baird, A.H.},
  title = {The Coral Trait Database},
  journal = {Nature Scientific Data},
  year = {2016},
  volume = {3},
  pages = {160017},
  doi = {10.1038/sdata.2016.17},
  url = {https://doi.org/10.1038/sdata.2016.17}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2014">
    Edmunds PJ, Adjeroud M, Baskett ML, Baums IB, Budd AF, Carpenter RC, Fabina NS, Fan T-Y, Franklin EC, Gross K, Han X, Jacobson L, Klaus JS, McClanahan TR, O’Leary JK, van Oppen MJH, Pochon X, Putnam HM, Smith TB, Stat M, Sweatman H, van Woesik R, Gates RD (2014). Persistence and change in community composition of reef corals through present, past and future climates. <em>PLoS ONE</em> 9(10): e107525. <a href="https://doi.org/10.1371/journal.pone.0107525">doi:10.1371/journal.pone.0107525</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('edmunds2014')">Cite</a>
  <a href="https://doi.org/10.1371/journal.pone.0107525" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="edmunds2014" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{edmunds_2014,
  author = {Edmunds, P.J. and Adjeroud, M. and Baskett, M.L. and Baums, I.B. and Budd, A.F. and Carpenter, R.C. and Fabina, N.S. and Fan, T.Y. and Franklin, E.C. and Gross, K. and Han, X. and Jacobson, L. and Klaus, J.S. and McClanahan, T.R. and O’Leary, J.K. and van Oppen, M.J.H. and Pochon, X. and Putnam, H.M. and Smith, T.B. and Stat, M. and Sweatman, H. and van Woesik, R. and Gates, R.D.},
  title = {Persistence and change in community composition of reef corals through present, past and future climates},
  journal = {PLoS ONE},
  year = {2014},
  volume = {9},
  number = {10},
  pages = {e107525},
  doi = {10.1371/journal.pone.0107525},
  url = {https://doi.org/10.1371/journal.pone.0107525}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2014">
    Ault JS, Smith SG, Browder J, Nuttle W, Franklin EC, DiNardo GT, Bohnsack JA (2014). Indicators for assessing the ecological dynamics and sustainability of southern Florida's coral reef and coastal fisheries. <em>Ecological Indicators</em> 44:164-172. <a href="https://doi.org/10.1016/j.ecolind.2014.04.013">doi:10.1016/j.ecolind.2014.04.013</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('ault2014')">Cite</a>
  <a href="https://doi.org/10.1016/j.ecolind.2014.04.013" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="ault2014" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{ault_2014,
  author = {Ault, J.S. and Smith, S.G. and Browder, J. and Nuttle, W. and Franklin, E.C. and DiNardo, G.T. and Bohnsack, J.A.},
  title = {Indicators for assessing the ecological dynamics and sustainability of southern Florida's coral reef and coastal fisheries},
  journal = {Ecological Indicators},
  year = {2014},
  volume = {44},
  pages = {164-172},
  doi = {10.1016/j.ecolind.2014.04.013},
  url = {https://doi.org/10.1016/j.ecolind.2014.04.013}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2014">
    Baums IB, Godwin LS, Franklin EC, Carlon DB, Toonen RJ (2014). Discordant population expansions in four species of coral-associated, Pacific hermit crabs (Anomura: Diogenidae) linked to habitat availability resulting from sea level change. <em>Journal of Biogeography</em> 41: 339-352. <a href="https://doi.org/10.1111/jbi.12181">doi:10.1111/jbi.12181</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('baums2014')">Cite</a>
  <a href="https://doi.org/10.1111/jbi.12181" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="baums2014" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{baums_2014,
  author = {Baums, I.B. and Godwin, L.S. and Franklin, E.C. and Carlon, D.B. and Toonen, R.J.},
  title = {Discordant population expansions in four species of coral-associated, Pacific hermit crabs (Anomura: Diogenidae) linked to habitat availability resulting from sea level change},
  journal = {Journal of Biogeography},
  year = {2014},
  volume = {41},
  pages = {339-352},
  doi = {10.1111/jbi.12181},
  url = {https://doi.org/10.1111/jbi.12181}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2013">
    Fabina NS, Putnam HM, Franklin EC, Stat M, Gates RD (2013). Symbiotic specificity, association patterns, and function determine community responses to global changes: Defining critical research areas for coral-Symbiodinium symbioses. <em>Global Change Biology</em> 19: 3306–3316. <a href="https://doi.org/10.1111/gcb.12320">doi:10.1111/gcb.12320</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('fabina2013')">Cite</a>
  <a href="https://doi.org/10.1111/gcb.12320" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="fabina2013" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{fabina_2013,
  author = {Fabina, N.S. and Putnam, H.M. and Franklin, E.C. and Stat, M. and Gates, R.D.},
  title = {Symbiotic specificity, association patterns, and function determine community responses to global changes: Defining critical research areas for coral-Symbiodinium symbioses},
  journal = {Global Change Biology},
  year = {2013},
  volume = {19},
  pages = {3306–3316},
  doi = {10.1111/gcb.12320},
  url = {https://doi.org/10.1111/gcb.12320}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2013">
    Bird CE, Franklin EC, Smith CM, Toonen RJ (2013). Between tide and wave marks: a unifying model of physical zonation on littoral shores. <em>PeerJ</em> 1:e154. <a href="https://doi.org/10.7717/peerj.154">doi:10.7717/peerj.154</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('bird2013')">Cite</a>
  <a href="https://doi.org/10.7717/peerj.154" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="bird2013" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{bird_2013,
  author = {Bird, C.E. and Franklin, E.C. and Smith, C.M. and Toonen, R.J.},
  title = {Between tide and wave marks: a unifying model of physical zonation on littoral shores},
  journal = {PeerJ},
  year = {2013},
  volume = {1},
  article = {e154},
  doi = {10.7717/peerj.154},
  url = {https://doi.org/10.7717/peerj.154}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2013">
    Farmer NA, Ault JS, Smith SG, Franklin EC (2013). Methods for assessment of short-term coral reef fish movements within an acoustic array. <em>Movement Ecology</em> 2013:1-7. <a href="https://doi.org/10.1186/2051-3933-1-7">doi:10.1186/2051-3933-1-7</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('farmer2013')">Cite</a>
  <a href="https://doi.org/10.1186/2051-3933-1-7" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="farmer2013" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{farmer_2013,
  author = {Farmer, N.A. and Ault, J.S. and Smith, S.G. and Franklin, E.C.},
  title = {Methods for assessment of short-term coral reef fish movements within an acoustic array},
  journal = {Movement Ecology},
  year = {2013},
  pages = {1-7},
  doi = {10.1186/2051-3933-1-7},
  url = {https://doi.org/10.1186/2051-3933-1-7}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2013">
    Franklin EC, Jokiel PL, Donahue MJ (2013). Predictive modeling of coral distribution and abundance in the Hawaiian Islands. <em>Marine Ecology Progress Series</em> 481:121-132. <a href="https://doi.org/10.3354/meps10252">doi:10.3354/meps10252</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('franklin2013')">Cite</a>
  <a href="https://doi.org/10.3354/meps10252" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="franklin2013" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{franklin_2013,
  author = {Franklin, E.C. and Jokiel, P.L. and Donahue, M.J.},
  title = {Predictive modeling of coral distribution and abundance in the Hawaiian Islands},
  journal = {Marine Ecology Progress Series},
  year = {2013},
  volume = {481},
  pages = {121-132},
  doi = {10.3354/meps10252},
  url = {https://doi.org/10.3354/meps10252}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2013">
    Stat M, Pochon X, Franklin EC, Bruno JF, Casey KS, Selig ER, Gates RD (2013). The distribution of the thermally tolerant symbiont lineage (Symbiodinium clade D) in corals from Hawaii: correlations with host and the history of ocean thermal stress. <em>Ecology and Evolution</em> 3:1317-1329. <a href="https://doi.org/10.1002/ece3.556">doi:10.1002/ece3.556</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('stat2013')">Cite</a>
  <a href="https://doi.org/10.1002/ece3.556" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="stat2013" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{stat_2013,
  author = {Stat, M. and Pochon, X. and Franklin, E.C. and Bruno, J.F. and Casey, K.S. and Selig, E.R. and Gates, R.D.},
  title = {The distribution of the thermally tolerant symbiont lineage (Symbiodinium clade D) in corals from Hawaii: correlations with host and the history of ocean thermal stress},
  journal = {Ecology and Evolution},
  year = {2013},
  volume = {3},
  pages = {1317-1329},
  doi = {10.1002/ece3.556},
  url = {https://doi.org/10.1002/ece3.556}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2012">
    Fabina NS, Putnam HM, Franklin EC, Stat M, Gates RD (2012). Transmission mode predicts specificity and interaction patterns in coral-Symbiodinium networks. <em>PLoS ONE</em> 7(9): e44970. <a href="https://doi.org/10.1371/journal.pone.0044970">doi:10.1371/journal.pone.0044970</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('fabina2012')">Cite</a>
  <a href="https://doi.org/10.1371/journal.pone.0044970" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="fabina2012" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{fabina_2012,
  author = {Fabina, N.S. and Putnam, H.M. and Franklin, E.C. and Stat, M. and Gates, R.D.},
  title = {Transmission mode predicts specificity and interaction patterns in coral-Symbiodinium networks},
  journal = {PLoS ONE},
  year = {2012},
  volume = {7},
  number = {9},
  pages = {e44970},
  doi = {10.1371/journal.pone.0044970},
  url = {https://doi.org/10.1371/journal.pone.0044970}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry conference 2012">
    Heron SF, Maynard J, Willis B, Christensen T, Harvell D, Vargas-Angel B, Beeden R, Sziklay J, Aeby G, Franklin EC, and 8 others (2012).  Developments in understanding relationships between environmental conditions and coral disease.<em>Proc 12th Int’l Coral Reef Symposium</em>, Cairns, Australia. 16B:4.
    
  <a href="#" class="badge badge-info" onclick="openModal('heron2012')">Cite</a>
</div>

<!-- Modal Structure -->
<div id="heron2012" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@inproceedings{heron_2012,
  author = {Heron, S.F. and Maynard, J. and Willis, B. and Christensen, T. and Harvell, D. and Vargas-Angel, B. and Beeden, R. and Sziklay, J. and Aeby, G. and Franklin, E.C. and others},
  title = {Developments in understanding relationships between environmental conditions and coral disease},
  booktitle = {Proceedings of the 12th International Coral Reef Symposium},
  location = {Cairns, Australia},
  year = {2012},
  volume = {16B},
  pages = {4}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
    </div>
</div>


<div class="publication-entry journal 2012">
    van Woesik R, Franklin EC, O’Leary J, McClanahan TR, Klaus JS, Budd AF (2012). Hosts of the Plio-Pleistocene past reflect modern-day coral vulnerability. <em>Proceedings of the Royal Society B</em>. <a href="https://doi.org/10.1098/rspb.2011.2621">doi:10.1098/rspb.2011.2621</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('vanWoesik2012')">Cite</a>
  <a href="https://doi.org/10.1098/rspb.2011.2621" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="vanWoesik2012" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{vanwoesik_2012,
  author = {van Woesik, R. and Franklin, E.C. and O’Leary, J. and McClanahan, T.R. and Klaus, J.S. and Budd, A.F.},
  title = {Hosts of the Plio-Pleistocene past reflect modern-day coral vulnerability},
  journal = {Proceedings of the Royal Society B},
  year = {2012},
  doi = {10.1098/rspb.2011.2621},
  url = {https://doi.org/10.1098/rspb.2011.2621}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
    </div>
</div>



<div class="publication-entry journal 2012">
    Franklin EC, Stat M, Pochon X, Putnam HM, Gates RD (2012). GeoSymbio: A hybrid, cloud-based web application of global geospatial bioinformatics and ecoinformatics for Symbiodinium-host symbioses. <em>Molecular Ecology Resources</em> 12(2): 369-373. <a href="https://doi.org/10.1111/j.1755-0998.2011.03081.x">doi:10.1111/j.1755-0998.2011.03081.x</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('Franklin2012GeoSymbio')">Cite</a>
  <a href="https://doi.org/10.1111/j.1755-0998.2011.03081.x" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="Franklin2012GeoSymbio" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{franklin_2012_geosymbio,
  author = {Franklin, E.C. and Stat, M. and Pochon, X. and Putnam, H.M. and Gates, R.D.},
  title = {GeoSymbio: A hybrid, cloud-based web application of global geospatial bioinformatics and ecoinformatics for Symbiodinium-host symbioses},
  journal = {Molecular Ecology Resources},
  year = {2012},
  volume = {12},
  number = {2},
  pages = {369-373},
  doi = {10.1111/j.1755-0998.2011.03081.x},
  url = {https://doi.org/10.1111/j.1755-0998.2011.03081.x}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
    </div>
</div>



<div class="publication-entry journal 2011">
    Franklin EC, Stat M, Pochon X, Putnam HM, Gates RD (2011). "Rapid Development of a Hybrid Web Application for Synthesis Science of Symbiodinium with Google Apps." In Jones, MB, Gries C (eds.) Proceedings of Environmental Information Management Conference 2011 (EIM 2011), Sep 28-29, 2011, UCSB, California, pp 44-48. <a href="https://doi.org/10.5060/D2NC5Z4X">doi:10.5060/D2NC5Z4X</a>

  <a href="#" class="badge badge-info" onclick="openModal('Franklin2011HybridApp')">Cite</a>
  <a href="https://doi:10.5060/D2NC5Z4X" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="Franklin2011HybridApp" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@inproceedings{franklin_2011,
  author = {Franklin, E.C. and Stat, M. and Pochon, X. and Putnam, H.M. and Gates, R.D.},
  title = {Rapid Development of a Hybrid Web Application for Synthesis Science of Symbiodinium with Google Apps},
  booktitle = {Proceedings of Environmental Information Management Conference 2011 (EIM 2011)},
  editor = {Jones, M.B. and Gries, C.},
  year = {2011},
  pages = {44-48},
  address = {UCSB, California},
  month = {September},
  doi = {10.5060/D2NC5Z4X}
  url = {https://doi:10.5060/D2NC5Z4X}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
    </div>
</div>


<div class="publication-entry journal 2011">
    Longenecker K, Chan Y, Franklin EC (2011). Relationships between the length of select head bones and body size for some Hawaiian parrotfishes (subfamily Scarinae). Bishop Museum Occasional Papers 111:13-26.

  <a href="#" class="badge badge-info" onclick="openModal('Longenecker2011Parrotfish')">Cite</a>
</div>

<!-- Modal Structure -->
<div id="Longenecker2011Parrotfish" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{longenecker_2011,
  author = {Longenecker, K. and Chan, Y. and Franklin, E.C.},
  title = {Relationships between the length of select head bones and body size for some Hawaiian parrotfishes (subfamily Scarinae)},
  journal = {Bishop Museum Occasional Papers},
  volume = {111},
  pages = {13-26},
  year = {2011}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
    </div>
</div>


<div class="publication-entry journal 2011">
    Aeby GS, Williams GJ, Franklin EC, Kenyon J, Cox EF, Coles S, Work TM (2011). Patterns of coral disease across the Hawaiian Archipelago: relating disease to environment. <em>PLoS ONE</em> 6(5): e20370. <a href="https://doi.org/10.1371/journal.pone.0020370">doi:10.1371/journal.pone.0020370</a>

  <a href="#" class="badge badge-info" onclick="openModal('Aeby2011CoralDisease')">Cite</a>
  <a href="https://doi:10.1371/journal.pone.0020370" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="Aeby2011CoralDisease" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{aeby_2011,
  author = {Aeby, G.S. and Williams, G.J. and Franklin, E.C. and Kenyon, J. and Cox, E.F. and Coles, S. and Work, T.M.},
  title = {Patterns of coral disease across the Hawaiian Archipelago: relating disease to environment},
  journal = {PLoS ONE},
  volume = {6},
  number = {5},
  pages = {e20370},
  year = {2011},
  doi = {10.1371/journal.pone.0020370}
  url = {https://doi:10.1371/journal.pone.0020370}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
    </div>
</div>


<div class="publication-entry journal 2011">
    Aeby GS, Williams GJ, Franklin EC, Haapkyla J, Harvell CD, Neale S, Page CA, Raymundo L, Vargas-Angel B, Willis BL, Work TM, Davy SK (2011). Growth anomalies on the coral genera Acropora and Porites are strongly associated with host density and human population size across the Indo-Pacific. <em>PLoS ONE</em> 6(2): e16887. <a href="https://doi.org/10.1371/journal.pone.0016887">doi:10.1371/journal.pone.0016887</a>

  <a href="#" class="badge badge-info" onclick="openModal('Aeby2011GrowthAnomalies')">Cite</a>
  <a href="https://doi:10.1371/journal.pone.0016887" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="Aeby2011GrowthAnomalies" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{aeby_2011_growth_anomalies,
  author = {Aeby, G.S. and Williams, G.J. and Franklin, E.C. and Haapkyla, J. and Harvell, C.D. and Neale, S. and Page, C.A. and Raymundo, L. and Vargas-Angel, B. and Willis, B.L. and Work, T.M. and Davy, S.K.},
  title = {Growth anomalies on the coral genera Acropora and Porites are strongly associated with host density and human population size across the Indo-Pacific},
  journal = {PLoS ONE},
  volume = {6},
  number = {2},
  pages = {e16887},
  year = {2011},
  doi = {10.1371/journal.pone.0016887}
  url = {https://doi:10.1371/journal.pone.0016887}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
    </div>
</div>


<div class="publication-entry book 2010">
    Franklin EC (2010). Marine landscape ecology of coral reefs emerges from developments in seafloor mapping, GPS, and GIS. Pp 193-204 in Breman J, Ocean Globe. ESRI Press: Redlands, CA.

  <a href="#" class="badge badge-info" onclick="openModal('Franklin2010MarineLandscape')">Cite</a>
</div>

<!-- Modal Structure -->
<div id="Franklin2010MarineLandscape" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@incollection{franklin_2010_marine_landscape,
  author = {Franklin, E.C.},
  title = {Marine landscape ecology of coral reefs emerges from developments in seafloor mapping, GPS, and GIS},
  booktitle = {Ocean Globe},
  editor = {Breman, J.},
  pages = {193--204},
  publisher = {ESRI Press},
  year = {2010},
  address = {Redlands, CA}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
    </div>
</div>


<div class="publication-entry journal 2010">
    Concepcion GT, Kahng SE, Crepeau MW, Franklin EC, Coles SL, Toonen RJ (2010). Resolving natural ranges and marine invasions in a globally distributed octocoral (genus Carijoa). <em>Marine Ecology Progress Series</em> 401:113-127. <a href="https://doi.org/10.3354/meps08364">doi:10.3354/meps08364</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('Concepcion2010ResolvingRanges')">Cite</a>
  <a href="https://doi.org/10.3354/meps08364" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="Concepcion2010ResolvingRanges" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{concepcion_2010_resolving_ranges,
  author = {Concepcion, G.T. and Kahng, S.E. and Crepeau, M.W. and Franklin, E.C. and Coles, S.L. and Toonen, R.J.},
  title = {Resolving natural ranges and marine invasions in a globally distributed octocoral (genus Carijoa)},
  journal = {Marine Ecology Progress Series},
  volume = {401},
  pages = {113-127},
  year = {2010},
  doi = {10.3354/meps08364},
  url = {https://doi.org/10.3354/meps08364}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2009">
    Franklin EC, Dow A, Brong C, Craig M (2009). Length-weight and length-length relationships of three endemic butterflyfish species (Chaetodontidae) from coral reefs of the Northwestern Hawaiian Islands, USA. Journal of Applied Ichthyology 25(5):616-617. <a href="https://doi:10.1111/j.1439-0426.2009.01281.x">doi:10.1111/j.1439-0426.2009.01281.x</a>

  <a href="#" class="badge badge-info" onclick="openModal('Franklin2009LengthWeight')">Cite</a>
  <a href="https://doi:10.1111/j.1439-0426.2009.01281.x" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="Franklin2009LengthWeight" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{franklin_2009_length_weight,
  author = {Franklin, E.C. and Dow, A. and Brong, C. and Craig, M.},
  title = {Length-weight and length-length relationships of three endemic butterflyfish species (Chaetodontidae) from coral reefs of the Northwestern Hawaiian Islands, USA},
  journal = {Journal of Applied Ichthyology},
  volume = {25},
  number = {5},
  pages = {616-617},
  year = {2009}
  doi = {10.1111/j.1439-0426.2009.01281.x}
  url = {https://doi:10.1111/j.1439-0426.2009.01281.x}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
    </div>
</div>


<div class="publication-entry journal 2009">
    Selkoe KA, Halpern BS, Ebert CM, Franklin EC, Selig ER, Casey KS, Bruno J, Toonen RJ (2009). A map of human impacts to a “pristine” coral reef ecosystem, the Papahanaumokuakea Marine National Monument. Coral Reefs 28(3):635-650. <a href=" https://doi.org/10.1007/s00338-009-0490-z">doi:10.1007/s00338-009-0490-z</a>

  <a href="#" class="badge badge-info" onclick="openModal('Selkoe2009HumanImpacts')">Cite</a>
  <a href=" https://doi.org/10.1007/s00338-009-0490-z" class = "badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="Selkoe2009HumanImpacts" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{selkoe_2009_human_impacts,
  author = {Selkoe, K.A. and Halpern, B.S. and Ebert, C.M. and Franklin, E.C. and Selig, E.R. and Casey, K.S. and Bruno, J. and Toonen, R.J.},
  title = {A map of human impacts to a “pristine” coral reef ecosystem, the Papahanaumokuakea Marine National Monument},
  journal = {Coral Reefs},
  volume = {28},
  number = {3},
  pages = {635-650},
  year = {2009}
  doi = {10.1007/s00338-009-0490-z}
  url = {https://doi.org/10.1007/s00338-009-0490-z}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
    </div>
</div>


<div class="publication-entry journal 2008">
    Franklin EC (2008). An assessment of vessel traffic patterns in the Northwestern Hawaiian Islands between 1994-2004. <em>Marine Pollution Bulletin</em> 56:150-153. <a href="https://doi.org/10.1016/j.marpolbul.2007.07.002">doi:10.1016/j.marpolbul.2007.07.002</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('Franklin2008VesselTraffic')">Cite</a>
  <a href="https://doi.org/10.1016/j.marpolbul.2007.07.002" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="Franklin2008VesselTraffic" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{franklin_2008_vessel_traffic,
  author = {Franklin, E.C.},
  title = {An assessment of vessel traffic patterns in the Northwestern Hawaiian Islands between 1994-2004},
  journal = {Marine Pollution Bulletin},
  volume = {56},
  pages = {150-153},
  year = {2008},
  doi = {10.1016/j.marpolbul.2007.07.002},
  url = {https://doi.org/10.1016/j.marpolbul.2007.07.002}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>



<div class="publication-entry journal 2006">
    Hudson JH, Franklin EC (2006). Structural Stabilization of a Large Montastrea faveolata (Ellis and Solander, 1786) Colony Damaged by Vessel Impact. <em>Caribbean Journal of Science</em> 42(2):252-254.
    
  <a href="#" class="badge badge-info" onclick="openModal('Hudson2006')">Cite</a>
</div>

<!-- Modal Structure -->
<div id="Hudson2006" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{hudson_2006_structural_stabilization,
  author = {Hudson, J.H. and Franklin, E.C.},
  title = {Structural Stabilization of a Large Montastrea faveolata (Ellis and Solander, 1786) Colony Damaged by Vessel Impact},
  journal = {Caribbean Journal of Science},
  volume = {42},
  number = {2},
  pages = {252-254},
  year = {2006},
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2006">
    Hudson JH, Franklin EC (2006). Coral reef restoration of a storm-disturbed vessel grounding site in the Florida Keys National Marine Sanctuary, USA. In: Proceedings of the 10th International Coral Reef Symposium, Okinawa, Japan, pp 1631-1636.
    
  <a href="#" class="badge badge-info" onclick="openModal('Hudson2006CoralRestoration')">Cite</a>
</div>

<!-- Modal Structure -->
<div id="Hudson2006CoralRestoration" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@inproceedings{hudson_2006_coral_restoration,
  author = {Hudson, J.H. and Franklin, E.C.},
  title = {Coral reef restoration of a storm-disturbed vessel grounding site in the Florida Keys National Marine Sanctuary, USA},
  booktitle = {Proceedings of the 10th International Coral Reef Symposium},
  year = {2006},
  location = {Okinawa, Japan},
  pages = {1631-1636}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2005">
    Hudson JH, Franklin EC (2005). Structural Reef Restoration and Coral Transplantation to the R/V Columbus Iselin Grounding Site in the Florida Keys National Marine Sanctuary. In: Proceedings of the OCEANS 2005 Americas MTS/IEEE Conference, Washington, DC, September 19-23, 2005. <a href="https://doi.org/10.1109/OCEANS.2005.1639763">doi:10.1109/OCEANS.2005.1639763</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('Hudson2005CoralRestoration')">Cite</a>
  <a href="https://doi.org/10.1109/OCEANS.2005.1639763" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="Hudson2005CoralRestoration" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@inproceedings{hudson_2005_structural_restoration,
  author = {Hudson, J.H. and Franklin, E.C.},
  title = {Structural Reef Restoration and Coral Transplantation to the R/V Columbus Iselin Grounding Site in the Florida Keys National Marine Sanctuary},
  booktitle = {Proceedings of the OCEANS 2005 Americas MTS/IEEE Conference},
  year = {2005},
  location = {Washington, DC},
  month = {September},
  pages = {},
  doi = {10.1109/OCEANS.2005.1639763},
  url = {https://doi.org/10.1109/OCEANS.2005.1639763}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2003">
    Franklin EC, Ault JS, Smith SG, Luo J, Meester GA, Diaz GA, Chiappone M, Swanson DW, Miller SL, Bohnsack JA (2003). Benthic habitat mapping in the Tortugas region, Florida. <em>Marine Geodesy</em> 26(1-2):19-34. <a href="https://doi.org/10.1080/01490410306706">doi:10.1080/01490410306706</a>

  <a href="#" class="badge badge-info" onclick="openModal('franklin2003')">Cite</a>
  <a href="https://doi.org/10.1080/01490410306706" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="franklin2003" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{franklin_2003,
  author = {Franklin, E.C. and Ault, J.S. and Smith, S.G. and Luo, J. and Meester, G.A. and Diaz, G.A. and Chiappone, M. and Swanson, D.W. and Miller, S.L. and Bohnsack, J.A.},
  title = {Benthic habitat mapping in the Tortugas region, Florida},
  journal = {Marine Geodesy},
  year = {2003},
  volume = {26},
  number = {1-2},
  pages = {19-34},
  doi = {10.1080/01490410306706},
  url = {https://doi.org/10.1080/01490410306706}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2002">
    Ault JS, Smith SG, Meester GA, Luo J, Franklin EC, Bohnsack JA, Harper DE, McClellan DB, Miller SL, Chiappone M, Swanson DW (2002). Synoptic habitat and reef fish surveys support establishment of marine reserves in Dry Tortugas, Florida USA. <em>Reef Encounter</em> 31:22-23. 

  <a href="#" class="badge badge-info" onclick="openModal('ault2002')">Cite</a>
</div>

<!-- Modal Structure -->
<div id="ault2002" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{ault_2002,
  author = {Ault, J.S. and Smith, S.G. and Meester, G.A. and Luo, J. and Franklin, E.C. and Bohnsack, J.A. and Harper, D.E. and McClellan, D.B. and Miller, S.L. and Chiappone, M. and Swanson, D.W.},
  title = {Synoptic habitat and reef fish surveys support establishment of marine reserves in Dry Tortugas, Florida USA},
  journal = {Reef Encounter},
  year = {2002},
  volume = {31},
  pages = {22-23}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry book 2002">
    Franklin EC, Ault JS, Smith SG (2002). Utilization of a GIS in a fisheries assessment and management system. In: J. Breman (ed) <em>Marine Geography: GIS for the Oceans and the Seas</em>. Redlands, CA: ESRI Press. 
    
  <a href="#" class="badge badge-info" onclick="openModal('franklin2002GIS')">Cite</a>
</div>

<!-- Modal Structure -->
<div id="franklin2002GIS" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@incollection{franklin_2002,
  author = {Franklin, E.C. and Ault, J.S. and Smith, S.G.},
  title = {Utilization of a GIS in a fisheries assessment and management system},
  booktitle = {Marine Geography: GIS for the Oceans and the Seas},
  editor = {Breman, J.},
  publisher = {ESRI Press},
  year = {2002},
  address = {Redlands, CA}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal 2001">
    Miller SL, Swanson DW, Chiappone M, Ault JS, Smith SG, Meester GA, Luo J, Franklin EC, Bohnsack JA, Harper DE, McClellan DB (2001). An extensive deep reef terrace on the Tortugas Bank, Florida Keys National Marine Sanctuary. <em>Coral Reefs</em> 20:299-300. 
    
  <a href="#" class="badge badge-info" onclick="openModal('miller2001DeepReef')">Cite</a>
</div>

<!-- Modal Structure -->
<div id="miller2001DeepReef" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre class="citation-text">
@article{miller_2001_deep_reef,
  author = {Miller, S.L. and Swanson, D.W. and Chiappone, M. and Ault, J.S. and Smith, S.G. and Meester, G.A. and Luo, J. and Franklin, E.C. and Bohnsack, J.A. and Harper, D.E. and McClellan, D.B.},
  title = {An extensive deep reef terrace on the Tortugas Bank, Florida Keys National Marine Sanctuary},
  journal = {Coral Reefs},
  volume = {20},
  pages = {299-300},
  year = {2001},
  doi = {10.1007/s00338-001-0162-1},
  url = {https://doi.org/10.1007/s00338-001-0162-1}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard()">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>



<script>
  function searchCitations() {
    const input = document.getElementById('searchBar').value.toLowerCase();
    const publicationEntries = document.querySelectorAll('.publication-entry'); // Update this selector based on your structure

    publicationEntries.forEach(entry => {
        const text = entry.textContent.toLowerCase();
        if (text.includes(input)) {
            entry.style.display = ''; // Show the entry
        } else {
            entry.style.display = 'none'; // Hide the entry
        }
    });
}
function filterPublications() {
    var filterValue = document.getElementById("filter").value;
    var yearValue = document.getElementById("yearFilter").value; // New year filter
    var publications = document.getElementsByClassName("publication-entry");

    for (var i = 0; i < publications.length; i++) {
        var publication = publications[i];
        var matchesFilter = filterValue === "all" || publication.classList.contains(filterValue);
        var matchesYear = yearValue === "all" || publication.classList.contains(yearValue);

        if (matchesFilter && matchesYear) {
            publication.style.display = "block"; // Show if both filter and year match
        } else {
            publication.style.display = "none"; // Hide if either filter or year doesn't match
        }
    }
}

</script>

<script>
function openModal(element) {
    const citationText = element.parentElement.getAttribute('data-citation');
    document.getElementById('citationText').textContent = citationText;
    document.getElementById('citationModal').style.display = 'block';
}

function closeModal() {
    document.getElementById('citationModal').style.display = 'none';
}


// Function to copy citation to clipboard
function copyToClipboard() {
    const openModal = document.querySelector('.modal[style*="block"]');  // Find the currently open modal
    const citationText = openModal.querySelector('.citation-text').innerText.trim();

    navigator.clipboard.writeText(citationText).then(() => {
        alert('Citation copied to clipboard');
    });
}

// Function to download citation (optional, implement as needed)
function downloadCitation() {
    const openModal = document.querySelector('.modal[style*="block"]');  // Find the currently open modal
    const citationText = openModal.querySelector('.citation-text').innerText.trim();

    // Create a Blob with the citation text content
    const blob = new Blob([citationText], { type: 'text/plain' });
    const url = URL.createObjectURL(blob);

    // Create a temporary download link
    const a = document.createElement('a');
    a.href = url;
    a.download = 'citation.txt';  // Name of the file
    document.body.appendChild(a);
    a.click();  // Trigger download

    // Clean up temporary link
    document.body.removeChild(a);
    URL.revokeObjectURL(url);
}
</script>
