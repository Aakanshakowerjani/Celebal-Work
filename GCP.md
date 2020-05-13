compute engine:
-it is a IAAS component of GCP which is built on the google infrastructur that runs google search engine,gmail,you tube and other services.
-it enables the users to launch VMs on demand.
-GCP users must authenticate based on OAuth 2.0 before launching the VMs.
-it can be accesed via developer console,RESTful APIor command-line interface(CLI).

app engine:
-it is a PAAS(platform as a service)
-it is a cloud computing platform for developing and hosting web applications in google managed data centers.
-it primarly supports go,php,python,ruby,node,.net,java apps although it can also support oter lang via custom runtimes.

kubernetes engine:
-it is an open source,container,orchestration system for automating application deployment,scaling,management.
-it is developed by google and now maintained by clod native , computing foundations.
-it is a platform for automating deployement,scaling and operations of application containers accross cluster of host.
-it works with a range of cotainer toos including docker(it is a paas products that uses os-level virtualization to deliver software in packages called containers . containers are isolated from one another and bundled their own software , libraries,and configy=uration files they can communicate with each other through well defined channels).

cloud functions:
-it is serverless
-automatic scaling
-no server management
-only pay for what you use 
-event driven-they executed when cloud event occur
--HTTP functions
--Background functions
----messaging
----firebase
----storage
----logs


Note:
** Docker:allows you to have a well sealed containers , these containers are secure , portable , also allow have social containers .





uploading files from local to GCP bucket using python scripts:

try
	import io
	from io import BytesIO
	import pandas as pd
	from google.cloud import storage
except Exception as e:
	print("Some Modules are missing {}".formulate(e))

storage_client=storage.Client.from_service_account_json("file name.json")

#crete a bucket object

bucket=storage_client.get_bucket("bucket name")

filename="%s/%s" %('',"image name")
blob=bucket.blob(filename)

with open('myimage.png','rb') as f:
	blob.upload_from_file(f)
print("upload complete")


cloud sdk:
gsutil cp -r path of image/file/folder gs://bucket_name

list of bucket:
gsutil ls gs://bucket_name

create a bucket:
gsutil mb -c regional -l us-central1 gs://new_bucket_name
					  -l asia-south1

giving public access to bucket:
gsutil ac1 ch -u AllUsers:R gs://new_bucket_name