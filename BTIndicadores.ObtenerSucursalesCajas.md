## Obtener Sucursales Cajas

Método para obtener Sucursales y Cajas

| Nombre publicación                   | Programa | Global/País |
| ------------------------------------ | -------- | ----------- |
| BTIndicadores.ObtenerSucursalesCajas | RBTPG705 | Global      |

> Ejemplo de invocación al servicio de Obtener Información Adicional:

```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:bts="http://uy.com.dlya.bantotal/BTSOA/">
   <soapenv:Header/>
   <soapenv:Body>
      <bts:BTIndicadores.ObtenerSucursalesCajas>
         <bts:Btinreq>
           <bts:Device>1</bts:Device>
            <bts:Canal>BTDIGITAL</bts:Canal>
            <bts:Token>959C2E0AEF210ABC0D8AA8F7</bts:Token>
            <bts:Usuario>INSTALADOR</bts:Usuario>
            <bts:Requerimiento>?</bts:Requerimiento>
         </bts:Btinreq>
      </bts:BTIndicadores.ObtenerSucursalesCajas>
   </soapenv:Body>
</soapenv:Envelope>
```

```json
curl -X POST \
	'http://btd-bantotal.eastus2.cloudapp.azure.com:4462/btdeveloper/servlet/com.dlya.bantotal.odwsbt_BTClientes?ObtenerInformacionAdicional' \
	-H 'cache-control: no-cache' \
	-H 'content-type: application/json' \
	-H 'postman-token: 52baf1dc-e302-90a6-0de1-24fa234c0379' \
	-d '{
   "Btinreq": {
      "Device": 1,
      "Canal": "BTDIGITAL",
      "Token": "959C2E0AEF210ABC0D8AA8F7",
      "Usuario": "INSTALADOR",
      "Requerimiento": "?"
   }
}'
```

> El POST retornará la siguiente estructura:

```xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:SOAP-ENC="http://schemas.xmlsoap.org/soap/encoding/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
   <SOAP-ENV:Body>
      <BTIndicadores.ObtenerSucursalesCajasResponse xmlns="http://uy.com.dlya.bantotal/BTSOA/">
         <Btinreq>
            <Device>1</Device>
            <Usuario>INSTALADOR</Usuario>
            <Requerimiento>?</Requerimiento>
            <Canal>BTDIGITAL</Canal>
            <Token>959C2E0AEF210ABC0D8AA8F7</Token>
         </Btinreq>
         <sdtSucursalesCajas>
            <cajasCerradas>0</cajasCerradas>
            <porcentajeCajasA>100.00</porcentajeCajasA>
            <ListadoCajasA>
               <SdtsBTCaja>
                  <usuario>ASESOR</usuario>
                  <nombre>ASESOR</nombre>
                  <indicador>400</indicador>
                  <sucursalId>1</sucursalId>
               </SdtsBTCaja>
               <SdtsBTCaja>
                  <usuario>BANTOTAL</usuario>
                  <nombre>BANTOTAL</nombre>
                  <indicador>111</indicador>
                  <sucursalId>1</sucursalId>
               </SdtsBTCaja>
               <SdtsBTCaja>
                  <usuario>CAJERO</usuario>
                  <nombre>CAJERO</nombre>
                  <indicador>402</indicador>
                  <sucursalId>1</sucursalId>
               </SdtsBTCaja>
               <SdtsBTCaja>
                  <usuario>CAPTACCONF</usuario>
                  <nombre>CAPTACCONF</nombre>
                  <indicador>350</indicador>
                  <sucursalId>1</sucursalId>
               </SdtsBTCaja>
               <SdtsBTCaja>
                  <usuario>CAPTACION</usuario>
                  <nombre>CAPTACION</nombre>
                  <indicador>401</indicador>
                  <sucursalId>1000</sucursalId>
               </SdtsBTCaja>
               <SdtsBTCaja>
                  <usuario>EJECCUENTA</usuario>
                  <nombre>EJECCUENTA</nombre>
                  <indicador>23</indicador>
                  <sucursalId>1000</sucursalId>
               </SdtsBTCaja>
               <SdtsBTCaja>
                  <usuario>GERENTE</usuario>
                  <nombre>GERENTE</nombre>
                  <indicador>400</indicador>
                  <sucursalId>1</sucursalId>
               </SdtsBTCaja>
               <SdtsBTCaja>
                  <usuario>INSTALADOR</usuario>
                  <nombre>INSTALADOR</nombre>
                  <indicador>400</indicador>
                  <sucursalId>1</sucursalId>
               </SdtsBTCaja>
               <SdtsBTCaja>
                  <usuario>INSTALADORBANTOTAL</usuario>
                  <nombre>INSTALADOR BANTOTAL2</nombre>
                  <indicador>5000</indicador>
                  <sucursalId>1000</sucursalId>
               </SdtsBTCaja>
               <SdtsBTCaja>
                  <usuario>JEFE</usuario>
                  <nombre>JEFE</nombre>
                  <indicador>400</indicador>
                  <sucursalId>1</sucursalId>
               </SdtsBTCaja>
               <SdtsBTCaja>
                  <usuario>SEGURIDAD</usuario>
                  <nombre>SEGURIDAD</nombre>
                  <indicador>55</indicador>
                  <sucursalId>1000</sucursalId>
               </SdtsBTCaja>
               <SdtsBTCaja>
                  <usuario>TESORSUC</usuario>
                  <nombre>TESORSUC</nombre>
                  <indicador>403</indicador>
                  <sucursalId>1000</sucursalId>
               </SdtsBTCaja>
               <SdtsBTCaja>
                  <usuario>USUARIOBIT</usuario>
                  <nombre/>
                  <indicador>17</indicador>
                  <sucursalId>1</sucursalId>
               </SdtsBTCaja>
            </ListadoCajasA>
            <ListadoSucursalesC>
               <SdtsBTSucursal>
                  <telefono/>
                  <descripcion>Sucursal 25634</descripcion>
                  <direccion/>
                  <identificador>25634</identificador>
                  <longitud>0E-14</longitud>
                  <latitud>0E-14</latitud>
               </SdtsBTSucursal>
            </ListadoSucursalesC>
            <cajasAbiertas>13</cajasAbiertas>
            <ListadoSucursalesA>
               <SdtsBTSucursal>
                  <telefono/>
                  <descripcion>Casa Matriz</descripcion>
                  <direccion/>
                  <identificador>1</identificador>
                  <longitud>0E-14</longitud>
                  <latitud>0E-14</latitud>
               </SdtsBTSucursal>
               <SdtsBTSucursal>
                  <telefono/>
                  <descripcion>Sucursal Ciudad de la Costa</descripcion>
                  <direccion/>
                  <identificador>1000</identificador>
                  <longitud>0E-14</longitud>
                  <latitud>0E-14</latitud>
               </SdtsBTSucursal>
            </ListadoSucursalesA>
            <sucursalesCerradas>1</sucursalesCerradas>
            <sucursalesAbiertas>2</sucursalesAbiertas>
            <porcentajeSucursalesC>33.33</porcentajeSucursalesC>
            <totalCajas>13</totalCajas>
            <porcentajeSucursalesA>66.66</porcentajeSucursalesA>
            <porcentajeCajasC>0.00</porcentajeCajasC>
            <totalSucursales>3</totalSucursales>
            <ListadoCajasC></ListadoCajasC>
         </sdtSucursalesCajas>
         <Erroresnegocio></Erroresnegocio>
         <Btoutreq>
            <Numero>11992</Numero>
            <Estado>OK</Estado>
            <Servicio>BTIndicadores.ObtenerSucursalesCajas</Servicio>
            <Requerimiento>?</Requerimiento>
            <Fecha>2023-05-22</Fecha>
            <Canal>BTDIGITAL</Canal>
            <Hora>15:20:16</Hora>
         </Btoutreq>
      </BTIndicadores.ObtenerSucursalesCajasResponse>
   </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

```json
{
   "Btinreq": {
      "Device": 1,
      "Usuario": "INSTALADOR",
      "Requerimiento": "?",
      "Canal": "BTDIGITAL",
      "Token": "959C2E0AEF210ABC0D8AA8F7"
   },
   "sdtSucursalesCajas": {
      "cajasCerradas": 0,
      "porcentajeCajasA": 100,
      "ListadoCajasA": {
      "SdtsBTCaja": [
         {
            "usuario": "ASESOR",
            "nombre": "ASESOR",
            "indicador": 400,
            "sucursalId": 1
         },
         {
            "usuario": "BANTOTAL",
            "nombre": "BANTOTAL",
            "indicador": 111,
            "sucursalId": 1
         },
         {
            "usuario": "CAJERO",
            "nombre": "CAJERO",
            "indicador": 402,
            "sucursalId": 1
         },
         {
            "usuario": "CAPTACCONF",
            "nombre": "CAPTACCONF",
            "indicador": 350,
            "sucursalId": 1
         },
         {
            "usuario": "CAPTACION",
            "nombre": "CAPTACION",
            "indicador": 401,
            "sucursalId": 1000
         },
         {
            "usuario": "EJECCUENTA",
            "nombre": "EJECCUENTA",
            "indicador": 23,
            "sucursalId": 1000
         },
         {
            "usuario": "GERENTE",
            "nombre": "GERENTE",
            "indicador": 400,
            "sucursalId": 1
         },
         {
            "usuario": "INSTALADOR",
            "nombre": "INSTALADOR",
            "indicador": 400,
            "sucursalId": 1
         },
         {
            "usuario": "INSTALADORBANTOTAL",
            "nombre": "INSTALADOR BANTOTAL2",
            "indicador": 5000,
            "sucursalId": 1000
         },
         {
            "usuario": "JEFE",
            "nombre": "JEFE",
            "indicador": 400,
            "sucursalId": 1
         },
         {
            "usuario": "SEGURIDAD",
            "nombre": "SEGURIDAD",
            "indicador": 55,
            "sucursalId": 1000
         },
         {
            "usuario": "TESORSUC",
            "nombre": "TESORSUC",
            "indicador": 403,
            "sucursalId": 1000
         },
         {
            "usuario": "USUARIOBIT",
            "nombre": "",
            "indicador": 17,
            "sucursalId": 1
         }
      ]
      },
      "ListadoSucursalesC": {
      "SdtsBTSucursal": {
         "telefono": "",
         "descripcion": "Sucursal 25634",
         "direccion": "",
         "identificador": 25634,
         "longitud": 0,
         "latitud": 0
      }
      },
      "cajasAbiertas": 13,
      "ListadoSucursalesA": {
      "SdtsBTSucursal": [
         {
            "telefono": "",
            "descripcion": "Casa Matriz",
            "direccion": "",
            "identificador": 1,
            "longitud": 0,
            "latitud": 0
         },
         {
            "telefono": "",
            "descripcion": "Sucursal Ciudad de la Costa",
            "direccion": "",
            "identificador": 1000,
            "longitud": 0,
            "latitud": 0
         }
      ]
      },
      "sucursalesCerradas": 1,
      "sucursalesAbiertas": 2,
      "porcentajeSucursalesC": 33.33,
      "totalCajas": 13,
      "porcentajeSucursalesA": 66.66,
      "porcentajeCajasC": 0,
      "totalSucursales": 3,
      "ListadoCajasC": ""
   },
   "Erroresnegocio": "",
   "Btoutreq": {
      "Numero": 11992,
      "Estado": "OK",
      "Servicio": "BTIndicadores.ObtenerSucursalesCajas",
      "Requerimiento": "?",
      "Fecha": "2023-05-22",
      "Canal": "BTDIGITAL",
      "Hora": "15:20:16"
   }
}'
```

### Datos de entrada

No aplica.

### Datos de salida

| Nombre                | Tipo           | Comentarios                     |
| --------------------- | -------------- | ------------------------------- |
| totalSucursales       | Int            | Informacion Adicional de datos. |
| sucursalesCerradas    | Int            | Informacion Adicional de datos. |
| sucursalesAbiertas    | Int            | Informacion Adicional de datos. |
| porcentajeSucursalesC | Int            | Informacion Adicional de datos. |
| porcentajeSucursalesA | Int            | Informacion Adicional de datos. |
| ListadoSucursalesC    | SdtsBTSucursal | Informacion Adicional de datos. |
| ListadoSucursalesA    | SdtsBTSucursal | Informacion Adicional de datos. |
| totalCajas            | Int            | Informacion Adicional de datos. |
| cajasCerradas         | Int            | Informacion Adicional de datos. |
| cajasAbiertas         | Int            | Informacion Adicional de datos. |
| porcentajeCajasC      | Int            | Informacion Adicional de datos. |
| porcentajeCajasA      | Int            | Informacion Adicional de datos. |
| ListadoCajasC         | SdtsBTCaja     | Informacion Adicional de datos. |
| ListadoCajasA         | SdtsBTCaja     | Informacion Adicional de datos. |

Los campos del tipo de dato estructurado SdtsBTSucursal son los siguientes:

| Campo         | Tipo   | Comentarios    |
| ------------- | ------ | -------------- |
| identificador | Int    | Identificador. |
| descripcion   | String | descripción.   |
| direccion     | String | dirección.     |
| telefono      | String | teléfono.      |
| latitud       | Int    | latitud.       |
| longitud      | Int    | longitud.      |

Los campos del tipo de dato estructurado SdtsBTCaja son los siguientes:

| Campo      | Tipo   | Comentarios  |
| ---------- | ------ | ------------ |
| sucursalId | Int    | sucursal ID. |
| usuario    | String | usuario.     |
| indicador  | Int    | indicador.   |
| nombre     | String | nombre.      |

### Errores

No aplica.
