# iFood Data Engineering Test

This test is not only a single test but a series of them in order to assess different skills that are valuable to our team.
Target audience: everyone looking for a spot at iFood's (Data Engineering) table.

At iFood, Data Engineers are encouraged to look up any tool that might help solve any challenge. Therefore, use whatever language, storage and tools you feel comfortable with. Also, briefly elaborate on your decisions.

So, without further ado, let's get started!

## Sandbox: ETL building

Have you ever heard of... data-driven ? Well, as it happens our Data Analysts and Data Scientists need data from Order, Customer and Restaurant services to create something unique that might impact how we run things around here...
Implement an ETL pipeline to process distinct files and store it in a structured way.

### Requirements

* Order data comes from our service architecture and are formatted in JSON files. They’re stored in this url: s3://ifood-data-architect-test-source/order.json.gz
* For this test, service teams offered us a dump from restaurant and customer databases as CSV files.
  * Restaurant: s3://ifood-data-architect-test-source/restaurant.csv.gz
  * Consumer: s3://ifood-data-architect-test-source/consumer.csv.gz
* There's also a kafka streaming order events
  * kafka #1: a49784be7f36511e9a6b60a341003dc2-1378330561.us-east-1.elb.amazonaws.com:9092
  * kafka #2: a4996369ef36511e9a6b60a341003dc2-1583999828.us-east-1.elb.amazonaws.com:9092
* Analysis are done in SQL. Thus, these data must be accessed in a SQL way.
* Data needs to be consistent, we can’t lose anything.
* This ETL needs to be scalable.

Feel free to use any solution to store these data.

### Deliverable

* You're a data engineer. Feel free to use any language and technology to reach your goal. Languages, frameworks, platforms are not a constraint, but your solution must be inside a docker image, script or notebook ready to be run. Running this container/script or notebook should start reading the specified files and store it in a structured format.

## Data governance & catalog

Privacy, data governance & data catalog are required skills in the Data Engineering team. We need to store all metadata so all datasets could be read on distinct tools.
How would you store all metadata to build a catalog and secure your data ? Your solution should take into account data access and private data protection.

### Deliverable

* Briefly elaborate on your solution, frameworks, algorithms. If possible, implement the solution on your previous task.

## Sandbox: API development

Everyone is addicted to Data, and your role here is to provide access not only for analysts and scientists, but also for services deployed in our infrastructure.

Requirements:

* There’s this fancy frontend page to restaurants that need to fetch some data. We need you to create an API that serves endpoints to return the following:
  * Count of orders per day for each city and state in our database
  * Top 10 restaurants per customer

* Use the data from the previous task to complete this one.
* The API should answer back a JSON with the desirable information
* Query needs to perform well, be maintainable and return accurate data.
* Business insists in doubling its size each month. This solution needs to be scalable!

You know the drill: Any language, any framework, any platform. Feel free to use anything to help you finishing this task.

### Deliverable

* Provide a docker image with a backend service. Running this container should start the necessary infrastructure to provide the endpoints


## References

* Databricks Community: https://community.cloud.databricks.com
* all-spark-notebook docker: https://hub.docker.com/r/jupyter/all-spark-notebook/
