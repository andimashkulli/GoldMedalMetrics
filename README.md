# Gold Medal Metrics Challenge Project

### Overview
In this project, you will use Spring Data JPA to power an Olympics analytics web app.

## How to Start
First clone this project and in the terminal type:
```shell
./mvnw spring-boot:run
```
Then, go to google and type localhost:3001 and you will see a frontend of Gold Medal Metrics that will show you medals based of the country,etc.

The ResftulAPIs are created based on the Java Spring JPA structure including the Controller, Repositories and Models.


### Testing
You can use cURL to manually test your API endpoints.

Here are some example cURL requests and responses.

#### Get countries, sorted by name in ascending order 

```shell
curl --request GET "http://localhost:3001/countries?sort_by=name&ascending=y"                                   

{"countries":[{"name":"Afghanistan","code":"AFG","gdp":594.32,"population":32526562,"medals":0},...]}
```

#### Get the details for the United States Olympic team

```shell
curl --request GET "http://localhost:3001/countries/united%20states"                                            

{"name":"United States","gdp":"56115.72","population":"321418820","numberMedals":"2477","numberSummerWins":"2302","percentageTotalSummerWins":"21.957268","yearFirstSummerWin":"1896","numberWinterWins":"175","percentageTotalWinterWins":"9.1098385","yearFirstWinterWin":"1924","numberEventsWonByFemaleAthletes":"747","numberEventsWonByMaleAthletes":"1730"}

```

#### Get the list of Gold medal winners for the United States Olympic team, sorted by the athlete's name in descending order

```shell
curl --request GET "http://localhost:3001/countries/united%20states/medals?sort_by=name&ascending=n"            

{"medals":[{"year":1968,"city":"Mexico","season":"Summer","name":"ZORN, Zachary","country":"United States","gender":"Men","sport":"Aquatics","discipline":"Swimming","event":"4X100M Freestyle Relay"},...]}
```

