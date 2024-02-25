<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Zendesk Görüş Formu</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f4f4f4;
    }

    .container {
      max-width: 600px;
      margin: 50px auto;
      padding: 20px;
      background-color: #fff;
      border-radius: 8px;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    }

    h1 {
      color: #333;
    }

    p {
      color: #666;
    }

    form {
      margin-top: 20px;
    }

    label {
      font-weight: bold;
      color: #333;
    }

    input[type="text"],
    input[type="email"],
    textarea {
      width: 100%;
      padding: 8px;
      margin-top: 5px;
      margin-bottom: 15px;
      border: 1px solid #ccc;
      border-radius: 4px;
      box-sizing: border-box;
    }

    button[type="submit"] {
      background-color: #007bff;
      color: #fff;
      border: none;
      border-radius: 4px;
      padding: 10px 20px;
      cursor: pointer;
      font-size: 16px;
    }

    button[type="submit"]:hover {
      background-color: #0056b3;
    }
  </style>
</head>
<body>
  <script type="text/javascript">
        window.zESettings = {
            webWidget: {
        color: { theme: '#78a300' },
            }
        };
  </script>
</script>
<!-- Start of Zendesk Widget script -->
<script id="ze-snippet" src="https://static.zdassets.com/ekr/snippet.js?key=e9c9d380-7e28-458d-8703-b2ad2bd96843">
</script>
<!-- End of Zendesk Widget script -->

  <div class="container">
    <h1>Görüşlerinizi Bizimle Paylaşın</h1>
    <p>Lütfen aşağıdaki formu kullanarak görüşlerinizi veya geribildirimlerinizi bizimle paylaşın.</p>
    <form action="https://scwx1682530387.zendesk.com/hc/en-us/requests/new" method="post" target="_blank">
      <input type="hidden" name="ticket_form_id" value="YOUR_TICKET_FORM_ID">
      <label for="name">Adınız:</label>
      <input type="text" id="name" name="name" required><br><br>
      <label for="email">E-posta Adresiniz:</label>
      <input type="email" id="email" name="email" required><br><br>
      <label for="subject">Konu:</label>
      <input type="text" id="subject" name="subject" required><br><br>
      <label for="description">Mesajınız:</label><br>
      <textarea id="description" name="description" rows="4" cols="50" required></textarea><br><br>
      <button type="submit">Gönder</button>
    </form>
  </div>
</body>
</html>
