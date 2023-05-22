## Obtener Posibles Rubros Bolsa

Método para obtener Posibles Rubros Bolsa

| Nombre publicación                | Programa | Global/País |
| --------------------------------- | -------- | ----------- |
| BTIndicadores.ObtenerRubrosBolsas | RBTPG708 | Global      |

> Ejemplo de invocación al servicio de Obtener Información Adicional:

```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:bts="http://uy.com.dlya.bantotal/BTSOA/">
   <soapenv:Header/>
   <soapenv:Body>
      <bts:BTIndicadores.ObtenerRubrosBolsas>
         <bts:Btinreq>
            <bts:Device>1</bts:Device>
            <bts:Canal>BTDIGITAL</bts:Canal>
            <bts:Token>959C2E0AEF210ABC0D8AA8F7</bts:Token>
            <bts:Usuario>INSTALADOR</bts:Usuario>
            <bts:Requerimiento>?</bts:Requerimiento>
         </bts:Btinreq>
      </bts:BTIndicadores.ObtenerRubrosBolsas>
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
      <BTIndicadores.ObtenerRubrosBolsasResponse xmlns="http://uy.com.dlya.bantotal/BTSOA/">
         <Btinreq>
            <Device>1</Device>
            <Usuario>INSTALADOR</Usuario>
            <Requerimiento>?</Requerimiento>
            <Canal>BTDIGITAL</Canal>
            <Token>959C2E0AEF210ABC0D8AA8F7</Token>
         </Btinreq>
         <sdtRubrosBolsas>
            <SdtsBTRubrosBolsa>
               <moneda>0</moneda>
               <cuentaCliente>0</cuentaCliente>
               <signoMoneda>$</signoMoneda>
               <ocurrencias>9</ocurrencias>
               <descripcion>Mon.Y Bill.En Empresa-Ventanilla</descripcion>
               <subOperacion>400</subOperacion>
               <rubro>101002001</rubro>
               <papel>0</papel>
               <nombreSucursal>Casa Matriz</nombreSucursal>
               <nombrePapel>Billete</nombrePapel>
               <empresa>1</empresa>
               <tipoOperacion>0</tipoOperacion>
               <operacion>0</operacion>
               <sucursal>1</sucursal>
               <nombreEmpresa>Finaxis</nombreEmpresa>
            </SdtsBTRubrosBolsa>
            <SdtsBTRubrosBolsa>
               <moneda>0</moneda>
               <cuentaCliente>119</cuentaCliente>
               <signoMoneda>$</signoMoneda>
               <ocurrencias>3</ocurrencias>
               <descripcion>Cuentas Corrientes P.Fis.Residentes</descripcion>
               <subOperacion>51</subOperacion>
               <rubro>140102001</rubro>
               <papel>0</papel>
               <nombreSucursal>Casa Matriz</nombreSucursal>
               <nombrePapel>Billete</nombrePapel>
               <empresa>1</empresa>
               <tipoOperacion>1</tipoOperacion>
               <operacion>0</operacion>
               <sucursal>1</sucursal>
               <nombreEmpresa>Finaxis</nombreEmpresa>
            </SdtsBTRubrosBolsa>
            <SdtsBTRubrosBolsa>
               <moneda>0</moneda>
               <cuentaCliente>176</cuentaCliente>
               <signoMoneda>$</signoMoneda>
               <ocurrencias>2</ocurrencias>
               <descripcion>Cuentas Corrientes P.Fis.Residentes</descripcion>
               <subOperacion>1</subOperacion>
               <rubro>140102001</rubro>
               <papel>0</papel>
               <nombreSucursal>Casa Matriz</nombreSucursal>
               <nombrePapel>Billete</nombrePapel>
               <empresa>1</empresa>
               <tipoOperacion>1</tipoOperacion>
               <operacion>0</operacion>
               <sucursal>1</sucursal>
               <nombreEmpresa>Finaxis</nombreEmpresa>
            </SdtsBTRubrosBolsa>
            <SdtsBTRubrosBolsa>
               <moneda>0</moneda>
               <cuentaCliente>176</cuentaCliente>
               <signoMoneda>$</signoMoneda>
               <ocurrencias>2</ocurrencias>
               <descripcion>Cuentas Corrientes P.Fis.Residentes</descripcion>
               <subOperacion>2</subOperacion>
               <rubro>140102001</rubro>
               <papel>0</papel>
               <nombreSucursal>Casa Matriz</nombreSucursal>
               <nombrePapel>Billete</nombrePapel>
               <empresa>1</empresa>
               <tipoOperacion>1</tipoOperacion>
               <operacion>0</operacion>
               <sucursal>1</sucursal>
               <nombreEmpresa>Finaxis</nombreEmpresa>
            </SdtsBTRubrosBolsa>
            <SdtsBTRubrosBolsa>
               <moneda>0</moneda>
               <cuentaCliente>59</cuentaCliente>
               <signoMoneda>$</signoMoneda>
               <ocurrencias>2</ocurrencias>
               <descripcion>Cuentas Corrientes P.Jur.Residentes</descripcion>
               <subOperacion>1</subOperacion>
               <rubro>140102002</rubro>
               <papel>0</papel>
               <nombreSucursal>Casa Matriz</nombreSucursal>
               <nombrePapel>Billete</nombrePapel>
               <empresa>1</empresa>
               <tipoOperacion>2</tipoOperacion>
               <operacion>0</operacion>
               <sucursal>1</sucursal>
               <nombreEmpresa>Finaxis</nombreEmpresa>
            </SdtsBTRubrosBolsa>
            <SdtsBTRubrosBolsa>
               <moneda>0</moneda>
               <cuentaCliente>166</cuentaCliente>
               <signoMoneda>$</signoMoneda>
               <ocurrencias>2</ocurrencias>
               <descripcion>BLOQUEO DE CUENTAS CORRIENTES</descripcion>
               <subOperacion>3</subOperacion>
               <rubro>902010150</rubro>
               <papel>0</papel>
               <nombreSucursal>Casa Matriz</nombreSucursal>
               <nombrePapel>Billete</nombrePapel>
               <empresa>1</empresa>
               <tipoOperacion>0</tipoOperacion>
               <operacion>0</operacion>
               <sucursal>1</sucursal>
               <nombreEmpresa>Finaxis</nombreEmpresa>
            </SdtsBTRubrosBolsa>
            <SdtsBTRubrosBolsa>
               <moneda>0</moneda>
               <cuentaCliente>166</cuentaCliente>
               <signoMoneda>$</signoMoneda>
               <ocurrencias>2</ocurrencias>
               <descripcion>CC. BLOQUEO DE CUENTAS CORRIENTES</descripcion>
               <subOperacion>3</subOperacion>
               <rubro>902020150</rubro>
               <papel>0</papel>
               <nombreSucursal>Casa Matriz</nombreSucursal>
               <nombrePapel>Billete</nombrePapel>
               <empresa>1</empresa>
               <tipoOperacion>0</tipoOperacion>
               <operacion>11</operacion>
               <sucursal>1</sucursal>
               <nombreEmpresa>Finaxis</nombreEmpresa>
            </SdtsBTRubrosBolsa>
         </sdtRubrosBolsas>
         <Erroresnegocio></Erroresnegocio>
         <Btoutreq>
            <Numero>11987</Numero>
            <Estado>OK</Estado>
            <Servicio>BTIndicadores.ObtenerRubrosBolsas</Servicio>
            <Requerimiento>?</Requerimiento>
            <Fecha>2023-05-22</Fecha>
            <Canal>BTDIGITAL</Canal>
            <Hora>13:55:55</Hora>
         </Btoutreq>
      </BTIndicadores.ObtenerRubrosBolsasResponse>
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
   "sdtRubrosBolsas": {
      "SdtsBTRubrosBolsa": [
      {
         "moneda": 0,
         "cuentaCliente": 0,
         "signoMoneda": "$",
         "ocurrencias": 9,
         "descripcion": "Mon.Y Bill.En Empresa-Ventanilla",
         "subOperacion": 400,
         "rubro": 101002001,
         "papel": 0,
         "nombreSucursal": "Casa Matriz",
         "nombrePapel": "Billete",
         "empresa": 1,
         "tipoOperacion": 0,
         "operacion": 0,
         "sucursal": 1,
         "nombreEmpresa": "Finaxis"
      },
      {
         "moneda": 0,
         "cuentaCliente": 119,
         "signoMoneda": "$",
         "ocurrencias": 3,
         "descripcion": "Cuentas Corrientes P.Fis.Residentes",
         "subOperacion": 51,
         "rubro": 140102001,
         "papel": 0,
         "nombreSucursal": "Casa Matriz",
         "nombrePapel": "Billete",
         "empresa": 1,
         "tipoOperacion": 1,
         "operacion": 0,
         "sucursal": 1,
         "nombreEmpresa": "Finaxis"
      },
      {
         "moneda": 0,
         "cuentaCliente": 176,
         "signoMoneda": "$",
         "ocurrencias": 2,
         "descripcion": "Cuentas Corrientes P.Fis.Residentes",
         "subOperacion": 1,
         "rubro": 140102001,
         "papel": 0,
         "nombreSucursal": "Casa Matriz",
         "nombrePapel": "Billete",
         "empresa": 1,
         "tipoOperacion": 1,
         "operacion": 0,
         "sucursal": 1,
         "nombreEmpresa": "Finaxis"
      },
      {
         "moneda": 0,
         "cuentaCliente": 176,
         "signoMoneda": "$",
         "ocurrencias": 2,
         "descripcion": "Cuentas Corrientes P.Fis.Residentes",
         "subOperacion": 2,
         "rubro": 140102001,
         "papel": 0,
         "nombreSucursal": "Casa Matriz",
         "nombrePapel": "Billete",
         "empresa": 1,
         "tipoOperacion": 1,
         "operacion": 0,
         "sucursal": 1,
         "nombreEmpresa": "Finaxis"
      },
      {
         "moneda": 0,
         "cuentaCliente": 59,
         "signoMoneda": "$",
         "ocurrencias": 2,
         "descripcion": "Cuentas Corrientes P.Jur.Residentes",
         "subOperacion": 1,
         "rubro": 140102002,
         "papel": 0,
         "nombreSucursal": "Casa Matriz",
         "nombrePapel": "Billete",
         "empresa": 1,
         "tipoOperacion": 2,
         "operacion": 0,
         "sucursal": 1,
         "nombreEmpresa": "Finaxis"
      },
      {
         "moneda": 0,
         "cuentaCliente": 166,
         "signoMoneda": "$",
         "ocurrencias": 2,
         "descripcion": "BLOQUEO DE CUENTAS CORRIENTES",
         "subOperacion": 3,
         "rubro": 902010150,
         "papel": 0,
         "nombreSucursal": "Casa Matriz",
         "nombrePapel": "Billete",
         "empresa": 1,
         "tipoOperacion": 0,
         "operacion": 0,
         "sucursal": 1,
         "nombreEmpresa": "Finaxis"
      },
      {
         "moneda": 0,
         "cuentaCliente": 166,
         "signoMoneda": "$",
         "ocurrencias": 2,
         "descripcion": "CC. BLOQUEO DE CUENTAS CORRIENTES",
         "subOperacion": 3,
         "rubro": 902020150,
         "papel": 0,
         "nombreSucursal": "Casa Matriz",
         "nombrePapel": "Billete",
         "empresa": 1,
         "tipoOperacion": 0,
         "operacion": 11,
         "sucursal": 1,
         "nombreEmpresa": "Finaxis"
      }
      ]
   },
   "Erroresnegocio": "",
   "Btoutreq": {
      "Numero": 11987,
      "Estado": "OK",
      "Servicio": "BTIndicadores.ObtenerRubrosBolsas",
      "Requerimiento": "?",
      "Fecha": "2023-05-22",
      "Canal": "BTDIGITAL",
      "Hora": "13:55:55"
   }
}'
```

### Datos de entrada

No aplica.

### Datos de salida

| Nombre          | Tipo              | Comentarios                     |
| --------------- | ----------------- | ------------------------------- |
| sdtRubrosBolsas | SdtsBTRubrosBolsa | Informacion Adicional de datos. |

Los campos del tipo de dato estructurado SdtsBTRubrosBolsa son los siguientes:

| Campo          | Tipo   | Comentarios      |
| -------------- | ------ | ---------------- |
| empresa        | Int    | empresa.         |
| sucursal       | Int    | sucursal.        |
| rubro          | Int    | rubro.           |
| moneda         | Int    | moneda.          |
| papel          | Int    | papel.           |
| cuentaCliente  | Int    | cuenta Cliente.  |
| operacion      | Int    | operación.       |
| subOperacion   | Int    | sub Operación.   |
| tipoOperacion  | Int    | tipo Operación.  |
| signoMoneda    | String | signo Moneda.    |
| nombreEmpresa  | String | nombre Empresa.  |
| nombreSucursal | String | nombre Sucursal. |
| nombrePapel    | String | nombre Papel.    |
| ocurrencias    | Int    | ocurrencias.     |
| descripcion    | String | descripción.     |

### Errores

No aplica.
