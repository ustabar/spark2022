FROM mcr.microsoft.com/dotnet/sdk:6.0 AS tools

RUN dotnet tool install --tool-path /tools dotnet-trace
RUN dotnet tool install --tool-path /tools dotnet-counters
RUN dotnet tool install --tool-path /tools dotnet-dump
RUN dotnet tool install --tool-path /tools dotnet-gcdump

FROM mcr.microsoft.com/dotnet/runtime:6.0

COPY --from=tools /tools /tools

ENV PATH="/tools:${PATH}"

WORKDIR /tools

