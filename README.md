# GA-Enhanced-Ecommerce-Tracking

#Ecommerce Checkout Tracking - Install in check out page 
<script>
/**
 * A function to handle a click on a checkout button. This function uses the eventCallback
 * data layer variable to handle navigation after the ecommerce data has been sent to Google Analytics.
 */
function onCheckout() {
  dataLayer.push({
    'event': 'checkout',
    'ecommerce': {
      'checkout': {
        'products': [{
          'name': '$productname',
          'id': '$productid',
          'price': '$price',
          'brand': '$brand',
          'category': '$category',
          'variant': '$varient',
          'quantity': $quqntity
       }]
     }
   },
   
  });
}
</script>



This should be in Order success page after payment

<script>
dataLayer.push({
  'ecommerce': {
    'purchase': {
      'actionField': {
        'id': '$orderid',                         // Transaction ID. Required for purchases and refunds
        'revenue': '$total',                     // Total transaction value (incl. tax and shipping)
        'tax':'$gst',
        'shipping': '$shipping',
        'coupon': '$coupon'
      },
      'products': [{                            // List of productFieldObjects.
          'name': '$productname',
          'id': '$productid',
          'price': '$price',
          'brand': '$brand',
          'category': '$category',
          'variant': '$varient',
          'quantity': $quqntity
       },
       {
          'name': '$productname',
          'id': '$productid',
          'price': '$price',
          'brand': '$brand',
          'category': '$category',
          'variant': '$varient',
          'quantity': $quqntity
       }]
    }
  }
});
</script>
