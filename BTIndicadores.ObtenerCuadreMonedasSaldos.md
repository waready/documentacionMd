## Obtener Cierre de Saldos por Moneda

Método para obtener Cierre de Saldos por Moneda

| Nombre publicación                       | Programa | Global/País |
| ---------------------------------------- | -------- | ----------- |
| BTIndicadores.ObtenerCuadreMonedasSaldos | RBTPG707 | Global      |

> Ejemplo de invocación al servicio de Obtener Información Adicional:

```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:bts="http://uy.com.dlya.bantotal/BTSOA/">
   <soapenv:Header/>
   <soapenv:Body>
      <bts:BTIndicadores.ObtenerCuadreMonedasSaldos>
         <bts:Btinreq>
            <bts:Device>1</bts:Device>
            <bts:Canal>BTDIGITAL</bts:Canal>
            <bts:Token>959C2E0AEF210ABC0D8AA8F7</bts:Token>
            <bts:Usuario>INSTALADOR</bts:Usuario>
            <bts:Requerimiento>?</bts:Requerimiento>
         </bts:Btinreq>
      </bts:BTIndicadores.ObtenerCuadreMonedasSaldos>
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
      <BTIndicadores.ObtenerCuadreMonedasSaldosResponse xmlns="http://uy.com.dlya.bantotal/BTSOA/">
         <Btinreq>
            <Device>1</Device>
            <Usuario>INSTALADOR</Usuario>
            <Requerimiento>?</Requerimiento>
            <Canal>BTDIGITAL</Canal>
            <Token>959C2E0AEF210ABC0D8AA8F7</Token>
         </Btinreq>
         <SdtBalanceMonedaSaldos>
            <SdtsBTBalanceMonedaSaldo>
               <saldo>1002305670465.91</saldo>
               <signo>$</signo>
               <codigo>0</codigo>
               <nombre>Pesos</nombre>
            </SdtsBTBalanceMonedaSaldo>
            <SdtsBTBalanceMonedaSaldo>
               <saldo>0.00</saldo>
               <signo>AUD</signo>
               <codigo>105</codigo>
               <nombre>DOLAR AUSTRALIANO</nombre>
            </SdtsBTBalanceMonedaSaldo>
            <SdtsBTBalanceMonedaSaldo>
               <saldo>10000.00</saldo>
               <signo>ARS</signo>
               <codigo>500</codigo>
               <nombre>PESOS ARGENTINOS</nombre>
            </SdtsBTBalanceMonedaSaldo>
            <SdtsBTBalanceMonedaSaldo>
               <saldo>1000616680.88</saldo>
               <signo>EUR</signo>
               <codigo>1111</codigo>
               <nombre>EURO</nombre>
            </SdtsBTBalanceMonedaSaldo>
            <SdtsBTBalanceMonedaSaldo>
               <saldo>2111507066.93</saldo>
               <signo>USD</signo>
               <codigo>2222</codigo>
               <nombre>DÓLAR ESTADOUNIDENSE</nombre>
            </SdtsBTBalanceMonedaSaldo>
            <SdtsBTBalanceMonedaSaldo>
               <saldo>0.00</saldo>
               <signo>U$D</signo>
               <codigo>2225</codigo>
               <nombre>DÓLAR ESTADOUNIDENSE - BILLETE</nombre>
            </SdtsBTBalanceMonedaSaldo>
            <SdtsBTBalanceMonedaSaldo>
               <saldo>0.00</saldo>
               <signo>JPY</signo>
               <codigo>3600</codigo>
               <nombre>YENS</nombre>
            </SdtsBTBalanceMonedaSaldo>
         </SdtBalanceMonedaSaldos>
         <Erroresnegocio></Erroresnegocio>
         <Btoutreq>
            <Numero>11996</Numero>
            <Estado>OK</Estado>
            <Servicio>BTIndicadores.ObtenerCuadreMonedasSaldos</Servicio>
            <Requerimiento>?</Requerimiento>
            <Fecha>2023-05-22</Fecha>
            <Canal>BTDIGITAL</Canal>
            <Hora>15:46:03</Hora>
         </Btoutreq>
      </BTIndicadores.ObtenerCuadreMonedasSaldosResponse>
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
   "SdtBalanceMonedaSaldos": {
      "SdtsBTBalanceMonedaSaldo": [
      {
         "saldo": 1002305670465.91,
         "signo": "$",
         "codigo": 0,
         "nombre": "Pesos"
      },
      {
         "saldo": 0,
         "signo": "AUD",
         "codigo": 105,
         "nombre": "DOLAR AUSTRALIANO"
      },
      {
         "saldo": 10000,
         "signo": "ARS",
         "codigo": 500,
         "nombre": "PESOS ARGENTINOS"
      },
      {
         "saldo": 1000616680.88,
         "signo": "EUR",
         "codigo": 1111,
         "nombre": "EURO"
      },
      {
         "saldo": 2111507066.93,
         "signo": "USD",
         "codigo": 2222,
         "nombre": "DÓLAR ESTADOUNIDENSE"
      },
      {
         "saldo": 0,
         "signo": "U$D",
         "codigo": 2225,
         "nombre": "DÓLAR ESTADOUNIDENSE - BILLETE"
      },
      {
         "saldo": 0,
         "signo": "JPY",
         "codigo": 3600,
         "nombre": "YENS"
      }
      ]
   },
   "Erroresnegocio": "",
   "Btoutreq": {
      "Numero": 11996,
      "Estado": "OK",
      "Servicio": "BTIndicadores.ObtenerCuadreMonedasSaldos",
      "Requerimiento": "?",
      "Fecha": "2023-05-22",
      "Canal": "BTDIGITAL",
      "Hora": "15:46:03"
   }
}'
```

### Datos de entrada

No aplica.

### Datos de salida

| Nombre                 | Tipo                     | Comentarios                     |
| ---------------------- | ------------------------ | ------------------------------- |
| SdtBalanceMonedaSaldos | SdtsBTBalanceMonedaSaldo | Informacion Adicional de datos. |

Los campos del tipo de dato estructurado SdtsBTBalanceMonedaSaldo son los siguientes:

| Campo  | Tipo   | Comentarios |
| ------ | ------ | ----------- |
| codigo | Int    | codigo.     |
| saldo  | Int    | saldo.      |
| nombre | String | nombre.     |
| signo  | String | signo.      |

### Errores

No aplica.
