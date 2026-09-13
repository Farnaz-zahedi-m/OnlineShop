# =========================
# BUILD
# =========================
FROM mcr.microsoft.com/dotnet/sdk:9.0 AS build

WORKDIR /src

COPY OnlineShop.sln .

COPY Application/Application.csproj Application/
COPY Domain/Domain.csproj Domain/
COPY Infra.Data/Infra.Data.csproj Infra.Data/
COPY Infra.IOC/Infra.IOC.csproj Infra.IOC/
COPY OnlineShop.web/OnlineShop.web.csproj OnlineShop.web/

RUN dotnet restore OnlineShop.sln

COPY . .

RUN dotnet publish OnlineShop.web/OnlineShop.web.csproj \
    -c Release \
    -o /app/publish \
    --no-restore


FROM mcr.microsoft.com/dotnet/aspnet:9.0 AS final

WORKDIR /app

COPY --from=build /app/publish .

ENV ASPNETCORE_HTTP_PORTS=8080

EXPOSE 8080

ENTRYPOINT ["dotnet", "OnlineShop.web.dll"]