
[![Platforms](https://img.shields.io/badge/Simple-JSON-brightgreen)]()
[![Platforms](https://img.shields.io/badge/License-GNU%20-blue)]()



#  SimpleJSON 


## 📑 About

As JSON is mainly used between a browser and server, it is also a simple solutuion to managing content within mobile apps (Android & iOS).

This file can be referenced or used for examples.

What you will find.
- Quick json run down
- Using json to displayed content in a mobile app.


## 🏃🏽‍♂️ Quick Run down

Json code can be found in `Categories.json`.

One nice thing about json is easy to understand. Below is a code snippet from the full json file.

Best to build a Json schema in a way that can be easily expanded and updated without modify the way it is parsed.  The example JSON below contains a array (`categories`)  that allows the
felixable with the amount of menu objects. Also, by using optional values `null` allows for some felixability but will need to be handled when parsed. When it comes to best practice, including an integrity check is crucial. Therefore, I used [MD5 hash](https://en.wikipedia.org/wiki/MD5) on the file to check for unwanted or accidental changes. More info on integrity checking can be found  at (https://stackoverflow.com/questions/30610545/checking-json-file-integrity) . Parsing json is common between languages, however,  matching data structures and syntexs can be a little tricky. So here is a great online tool that matches json to different code structures [](https://quicktype.io/).

    categories :    List of menu objects
    
                    Menu Object :       id:Integer        - Id of the selected menu object
                                        name:String       - Name of menu object
                                        sub:Array         - Optional subcategorie list of strings 
                                        image_url:String  - Url of a image 


    categoriesToShow:Integer  - Used for default menu object, by id 
    catId:String              - Used for integrity checksum (MD5 hash of the file)


```
{
    "categories":[
          {
            "id": 0,
            "name": "Soups",
            "sub": null,
            "image_url": "https://www.cscassets.com/recipes/large_cknew/large_12216.jpg"
          },
          {
            "id": 1,
            "name": "Cooking Style",
            "sub": [
              "Instant Pot®",
              "Slow Cooker",
              "One Pot",
              "Casserole",
              "Stew",
              "Skillet",
              "Roasted",
              "Grilled",
              "BBQ",
              "Breaded"
            ],
            "image_url": "https://www.cscassets.com/recipes/large_cknew/large_12208.jpg"
          },
      ],
      "categoriesToShow": 1,
      "catId":"adee68c3e030d723664bbbcfa12908de"
  }
```
## 📱Manage Content

The file is used to manage content with my ClassicRecipes app on both iOS and Android.

Below are images showing how I used the json to determine the layout of the user interface and the content it displays. Check out my design behind the user interface in this [repo](https://github.com/MitchTODO/Recipes).

![alt text](readmeAssets/example1.png "Example 1")
![alt text](readmeAssets/example2.png "Example 2")
![alt text](readmeAssets/example3.png "Exmaple 3")


Check out the ClassicRecipes app for yourself.

iOS
https://apps.apple.com/us/app/classic-recipes/id1544630699

Scan with camera 

![alt text](readmeAssets/apple.png "Apple QR")

Android 
https://play.google.com/store/apps/details?id=com.mitchelltucker.classicRecipes

![alt text](readmeAssets/android.png "Android QR")

## ❗️Issues  

If you feel that I left some thing out or want more code examples open a new issue for this repo. 







