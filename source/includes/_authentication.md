# Autenticación

> Ejemplo elemento credentials, presente en todas las peticiones XML

````xml
<credentials>
    <systemCode>SFO</systemCode>
    <vendorCode>FOO</vendorCode>
    <user>BAR</user>
    <password>FOOBAR</password>
</credentials>
````

````json
{
   "credentials": {
       "systemCode": "SFO",
       "vendorCode": "FOO",
       "user": "BAR",
       "password": "FOOBAR"
   }
}
````

Todas las peticiones contienen el elemento credentials (ejemplo a la derecha), el cuál contiene las credenciales de autenticación.

- URL XML: **https://xml.hotetec.com/unibox-api/supplier/xmlservice.srv**

<aside class="notice">Por favor, solicitar credenciales de acceso a <b>connectivity@hotetec.com</b></aside>

