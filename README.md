# flask_5_tailwind

# 1. Video Creation or Procurement:
I have decided to use this [video](https://www.youtube.com/shorts/-lpDi_if-Jc) and downloaded it on my desktop

# 2. Cloud CDN & Video Hosting 
Using Azure, I created a cloud CDN using this [guide](https://learn.microsoft.com/en-us/azure/cdn/cdn-create-a-storage-account-with-cdn).
1. sign in Azure with credentials
2. Search for `storage accounts`
3. click `create`
4. Select `subscription` and `resource group` leave everything else the same, create `Storage account name` and press `create`
5. under `overview`, click on `Security`, Make sure `Secure transfer required`, `Allow Blob anonymous access`, and `Allow storage account key access` are **enabled**
6. Under `data storage`, click `containers`
7. click `+ containers`, change anonymous access level to `container(anonymous read access for containers and blob)` and create a name
8. under `Security + networking` click `Front Door and CDN`
Under service type, click `Azure CDN`, `create new`, `profile name`, `endpoint name`
Under `Query string caching behavior` click `Ignore Query String`, press `create`
click on the name and press `upload a video of choice that is less than 60 seconds`


https://eugene-cdn.azureedge.net/eugene-flask-app/nba-s-top-plays-of-the-night-in-60-seconds-april-24-2023-1280-ytshorts.savetube.me.mp4 
