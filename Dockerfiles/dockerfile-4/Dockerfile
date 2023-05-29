FROM ubuntu:latest AS build


WORKDIR /app/atom/IAP/R6

COPY /app/atom/scripts/requirements.txt  .

COPY . .

RUN apt-get update && apt install python3 && \
    pip install requirements.txt

FROM openjdk:8
ENV PORT=8012

WORKDIR /app/atom/IAP/R6
COPY --from=build /app/atom/IAP/R6/compute .

EXPOSE $PORT 

ENTRYPOINT [ "java", "-jar", "/app/atom/IAP/R6/compute.jar" ]