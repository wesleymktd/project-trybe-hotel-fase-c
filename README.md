## 🧐 Sobre

<p align="left"> 
O projeto Trybe Hotel se trata da implementação de uma Api de um site de reserva de uma rede de Hoteis, onde nessa terceira fase foram implementados os seguintes processos:

### Refatoração de processos para que as Cidades possuam um dado do Estado.

### Rota para verificar o funcionamento de uma API externa
  - Este endpoint será responsável por conferir o status da api externa responsável pela geolocalização.
  - O endpoint deve ser acessível através da URL `/geo/status` e deve ser do tipo `GET`.
    - A API externa retorna como response, em caso de sucesso, um status code `200` e um objeto `JSON` no seguinte formato:

```json
{
    "status": 0,
    "message": "OK",
    "data_updated": "2020-05-04T14:47:00+00:00",
    "software_version": "3.6.0-0",
    "database_version": "3.6.0-0"
}
```
### Rota para buscar hotéis próximos de um endereço
  - Este endpoint será responsável por conferir o status da api externa responsável pela geolocalização.
  - O endpoint deve ser acessível através da URL `/geo/address` e deve ser do tipo `GET`.
  - O corpo da requisição deve seguir o padrão abaixo:
```json
{
  "Address":"Rua Arnaldo Barreto",
    "City":"Campinas",
    "State":"SP"
}
```
  - A resposta em caso de sucesso deverá ser um status `200`.
  - O corpo da resposta deve seguir o formato abaixo:
```json
  [
      {
  	    "hotelId": 2,
  	    "name": "Trybe Hotel SP",
  	    "address": "Avenida Paulista, 2000",
  	    "cityName": "São Paulo",
  	    "state": "SP",
  	    "distance": 82
      },
      {
  	    "hotelId": 1,
  	    "name": "Trybe Hotel RJ",
  	    "address": "Avenida Atlântica, 1400",
  	    "cityName": "Rio de Janeiro",
  	    "state": "RJ",
  	    "distance": 399
      },
    /* ... */
  }
```

## ⚒ Instalando <a name = "installing"></a>

```bash
# Clone o projeto
$ git clone git@github.com:wesleymktd/project-trybe-hotel-fase-b.git
# Acesse
$ cd ./project-trybe-hotel-fase-b/src
# Instale as dependencias
$ dotnet restore
# Acesse o diretório TrybeHotel
$ cd TrybeHotel
# Inicie o projeto
$ dotnet run

```

## ⚒ Testes automatizados <a name = "installing"></a>

```bash
# Clone o projeto
$ git clone git@github.com:wesleymktd/project-trybe-hotel-fase-b.git
# Acesse o diretório TrybeHotel.test

# Execute o comando dotnet test
# para filtrar por algum teste específico execute o comando
$ dotnet test --filter `nome_do_teste`

```

## Principais tecnologias utilizadas:
- C#;
- ASP.NET
- EntityFramework
- Xunit
- JWT
- azure sql edge
