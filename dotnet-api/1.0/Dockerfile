FROM microsoft/dotnet:1.1.0-sdk-projectjson

RUN apt-get update

COPY . /app

WORKDIR /app

RUN ["dotnet", "restore"]

RUN ["dotnet", "build"]

EXPOSE 5000
ENV ASPNETCORE_URLS http://*:5000
 
ENTRYPOINT ["dotnet", "run"]