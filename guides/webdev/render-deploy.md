# Deploy on Render.com

First make a file in the root directory of your project before uploading to github called `.node-version`, inside that file type your node version, this allows render to know what node version to run. 

1. Upload your project to github. 
2. Make a render account, connect it to your github account
3. On your dashboard for this type of project hit New+ and select Web Service
![image](https://github.com/Triv2/writing/assets/126743500/d8dbcf6b-c725-42b6-9cbc-bf34cd403c07)
![image](https://github.com/Triv2/writing/assets/126743500/a8100970-4df1-487e-9953-adb5665d9c27)

4. Select your github project to connect it to. 
![image](https://github.com/Triv2/writing/assets/126743500/67d8d803-915b-4d62-b2f7-8a2999d8730d)

5. Set the unique name you want for the webaddress.
![image](https://github.com/Triv2/writing/assets/126743500/80c49232-b114-4e0d-a242-85f9e1d50ebd)

6. Set the build/start commands like the attached image.
![image](https://github.com/Triv2/writing/assets/126743500/605815a0-2cf6-4171-9cf5-b14797bd57c9)

7. Go to environment section. Create secret file call it ".env", copy paste your .env in there.
![image](https://github.com/Triv2/writing/assets/126743500/028c9da3-18a8-43ba-a43b-72f222f5515a)

8. Hit build and see if you have any errors, if not it might take like 10-15 min to build. But after that it will be active and you can go to the webaddress to test it.
