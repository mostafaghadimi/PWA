# PWA Presentation
## Mobile Programming Course
> 26 May 2019


**Instructor:** Mostafa Ghadimi


## Apple IOS meta tags:

[Useful link](https://medium.com/appscope/designing-native-like-progressive-web-apps-for-ios-1b3cdda1d0e8)

```HTML
<meta name="apple-mobile-web-app-capable" content="yes"> <!-- Make it standalone -->
<meta name="apple-mobile-web-app-status-bar-style" content="some-color"> <!-- Change the status bar -->
<meta name="aoole-mobile-web-app-title" content="desired-title">
<link rel="apple-touch-startup-image" href="launch.png"> <!-- Add a custom splash screen -->
<link rel="apple-touch-icon" href="single-page-icon.png">
```

## Important Manifest.json keys:

- `background_color`: The background_color member defines a placeholeder background color for the application page to display before its stylesheet is loaded. `"background_color": "red"`

- `categories`: The categories member is an array of strings defining the names of categories that the application supposedly belongs to. `"categories": ["books", "education", "medical"]`

- `description`: The description member is a string in which developers can explain what the application does. description is directionality-capable, which means it can be displayed left to right or right to left based on the values of the dir and lang manifest members. `"description": "Awesome application that will help you acheive your dreams."`

- **dir**: The base direction in which to display direction-capable members of the manifest. Together with the lang member, it helps to correctly display right-to-left languages. `"dir": "rtl"`

- **display**: The display member is a string that determines the developers’ preferred display mode for the website. display mode options are `fullscreen`, `standalone`, `minimal-ui` and `browser`. 

- **icons**: The icons member specifies an array of objects representing image files that can serve as application icons for different contexts. `"icons": [ { "src": "icon.webp", "sizes": "48x48", "type": "image/webp" } ]`

- **lang**: The lang member is a string containing a single language tag. `"lang": "fa-IR"`

- **name**: The name member is a string that represents the name of the web application as it is usually displayed to the user (e.g., amongst a list of other applications, or as a label for an icon).

- **orientation**: The orientation member defines the default orientation for all the website's top-level browsing contexts. Orientation options are `any`, `natural`, `landscape`, `landscape-primary`, `landscape-secondary`, `portrait`, `portrait-primary`, `portrait-secondary`.

- **scope**: The scope member is a string that defines the navigation scope of this web application's application context. It restricts what web pages can be viewed while the manifest is applied. If the user navigates outside the scope, it reverts to a normal web page inside a browser tab or window. `"scope": "."`

- **screenshots**: The screenshots member defines an array of screenshots intended to showcase the application. These images are intended to be used by progressive web app stores.

```json
"screenshots" : [
  {
    "src": "screenshot1.webp",
    "sizes": "1280x720",
    "type": "image/webp"
  },
  {
    "src": "screenshot2.webp",
    "sizes": "1280x720",
    "type": "image/webp"
  }
]
```

- **serviceworker**: The serviceworker member describes a service worker that the developer intends to install to control the PWA.

```json 
"serviceworker": {
  "src": "./serviceworker.js",
  "scope": "/app",
  "type": "",
  "update_via_cache": "none"
}
```

- **shortname**: The short_name member is a string that represents the name of the web application displayed to the user if there is not enough space to display name (e.g., as a label for an icon on the phone home screen). short_name is directionality-capable, which means it can be displayed left-to-right or right-to-left based on the value of the dir and lang manifest members. `"short_name": "Awesome app"` 

- **start_url**: The start_url member is a string that represents the start URL of the web application — the prefered URL that should be loaded when the user launches the web application (e.g., when the user taps on the web application's icon from a device's application menu or homescreen). `"start_url": "/"`

- **theme_color**: The theme_color member is a string that defines the default theme color for the application. This sometimes affects how the OS displays the site (e.g., on Android's task switcher, the theme color surrounds the site). `"theme_color": "red"`
