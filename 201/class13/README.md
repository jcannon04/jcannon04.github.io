# Local Storage

## Reading Q&A

* **Why would a developer use local storage for a web application?** Local storage enables you to cache information on the client computer than persists between pages loads. Do you could store information about how they set up their UI or data from apis that way you only have to request the data the first time they visit your page.

* **What information should not be stored in local storage?** Sensitive information such as password or personal info.

* **Local storage can store what type of data? How would you convert it to that type before storing?** You can only store stings in local storage. You can get around this by using json.stringify to parse your object and convert it to a string before saving and then using json.parse to turn it back into a object when retrieving the data.

## Things I want to learn more about