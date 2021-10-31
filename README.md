### Owlings Pay Javascript SDK

Owlings enables businesses to receive contactless payment both onsite and online on their websites.



This is a guide on how to implement Owlings Pay on your website using Owlings inline js.

Step 1: Import the Owlings Pay inline SDK into your page
<script async type="text/javascript" src="cdn/owlings.js"></script>
Step 2: Setup and Initiate payment on your website
To initiate payment, pass the setup parameters to Owlings.pay as show in the code snippet below

Owlings.pay({
key:"Your public key comes here",
amount:"Amount to pe paid in kobo",
currency:"NGN",
onSuccess:function(ref){}// Your on success handler. A reference will be returned when payment is successful,
onError:function(e){}// your on error handler,
onClose:function(){}// your on close handler
})
Step 3: Handle Payment outcome
You should handle payment outcome by passing the onSuccess, onClose, and onError methods to the setup
Step 4: Verify Payment
You can verify this payment on your server by calling the verify endpoint

https://api.pay.owlings.com/verify
Step 5: Error Handling
Your setup will be validated before we initiate payment, if something is amiss, an error will be thrown. This should help during your integration.


Sample Pay
See the implementation below as example

Pay 1000
