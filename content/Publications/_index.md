---
title: Peer-Reviewed Publications
authors:
  - erik-franklin

# Optional banner image (relative to `assets/media/` folder).
#banner:
  #caption: ''
  #image: ''
---
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
    }

    .button-outline:hover {
        background-color: teal; /* Background color on hover */
        color: white; /* Text color on hover */
    }
</style>

<!-- Search bars and filters -->
<div style="display: flex; align-items: center; margin-bottom: 20px;">
    <!-- Search Bar -->
    <input type="text" id="searchBar" placeholder="Search publications..." onkeyup="searchCitations()" style="padding: 10px; width: 100%; max-width: 300px; margin-right: 20px;">
    <!-- Drop down filter -->
    <label for="filter" style="margin-right: 10px;">Filter by:</label>
    <select id="filter" onchange="filterPublications()">
        <option value="all">All</option>
        <option value="journal">Journal Articles</option>
        <option value="book">Book Sections</option>
    </select>
</div>


<!-- Citations -->
<div class="publication-entry journal">
    Franklin EC, Platt MT*, Andrade P (accepted). Increased occurrence of the rare golden color morph of Pacific chub Kyphosus sandwicensis in a no-take marine reserve. <em>Journal of Fish Biology</em>. <a href="https://doi.org/10.1111/jfb.15644">doi:10.1111/jfb.15644</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('franklin2023')">Cite</a>
  <a href="https://doi.org/10.1111/jfb.15644" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="modal" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre id="citationText">
