# final_project-ftgo-h8

#email
timothypartaliano@gmail.com
bimaputrasejati9999@gmail.com

#build image docker
docker build (folder) -t (nama image)

-product service
docker build product-service -t fl-product-service:v1

docker tag fl-product-service:v1 gcr.io/copper-diorama-388207/fl-product-service:v1

docker push gcr.io/copper-diorama-388207/fl-product-service:v1

-notification service

docker build notification-service -t fl-mainapi-service

docker tag fl-mainapi gcr.io/copper-diorama-388207/fl-mainapi

-main api
docker build api -t fl-mainapi-service
docker tag fl-notification-service gcr.io/copper-diorama-388207/fl-notification-service

container registry gcp auth :
gcloud auth login

docker run without compose
docker run -it --rm --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:3.12-management
