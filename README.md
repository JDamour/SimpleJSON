<h1 align="center">SimpleJSON 👋</h1>
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-1.0.0-blue.svg?cacheSeconds=2592000" />
  <a href="https://twitter.com/{AUTHOR.TWITTER}">
    <img alt="Twitter: coryleach" src="https://img.shields.io/twitter/follow/coryleach.svg?style=social" target="_blank" />
  </a>
</p>

Package for creating packages!

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

# SimpleJSON
A C# json reader/writer which is Unity3D compatible based on http://wiki.unity3d.com/index.php/SimpleJSON

The official Github repo for this script can be found at https://github.com/Bunny83/SimpleJSON/blob/master/SimpleJSON.cs

This repository includes improvements that are mostly a bunch of unit tests (compatible with Unity test runner) which verify that things work like it should, and some performance improvements. The unit tests helped discover some stuff where this implemention did not follow the json standard and they were fixed.

<!-- DOC-END -->

## Author

👤 **Cory Leach**

* Twitter: [@coryleach](https://twitter.com/coryleach)
* Github: [@coryleach](https://github.com/coryleach)


## Show your support

Give a ⭐️ if this project helped you!

***
_This README was generated with ❤️ by [Gameframe.Packages](https://github.com/coryleach/unitypackages)_
