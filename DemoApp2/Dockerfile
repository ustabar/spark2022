# FROM mcr.microsoft.com/dotnet/core/aspnet:3.1
FROM mcr.microsoft.com/dotnet/aspnet:5.0

ENV ASPNETCORE_URLS=http://+:80
ENV COMPlus_DbgEnableMiniDump="1"
ENV COMPlus_DbgMiniDumpName="/dumps/coredump.1.2"
ENV COMPlus_DbgMiniDumpType="4"

EXPOSE 80

COPY publish/ App/
WORKDIR /App
ENTRYPOINT ["dotnet", "SampleAspNetCore.dll"]
