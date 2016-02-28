FROM microsoft/aspnet:1.0.0-rc1-update1
COPY project.json /app/
WORKDIR /app
RUN ["dnu", "restore"]
COPY . /app
EXPOSE 80
ENV SERVER.URLS http://*:80
ENTRYPOINT ["dnx", "-p", "project.json", "web"]
