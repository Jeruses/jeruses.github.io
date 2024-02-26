<html>
<head>
  <!-- Load deepar.js -->
  <script src='https://cdn.jsdelivr.net/npm/deepar/js/deepar.js'> </script>
</head>

<body>
  <!-- Div element where AR preview will be inserted -->
  <div style='width: 640px; height: 360px' id='deepar-div'></div>
  <!-- Initialize DeepAR and load AR effect/filter -->
  <script>
    (async function() {
      const deepAR = await deepar.initialize({
        licenseKey: 'your_license_key_here',
        previewElement: document.querySelector('#deepar-div'),
        effect: 'https://cdn.jsdelivr.net/npm/deepar/effects/aviators'
      });
    })();
  </script>
</body>
</html>
