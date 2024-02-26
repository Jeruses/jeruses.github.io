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
        licenseKey: 'e187c2a41fe60c0fc702428d9927f43a4cbff4b3b7f6900abd61c5fae5057256058d13c3dbc65638',
        previewElement: document.querySelector('#deepar-div'),
        effect: 'https://cdn.jsdelivr.net/npm/deepar/effects/aviators'
      });
    })();
  </script>
</body>
</html>
