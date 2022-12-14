## Download Docker Desktop app in your machine ##

## Running a Docker container ##

## Method 1 ##
## Build an image using the Docker File ##

```docker build --tag image_name .```

## Run an image ##

```docker run --name container_name -p 8090:8080 image_name```

## Method 2 ##
## Using Docker compose file ##

```docker-compose up```

## Once Docker is up, run the following CURL commands ##

## If you are using windows operating system try to run the below command before running the CURL commands ##

```Remove-item alias:curl```

## Run the curl command ##

This transfers ETH:

```curl -i -X POST -H "Content-Type: application/json" -d '{\"address\":\"Destination Account Address\", \"amount\":\"0.05\"}' http://localhost:8090/eth```

This transfers token:

```curl -i -X POST -H "Content-Type: application/json" -d '{\"address\": \"Destination Account Address\"}' http://localhost:8090/token```


## If you are using Mac operating system try to run the below command before running the CURL commands ##

This transfers ETH:

```curl --header "Content-Type: application/json" --request POST --data '{"address":"Destination Account Address", "amount":"Ether amount to be transfered"}' http://localhost:8090/eth```

This transfers token:

```curl --header "Content-Type: application/json" --request POST --data '{"address":"Destination Account Address"}' http://localhost:8090/token```




















