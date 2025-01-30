<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Welcome to The Franklin Lab!</title>
  <style>
    /* Hero Section Styles */
    .hero {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: #ffffff;
      height: 100vh;
      padding: 20px;
      position: relative;
      background-image: url('/images/kaneohe-bay.jpg');
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
    }
    .hero .images {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-top: 20px;
      position: relative;
      z-index: 1;
    }
    .hero .images img {
      max-width: 100px;
      height: auto;
      z-index: 2;
    }
    /* CTA Links Section Styles */
    .cta-links {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px; /* Space between links */
      margin-top: 40px; /* Add space between sections */
    }
    .cta-links .cta {
      display: inline-block;
      padding: 15px 25px;
      text-align: center;
      border-radius: 5px;
      text-decoration: none;
      color: white;
      font-size: 16px;
      flex: 1 1 150px;
      background-size: cover;
      background-position: center;
      height: 150px; /* Fixed height for the links */
    }
    .cta-links .cta:nth-child(1) {
      background-image: url('images/Papio.jpeg');
    }
    .cta-links .cta:nth-child(2) {
      background-image: url('images/Papio.jpeg');
    }
    .cta-links .cta:nth-child(3) {
      background-image: url('images/Papio.jpeg');
    }
    .cta-links .cta:nth-child(4) {
      background-image: url('images/Papio.jpeg');
    }
    .cta-links .cta:nth-child(5) {
      background-image: url('images/Papio.jpeg');
    }
    .cta-links .cta:nth-child(6) {
      background-image: url('images/Papio.jpeg');
    }
    .cta-links .cta:hover {
      opacity: 0.8;
    }
  </style>
</head>
<body>

  <!-- Hero Section -->
  <section class="hero">
    <h1>Welcome to The Franklin Lab!</h1>
    <p>Hawaii Institute of Marine Biology</p>
    <p>School of Ocean and Earth Science and Technology</p>
    <p>University of Hawaii at Manoa</p>
    <div class="images">
      <img src="images/HIMB_Icon_White.png" alt="HIMB Logo">
      <img src="images/SOEST_logo.jpg" alt="SOEST Logo">
      <img src="images/manoaseal_logo.png" alt="Manoaseal Logo">
    </div>
  </section>

  <!-- Links Section -->
  <section class="cta-links">
    <h2>Explore Our Work</h2>
    <p>Research and Publications</p>
    <a href="./about/" class="cta">About</a>
    <a href="./research/" class="cta">Research</a>
    <a href="./people/" class="cta">People</a>
    <a href="./publications/" class="cta">Publications</a>
    <a href="./resources/" class="cta">Resources</a>
    <a href="./want-to-join-us/" class="cta">Want to Join Us?</a>
  </section>

</body>
</html>
