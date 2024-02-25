<html>

<head>
  <meta charset="utf-8">
</head>

<body>

  <!-- dynamic content placeholder -->
  <div id="content" style="padding-top: 20px;"></div>

  <!-- Web Widget -->
  <script id="ze-snippet" src="https://static.zdassets.com/ekr/snippet.js?key=e9c9d380-7e28-458d-8703-b2ad2bd96843"></script>

  <!-- hello template -->
  <script id="hello-template" type="text/x-handlebars-template">
    <p>Hello!</p>
    <a id="link-goodbye" href="#">I'm finished reading this page!</a>
  </script>

  <!-- goodbye template -->
  <script id="goodbye-template" type="text/x-handlebars-template">
    <p>Goodbye!</p>
    <a id="link-hello" href="#">No, take me back!</a>
  </script>

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
  <script>
    var VIRTUAL_AGENT_NAME = 'replace me with name of the virtual department';
    var HUMAN_DEPARTMENT_NAME = 'replace me with name of human department';

    zE('webWidget:on', 'chat:departmentStatus', function(dept) {
        if (dept.name === VIRTUAL_AGENT_NAME && dept.status === 'online') {
            zE('webWidget', 'updateSettings', {
                webWidget: {
                    chat: {
                        departments: {
                            enabled: [''],
                            select: VIRTUAL_AGENT_NAME
                        },
                    }
                }
            });
        } else if (dept.name === VIRTUAL_AGENT_NAME && dept.status !== 'online') {
            zE('webWidget', 'updateSettings', {
                webWidget: {
                    chat: {
                        departments: {
                            enabled: [''],
                            select: HUMAN_DEPARTMENT_NAME
                        },
                    }
                }
            });
        }
    });
</script>

</body>

</html>
