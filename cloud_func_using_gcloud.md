Steps to Create and Test Cloud Function using GCLOUD:

A. Add two Numbers:
 
1. Install cloud sdk.
2. Clone the sample repository to your local machine:
   git clone https://github.com/...
3. Change to the directory that contains the Cloud Functions sample code:
   cd ... (dir in which your code is)
4. Take a look at the sample code:
   Save this file with main.py name

	def sum(request):
		request_dict=request.get_json()
		if request.method=='POST':
			num1=request_dict['num1']
			num2=request_dict['num2']
			return str(num1+num2)
		elif request.method=="GET":
			return 'POST method required'

5. To deploy the function with an HTTP trigger, run the following command in the directory in which your code file is:
    gcloud functions deploy sum --runtime python37 --trigger-http
6. When the function finishes deploying, take note of the httpsTrigger's url property or find it using the following command:

	gcloud functions describe sum

7. It should look like:

	https:// ... .cloudfunctions.net/sum

8. Visit this URL in your browser. You should see a "POST method required" message.

Calling the Cloud Function through gcloud:

1. run the following commands:
  	
  	gcloud functions call sum --data "{\"num1\":10,\"num2\":20}"

 where sum is the function name and data field is body of POST method.

 Creating a cloud function that returns a name which will be the name of cloud storage bucket:

 main.py

from gcloud import storage

 def create_bucket(request):
    request_dict=request.get_json()
    if request.method=='POST':
        buc_name=request_dict['name']
        client=storage.client()
        client.create_bucket(buc_name)
        return "Success"
    elif request.method=="GET":
        return 'POST method required'

requirements.txt

this can be done by folling command:
>pip freeze >> requirements.txt  # for appending in requirements file
>pip freeze > requirements.txt   # for overwriting

create virtual env
activate it
install gcloud