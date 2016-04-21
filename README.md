# wethepeople-petition-api
An API to extract petition data from the [White House's We the People initiative](https://petitions.whitehouse.gov/responses)

I used [Import.io](www.Import.io) to generate an extractor template from the link  https://petitions.whitehouse.gov/responses?page={num}

***The API's endpoint is:***

https://api.import.io/store/connector/b7372339-5fb9-4896-ad81-525ab293d2b9/_query?input=webpage/url:https%3A%2F%2Fpetitions.whitehouse.gov%2Fresponses%3Fpage%3D1&&_apikey=a439601203144a9bbb1dd390bcb947080d15cb3d23585f35382bfc4d4ca3fe9c91ba5c6c7d70982837ff556a9ed9ece847b60bddc87e1c4701567f70b8a111c05a65f2522e2e28609fdc2616a3ea3ae6

The Endpoint's pagination can be changed by changing the ```page%3D{num}``` from the above API

so this is **PAGE 1** of petitions
    https://api.import.io/store/connector/b7372339-5fb9-4896-ad81-525ab293d2b9/_query?input=webpage/url:https%3A%2F%2Fpetitions.whitehouse.gov%2Fresponses%3Fpage%3D1&&_apikey=a439601203144a9bbb1dd390bcb947080d15cb3d23585f35382bfc4d4ca3fe9c91ba5c6c7d70982837ff556a9ed9ece847b60bddc87e1c4701567f70b8a111c05a65f2522e2e28609fdc2616a3ea3ae6
  
and this is **PAGE 2**
    https://api.import.io/store/connector/b7372339-5fb9-4896-ad81-525ab293d2b9/_query?input=webpage/url:https%3A%2F%2Fpetitions.whitehouse.gov%2Fresponses%3Fpage%3D2&&_apikey=a439601203144a9bbb1dd390bcb947080d15cb3d23585f35382bfc4d4ca3fe9c91ba5c6c7d70982837ff556a9ed9ece847b60bddc87e1c4701567f70b8a111c05a65f2522e2e28609fdc2616a3ea3ae6

This will generate a JSON containing the following fields for each petition. 

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


