
# Serverless Compute and Cloud Database

#### building an serverless compute with Azure functions and connect it to Cosmos Db

## 1. Description

Azure function is a serverless framework that helps you to develop and deploy serverless applications. 

I have created all four CRUD functionalities about heroes, and connected data with Cosmos Db using MongoClient. MongoClient is the interface between our program and MongoDB server. I set the `CosmosDBConnectionString` to pass the result from calling functions to database. 

When start debugging, there are four CRUD https.

<img src="Img/http.png" width="700px" />

## 2. Postman 

Below are images for API tests in Postman. 

#### Create function test

<img src="Img/create.png" width="700px" />

#### Get function test

<img src="Img/get.png" width="700px" />

## 3. Development

### Tech stack:

+ [NPM](https://www.npmjs.com/) for package management
+ [Azure functions](https://azure.microsoft.com/en-us/services/functions/?&ef_id=CjwKCAjwkun1BRAIEiwA2mJRWTnECYvz_9H5LYcwGeD4xYNMsMLUJMVdNABo2YQzlaZIEWyizWOu9RoCXqIQAvD_BwE:G:s&OCID=AID2000128_SEM_CjwKCAjwkun1BRAIEiwA2mJRWTnECYvz_9H5LYcwGeD4xYNMsMLUJMVdNABo2YQzlaZIEWyizWOu9RoCXqIQAvD_BwE:G:s&gclid=CjwKCAjwkun1BRAIEiwA2mJRWTnECYvz_9H5LYcwGeD4xYNMsMLUJMVdNABo2YQzlaZIEWyizWOu9RoCXqIQAvD_BwE) for serverless compute
+ [Cosmos Db](https://docs.microsoft.com/en-us/azure/cosmos-db/introduction) for database

### Extensions and Packages used
* `Azure Cosmos DB` `Azure Functions` in Visual Studio
* `mongodb` package

### To run dev mode locally:

```bash
  $ git clone 
  $ cd the repository
  $ npm install
```

After successfull package installation, run the `Attach to Node` debug.
Now, it will automatically give you four http urls for each functions. You can test it with Postman or Swagger UI.

## 3. Solved Bugs

1. `File \AppData\Roaming\npm\ng.ps1 cannot be loaded. The file npm\ng.ps1 is not digitally signed Angular Error when running commands`

I ran command from Visual Studio Code Terminal and got above issue. I solved this by running following command from the same terminal.<br/>

`Set-ExecutionPolicy RemoteSigned -Scope CurrentUser`<br/>

2. ReadOnly setting <br/>
`Your app is currently in read only mode because you are running from a package file. To make any changes update the content in your zip file and WEBSITE_RUN_FROM_PACKAGE app setting.`
I changed `WEBSITE_RUN_FROM_PACKGE`'s setting value from 1 to 0. Now editing is available on App Functions.








