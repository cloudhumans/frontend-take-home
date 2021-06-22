# Cloud Humans - Frontend Take Home Assignment

People are the fuel that moves Cloud Humans. In order to speed up the company we need to be great at pairing people (we call them Pros) to problems as fast as possible. 

Cloud Humans determines which project a new Pro will tackle based on the answers they provide in the Pro Portal (a frontend application). The frontend send this Pro's **application** to an API that runs an algorithm upon the data and returns the project in which the Pro will be allocated. 

For this assignment, you will create a simple version of that application by coding a page with the Pro application form - you don’t have to worry about the API.

## The layout
You must follow [this layout](https://www.figma.com/file/HhLmn5czZCYmMFUOePcTZB/Cloud-Humans-Frontend-Take-Home?node-id=0%3A1) but you're free to modify, add some animations and cool things (keep in mind you will be evaluated for every change).

You don't need to worry about mobile resolution, the minimun width required is `1280px` and the max width is `1920px`, the application must work fine to this width range.

## The output
When the user submit the form, you need to generate a JSON like this one:

```JSON
{
  "age": 35,
  "education_level": "high_school",
  "past_experiences": {
    "sales": false,
    "support": true
  },
  "internet_test": {
    "download_speed": 50.4,
    "upload_speed": 40.2
  },
  "writing_score": 0.6,
  "referral_code": "token1234"
}
```

You don't need to call an API, just print this JSON in the console on form submit.

### Pro Application
All attributes are required except for the `referral_code`.

- Age: an integer equal or greater than 0.
- Education Level: `"no_education", "high_school"` or `"bachelors_degree_or_high"`)
- Past experiences: JSON object with bool attributes `sales` and `support`
- Internet Test: JSON object with the result of an internet test (the attributes are positive floats, where 50.4 == 50.4 megabytes)
  - To this test, consider that when the user click on the button, you can generate the values (`download_speed` and `upload_speed`) randomly
- Writing Score: float between 0 and 1
- Referral code: a string with a referral token provided by another Pro

## Criteria
You may use any language and framework provided that you build a solid system with an emphasis on code quality, simplicity, readability, maintainability, and reliability, particularly regarding architecture and testing.

Be aware that we will mainly take into consideration the following evaluation criteria:
* Good form inputs (with masks, error handlers, etc);
* How clean and organized your code is;
* How good your automated tests are (qualitative over quantitative);
* Publish your final static build (we recommend https://surge.sh/). 

Other important notes:
* Add to the README file: (1) instructions to run the code; (2) what were the main technical decisions you made; (3) relevant comments about your project 
* You must use English in your code and also in your docs

This assignment should be doable in less than one day. We expect you to learn fast, communicate with us if you need, and make decisions regarding its implementation & scope to achieve the expected results on time.

