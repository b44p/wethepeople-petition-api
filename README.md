# wethepeople-petition-api
Super simple API to extract petition data from the [White House's We the People initiative](https://petitions.whitehouse.gov/responses)

I used [Import.io](www.Import.io) to generate an extractor template from the link  https://petitions.whitehouse.gov/responses?page={num}

***The API's endpoint is:***

https://api.import.io/store/connector/b7372339-5fb9-4896-ad81-525ab293d2b9/_query?input=webpage/url:https%3A%2F%2Fpetitions.whitehouse.gov%2Fresponses%3Fpage%3D1&&_apikey=IMPORT-IO-API-KEY

Sign up wtih Import.io and get an API-key. Once you plug your key into the URL, each page contains a JSON containing petition data.

Each page contains 20 petitions. Pages can be changed by changing the ```page%3D{num}``` of the URL.

so this is **PAGE 1** of petitions
    ![Page 1](http://i.imgur.com/HCnbKvx.png)
and this is **PAGE 2**
    ![Page 2](http://i.imgur.com/lXGAq6v.png)

Output fields
  * signed_label
  * goal_number
  * view_description
  * signatures_number
  * nodepetition_link/_text
  * nodepetition_link
  * signatures_number
  * view_label
  * goal_number
  * nodepetition_link
  * goal_label

###[Here is  an example CSV extract](https://github.com/b44p/wethepeople-petition-api/blob/master/petitions.whitehouse.gov%20API%2021st%20Apr%2011_46.csv)

### TODO
Ask Import.io whether csv extracts can be performed using the API 
https://twitter.com/vr00n/status/723175332648382464
