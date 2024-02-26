<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PayPal SDK Test</title>
    <script src="https://www.paypal.com/sdk/js?client-id=AftTXN0blRv0ltUpXOXhTWgUgyoMXw83iV54WUwm2VFXevA-_z4oWajYoxeWwZ-Y_mK1kxIBBXG0HqQ1"></script>
</head>
<body>

<h1>PayPal SDK Test Form</h1>

<div id="paypal-button-container"></div>

<script>
    paypal.Buttons({
        createOrder: function(data, actions) {
            return actions.order.create({
                purchase_units: [{
                    amount: {
                        value: '0.01' // Ödeme miktarı
                    }
                }]
            });
        },
        onApprove: function(data, actions) {
            return actions.order.capture().then(function(details) {
                alert('Transaction completed by ' + details.payer.name.given_name);
            });
        }
    }).render('#paypal-button-container');
</script>

</body>
</html>
