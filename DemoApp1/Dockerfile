FROM mcr.microsoft.com/dotnet/sdk:6.0 AS builder

RUN git clone  --depth 1 https://github.com/pamir/lldb-netcore-use-cases.git /sources
RUN dotnet publish /sources/src/Runner/Runner.csproj -o /app -c Debug

FROM mcr.microsoft.com/dotnet/runtime:6.0

WORKDIR /app
COPY --from=builder /app .

ENTRYPOINT ["dotnet", "Runner.dll"]
