## Obtener Monedas Indices

Método para obtener Monedas e Indices en funcionamiento

| Nombre publicación                  | Programa | Global/País |
| ----------------------------------- | -------- | ----------- |
| BTIndicadores.ObtenerMonedasIndices | RBTPG704 | Global      |

> Ejemplo de invocación al servicio de Obtener Información Adicional:

```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:bts="http://uy.com.dlya.bantotal/BTSOA/">
   <soapenv:Header/>
   <soapenv:Body>
      <bts:BTIndicadores.ObtenerMonedasIndices>
         <bts:Btinreq>
           <bts:Device>1</bts:Device>
            <bts:Canal>BTDIGITAL</bts:Canal>
            <bts:Token>959C2E0AEF210ABC0D8AA8F7</bts:Token>
            <bts:Usuario>INSTALADOR</bts:Usuario>
            <bts:Requerimiento>?</bts:Requerimiento>
         </bts:Btinreq>
      </bts:BTIndicadores.ObtenerMonedasIndices>
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
      <BTIndicadores.ObtenerMonedasIndicesResponse xmlns="http://uy.com.dlya.bantotal/BTSOA/">
         <Btinreq>
            <Device>1</Device>
            <Usuario>INSTALADOR</Usuario>
            <Requerimiento>?</Requerimiento>
            <Canal>BTDIGITAL</Canal>
            <Token>959C2E0AEF210ABC0D8AA8F7</Token>
         </Btinreq>
         <sdtMonedas>
            <SdtsBTMonedaIndice>
               <tipoCambio>N</tipoCambio>
               <codigo>0</codigo>
               <nombre>Pesos</nombre>
            </SdtsBTMonedaIndice>
            <SdtsBTMonedaIndice>
               <tipoCambio>N</tipoCambio>
               <codigo>105</codigo>
               <nombre>DOLAR AUSTRALIANO</nombre>
            </SdtsBTMonedaIndice>
            <SdtsBTMonedaIndice>
               <tipoCambio>N</tipoCambio>
               <codigo>500</codigo>
               <nombre>PESOS ARGENTINOS</nombre>
            </SdtsBTMonedaIndice>
            <SdtsBTMonedaIndice>
               <tipoCambio>N</tipoCambio>
               <codigo>1111</codigo>
               <nombre>EURO</nombre>
            </SdtsBTMonedaIndice>
            <SdtsBTMonedaIndice>
               <tipoCambio>N</tipoCambio>
               <codigo>2222</codigo>
               <nombre>DÓLAR ESTADOUNIDENSE</nombre>
            </SdtsBTMonedaIndice>
            <SdtsBTMonedaIndice>
               <tipoCambio>N</tipoCambio>
               <codigo>2225</codigo>
               <nombre>DÓLAR ESTADOUNIDENSE - BILLETE</nombre>
            </SdtsBTMonedaIndice>
            <SdtsBTMonedaIndice>
               <tipoCambio>N</tipoCambio>
               <codigo>3600</codigo>
               <nombre>YENS</nombre>
            </SdtsBTMonedaIndice>
         </sdtMonedas>
         <sdtIndices>
            <SdtsBTMonedaIndice>
               <tipoCambio>N</tipoCambio>
               <codigo>0</codigo>
               <nombre>Billete</nombre>
            </SdtsBTMonedaIndice>
            <SdtsBTMonedaIndice>
               <tipoCambio>N</tipoCambio>
               <codigo>50</codigo>
               <nombre>Unidad de Valor Adquisitivo</nombre>
            </SdtsBTMonedaIndice>
         </sdtIndices>
         <Erroresnegocio></Erroresnegocio>
         <Btoutreq>
            <Numero>11991</Numero>
            <Estado>OK</Estado>
            <Servicio>BTIndicadores.ObtenerMonedasIndices</Servicio>
            <Requerimiento>?</Requerimiento>
            <Fecha>2023-05-22</Fecha>
            <Canal>BTDIGITAL</Canal>
            <Hora>15:09:29</Hora>
         </Btoutreq>
      </BTIndicadores.ObtenerMonedasIndicesResponse>
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
   "sdtMonedas": {
      "SdtsBTMonedaIndice": [
      {
         "tipoCambio": "N",
         "codigo": 0,
         "nombre": "Pesos"
      },
      {
         "tipoCambio": "N",
         "codigo": 105,
         "nombre": "DOLAR AUSTRALIANO"
      },
      {
         "tipoCambio": "N",
         "codigo": 500,
         "nombre": "PESOS ARGENTINOS"
      },
      {
         "tipoCambio": "N",
         "codigo": 1111,
         "nombre": "EURO"
      },
      {
         "tipoCambio": "N",
         "codigo": 2222,
         "nombre": "DÓLAR ESTADOUNIDENSE"
      },
      {
         "tipoCambio": "N",
         "codigo": 2225,
         "nombre": "DÓLAR ESTADOUNIDENSE - BILLETE"
      },
      {
         "tipoCambio": "N",
         "codigo": 3600,
         "nombre": "YENS"
      }
      ]
   },
   "sdtIndices": {
      "SdtsBTMonedaIndice": [
      {
         "tipoCambio": "N",
         "codigo": 0,
         "nombre": "Billete"
      },
      {
         "tipoCambio": "N",
         "codigo": 50,
         "nombre": "Unidad de Valor Adquisitivo"
      }
      ]
   },
   "Erroresnegocio": "",
   "Btoutreq": {
      "Numero": 11991,
      "Estado": "OK",
      "Servicio": "BTIndicadores.ObtenerMonedasIndices",
      "Requerimiento": "?",
      "Fecha": "2023-05-22",
      "Canal": "BTDIGITAL",
      "Hora": "15:09:29"
   }
}'
```

### Datos de entrada

No aplica.

### Datos de salida

| Nombre     | Tipo               | Comentarios                     |
| ---------- | ------------------ | ------------------------------- |
| sdtMonedas | SdtsBTMonedaIndice | Informacion Adicional de datos. |

| Nombre     | Tipo               | Comentarios                     |
| ---------- | ------------------ | ------------------------------- |
| sdtIndices | SdtsBTMonedaIndice | Informacion Adicional de datos. |

Los campos del tipo de dato estructurado SdtsBTMonedaIndice son los siguientes:

| Campo      | Tipo   | Comentarios           |
| ---------- | ------ | --------------------- |
| codigo     | Int    | Codigo Identificador. |
| nombre     | String | nombre.               |
| tipoCambio | String | tipo Cambio.          |

### Errores

No aplica.
