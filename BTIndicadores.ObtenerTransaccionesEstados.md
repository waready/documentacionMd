## Obtener Transacciones por Estados

Método para obtener Transacciones por Estados

| Nombre publicación                        | Programa | Global/País |
| ----------------------------------------- | -------- | ----------- |
| BTIndicadores.ObtenerTransaccionesEstados | RBTPG706 | Global      |

> Ejemplo de invocación al servicio de Obtener Información Adicional:

```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:bts="http://uy.com.dlya.bantotal/BTSOA/">
   <soapenv:Header/>
   <soapenv:Body>
      <bts:BTIndicadores.ObtenerTransaccionesEstados>
         <bts:Btinreq>
            <bts:Device>1</bts:Device>
            <bts:Canal>BTDIGITAL</bts:Canal>
            <bts:Token>959C2E0AEF210ABC0D8AA8F7</bts:Token>
            <bts:Usuario>INSTALADOR</bts:Usuario>
            <bts:Requerimiento>?</bts:Requerimiento>
         </bts:Btinreq>
      </bts:BTIndicadores.ObtenerTransaccionesEstados>
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
      <BTIndicadores.ObtenerTransaccionesEstadosResponse xmlns="http://uy.com.dlya.bantotal/BTSOA/">
         <Btinreq>
            <Device>1</Device>
            <Usuario>INSTALADOR</Usuario>
            <Requerimiento>?</Requerimiento>
            <Canal>BTDIGITAL</Canal>
            <Token>959C2E0AEF210ABC0D8AA8F7</Token>
         </Btinreq>
         <sdtTransaccionesEstados>
            <transaccionM>0</transaccionM>
            <transaccionL>3</transaccionL>
            <transaccionH>0</transaccionH>
            <otros>54</otros>
            <transaccionE>31</transaccionE>
            <transaccionB>42</transaccionB>
            <transaccionX>0</transaccionX>
            <transaccionA>0</transaccionA>
            <exito>17</exito>
            <error>31</error>
            <transaccionS>17</transaccionS>
            <transaccionR>0</transaccionR>
            <transaccionSP>0</transaccionSP>
            <sucursalParametros>0</sucursalParametros>
            <transaccionP>9</transaccionP>
            <transaccionN>0</transaccionN>
         </sdtTransaccionesEstados>
         <Erroresnegocio></Erroresnegocio>
         <Btoutreq>
            <Numero>11993</Numero>
            <Estado>OK</Estado>
            <Servicio>BTIndicadores.ObtenerTransaccionesEstados</Servicio>
            <Requerimiento>?</Requerimiento>
            <Fecha>2023-05-22</Fecha>
            <Canal>BTDIGITAL</Canal>
            <Hora>15:37:04</Hora>
         </Btoutreq>
      </BTIndicadores.ObtenerTransaccionesEstadosResponse>
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
   "sdtTransaccionesEstados": {
      "transaccionM": 0,
      "transaccionL": 3,
      "transaccionH": 0,
      "otros": 54,
      "transaccionE": 31,
      "transaccionB": 42,
      "transaccionX": 0,
      "transaccionA": 0,
      "exito": 17,
      "error": 31,
      "transaccionS": 17,
      "transaccionR": 0,
      "transaccionSP": 0,
      "sucursalParametros": 0,
      "transaccionP": 9,
      "transaccionN": 0
   },
   "Erroresnegocio": "",
   "Btoutreq": {
      "Numero": 11993,
      "Estado": "OK",
      "Servicio": "BTIndicadores.ObtenerTransaccionesEstados",
      "Requerimiento": "?",
      "Fecha": "2023-05-22",
      "Canal": "BTDIGITAL",
      "Hora": "15:37:04"
   }
}'
```

### Datos de entrada

No aplica.

### Datos de salida

<!-- | Nombre                | Tipo           | Comentarios                     |
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
| ListadoCajasA         | SdtsBTCaja     | Informacion Adicional de datos. | -->

Los campos del tipo de dato estructurado sdtTransaccionesEstados son los siguientes:

| Campo              | Tipo | Comentarios         |
| ------------------ | ---- | ------------------- |
| exito              | Int  | exito.              |
| error              | Int  | error.              |
| otros              | Int  | otros.              |
| transaccionA       | Int  | transacción A.      |
| transaccionB       | Int  | transacción B.      |
| transaccionE       | Int  | transacción E.      |
| transaccionH       | Int  | transacción H.      |
| transaccionL       | Int  | transacción L.      |
| transaccionM       | Int  | transacción M.      |
| transaccionN       | Int  | transacción N.      |
| transaccionP       | Int  | transacción P.      |
| transaccionR       | Int  | transacción R.      |
| transaccionS       | Int  | transacción S.      |
| transaccionX       | Int  | transacción X.      |
| transaccionSP      | Int  | transacción SP.      |
| sucursalParametros | Int  | sucursal Parametros |

### Errores

No aplica.
