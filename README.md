<!DOCTYPE html>
<html lang="en">

<head>
    <title>Hello, World!</title>
    <meta charset="utf-8">
</head>

<body>
    <p>Hello, World!</p>

    <script type="text/javascript">
        window.zESettings = {
            webWidget: {
                color: {
                    theme: '#78a300'
                },
                offset: {
                    horizontal: '100px',
                    vertical: '100px'
                },

        };
    </script>
    <!-- Start of Zendesk Widget script -->
    <script id="ze-snippet" src="https://static.zdassets.com/ekr/e9c9d380-7e28-458d-8703-b2ad2bd96843">
    </script>
    <!-- End of Zendesk Widget script -->
<script type="text/javascript">
  zE('webWidget', 'setLocale', 'fr');
</script>

  <button onclick="zE('webWidget', 'hide')">Hide Web Widget</button>
</body>
</html>
  <!-- show templates -->
  <script src="https://cdn.jsdelivr.net/npm/handlebars@4.3.3/dist/handlebars.min.js"></script>
  <script>
    (function () {
      // showHello function
      function showHello() {
        var source = document.getElementById("hello-template").innerHTML;
        var template = Handlebars.compile(source);
        document.getElementById("content").innerHTML = template();

        var linkGoodbye = document.getElementById("link-goodbye");
        linkGoodbye.addEventListener("click", showGoodbye);
      }

      // showGoodbye function
      function showGoodbye() {
        var source = document.getElementById("goodbye-template").innerHTML;
        var template = Handlebars.compile(source);
        document.getElementById("content").innerHTML = template();

        var linkHello = document.getElementById("link-hello");
        linkHello.addEventListener("click", showHello);
      }

      // show hello content to start
      showHello();
    })();
  </script>

</script>

</body>

</html>
