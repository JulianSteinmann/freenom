# freenom


## Free Domains for your coding exercises  
Allows you to register free domain names (.tk .ml .cf .gq)   
Registration is valid for up to 12 mondths with free renevals. (no auto-reneval)  


## Downsides
Those domains has several drawbacks and therefore probably should not be used for any production app.  
– SEO  
Domain extension may have bad effects for SEO.  
  
– Blocked domain extension  
Some company networks may block these 'newcomer' domains  
  
– Only "www." with Heroku  
As Heroku does not provide a static IP address and freenom only allows directing the root domain through a A-Record only the domain "www.example.tk" will work and not "example.tk". (I have been unsuccesfully looking for a workaround for this...)
  
  
## How To Setup
– Go to "freenom.com" and sign in.  
– Click on Servces/Register new domain  
– Search for desired domain and checkout (doing this before loggin in may cause bugs on the website)  
– In heroku app settings tab add your domain with "www." prefix (www.example.tk)  
– Copy DNS Target you get.  
– Go to Freenom Services/MyDomains/Manage Domain/Manage Freenom DNS  
– Add record with  
Name:www  
Type: CNAME  
Target: Paste DNS Target here  
– Test if your site is loading (make sure to open it with "www.") (may take up to a day to resolve DNS)  