@article{franklin_2023,
  author = {Franklin, E.C. and Platt, M.T. and Andrade, P.},
  title = {Increased occurrence of the rare golden color morph of Pacific chub Kyphosus sandwicensis in a no-take marine reserve},
  journal = {Journal of Fish Biology},
  year = {accepted},
  doi = {10.1111/jfb.15644},
  url = {https://doi.org/10.1111/jfb.15644}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard('citationText')">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal">
    Winans WR+, Chen Q, Qiang Y, Franklin EC (2023). Large-area automatic detection of shoreline stranded marine debris using deep learning. <em>International Journal of Applied Earth Observation and Geoinformation</em>. <a href="https://doi.org/10.1016/j.jag.2023.103515">doi:10.1016/j.jag.2023.103515</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('winans2023')">Cite</a>
  <a href="https://doi.org/10.1016/j.jag.2023.103515" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="modal" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre id="citationText">
@article{winans_2023,
  author = {Winans, W.R. and Chen, Q. and Qiang, Y. and Franklin, E.C.},
  title = {Large-area automatic detection of shoreline stranded marine debris using deep learning},
  journal = {International Journal of Applied Earth Observation and Geoinformation},
  year = {2023},
  doi = {10.1016/j.jag.2023.103515},
  url = {https://doi.org/10.1016/j.jag.2023.103515}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard('citationText')">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal">
    Purwanto, Franklin EC, Mardiani SR, White AT (2023). Multiple-goal bioeconomic programming to address conflicting management objectives in Indonesian small pelagic fisheries. <em>Marine Policy</em> 150: 105519. <a href="https://doi.org/10.1016/j.marpol.2023.105519">doi:10.1016/j.marpol.2023.105519</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('purwanto2023')">Cite</a>
  <a href="https://doi.org/10.1016/j.marpol.2023.105519" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="modal" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre id="citationText">
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
        <button class="button-outline" onclick="copyToClipboard('citationText')">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal">
    Carlson KM, Mora C, Xu J+, Setter RO+, Harangody M+, Franklin EC, Kantar MB, Lucas M, Menzo ZM+, Spirandelli D, Schanzenbach D, Warr CC, Wong AE+, Businger S (2022). Global rainbow distribution under current and future climates. <em>Global Environmental Change</em> 77: 102604. <a href="https://doi.org/10.1016/j.gloenvcha.2022.102604">doi:10.1016/j.gloenvcha.2022.102604</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('carlson2022')">Cite</a>
  <a href="https://doi.org/10.1016/j.gloenvcha.2022.102604" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="modal" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre id="citationText">
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
        <button class="button-outline" onclick="copyToClipboard('citationText')">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal">
    Setter RO+, Franklin EC, Mora C (2022). Co-occurring anthropogenic stressors reduce the timeframe of environmental viability for the world’s coral reefs. <em>PLoS Biology</em> 20: e3001821. <a href="https://doi.org/10.1371/journal.pbio.3001821">doi:10.1371/journal.pbio.3001821</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('setter2022')">Cite</a>
  <a href="https://doi.org/10.1371/journal.pbio.3001821" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="modal" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre id="citationText">
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
        <button class="button-outline" onclick="copyToClipboard('citationText')">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal">
    Barkley YM*, Sakai T, Oleson EM, Franklin EC (2022). Examining distribution patterns of foraging and non-foraging sperm whales in Hawaiian waters using visual and passive acoustic data. <em>Frontiers in Remote Sensing</em> 3: 940186. <a href="https://doi.org/10.3389/frsen.2022.940186">doi:10.3389/frsen.2022.940186</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('barkley2022')">Cite</a>
  <a href="https://doi.org/10.3389/frsen.2022.940186" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="modal" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre id="citationText">
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
        <button class="button-outline" onclick="copyToClipboard('citationText')">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal">
    Akiona AK*, Popp BN, Toonen RJ, Siple MC, Kotubetey K, Kawelo H, Franklin EC (2022). Predatory fish diets shift toward an invasive mullet in a traditional Hawaiian aquaculture system. <em>Aquaculture, Fish and Fisheries</em>. <a href="https://doi.org/10.1002/aff2.68">doi:10.1002/aff2.68</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('akiona2022')">Cite</a>
  <a href="https://doi.org/10.1002/aff2.68" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="modal" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre id="citationText">
@article{akiona_2022,
  author = {Akiona, A.K. and Popp, B.N. and Toonen, R.J. and Siple, M.C. and Kotubetey, K. and Kawelo, H. and Franklin, E.C.},
  title = {Predatory fish diets shift toward an invasive mullet in a traditional Hawaiian aquaculture system},
  journal = {Aquaculture, Fish and Fisheries},
  year = {2022},
  doi = {10.1002/aff2.68},
  url = {https://doi.org/10.1002/aff2.68}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard('citationText')">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal">
    Mora C, McKenzie T, Gaw IM+, Dean JM+, von Hammerstein H+, Knudson TA+, Setter RO+, Smith CZ+, Webster KM+, Patz JA, Franklin EC (2022). Over half of known human pathogenic diseases can be aggravated by climate change. <em>Nature Climate Change</em> 12: 869-875. <a href="https://doi.org/10.1038/s41558-022-01426-1">doi:10.1038/s41558-022-01426-1</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('mora2022')">Cite</a>
  <a href="https://doi.org/10.1038/s41558-022-01426-1" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="modal" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre id="citationText">
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
        <button class="button-outline" onclick="copyToClipboard('citationText')">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal">
    Nichols RS*, DeMartini EE, Franklin EC (2022). No butts about it: using urogenital disparity in a deep water snapper, <em>Etelis carbunculus</em> (Lutjanidae), for field based sexual identification. <em>Journal of Fish Biology</em>. <a href="https://doi.org/10.1111/jfb.15166">doi:10.1111/jfb.15166</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('nichols2022')">Cite</a>
  <a href="https://doi.org/10.1111/jfb.15166" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="modal" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre id="citationText">
@article{nichols_2022,
  author = {Nichols, R.S. and DeMartini, E.E. and Franklin, E.C.},
  title = {No butts about it: using urogenital disparity in a deep water snapper, Etelis carbunculus (Lutjanidae), for field based sexual identification},
  journal = {Journal of Fish Biology},
  year = {2022},
  doi = {10.1111/jfb.15166},
  url = {https://doi.org/10.1111/jfb.15166}
}
        </pre>
        <button class="button-outline" onclick="copyToClipboard('citationText')">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal">
    Andrade P, Morishige K, Mau A, Kapono L, Franklin EC (2022). Re-imagining contemporary conservation to support ʻĀina Momona: Productive and thriving communities of people, place, and natural resources. <em>Parks Stewardship Forum</em> 38: 186–198. <a href="https://doi.org/10.5070/P538257511">doi: 10.5070/P538257511</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('andrade2022')">Cite</a>
  <a href="https://doi.org/10.5070/P538257511" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="modal" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre id="citationText">
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
        <button class="button-outline" onclick="copyToClipboard('citationText')">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal">
    Purwanto, Franklin EC, Mardiani SR, White AT (2022). Stock assessment and overexploitation risk of small pelagic fish in Fisheries Management Area 715 of Indonesia. <em>Asian Fisheries Science</em> 35: 76-89. <a href="https://doi.org/10.33997/j.afs.2022.35.1.007">doi:10.33997/j.afs.2022.35.1.007</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('purwanto2022')">Cite</a>
  <a href="https://doi.org/10.33997/j.afs.2022.35.1.007" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="modal" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre id="citationText">
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
        <button class="button-outline" onclick="copyToClipboard('citationText')">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal">
    Jaya I, Satria F, Wudianto, Nugroho D, Sadiyah L, Buchary EA, White AT, Franklin EC, Courtney CA, Green G, Green S (2022). Are the working principles of fisheries management at work in Indonesia? <em>Marine Policy</em> 140: 105047. <a href="https://doi.org/10.1016/j.marpol.2022.105047">doi:10.1016/j.marpol.2022.105047</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('jaya2022')">Cite</a>
  <a href="https://doi.org/10.1016/j.marpol.2022.105047" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="modal" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre id="citationText">
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
        <button class="button-outline" onclick="copyToClipboard('citationText')">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal">
    Longenecker K, Franklin EC, Hill-Lewenilovo R+, Lalavanua W, Langston R, Mangubhai, Piovano S (2022). Many immature individuals and largest size classes lacked females from three coral reef fishes (Actinopterygii) in Fiji market surveys: Implications for fishery management. <em>Acta Ichthyologica et Piscatoria</em> 52: 53-65. <a href="https://doi.org/10.3897/aiep.52.80586">doi:10.3897/aiep.52.80586</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('longenecker2022')">Cite</a>
  <a href="https://doi.org/10.3897/aiep.52.80586" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="modal" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre id="citationText">
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
        <button class="button-outline" onclick="copyToClipboard('citationText')">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


<div class="publication-entry journal">
    Johannsen T+, Franklin EC, Hunter CL (2022). A short-term winner? Dramatic increases in the population of mushroom coral Lobactis scutaria (Anthozoa: Fungiidae) in Kaneohe Bay, Hawaii from 2000 to 2018. <em>Pacific Science</em> 76: 79-93. <a href="https://doi.org/10.2984/76.1.7">doi:10.2984/76.1.7</a>
    
  <a href="#" class="badge badge-info" onclick="openModal('johannsen2022')">Cite</a>
  <a href="https://doi.org/10.2984/76.1.7" class="badge badge-info" target="_blank">DOI</a>
</div>

<!-- Modal Structure -->
<div id="modal" class="modal" style="display:none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <pre id="citationText">
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
        <button class="button-outline" onclick="copyToClipboard('citationText')">Copy Citation</button>
        <button class="button-outline" onclick="downloadCitation()">Download Citation</button>
    </div>
</div>


Counsell CWW+, Coleman RR+, Lal SS+, Bowen BW, Franklin EC, Neuheimer AB, Powell BS, Toonen RJ, Donahue MJ, Hixon MA, McManus MA (2022) Interdisciplinary analysis of larval dispersal for a coral reef fish: opening the black box. Marine Ecology Progress Series 684: 117-132 doi: 10.3354/meps13971 \

Limmon GV, Longenecker KL, Langston R, Franklin EC (2022) Capacity development in reproductive life history studies of tropical fishes in Ambon, Maluku, Indonesia for data limited fisheries. Marine Policy 136: 104948 doi: 10.1016/j.marpol.2021/104948 \

Hixon MA, Bowen BW, Coleman RR+, Counsell CW+, Donahue MJ, Franklin EC, Kittinger JN, McManus MA, Toonen RJ (2022) Fish flow: following fisheries from spawning to supper. Frontiers in Ecology and the Environment 20: 247-254 doi: 10.1002/fee.2449 \

Mau A+, Franklin EC, Huss GR, Nagashima K, Nicodemus P, Valdez A, Bingham J-P (2021) Near-daily reconstruction of tropical intertidal SST from limpet shells to infer their growth rates. Nature Communications Earth & Environment 2, 171 doi.org: 10.1038/s43247-021-00251-2 \

Carlson B, Awai M, Saunders WB, Franklin EC (2021) Nautilus belauensis population demographics and trap yields in Palau were similar between surveys in 1982 and 2015. Marine Ecology Progress Series 670: 239-245 doi.org: 10.3354/meps13773 \

Gill A+, Franklin EC, Donaldson TJ (2021) Fore reef location influences spawning success and egg predation in lek-like mating territories of the bird wrasse Gomphosus varius. Journal of Fish Biology doi: 10.1007/s10641-021-01084-w \

Altman-Kurosaki NT*, Smith CM, Franklin EC (2021) Oahu's marine protected areas have limited success in protecting coral reef herbivore functional assemblages. Coral Reefs doi.org: 10.1007/s00338-021-02054-5 \

Scherrer SR+, Kobayashi DR, Weng KC, Okamoto HY, Oishi FG, Franklin EC (2021) Estimation of growth parameters integrating tag-recapture, length-frequency, and direct aging data using likelihood and Bayesian methods for the tropical deepwater snapper Pristipomoides filamentous in Hawaii. Fisheries Research 233: 105753 doi.org: 10.1016/j.fishres.2020.105753 \

Longenecker K, Langston R, Gill A+, Kelokelo M+, Donaldson TJ, Franklin EC (2020) Rapid reproductive analysis and weight-length relation of the humpnose big-eye bream Monotaxis grandoculis (Actinopterygii: Perciformes: Lethrinidae) from Micronesia with implications for fisheries. Acta Ichthyologica et Piscatoria 50 (4): 493–500. doi: 10.3750/AIEP/02965. \

Winter KB, Rii YM, Reppun FAWL, Hintzen KD, Alegado R, Bowen BW, Bremer LL, Coffman M, Deenik JL, Donahue MJ, Falinski FA, Frank K, Franklin EC, Kurashima N, Lincoln NK, Madin E, McManus MA, Nelson CE, Okano R, Olegario A, Pascua P, Oleson KLL, Price MR, Rivera MAJ, Rodgers KS, Ticktin T, Sabine C, Smith CM, Hewett A, Kaluhiwa R, Cypher M, Thomas B, Leong J, Kekuewa K, Tanimoto J, Kukea-Shultz K, Kawelo H, Kotubetey K, Neilson B, Lee T, Toonen RJ (2020) Collaborative research to inform adaptive co-management: A framework for the Heʻeia National Estuarine Research Reserve. Ecology and Society 25(4): 15. doi.org: 10.5751/ES-11895-27750415 \

Winter KB, Lincoln NK, Berkes F, Kawelo H, Kotubetey K, Kukea-Shutlz K, Alegado R, Kurashima N, Frank K, Pascua P, Rii Y, Reppun F, Knapp I, McClatchey W, Ticktin T, Smith C, Franklin EC, Oleson K, Price M, McManus M, Donahue M, Rodgers K, Bowen B, Nelson C, Beilson B, Thomas B, Leong J-A, Madin E, Rivera MA, Falinski K, Bremer L, Deenik J, Gon III S, Okano R, Olegario A, Toonen R (2020) Eco-mimicry in indigenous resource management: optimizing ecosystem services to achieve resource abundance in Hawai'i. Ecology and Society 25: 26. doi: 10.5751/ES-11539-250226 \

Oyafuso ZS*, Leung PS, Franklin EC (2020) Evaluating biological and socioeconomic tradeoffs of marine reserve planning via a flexible integer linear programming approach. Biological Conservation 241: 108319 doi.org/10.1016/j.biocon.2019.108319 \

Franklin EC, Gray AE, Mundy BC (2019) Three new records of coastal fishes in the Hawaiian Islands. Journal of the Ocean Science Foundation, 33: 99–106 doi.org/10.5281/zenodo.3572888 \

Barkley YM*, Oleson EM, Oswald JN, Franklin EC (2019) Whistle classification of sympatric false killer whale populations in Hawaiian waters yields low accuracy rates. Frontiers in Marine Science 6: 645 doi.org/10.3389/fmars.2019.00645 \

Mora C, Rollins R+, Taladay K+, Kantar M, Chock M+, Shimada M+, Franklin EC (2019) Mora et al. reply. Nature Climate Change 9: 658-659 doi.org/10.1038/s41558-019-0538-1 \

Darling ES, McClanahan TR, Maina J, Gurney G, Graham NAJ, Januchowski-Hartley F, Cinner JE, Mora C, Hicks CC, Maire E, Puotinen M, Skirving WJ, Adjeroud M, Ahmadia G, Arthur R, Bauman AG, Beger M, Berumen ML, Bigot L, Bouwmeester, Brenier, Bridge T, Brown E, Campbell SJ, Cannon S, Cauvin B, Chen AC, Claudet J, Denis V, Donner S, Estradivari, Fadli N, Feary DA, Fenner D, Fox H, Franklin EC, Friedlander A, Gilmour J, Goiran C, Guest J, Hobbs, J-PA, Hoey AS, Houk P, Johnson S, Jupiter S, Kayal M, Kuo C-Y, Lamb J, Lee MAC, Low J, Muthiga N, Muttaqin, Nand Y, Nash KL, Nedlic O, Pandolfi JM, Pardede S, Patankar V, Penin L, Ribas-Deulofeu L, Richards Z, Roberts TE, Rodgers KS, Safuari CDM, Sala E, Shedrawi G, Sin TM, Smallhorn-West P, Smith JE, Sommer B, Steinberg PD, Sutthacheep M, Tan CHJ, Williams GJ, Wilson S, Yeemin T, Bruno JF, Fortin MJ, Krkosek M, Mouillot D (2019) Social-environmental drivers inform strategic management of coral reefs in the Anthropocene. Nature Ecology and Evolution 3: 1341–1350 doi.org/10.1038/s41559-019-0953-8 \

Randall JE, Gray A, Franklin EC, Mundy BC, McCosker JE (2019) Five new records of fishes for the Hawaiian Islands. Journal of Ocean Science Foundation 33: 28-43. http://dx.doi.org/10.5281/zenodo.3255089 \

Johnson GB + , Taylor BM, Robbins WD, Franklin EC, Toonen R, Bowen BW, Choat JH (2019) Diversity and structure of parrotfish assemblages across the northern Great Barrier Reef. Diversity 11(1):14 doi.org/10.3390/d11010014 \

Oyafuso ZS*, Leung PS, Franklin EC (2018) Evaluating bioeconomic tradeoffs of fishing reserves via spatial optimization. Marine Policy doi.org/10.1016/j.marpol.2018.11.016 \

Mora C, Spirandelli D, Franklin EC, Lynham J, Kantar MB, Miles W, Smith CZ + , Freel K, Moy J + , Louis LV + , Barba EW + , Bettinger K, Frazier AG, Colburn IX JF + , Hanasaki N, Hawkins E, Hirabayashi Y, Knorr W, Little CM, Emanuel K, Sheffield J, Patz JA, Hunter CL (2018) Broad threat to humanity from cumulative climate hazards intensified by greenhouse gas emissions. Nature Climate Change 8: 1062-1071. doi.org/10.1038/s41558-018-0315-6 \

Mora C, Rollins R + , Taladay K + , Kantar MB, Chock MK + , Shimada M + , Franklin EC (2018) Bitcoin emissions alone could push global warming above 2°C. Nature Climate Change 8: 931-933. doi.org/10.1038/s41558-018-0321-8 \

Geronimo, R + , Franklin EC, Brainard RE, Elvidge CD, Santos MD, Venegas R, Mora C (2018) Mapping fishing activities and suitable fishing grounds using nighttime satellite images and maximum entropy modelling. Remote Sensing 10: 1604 doi.org/10.3390/rs10101064 \

Forsman ZH, Maurin P, Parry M, Chung A + , Sartor C, Hixon MA, Hughes K, Rodgers K, Knapp I, Gulko DA, Franklin EC, Del Rio Torres L, Chan NT, Wolke CS, Gates RD, Toonen RJ (2018) The First Hawai‘i Workshop For Coral Restoration & Nurseries. Marine Policy 96:133-135 doi.org/10.1016/j.marpol.2018.08.009 \

Counsell CWW + , Donahue MJ, Edwards K, Franklin EC, Hixon MA (2018) Variation in coral-associated cryptofaunal communities along spatial scales and environmental gradients. Coral Reefs 37:827-840. doi: 10.1007/s00338-018-1709-7 \

Levy J + , Hunter C, Lukaczyk, Franklin EC (2018) Assessing the spatial distribution of coral bleaching using small unmanned aerial systems. Coral Reefs 37: 373-387 doi.org: 10.1007/s00338-018-1662-5 \

Franklin EC (2017) Vagrancy in paradise: documentation of the chevron butterflyfish Chaetodon trifascialis in Kaneohe Bay, Oahu, Hawaiian Islands. Marine Biodiversity Records 10:22 doi: 10.1186/s41200-017-0124-z \

Longenecker K, Langston R, Bolick H, Crane M, Donaldson TJ, Franklin EC, Kelokelo M, Kondio U, Potuku T (2017) Rapid reproductive analysis and length–weight relations for five species of coral-reef fishes from Papua New Guinea: Nemipterus isacanthus, Parupeneus barberinus, Kyphosus cinerascens, Ctenochaetus striatus, and Balistapus undulatus. Acta Ichthyol. Piscatoria 47:107-124. doi: 10.3750/AIEP/02146 \

Oyafuso ZS*, Drazen JC, Moore CH, Franklin EC (2017) Habitat-based species distribution modelling of the Hawaiian deepwater snapper-grouper complex Fisheries Research 195: 19-27 doi: 10.1016/j.fishres.2017.06.011 \

Winston MS*, Taylor B, Franklin EC (2017) Intraspecific variability in the life history of endemic coral reef fishes between photic and mesophotic populations. Coral Reefs 36: 663-674. doi: 10.1007/s00338-017-1559-8 \

Kapur MR*, Franklin EC (2017) Predicting climate impacts on tropical fisheries: are contemporary spatial management strategies sufficient? Canadian Journal of Fisheries and Aquatic Sciences doi: 10.1139/cjfas-2016-0200 \

Veazey LM + , Franklin EC, Kelley C, Rooney J, Frazer NL, Toonen RJ (2016) The implementation of rare events logistic regression to predict the distribution of mesophotic hard corals across the main Hawaiian Islands. PeerJ 4:e2189 doi: 10.7717/peerj.2189 \

Selkoe KA, Gaggiotti OE, Donovan MK + , Treml EA, Wren JLK + , Hawai‘i Reef Connectivity Consortium†, Toonen RJ (2016) The DNA of coral reef biodiversity – predicting and protecting genetic diversity of reef assemblages. Proceedings of the Royal Society B 283: 20160354. doi: 10.1098/rspb.2016.0354 \

Oyafuso ZS*, Toonen RJ, Franklin EC (2016) Temporal and spatial trends in prey diversity of wahoo (Acanthocybium solandri): A diet analysis from the central North Pacific using visual and DNA bar-coding techniques. Journal of Fish Biology 88:1501-1523. doi:10.1111/jfb.12928 \

Madin JS, Andreasen M, Bridge T, Connolly SR, Darling E, Diaz M, Falster D, Franklin EC, Gates RD, Hoogenboom MO, Huang D, Keith SA, Kuo CY, Lovelock CE, Luiz O, Martinelli J, Mizere T, Pandolfi JM, Pochon X, Putnam HM, Roberts TE, Stat M, Baird AH (2016) The Coral Trait Database. Nature Scientific Data 3:160017. doi:10.1038/sdata.2016.17 \

Edmunds PJ, Adjeroud M, Baskett ML, Baums IB, Budd AF, Carpenter RC, Fabina NS, Fan T-Y, Franklin EC, Gross K, Han X, Jacobson L, Klaus JS, McClanahan TR, O’Leary JK, van Oppen MJH, Pochon X, Putnam HM, Smith TB, Stat M, Sweatman H, van Woesik R, Gates RD (2014) Persistence and change in community composition of reef corals through present, past and future climates. PLoS ONE 9(10): e107525. doi:10.1371/journal.pone.0107525 \

Ault JS, Smith SG, Browder J, Nuttle W, Franklin EC, DiNardo GT, Bohnsack JA (2014) Indicators for assessing the ecological dynamics and sustainability of southern Florida's coral reef and coastal fisheries. Ecological Indicators 44:164-172. doi: 10.1016/j.ecolind.2014.04.013 \

Baums IB, Godwin LS, Franklin EC, Carlon DB, Toonen RJ (2014) Discordant population expansions in four species of coral-associated, Pacific hermit crabs (Anomura: Diogenidae) linked to habitat availability resulting from sea level change. Journal of Biogeography 41: 339-352. doi: 10.1111/jbi.12181 \

Fabina NS, Putnam HM, Franklin EC, Stat M, Gates RD (2013) Symbiotic specificity, association patterns, and function determine community responses to global changes: Defining critical research areas for coral-Symbiodinium symbioses. Global Change Biology 19: 3306–3316. doi: 10.1111/gcb.12320 \

Bird CE, Franklin EC, Smith CM, Toonen RJ (2013) Between tide and wave marks: a unifying model of physical zonation on littoral shores. PeerJ 1:e154 doi: 10.7717/peerj.154 \

Farmer NA, Ault JS, Smith SG, Franklin EC (2013) Methods for assessment of short-term coral reef fish movements within an acoustic array. Movement Ecology 2013:1-7. doi:10.1186/2051-3933-1-7 \

Franklin EC, Jokiel PL, Donahue MJ (2013) Predictive modeling of coral distribution and abundance in the Hawaiian Islands. Marine Ecology Progress Series 481:121-132. doi:10.3354/meps10252 \

Stat M, Pochon X, Franklin EC, Bruno JF, Casey KS, Selig ER, Gates RD (2013) The distribution of the thermally tolerant symbiont lineage (Symbiodinium clade D) in corals from Hawaii: correlations with host and the history of ocean thermal stress. Ecology and Evolution 3:1317-1329. doi: 10.1002/ece3.556 \

Fabina NS, Putnam HM, Franklin EC, Stat M, Gates RD (2012) Transmission mode predicts specificity and interaction patterns in coral-Symbiodinium networks. PLoS ONE 7(9): e44970. doi:10.1371/journal.pone.0044970 \

Heron SF, Maynard J, Willis B, Christensen T, Harvell D, Vargas-Angel B, Beeden R, Sziklay J, Aeby G, Franklin EC, and 8 others (2012) Developments in understanding relationships between environmental conditions and coral disease. Proc 12th Int’l Coral Reef Symposium, Cairns, Australia. 16B:4. \

van Woesik R, Franklin EC, O’Leary J, McClanahan TR, Klaus JS, Budd AF (2012) Hosts of the Plio-Pleistocene past reflect modern-day coral vulnerability. Proceedings of the Royal Society B doi: 10.1098/rspb.2011.2621. \

Franklin EC, Stat M, Pochon X, Putnam HM, Gates RD (2012) GeoSymbio: A hybrid, cloud-based web application of global geospatial bioinformatics and ecoinformatics for Symbiodinium-host symbioses. Molecular Ecology Resources 12(2): 369-373. doi:10.1111/j.1755-0998.2011.03081.x. \

Franklin EC, Stat M, Pochon X, Putnam HM, Gates RD (2011) "Rapid Development of a Hybrid Web Application for Synthesis Science of Symbiodinium with Google Apps". In Jones, MB, Gries C (eds.) Proceedings of Environmental Information Management Conference 2011 (EIM 2011), Sep 28-29, 2011, UCSB, California, pp 44-48, doi:10.5060/D2NC5Z4X \

Longenecker K, Chan Y, Franklin EC (2011) Relationships between the length of select head bones and body size for some Hawaiian parrotfishes (subfamily Scarinae). Bishop Museum Occasional Papers 111:13-26. \

Aeby GS, Williams GJ, Franklin EC, Kenyon J, Cox EF, Coles S, Work TM (2011) Patterns of coral disease across the Hawaiian Archipelago: relating disease to environment. PLoS ONE 6(5): e20370. doi:10.1371/journal.pone.0020370 \

Aeby GS, Williams GJ, Franklin EC, Haapkyla J, Harvell CD, Neale S, Page CA, Raymundo L, Vargas-Angel B, Willis BL, Work TM, Davy SK. (2011) Growth anomalies on the coral genera Acropora and Porites are strongly associated with host density and human population size across the Indo-Pacific. PLoS ONE 6(2): e16887. doi:10.1371/journal.pone.0016887 \

Franklin EC (2010) Marine landscape ecology of coral reefs emerges from developments in seafloor mapping, GPS, and GIS. Pp 193-204 in Breman J, Ocean Globe. ESRI Press: Redlands, CA. \

Concepcion, GT, Kahng SE, Crepeau MW, Franklin EC, Coles SL, Toonen RJ (2010) Resolving natural ranges and marine invasions in a globally distributed octocoral (genus Carijoa). Marine Ecology Progress Series 401:113-127. \

Franklin EC, Dow A, Brong C, Craig M. Length-weight and length-length relationships of three endemic butterflyfish species (Chaetodontidae) from coral reefs of the Northwestern Hawaiian Islands, USA. (2009) Journal of Applied Ichthyology 25(5):616-617. \

Selkoe KA, Halpern BS, Ebert CM, Franklin EC, Selig ER, Casey KS, Bruno J, Toonen RJ (2009) A map of human impacts to a “pristine” coral reef ecosystem, the Papahanaumokuakea Marine National Monument. Coral Reefs 28(3):635-650. \

Franklin EC (2008) Vessel traffic patterns in the Northwestern Hawaiian Islands between 1994-2004. Marine Pollution Bulletin 56:150-153 \

Hudson JH, Franklin EC. (2006) Structural Stabilization of a Large Montastrea faveolata (Ellis and Solander, 1786) Colony Damaged by Vessel Impact. Caribbean Journal of Science 42(2):252-254 \

Hudson JH, Franklin EC (2006) Coral reef restoration of a storm-disturbed vessel grounding site in the Florida Keys National Marine Sanctuary, USA. Proc 10th Int’l Coral Reef Symposium, Okinawa, Japan. 1631-1636. \

Hudson JH, Franklin EC (2005) Structural Reef Restoration and Coral Transplantation to the R/V Columbus Iselin Grounding Site in the Florida Keys National Marine Sanctuary. Proc OCEANS 2005 Americas MTS/IEEE Conference, Washington, DC, September 19-23, 2005. \

Franklin EC, Ault JS, Smith SG, Luo J, Meester GA, Diaz GA, Chiappone M, Swanson DW, Miller SL, Bohnsack JA (2003) Benthic habitat mapping in the Tortugas region, Florida. Marine Geodesy 26(1-2):19-34. \

Ault JS, Smith SG, Meester GA, Luo J, Franklin EC, Bohnsack JA, Harper DE, McClellan DB, Miller SL, Chiappone M, Swanson DW (2002) Synoptic habitat and reef fish surveys support establishment of marine reserves in Dry Tortugas, Florida USA. Reef Encounter 31:22-23. \

Franklin EC, Ault JS, Smith SG (2002) Utilization of a GIS in a fisheries assessment and management system. In: J. Breman (ed) Marine Geography: GIS for the Oceans and the Seas. Redlands, CA: ESRI Press. \

Miller SL, Swanson DW, Chiappone M, Ault JS, Smith SG, Meester GA, Luo J, Franklin EC, Bohnsack JA, Harper DE, McClellan DB (2001) An extensive deep reef terrace on the Tortugas Bank, Florida Keys National Marine Sanctuary. Coral Reefs 20:299-300.


<script>
    function filterPublications() {
        var filterValue = document.getElementById("filter").value;
        var publications = document.getElementsByClassName("publication-entry");

        for (var i = 0; i < publications.length; i++) {
            var publication = publications[i];
            if (filterValue === "all") {
                publication.style.display = "block";
            } else if (publication.classList.contains(filterValue)) {
                publication.style.display = "block";
            } else {
                publication.style.display = "none";
            }
        }
    }
</script>
<script>
    function openModal(id) {
        var modal = document.getElementById("modal");
        modal.style.display = "flex"; // Show the modal
    }

    function closeModal() {
        var modal = document.getElementById("modal");
        modal.style.display = "none"; // Hide the modal
    }

    function copyToClipboard(elementId) {
        var citationText = document.getElementById(elementId).innerText;
        navigator.clipboard.writeText(citationText).then(function() {
            alert("Citation copied to clipboard!");
        }, function(err) {
            console.error("Could not copy text: ", err);
        });
    }

    function downloadCitation() {
        var citationText = document.getElementById('citationText').innerText;
        var blob = new Blob([citationText], { type: 'text/plain' });
        var link = document.createElement('a');
        link.href = window.URL.createObjectURL(blob);
        link.download = 'citation.txt';
        link.click();
    }
</script>
