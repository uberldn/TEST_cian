<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>coe_entry</title>
    <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.1.1/jquery.js"></script>
    <script type="text/javascript">
      $(function() {
        // Parse the user agent to determine the device
        var isiPad = navigator.userAgent.match(/iPad/i) != null,
            isiPhone = !isiPad && ((navigator.userAgent.match(/iPhone/i) != null) || (navigator.userAgent.match(/iPod/i) != null)),
            isiOS = isiPad || isiPhone,
            isAndroid = !isiOS && navigator.userAgent.match(/android/i) != null,
            isMobile = isiOS || isAndroid,
            isDesktop = !isMobile;
        // Define all the potential redirection Urls
        var deepLink = 'uber://?action=applyPromo&promo=coe_entry',
            appStoreUrl = 'https://itunes.apple.com/us/app/uber/id368677368',
            androidIntentUrl = 'https://m.uber.com/ul/?action=applyPromo&promo=coe_entry',
            muberDotCom = 'https://login.uber.com/login';
        // Handle each case with a seamless fallback to the application store on mobile devices
        if (isiOS) {
          window.location = deepLink;
          setTimeout(function() { window.location = appStoreUrl; }, 25);
        } else if (isAndroid) {
          window.location = androidIntentUrl;
        } else if (isDesktop) {
          window.location = muberDotCom;
        }
      });
    </script>
  </head>
  <body>
  </body>
</html>
