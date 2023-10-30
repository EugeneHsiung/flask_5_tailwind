# flask_5_tailwind

follow guide: https://learn.microsoft.com/en-us/azure/cdn/cdn-create-a-storage-account-with-cdn

sign in azure
search up storage accounts 
click create,  
select subscription and resrouce group leave everything else the same, create Storage account name and press create
under overview, click on secruity, Make sure Secure transfer required, Allow Blob anonymous access, and Allow storage account key access are enabled
under data storage, click containers
click + containers, change anonymous access level to container(anoynymus read access for containers and blob) and create a name
under Security + networking click Front Door and CDN
Under service type, click azure CDN, create new, profile name, endpoint name. Under Query string caching behavior click Ignore Query String, press create
click on the name and press upload a video of choice that is less than 60 seconds

