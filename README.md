<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>FullPage.js Example</title>
<style>
  .section {
    text-align: center;
    font-size: 3em;
    font-family: arial;
  }
</style>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/fullPage.js/3.1.2/fullpage.min.css">
</head>
<body>

<div id="fullpage">
  <div class="section"><h1>Section 1</h1></div>
  <div class="section">
    <div class="slide" data-anchor="slide1">
      <h1>Slide 2.1</h1>
    </div>
    <div class="slide" data-anchor="slide2">
      <h1>Slide 2.2</h1>
    </div>
  </div>
  <div class="section"> 
    <h2>Section 3</h2>
  </div>
</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/fullPage.js/3.1.2/fullpage.min.js"></script>
<script>
  new fullpage('#fullpage', {
    sectionsColor: ['yellow', 'orange', '#C0C0C0', '#ADD8E6'],
    
    // Get your license at https://alvarotrigo.com/fullPage/pricing/
    licenseKey: 'YOUR LICENSE KEY HERE'
  });
</script>

</body>
</html>
