# Owlings Pay Javascript SDK

Owlings enables businesses to receive contactless payment both onsite and online on their websites.



This is a guide on how to implement Owlings Pay on your website using Owlings inline js.

### Step 1: Import the Owlings Pay inline SDK into your page

```html
<script async type="text/javascript" src="https://cdn.jsdelivr.net/gh/OwlingsHQ/owlingspay-js-sdk@main/owlingspay.js"></script>
```

### Step 2: Setup and Initiate payment on your website

To initiate payment, pass the setup parameters to Owlings.pay as shown in the code snippet below

```javascript
Owlings.pay({
key:"Your public key comes here",   //string
amount:"Amount to pe paid in kobo", //number. Cannot be less than 10000
currency:"NGN", //string
onSuccess:function(ref){}, //function Your on success handler. A reference will be returned when payment is successful,
onError:function(e){}, //function your on error handler,
onClose:function(){}, //functon your on close handler
env:"sandbox",  //string. One of sandbox or production
title:"title of this payment", //string
description: "Description/narrative of this payment", //string
})
```

### Step 3: Handle Payment outcome

You should handle payment outcome by passing the onSuccess, onClose, and onError methods to the setup


### Step 4: Verify Payment
You can verify this payment on your server by calling the verify endpoint
```
https://api.pay.owlings.com/verify
```

### Step 5: Error Handling

Your setup will be validated before we initiate payment, if something is amiss, an error will be thrown. This should help during your integration.


## Live Demo

To see a live demo of Owlings Pay, visit:
```
https://merchants.owlings.com/demo
```


