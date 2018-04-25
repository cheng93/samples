FROM microsoft/dotnet:2.1.300-preview2-sdk-alpine

WORKDIR /app

ADD . /app

EXPOSE 8080

ENV ASPNETCORE_URLS http://*:8080
ENV ASPNETCORE_ENVIRONMENT Development

RUN dotnet build FlightFinder.Server/FlightFinder.Server.csproj -c Release

CMD [ "dotnet", "run", "--project",  "FlightFinder.Server/FlightFinder.Server.csproj", "-c", "Release", "--no-build" ]
