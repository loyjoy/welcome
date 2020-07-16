# How to set up a barcode scanner process

## 1. What this solution will do for you
In this article we explain how to set up a process where users can scan a product's barcode and get information on it.

## 2. What you need for this solution to work
You will need two things to implement this article:
- A product feed microservice and its URL & endpoints
- Data of your specific products in the feed (prefix, shop-directory, url)

## 3. Set up the process

You can also copy a finished process from a toolbox. Then you only have to change the specific parameters in webservice process bricks (see below).

### Add a snapshot process brick

This snapshot process brick will present the user with the option to scan a barcode.

Add one category and enter `*` as the recognized barcode. This will recognize all barcodes as belonging to this category. 

### Add a webservice process brick

In this webservice we will send the recognized barcode to our product feed microservice. It will then create a message with
information about the product for us. It will also create some process variables, that we will use later on.

You will need to enter the URL of the microservice as well as the parameters the microservice requires.

These parameters are usually:

| Name                | Purpose                                                |
|---------------------|--------------------------------------------------------|
| authentication      | Verifying that we are allowed to call the microservice |
| prefix              | Prefix of your specific products (e.g. country code)   |
| shop                | Name of the shop directory on your URL                 |
| url                 | URL of your website, links will point to this          |

### Add a questionnaire

This questionnaire will ask the user, which further information he/she wants from the product feed.

This information will be saved in a variable and sent back to the products feed (at a different end point). 

### Add second web service 

Here, we will send the selection of the user for additional data and the microservice will create a corresponding message.

Again, we will need to configure the URL and params (see above).

