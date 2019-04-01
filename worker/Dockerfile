#FROM microsoft/dotnet:2.0.0-sdk
FROM microsoft/dotnet:2.2-sdk

WORKDIR /code

ADD src/Worker /code/src/Worker

RUN dotnet restore -v minimal src/Worker \
    && dotnet publish -c Release -o "./" "src/Worker/" 

CMD dotnet src/Worker/Worker.dll
