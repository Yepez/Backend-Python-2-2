# Serverless Python
[![serverless](http://public.serverless.com/badges/v3.svg)](http://www.serverless.com)

El servicio se ejecuta en AWS Lambda mediante [Serverless Framework](https://github.com/serverless/serverless).

El servicio depende del paquete externo (`requests`) y expone 1 REST API endpoints:

| **Endpoint** |**Description**|
|-------|------|
| `GET /negocios/{condicion}/{entidad}` | Recupera un listado de negocios por categoria, municipio dependiendo de la entidad  específica (e.g. `GET /negocios/guadalajara/jalisco`) |


# Usage
## Setup
| **Step** | **Command** |**Description**|
|---|-------|------|
|  1. | `npm install -g serverless` | Install Serverless CLI  |
|  2. | `npm install` | Install Serverless dependencies  |
|  3. | Set up an AWS account with admin permissions | [Documentation](https://serverless.com/framework/docs/providers/aws/guide/credentials/)  |

## Development
| **Step** | **Command** |**Description**|
|---|-------|------|
|  1. | `mkvirtualenv negocios` | Create virtual environment (using [virtualenvwrapper](https://virtualenvwrapper.readthedocs.io/en/latest/)) |
|  2. | `pip install -r requirements.txt` | Install dependencies|


## Deployment

	sls deploy

### Invocation

	curl <host>/negocios/restaurantes/jalisco
