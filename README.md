<h1 align="center">SimpleJSON 👋</h1>
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-1.0.0-blue.svg?cacheSeconds=2592000" />
  <a href="https://twitter.com/{AUTHOR.TWITTER}">
    <img alt="Twitter: coryleach" src="https://img.shields.io/twitter/follow/coryleach.svg?style=social" target="_blank" />
  </a>
</p>

A C# json reader/writer which is Unity3D compatible based on http://wiki.unity3d.com/index.php/SimpleJSON<\br>
The official Github repo for this script can be found at https://github.com/Bunny83/SimpleJSON/blob/master/SimpleJSON.cs<\br>
Original improvements from https://github.com/HenrikPoulsen/SimpleJSON<\br>
This repository is a fork that has been updated for direct import with the Unity PackageManager.

## Quick Package Install

#### Using UnityPackageManager (for Unity 2019.3 or later)
Open the package manager window (menu: Window > Package Manager)<br/>
Select "Add package from git URL...", fill in the pop-up with the following link:<br/>
https://github.com/coryleach/SimpleJSON.git#1.0.0<br/>

#### Using UnityPackageManager (for Unity 2019.1 or later)

Find the manifest.json file in the Packages folder of your project and edit it to look like this:
```js
{
  "dependencies": {
    "com.gameframe.simplejson": "https://github.com/coryleach/SimpleJSON.git#1.0.0",
    ...
  },
}
```

<!-- DOC-START -->
<!-- 
Changes between 'DOC START' and 'DOC END' will not be modified by readme update scripts
-->

## Usage

```C#
//From http://wiki.unity3d.com/index.php/SimpleJSON

var N = JSON.Parse(the_JSON_string);
var versionString = N["version"].Value;        // versionString will be a string containing "1.0"
var versionNumber = N["version"].AsFloat;      // versionNumber will be a float containing 1.0
var name = N["data"]["sampleArray"][2]["name"];// name will be a string containing "sub object"
 
//C#
string val = N["data"]["sampleArray"][0];      // val contains "string value"
 
//UnityScript
var val : String = N["data"]["sampleArray"][0];// val contains "string value"
 
var i = N["data"]["sampleArray"][1].AsInt;     // i will be an integer containing 5
N["data"]["sampleArray"][1].AsInt = i+6;       // the second value in sampleArray will contain "11"
 
N["additional"]["second"]["name"] = "FooBar";  // this will create a new object named "additional" in this object create another
                                               //object "second" in this object add a string variable "name"
 
var mCount = N["countries"]["germany"]["moronCount"].AsInt; // this will return 0 and create all the required objects and
                                                            // initialize "moronCount" with 0.
 
if (N["wrong"] != null)                        // this won't execute the if-statement since "wrong" doesn't exist
{}
if (N["wrong"].AsInt == 0)                     // this will execute the if-statement and in addition add the "wrong" value.
{}
 
N["data"]["sampleArray"][-1] = "Test";         // this will add another string to the end of the array
N["data"]["sampleArray"][-1]["name"] = "FooBar"; // this will add another object to the end of the array which contains a string named "name"
 
N["data"] = "erased";                          // this will replace the object stored in data with the string "erased"
```

<!-- DOC-END -->

## Author

👤 **Cory Leach**

* Twitter: [@coryleach](https://twitter.com/coryleach)
* Github: [@coryleach](https://github.com/coryleach)


## Show your support

Give a ⭐️ if this project helped you!

***
_This README was generated with ❤️ by [Gameframe.Packages](https://github.com/coryleach/unitypackages)_
