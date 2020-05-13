Cloud Functions can be associated with a specific trigger. The trigger type determines how and when your function executes. Cloud Functions supports the following native trigger mechanisms:

HTTP Triggers
Cloud Pub/Sub Triggers
Cloud Storage Triggers
Direct Triggers
Cloud Firestore
Analytics for Firebase
Firebase Realtime Database
Firebase Authentication


Steps to Create Cloud Function:

A. Printing Message through Cloud Function.

1. Go to console.cloud.google.com
2. In the search bar type Cloud Function or in the left menu COMPUTE>Cloud Functions.
3. Click on Create Project and enter name of your project and click Create.
4. Now create an GCP account by sign up for free trial (this free trial is valid either for 12 months or until you exhaust $300)
5. After sign up you click on Create Function.
6. Enter Name of function , Trigger (HTTP) , Change Runtime according to your requirement (Nodejs,Python).
7. Click Create and HTTP has been Created.
8. Click on the function name displayed on next appeared screen.
9. click the Edit button on the top of page.
10. change the default message 'helloworld' to the required message ('Hello ! I am Aakansha').
11. Then Click Save button.
12. Now you can test your Programm by clicking to Testing Field .
13. Enter {"message":"Hey"}
14. Click Test the function and Output "Hey" (without quotes) will shown on to the output screen , so success in testing.
15. Move to Trigger and hit the URL , you will have a screen displaying "Hello ! I am Aakansha" (without quotes).

Calling Cloud functions Using Postman :

1. Copy the url of displayed window and paste it in postman url portion.
2. Select the method
3. Send the Request
4. You will get the response "Hello ! I am Aakansha" (without quotes).



B. Sum of two numbers:

Creating Cloud Function:

1. Go to console.cloud.google.com
2. In the search bar type Cloud Function or in the left menu COMPUTE>Cloud Functions.
3. Click on Create Project and enter name of your project and click Create.
4. Now create an GCP account by sign up for free trial (this free trial is valid either for 12 months or until you exhaust $300)
5. After sign up you click on Create Function.
6. Enter Name of function , Trigger (HTTP) , Change Runtime according to your requirement (Nodejs,Python) and click the checkbox of allowing unauthorized (Your API can access publicly).
7. Click Create and HTTP has been Created.
8. Click on the function name displayed on next appeared screen.
9. Click the Edit button on the top of page.
10. Change the default code to :
 
	def sum(request):
		request_dict=request.get_json()
		if request.method=='POST':
			num1=request_dict['num1']
			num2=request_dict['num2']
			return str(num1+num2)
		elif request.method=="GET":
			return 'POST method required'

11. Deploy this function.
12. Move to Trigger and hit the URL , you will have a screen displaying "POST method required" (without quotes).
13. Copy the URL.


Calling the function through Postman:

1. Paste the copied URL in the URL bar.
2. Select POST as the method.
3. Select the JSON representation from the dropdown.
4. Give the input data through Body>raw
	
	{
	"num1":10,
	"num2":20
	}

5. Hit the send button , you will get the response as 30 on the request portion.







Cloud Functions can be associated with a specific trigger. The trigger type determines how and when your function executes. Cloud Functions supports the following native trigger mechanisms:

HTTP Triggers
Cloud Pub/Sub Triggers
Cloud Storage Triggers
Direct Triggers
Cloud Firestore
Analytics for Firebase
Firebase Realtime Database
Firebase Authentication