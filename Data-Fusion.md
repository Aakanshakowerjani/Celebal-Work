Key Challenges:

1. Do it yourself: Manage integrations are time consuming and error prone.
2. Point - to - Point: Slow , complex , high overhead and maintaince cost.
3. Skills Gap: Slower adoption , limited resource availability,delayed time to market.
4. Hybrid: Build it every time,high total cost of ownership,special expertise.

Who can use this / where it can be used?

Developer , Data Scientist , and Buiseness Analyst
1. Need to cleanse , match,de-dupe,blend,transform,partition,transfer,standardize,automate, and monitor.
2. Use Cloud Fusion to visually build integration pipeline , test,debug,and deploy.
3. Run it at scale on GCP,operationalize(monitor,report) pipelines,inspect rich integration metadata.
4. It provide graphical Interface.

Data fusion Use Cases:

1. Data Warehouse
2. Data Migration
3. Data Consolidation
4. Master Data Management
5. Data Consistency


What is Cloud Data Fusion?

It is a fully managed , cloud native,enterprise data Integration service for quickly building and managing data pipelines.
It has Graphical interface (drag and drop element) and broad open source library for collectors and and transformations.
In this we have to just concern on action not on code.
It is done on open source that is CDAC which help in data portablity.
The cloud data fusion web UI allows you to build scalabel data integration solution to clean , prepare , blend , transfer , and transform data , without having to manage the infrastructure.
It is powered by the open source project CDAP .

Interfaces:
To use the cloud data fusion you can use the visual web UI or command line tools.

Using code-free web UI:
When using cloud data fusion , you can use both the cloud console and separate cloud data fusion web UI.
1. In cloud console,you create cloud project , create and delete cloud data fusion instances and view cloud data fusion instances details.
2. In the cloud data fusion UI,you can use the various pages, such as Pipeline studio or wrangler,to visually design data pipelines and use cloud data fusion functionality.

Process of starting data fusion using console:
1. Create a cloud data fusion instance in console.
2. This will create a instance of cloud data fusion click on the View Instance Page , this opens the Data Fusion UI in a new browser tab.
3. Visually Design your pipelines and meta data.
4. Instance can be of two types Basic and Enterprise.

CDF build on open source technology called CDAP.
CDAP helps in forming Analytic program and data pipeline which help in performing data integration without writing code.

Any Database that uses JDBC can be connected easily here.
It provide Graphical Interface.

Data Pipeline:
1. It is used for data transportation btw source and destination where destination called sink.
2. source can be social media site/travel website/e-commerce site.
3. sink can be data warehouse , data lake or application like web scrapping tool.
4. common processing steps in data pipelines include data transformation,augmentation,enrichment,filtering,grouping,aggregting and running of ml algo against the data.
5. key attribute of big data-3V(velocity,volume,variety)
6. pipelines are represented by a series of nodes arranged in directed ascyclic graph (DAG) , fforming a one way flow. Nodes represent the various action you can take with your pipelines, such as reading from source , performing data transformation and writing output to sinks. 
7. Depending on the nature of usage of the data, the data pipelines are broadly classified into  a)Realtime , b) Batch data and c) Cloud native data.
a) Realtime: in which sub-second decision making is required and ths type shows the velocity attribute off big data.
b) Batch data: where large volume of data is to be processed at regular intervals.
c) Cloud Native: Work with cloud based data like AWS data pipeline is a web service automates and transforms data.

Plugins:
1. It is a customizable module that can be used to extend the capabilities of cloud data fusion.
2. These can be:
a)sources:- These are connectors to the database , files, or real time stream from which you can retrieve data.
This enable you to ingest data,using simple UI , so there is no worry of codding for connections.
b) Transforms:- This allow you to manipulate data after the data is ingested. Example:-clone a record , format JSON/csv or other.
c) Analytic: this used to perform aggregation such as grouping , and joining data from different sources as well as running analytic and ml operations.
d) Actions:- this defines custom action that are scheduled to take place during a workflow but don't directly manipulate data in the workflow.example:-using DATABASE CUSTOM ACTION , you can run an arbitary database command at the end of your pipeline, alternatively you can trigger an action to move files within cloud storage.
e) Sinks:- Data must be written to sink. Sinks like cloud storage, BigQuery,Spanner,relational Database, file system,mainframes.
f) Error collector:- when nodes encounter null values,logical errors, or other sources of errors,you can use erroe collector plugin to catch error.
g) Alert Publishers:-This allow to publish notifications when uncommon events occur.
h) Conditionals:-This is the condition plugin where there are two path whether true or false.
You can make your own plugin if required.

Data Sources:

1. Big data
2. Cloud data store
3. Cloud Storage
4. Cloud Spanner
5. Microsoft Excel
6. FTP