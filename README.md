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
7. Click `+ containers`, change anonymous access level to `container(anonymous read access for containers and blob)` and create a name
8. Under `Security + networking` click `Front Door and CDN`
9. Under service type, click `Azure CDN`, `create new`, `profile name`, `endpoint name`
10. Under `Query string caching behavior` click `Ignore Query String`, press `create`
11. Click on the name and press `upload` a video of choice that is less than 60 seconds
12. Click on the video and copy the URL into a new tab to show that the video works.
13. Using the endpoint username URL, copy everything after the .net from the video link. This [link](https://eugene-cdn.azureedge.net/eugene-flask-app/nba-s-top-plays-of-the-night-in-60-seconds-april-24-2023-1280-ytshorts.savetube.me.mp4 
) would be the outcome  

# 3. Flask App with Tailwind CSS:
Using templates from previous assignments, I created an `about.html`, `home.html`, and `video.html`. These can be found under [templates](https://github.com/EugeneHsiung/flask_5_tailwind/tree/main/templates). These templates contained Tailwind CSS. An `app.py` was also created for the flask app. 

# 4. Cloud Deployment:
1. In the Google Shell terminal, you will need to install AZURE CLI. Type in `curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash`
2. Type in `az login --use-device-code`, click on the link and paste the code shown in the terminal to connect Google Shell with Azure
3. Type in `az account list --output table`, and make sure the correct subscription is selected. If not type in `az account set --subscription <paste the desired SubscriptionId here>`
4. Type in az `webapp up --name <replace with what you would like to name the webapp> --runtime PYTHON:3.9 --sku B1` and wait for deployment to finish
5. Go to `App Service` in Azure and click on the link in `Default domain`
6. Screenshots of the deployment being successful can be seen in [flaskapp](https://github.com/EugeneHsiung/flask_5_tailwind/tree/main/flaskapp). 

