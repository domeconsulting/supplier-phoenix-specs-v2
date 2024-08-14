# BookingResale

> Ejemplo BookingResaleRequest para revender una reserva en particular

````xml
<?xml version="1.0" encoding="UTF-8"?>
<BookingResaleRequest>
    <credentials>
        <systemCode>SFO</systemCode>
        <vendorCode>FOO</vendorCode>
        <user>BAR</user>
        <password>FOOBAR</password>
    </credentials>
    <hotelCode>1234</hotelCode>
    <reference>TESTHTT240326SFESKH</reference>
    <endCustomer>
        <name>Customer Name</name>
        <firstName>Customer</firstName>
        <lastName>Name</lastName>
        <mail>customername@hotetec.com</mail>
        <phone>+34666777888</phone>
        <document>
            <typeDocument>DNI</typeDocument>
            <numberDocument>43136559E</numberDocument>
        </document>
        <nationality>es</nationality>
        <language>ES</language>
    </endCustomer>
    <guest id="1">
        <name>Guest</name>
        <firstName>1</firstName>
        <lastName>Guest 1</lastName>
    </guest>
    <guest id="2">
        <name>Guest</name>
        <firstName>2</firstName>
        <lastName>Guest 2</lastName>
    </guest>
    <guest id="3">
        <name>Guest</name>
        <firstName>3</firstName>
        <lastName>Guest 3</lastName>
    </guest>
</BookingResaleRequest>
````

````json
{
  "BookingResaleRequest": {
    "credentials": {
      "systemCode": "SFO",
      "vendorCode": "FOO",
      "user": "BAR",
      "password": "FOOBAR"
    },
    "hotelCode": 1234,
    "reference": "TESTHTT240326SFESKH",
    "endCustomer": {
      "name": "Customer Name",
      "firstName": "Customer",
      "lastName": "Name",
      "mail": "customername@hotetec.com",
      "phone": 34666777888,
      "document": {
        "typeDocument": "DNI",
        "numberDocument": "43136559E"
      },
      "nationality": "es",
      "language": "ES"
    },
    "guest": [
      {
        "name": "Guest",
        "firstName": 1,
        "lastName": "Guest 1"
      },
      {
        "name": "Guest",
        "firstName": 2,
        "lastName": "Guest 2"
      },
      {
        "name": "Guest",
        "firstName": 3,
        "lastName": "Guest 3"
      }
    ]
  }
}
````

> Ejemplo respuesta BookingConfirmResponse procesada correctamente

````xml
<?xml version="1.0" encoding="UTF-8"?>
<BookingResaleResponse>
    <sessionId>SFO#12345#199934329361320</sessionId>
    <booking>
        <reference>TESTHTT240326SFESKH</reference>
        <creationDate>26/03/2024 16:11</creationDate>
        <cancellationDate>28/05/2024 14:25</cancellationDate>
        <country>ES</country>
        <checkIn>14/05/2024</checkIn>
        <checkOut>15/05/2024</checkOut>
        <status>Cancelled</status>
        <amount>18.17</amount>
        <amountToInvoice>18.17</amountToInvoice>
        <bookingClient>
            <clientCode>TESTHTT</clientCode>
            <clientName>Test Hotetec</clientName>
            <fiscalClientName>Test Hotetec</fiscalClientName>
            <addressClient>Parc Bit</addressClient>
            <postalClientCode>07079</postalClientCode>
            <countryClient>ES</countryClient>
            <cifClient>A00000000</cifClient>
            <emailClient>soporte@hotetec.com</emailClient>
        </bookingClient>
        <endCustomer>
            <name>Customer Name</name>
            <firstName>Customer</firstName>
            <lastName>Name</lastName>
            <mail>customername@hotetec.com</mail>
            <phone>+34666777888</phone>
            <nationality>es</nationality>
            <language>ES</language>
        </endCustomer>
        <commission>
            <serviceCommission>
                <serviceId>1</serviceId>
                <commissionAmount>0.0</commissionAmount>
                <commissionPercentage>0.0</commissionPercentage>
            </serviceCommission>
        </commission>
        <hotelCode>1234</hotelCode>
        <currencyCode>EUR</currencyCode>
        <bookingRoom id="1">
            <checkIn>14/05/2024</checkIn>
            <checkOut>15/05/2024</checkOut>
            <status>Cancelled</status>
            <roomCode>DBL#STD</roomCode>
            <mealPlanCode>RO</mealPlanCode>
            <amount>18.17</amount>
            <totalRoomAmount>18.17</totalRoomAmount>
            <commissionRoomAmount>0.0</commissionRoomAmount>
            <netRoomAmount>18.17</netRoomAmount>
            <amountRoomToInvoice>18.17</amountRoomToInvoice>
            <roomRateDay>
                <day>14/05/2024</day>
                <rateCode>31299</rateCode>
                <rateName>Semiflexible</rateName>
                <internalRateName>Semiflexible</internalRateName>
                <amount>28.86</amount>
            </roomRateDay>
            <guest id="1">
                <type>Adult</type>
                <amount>30.28</amount>
                <name>Guest 1</name>
                <firstName>Guest</firstName>
                <lastName>1</lastName>
                <birthDate>14/05/1994</birthDate>
                <age>30</age>
            </guest>
            <guest id="2">
                <type>Adult</type>
                <amount>30.28</amount>
                <name>Guest 2</name>
                <firstName>Guest</firstName>
                <lastName>2</lastName>
                <birthDate>14/05/1994</birthDate>
                <age>30</age>
            </guest>
            <guest id="3">
                <type>Baby</type>
                <name>Guest 3</name>
                <firstName>Guest</firstName>
                <lastName>3</lastName>
                <birthDate>14/05/2023</birthDate>
                <age>1</age>
            </guest>
            <cancellationData>
                <cancelPenaltyPolicy id="3">
                    <date>19/08/2021 00:00</date>
                    <timeRelevant>false</timeRelevant>
                    <amount>18.17</amount>
                </cancelPenaltyPolicy>
            </cancellationData>
        </bookingRoom>
        <bookingSupplement>
            <code>[EtT]SalePolicy(PpT)TESTHTT@71244</code>
            <name>Detalle de bienvenida</name>
            <typeSupplement>SalePolicy</typeSupplement>
            <internalTypeSupplement>SPS</internalTypeSupplement>
            <bookingRoomId>1</bookingRoomId>
            <mandatory>true</mandatory>
        </bookingSupplement>
        <bookingSupplement>
            <code>[EtT]SalePolicy(PpT)TESTHTT@71242</code>
            <name>Cliente registrado</name>
            <typeSupplement>SalePolicy</typeSupplement>
            <internalTypeSupplement>SPS</internalTypeSupplement>
            <checkIn>14/05/2024</checkIn>
            <checkOut>14/05/2024</checkOut>
            <bookingRoomId>1</bookingRoomId>
            <amount>-10.69</amount>
            <mandatory>true</mandatory>
        </bookingSupplement>
        <bookingSupplement>
            <code>[EtT]SalePolicy(PpT)TESTHTT@71660</code>
            <name>TEST VIRTUAL Increment</name>
            <typeSupplement>SalePolicy</typeSupplement>
            <internalTypeSupplement>SPS</internalTypeSupplement>
            <checkIn>14/05/2024</checkIn>
            <checkOut>14/05/2024</checkOut>
            <bookingRoomId>1</bookingRoomId>
            <amount>47.5</amount>
            <mandatory>true</mandatory>
        </bookingSupplement>
        <bookingSupplement>
            <code>[EtT]SalePolicy(PpT)TESTHTT@-71660</code>
            <name>TEST VIRTUAL Decrement</name>
            <typeSupplement>SalePolicy</typeSupplement>
            <internalTypeSupplement>SPS</internalTypeSupplement>
            <checkIn>14/05/2024</checkIn>
            <checkOut>14/05/2024</checkOut>
            <bookingRoomId>1</bookingRoomId>
            <amount>-47.5</amount>
            <mandatory>true</mandatory>
        </bookingSupplement>
        <bookingPayment>
            <modality>ExternManagement</modality>
            <internalModalityName>Transferencia bancaria del 50%</internalModalityName>
            <type>BankTransfer</type>
            <status>Pending</status>
        </bookingPayment>
        <paymentDetail>
            <action>Charge</action>
            <paymentStatus>Pending</paymentStatus>
            <type>BankTransfer</type>
            <date>26/03/2024 00:00</date>
            <amount>30.28</amount>
            <breakdown>
                <bookingRoomId>1</bookingRoomId>
                <amount>30.28</amount>
            </breakdown>
        </paymentDetail>
        <extraCustomData>
            <customData>
                <key>CreationSystem</key>
                <value>HPH</value>
            </customData>
            <customData>
                <key>ParentSystem</key>
                <value>WEB</value>
            </customData>
            <customData>
                <key>Country</key>
                <value>ES</value>
            </customData>
            <customData>
                <key>IpAddress</key>
                <value>206.204.156.105</value>
            </customData>
            <customData>
                <key>BookingEngineCode</key>
                <value>120</value>
            </customData>
            <customData>
                <key>WebsiteUrl</key>
                <value>webtest.hotetec.in</value>
            </customData>
            <customData>
                <key>PriceType</key>
                <value>PVP</value>
            </customData>
            <customData>
                <key>ClientType</key>
                <value>A</value>
            </customData>
            <customData>
                <key>StatusPaymentBooking</key>
                <value>Pending</value>
            </customData>
            <customData>
                <key>OriginalAmount</key>
                <value>60.560</value>
            </customData>
            <customData>
                <key>SUPPLIER.Tripresale.Resaled</key>
                <value>S</value>
            </customData>
            <customData>
                <key>Agency</key>
                <value>1234</value>
            </customData>
            <customData>
                <key>NotSendTimonFare</key>
                <value>S</value>
            </customData>
        </extraCustomData>
        <saleRules/>
    </booking>
</BookingResaleResponse>
````

````json
{
  "BookingResaleResponse": {
    "sessionId": "SFO#12345#199934329361320",
    "booking": {
      "reference": "TESTHTT240326SFESKH",
      "creationDate": "26/03/2024 16:11",
      "cancellationDate": "28/05/2024 14:25",
      "country": "ES",
      "checkIn": "14/05/2024",
      "checkOut": "15/05/2024",
      "status": "Cancelled",
      "amount": 18.17,
      "amountToInvoice": 18.17,
      "bookingClient": {
        "clientCode": "TESTHTT",
        "clientName": "Test Hotetec",
        "fiscalClientName": "Test Hotetec",
        "addressClient": "Parc Bit",
        "postalClientCode": 7079,
        "countryClient": "ES",
        "cifClient": "A00000000",
        "emailClient": "soporte@hotetec.com"
      },
      "endCustomer": {
        "name": "Customer Name",
        "firstName": "Customer",
        "lastName": "Name",
        "mail": "customername@hotetec.com",
        "phone": 34666777888,
        "nationality": "es",
        "language": "ES"
      },
      "commission": {
        "serviceCommission": {
          "serviceId": 1,
          "commissionAmount": 0,
          "commissionPercentage": 0
        }
      },
      "hotelCode": 1234,
      "currencyCode": "EUR",
      "bookingRoom": {
        "checkIn": "14/05/2024",
        "checkOut": "15/05/2024",
        "status": "Cancelled",
        "roomCode": "DBL#STD",
        "mealPlanCode": "RO",
        "amount": 18.17,
        "totalRoomAmount": 18.17,
        "commissionRoomAmount": 0,
        "netRoomAmount": 18.17,
        "amountRoomToInvoice": 18.17,
        "roomRateDay": {
          "day": "14/05/2024",
          "rateCode": 31299,
          "rateName": "Semiflexible",
          "internalRateName": "Semiflexible",
          "amount": 28.86
        },
        "guest": [
          {
            "type": "Adult",
            "amount": 30.28,
            "name": "Guest 1",
            "firstName": "Guest",
            "lastName": 1,
            "birthDate": "14/05/1994",
            "age": 30
          },
          {
            "type": "Adult",
            "amount": 30.28,
            "name": "Guest 2",
            "firstName": "Guest",
            "lastName": 2,
            "birthDate": "14/05/1994",
            "age": 30
          },
          {
            "type": "Baby",
            "name": "Guest 3",
            "firstName": "Guest",
            "lastName": 3,
            "birthDate": "14/05/2023",
            "age": 1
          }
        ],
        "cancellationData": {
          "cancelPenaltyPolicy": {
            "date": "19/08/2021 00:00",
            "timeRelevant": false,
            "amount": 18.17
          }
        }
      },
      "bookingSupplement": [
        {
          "code": "[EtT]SalePolicy(PpT)TESTHTT@71244",
          "name": "Detalle de bienvenida",
          "typeSupplement": "SalePolicy",
          "internalTypeSupplement": "SPS",
          "bookingRoomId": 1,
          "mandatory": true
        },
        {
          "code": "[EtT]SalePolicy(PpT)TESTHTT@71242",
          "name": "Cliente registrado",
          "typeSupplement": "SalePolicy",
          "internalTypeSupplement": "SPS",
          "checkIn": "14/05/2024",
          "checkOut": "14/05/2024",
          "bookingRoomId": 1,
          "amount": -10.69,
          "mandatory": true
        },
        {
          "code": "[EtT]SalePolicy(PpT)TESTHTT@71660",
          "name": "TEST VIRTUAL Increment",
          "typeSupplement": "SalePolicy",
          "internalTypeSupplement": "SPS",
          "checkIn": "14/05/2024",
          "checkOut": "14/05/2024",
          "bookingRoomId": 1,
          "amount": 47.5,
          "mandatory": true
        },
        {
          "code": "[EtT]SalePolicy(PpT)TESTHTT@-71660",
          "name": "TEST VIRTUAL Decrement",
          "typeSupplement": "SalePolicy",
          "internalTypeSupplement": "SPS",
          "checkIn": "14/05/2024",
          "checkOut": "14/05/2024",
          "bookingRoomId": 1,
          "amount": -47.5,
          "mandatory": true
        }
      ],
      "bookingPayment": {
        "modality": "ExternManagement",
        "internalModalityName": "Transferencia bancaria del 50%",
        "type": "BankTransfer",
        "status": "Pending"
      },
      "paymentDetail": {
        "action": "Charge",
        "paymentStatus": "Pending",
        "type": "BankTransfer",
        "date": "26/03/2024 00:00",
        "amount": 30.28,
        "breakdown": {
          "bookingRoomId": 1,
          "amount": 30.28
        }
      },
      "extraCustomData": {
        "customData": [
          {
            "key": "CreationSystem",
            "value": "HPH"
          },
          {
            "key": "ParentSystem",
            "value": "WEB"
          },
          {
            "key": "Country",
            "value": "ES"
          },
          {
            "key": "IpAddress",
            "value": "206.204.156.105"
          },
          {
            "key": "BookingEngineCode",
            "value": 120
          },
          {
            "key": "WebsiteUrl",
            "value": "webtest.hotetec.in"
          },
          {
            "key": "PriceType",
            "value": "PVP"
          },
          {
            "key": "ClientType",
            "value": "A"
          },
          {
            "key": "StatusPaymentBooking",
            "value": "Pending"
          },
          {
            "key": "OriginalAmount",
            "value": 60.56
          },
          {
            "key": "SUPPLIER.Tripresale.Resaled",
            "value": "S"
          },
          {
            "key": "Agency",
            "value": 1234
          },
          {
            "key": "NotSendTimonFare",
            "value": "S"
          }
        ]
      },
      "saleRules": ""
    }
  }
}
````

> Ejemplo respuesta BookingResaleResponse procesada incorrectamente

````xml
<?xml version="1.0" encoding="UTF-8"?>
<BookingResaleResponse>
    <sessionId>SFO#12345#199934329361320</sessionId>
    <notification code="DSUP-7">
        <type>E</type>
        <text>La funcionalidad ResaleBooking-Inbound no está activada. Por favor, consulte su Account Manager</text>
    </notification>
</BookingResaleResponse>
````

````json
{
  "BookingResaleResponse": {
    "sessionId": "SFO#12345#199934329361320",
    "notification": {
      "-code": "DSUP-7",
      "type": "E",
      "text": "La funcionalidad ResaleBooking-Inbound no está activada. Por favor, consulte su Account Manager"
    }
  }
}
````

Mensaje utilizado para la reventa de reservas.

### BookingResaleRequest

Mensaje petición de reventa de reserva
 
Elemento | Tipo | Obl? |  Descripción
--------- | ----------- | ----------- | -----------
credentials | **Credentials** | Sí |Credenciales de autenticación del usuario (Ver Autenticación)
reference | *String* | Sí | Localizador de la reserva de Hotetec
hotelCode | *Integer* | Sí | Código de hotel
endCustomer| **EndCustomer** | Sí | Información del cliente final de la reserva
↳ name| *String* | Sí | Nombre completo del cliente final
↳ firstName| *String* | Sí | Nombre del cliente final
↳ lastName| *String* | Sí | Apellido del cliente final
↳ birthDate| *Date* | No | Fecha de nacimiento (dd/MM/yyy)
↳ mail| *String* | Sí | Email del cliente final
↳ phone| *String* | No | Teléfono de contacto del cliente final
↳ nationality| *String* | No | Nacionadlidad (2 letter ISO 3166)
↳ language| *String* | No | Idioma del cliente
↳ address| *String* | No | Dirección indicada para el cliente
↳ document| **Document** | No | Información referente al documento de identificación de la persona de contacto
↳↳ typeDocument| *String* | No | Tipo de documento (DNI, NIE, Passport o IdentityCard)
↳↳ numberDocument| *String* | No | Número de document
guest[]| **Guest** | Sí | Pasajero de la reserva
↳ @id| *Integer* | Sí | Identificador del pasajero
↳ name| *String* | Sí | Nombre completo del pasajero. Si el nombre no ha sido informado en la reserva, se substituirá por el nombre de la persona de contacto
↳ firstName| *String* | Sí | Nombre del pasajero
↳ lastName| *String* | Sí | Apellido del pasajero

### BookingResaleResponse

Mensaje respuesta de reventa de reserva

Elemento | Tipo | Obl? | Descripción
--------- | ----------- | ----------- | -----------
sessionId | *String* | Sí |Identificador de la sesión que ha procesado la transacción
booking | **Booking** | No | Información de una reserva de hotel
↳ reference| *String* | Sí | Localizador de la reserva
↳ creationDate| *DateTime* | Sí | Fecha de creación de la reserva (dd/MM/yyy HH:mm)
↳ modificationDate| *DateTime* | No | Fecha de modificación de la reserva (dd/MM/yyyy HH:mm). Sólo viene informado cuando es una modificación de reserva
↳ cancellationDate| *DateTime* | No | Fecha de cancelación de la reserva (dd/MM/yyyy HH:mm). Sólo viene informado cuando es una cancelación de reserva
↳ country| *String* | No | Código del país de origen de la reserva (2 letter ISO 3166). Sólo vendrá informado en la reservas propias de Hotetec
↳ checkIn| *Date* | Sí | Fecha de entrada (dd/MM/yyy)
↳ checkOut| *Date* | Sí | Fecha de salida (dd/MM/yyy)
↳ status| *Enum* | Sí | Estado de la reserva (Confirmed, Cancelled, OnRequest)
↳ amount| *Double* | Sí | Importe total de la reserva (#.##)
↳ bookingClient| **BookingClient** | Sí | Información del cliente que ha realizado la reserva, refiriéndose a la agencia (Ej: Logitravel), OTA (Ej: Booking.com), o el propio hotel
↳↳ clientCode| *String* | Sí | Código de cliente
↳↳ clientName| *String* | Sí | Nombre de cliente
↳↳ fiscalClientName| *String* | No | Nombre fiscal referente al cliente de la reserva
↳↳ addressClient| *String* | No | Dirección física de la empresa cliente
↳↳ postalClientCode| *String* | No | Código postal de la empresa cliente
↳↳ countryClient| *String* | No | País de la empresa cliente
↳↳ cifClient| *String* | No | Número CIF de la empresa cliente
↳↳ emailClient| *String* | No | Correo electrónico de la empresa cliente
↳↳ clientReference| *String* | No | Referencia de la reserva del cliente (habitualmente su localizador)
↳ endCustomer| **EndCustomer** | Sí | Información del cliente final de la reserva
↳↳ name| *String* | Sí | Nombre del cliente final
↳↳ birthDate| *Date* | No | Fecha de nacimiento (dd/MM/yyy)
↳↳ mail| *String* | No | Email del cliente final
↳↳ phone| *String* | No | Teléfono de contacto del cliente final
↳↳ nationality| *String* | No | Nacionadlidad (2 letter ISO 3166)
↳↳ document| **Document** | No | Información referente al documento de identificación de la persona de contacto
↳↳↳ typeDocument| *String* | No | Tipo de documento (DNI, NIE, Passport o IdentityCard)
↳↳↳ numberDocument| *String* | No | Número de documento
↳ commision| **Commission** | No | Información sobre las comisiones aplicadas en la reserva
↳↳ serviceCommission[]| *ServiceCommission* | No | Información específica sobre un servicio reservado
↳↳↳ serviceId| *String* | Sí | Identificador que identifica la habitación reservada
↳↳↳ commissionAmount| *Double* | No| Importe de la comisión aplicada
↳↳↳ commissionPercentage| *Double* | No | Porcentage de la comisión aplicada
↳ hotelCode| *Integer* | Sí | Código de hotel
↳ currencyCode| *String* | Sí | Código de divisa (Códigos ISO 4217)
↳ bookingRoom[]| **BookingRoom** | Sí | Información de habitación de hotel reservada
↳↳ @id| *String* | Sí | Identificador de la habitación
↳↳ checkIn| *Date* | Sí | Fecha de entrada (dd/MM/yyy)
↳↳ checkOut| *Date* | Sí | Fecha de salida (dd/MM/yyy)
↳↳ status| *Enum* | Sí | Estado de la reserva (Confirmed, Cancelled, OnRequest)
↳↳ roomCode| *String* | Sí | Código de habitación
↳↳ mealPlanCode| *String* | Sí | Código de régimen alimenticio
↳↳ amount| *Double* | Sí | Importe de la habitación reservada (#.##)
↳↳ totalRoomAmount| *Double* | No | Coste de la habitación: Precio Hab x Noches + Suplementos Obligatorios (#.##)
↳↳ commissionRoomAmount| *Double* | No | Comisión de la habitación: Coste de la habitación * Porcentaje comisión (#.##)
↳↳ netRoomAmount| *Double* | No | Coste neto de la habitación: Coste de la habitación - Comisión habitación (#.##)
↳↳ amountRoomToInvoice| *Double* | No | Coste a facturar de la habitación: Amount - porcentaje de comisión (#.##)
↳↳ roomRateDay[]| **RoomRateDay** | Sí | Desglose de reserva por día, informando la tarifa y precio correspondiente a cada día de la estancia
↳↳↳ day| *Date* | Sí | Día de la estancia (dd/MM/yyy)
↳↳↳ rateCode| *String* | No | Código de tarifa
↳↳↳ amount| *String* | Sí | Importe del día
↳↳ guest[]| **Guest** | Sí | Pasajero de la reserva
↳↳↳ @id| *Integer* | Sí | Identificador del pasajero
↳↳↳ name| *String* | Sí | Nombre del pasajero. Si el nombre no ha sido informado en la reserva, se substituirá por el nombre de la persona de contacto
↳↳↳ gender| *String* | No | Género del pasajero ('Male': Hombre, 'Female': Mujer y 'Undefined': Indefinido). 
↳↳↳ type| *Enum* | Sí | Tipo (Adult, Child, Baby)
↳↳↳ amount| *Double* | Sí | Importe correspondiente al pasajero
↳↳↳ birthDate| *Date* | No | Fecha de nacimiento
↳↳↳ nationality[]| *String* | No | Nacionalidad del huésped
↳↳↳ document[]| *Document* | No | Información relativa a los documentos aportados por el huésped
↳↳↳↳ typeDocument| *String* | No | Tipo del documento aportado ('D': Dni, 'E': Nie y 'P':Pasaporte)
↳↳↳↳ numberDocument| *String* | No | Número del documento aportado
↳↳↳↳ expeditionDate| *Date* | No | Fecha de expedición del documento (dd/MM/yyyy)
↳↳↳↳ expiryDocument| *Date* | No | Fecha de caducidad del documento (dd/MM/yyyy)
↳↳↳ contact[]| *ContactAddress* | No | Información relativa a los datos de contacto aportados por el huésped
↳↳↳↳ phone| *String* | No | Teléfono aportado por el huésped
↳↳↳↳ email| *String* | No | Email aportado por el huésped
↳↳↳↳ addressText| *String* | No | Dirección aportada por el huésped
↳↳↳↳ postalCode| *String* | No | Código postal
↳↳ cancellationData| **CancellationData** | No| Gastos de cancelación de la habitación
↳↳↳ cancelPenaltyPolicy[]| *CancelPenaltyPolicy* | Sí | Gasto de cancelación aplicable a partir de una fecha de cancelación
↳↳↳↳ @id| *Integer* | Sí | Identificador del gasto de cancelación
↳↳↳↳ date| *Calendar* | Sí | Elemento que contiene la fecha a partir de la cual se aplican los gastos de cancelación
↳↳↳↳ timeRelevant| *Boolean* | Sí | Elemento que indica si las horas en la fecha de cancelación son relevantes o se debe tomar sólo la fecha como dato significativo
↳↳↳↳ amount| *Double* | Sí | Importe que se aplicará al cancelar la habitación
↳↳↳↳ description| *String* | No | Descripción de los gastos de cancelación
↳ bookingSupplement[]| **BookingSupplement** | No | Información de suplemento reservado
↳↳ code| *String* | Sí | Código del suplemento opcional reservado
↳↳ name| *String* | Sí | Nombre del suplemento opcional reservado
↳↳ typeSupplement| *String* | Sí | Indica el tipo de suplemento que tratamos (Mandatory / Optional / SalePolicy)
↳↳ internalName| *String* | No | Nombre interno de la política comercial (suplementos del tipo SP) aplicada en la reserva.
↳↳ description| *String* | No | Descripción detallada del suplemento opcional reservado
↳↳ checkIn| *Date* | No | Fecha de inicio del suplemento (dd/MM/yyy)
↳↳ checkOut| *Date* | No | Fecha de fin del suplemento (dd/MM/yyy)
↳↳ bookingRoomId| *String* | No | Identificador de la habitación reservada, si el suplemento referencia a una habitación en concreto
↳↳ guestId[]| *Integer* | No | Identificador del pasajero al que se hace referencia, si el suplemento referencia a un pasajero/os en concreto
↳↳ amount| *Double* | Sí | Importe total del suplemento opcional reservado
↳↳ commissionSupplementAmount| *Double* | No | Comisión del suplemento (#.##)
↳↳ netSupplementAmount| *Double* | No | Coste neto del suplemento: Valor total del Suplemento -  Importe de Comisión del suplemento (#.##)
↳↳ promotionalCode[]| *String* | No | Indica los códigos aplicados en el suplemento en cuestión
↳↳ mandatory| *Boolean* | Sí | Indica si el suplemento es obligatorio (true) o opcional (false)
↳↳ detail| **SupplementDetail** | No | Indica los detalles del suplemento.
↳↳↳ shuttleDetail| **SupplementShuttleDetail** | No | Indica los detalles de transporte (siempre y cuando el suplemento sea de tipo TRF)
↳↳↳↳ mailTransferProvider| *String* | No | Indica el email del proveedor del transfer
↳↳↳↳ arrivalFlight| **ShuttleFlightDetail** | No | Indica los detalles del vuelo de llegada
↳↳↳↳↳ airportCode| *String* | No | Indica el código del aeropuerto
↳↳↳↳↳ airportName| *String* | No | Indica el nombre del aeropuerto
↳↳↳↳↳ companyCode| *String* | No | Indica el código de la compañía que emite el billete
↳↳↳↳↳ companyName| *String* | No | Indica el nombre de la compañía que emite el billete
↳↳↳↳↳ flightNumber| *String* | No | Indica el número de vuelo
↳↳↳↳↳ flightTime| *Calendar* | No | Indica la fecha y hora del vuelo (dd/MM/yyyy HH:mm)
↳↳↳↳ departureFlight| **ShuttleFlightDetail** | No | Indica los detalles del vuelo de salida
↳↳↳↳↳ airportCode| *String* | No | Indica el código del aeropuerto
↳↳↳↳↳ airportName| *String* | No | Indica el nombre del aeropuerto
↳↳↳↳↳ companyCode| *String* | No | Indica el código de la compañía que emite el billete
↳↳↳↳↳ companyName| *String* | No | Indica el nombre de la compañía que emite el billete
↳↳↳↳↳ flightNumber| *String* | No | Indica el número de vuelo
↳↳↳↳↳ flightTime| *Calendar* | No | Indica la fecha y hora del vuelo (dd/MM/yyyy HH:mm)
↳ bookingPayment| **BookingPayment** | No | Información del pago de la reserva<sup>1</sup>
↳↳ modality| *Enum* | Sí | Modalidad de pago (Establishment / Inmediate / Deferred / CancelPenalty / Instalment / ExternManagement)
↳↳ type| *Enum* | Sí | Tipo de pago (BankTransfer / Card / VirtualCard / PrepaidCard / WarrantyCard / Cash / Cheque / Credit / Voucher / ExternalManaged / PinPad)
↳↳ otaType| *Enum* | No | Tipo de pago OTA (PA: Agency prepaid/PC: Customer prepaid/PD: Customer payment/PB: Voucher Payment/FC: Credit invoice/PM: Loyalty points + money PU: Loyalty Points/SC: By contract/SD: OTA Virtual card/NN: TPV pending/AW: Prepaid TPV with AMEX/VW: Prepaid TPV NO AMEX)
↳↳ status| *Enum* | Sí | Estado de pago (Pending / Ok / Error / Cancelled / Inapplicable)
↳↳ description| *String* | No | Contiene el nombre comercial asignado a a la modalidad de pago
↳ paymentCardDetail| **PaymentCardDetail** | No | Detalles de la tarjeta que ha realizado el pago (sólo viene informado si bookingPayment.type es Card, PrepaidCard, VirtualCard o WarrantyCard)
↳↳ holder| *String* | Sí | Nombre del titular de la tarjeta
↳↳ number| *String* | Sí | Número de la tarjeta
↳↳ expiryDate| *Date* | Sí | Fecha de caducidad (dd/MM/yyy)
↳↳ securityCode| *String* | No | Código de seguridad (cvc2)
↳ paymentDetail[]| **PaymentDetail** | No | Log con todos los pagos realizados en la reserva
↳↳ action| *String* | Sí | Tipo de operación (charge / refund)
↳↳ paymentStatus| *String* | Sí | Estado del pago (Pending / Ok / Error / Cancelled / Inapplicable)
↳↳ type| *String* | Sí | Código del tipo de pago (Establishment / Inmediate / Deferred / CancelPenalty / Instalment / ExternManagement)
↳↳ otaType| *Enum* | No | Tipo de pago OTA (PA: Agency prepaid/PC: Customer prepaid/PD: Customer payment/PB: Voucher Payment/FC: Credit invoice/PM: Loyalty points + money PU: Loyalty Points/SC: By contract/SD: OTA Virtual card/NN: TPV pending/AW: Prepaid TPV with AMEX/VW: Prepaid TPV NO AMEX)
↳↳ date| *Calendar* | Sí | Fecha de la transacción
↳↳ amount| *Double* | Sí | Importe (#.##)
↳↳↳ cardDetail| *PaymentDetailCardDetail* | No | Detalle pago con tarjeta de crédito
↳↳↳↳ status| *String* | Sí | Estado del pago (Pending / Ok / Error / Cancelled / Inapplicable)
↳↳↳↳ card| *CreditCard* | Sí | Información de la tarjeta de crédito
↳↳↳↳↳ cardTypeCode| *String* | No | Código de la tarjeta de crédito
↳↳↳↳↳ cardTypeDescription| *String* | No | Nombre del tipo de tarjeta de crédito
↳↳↳↳↳ holder| *String* | Sí | Nombre del titular de la tarjeta
↳↳↳↳↳ number| *String* | Sí | Número de la tarjeta
↳↳↳↳↳ hashedValue| *String* | No | Número de la tarjeta
↳↳↳↳↳ seriesCode| *String* | No | CVC
↳↳↳↳↳ expiryDate| *Date* | Sí | Fecha de caducidad (dd/MM/yyy)
↳↳↳↳ systemCode| *String* | Sí | Identificador del sistema de pago
↳↳↳↳ reference| *String* | Sí | Localizador de la reserva
↳↳↳↳ authorizedCode| *String* | Sí | Código de autorización
↳↳↳↳ errorDescription| *String* | No | Descripción del error en el pago
↳↳↳ externalManagedDetail| *PaymentExternalManagedDetail* | No | Datos detallados de un sistema de pago externo, por ejemplo Paypal
↳↳↳↳ externalSystemCode| *String* | Sí | Código del sistema externo
↳↳↳↳ externalReference| *String* | Sí | Referencia externa
↳↳↳↳ status| *String* | Sí | Estado del pago (Pending / Ok / Error / Cancelled / Inapplicable)
↳↳↳ virtualCard| *VirtualCard* | No | Información de la tarjeta virtual
↳↳↳↳ code| *String* | Sí | Código de tarjeta virtual
↳↳↳↳ accountCode| *String* | Sí | Código de la cuenta que gestiona las tarjetas virtuales
↳↳↳↳ authorizedCode| *String* | Sí | Código de autorización del pago
↳↳↳↳ currencyCode| *String* | Sí | Código de divisa asociada al usuario
↳↳↳↳ availableAmount| *String* | Sí | Importe disponible en la cuenta que gestiona las tarjetas virtuales
↳↳↳↳ status| *String* | Sí | Estado de la tarjeta virtual (Active / Inactive / Blocked / Close)
↳↳↳↳ referencePayClient| *String* | Sí | eferencia del pago para el cliente
↳↳↳↳ description| *String* | No | Descripción del elemento
↳↳↳↳ person| *BasePerson* | No | Persona con los datos básicos
↳↳↳↳↳ firstName| *String* | No | Nombre de la persona
↳↳↳↳↳ firstLastName| *String* | No | Primer apellido de la persona
↳↳↳↳↳ secondLastName| *String* | No | Segundo apellido de la persona
↳↳↳↳↳ birthDate| *Date* | No | Fecha de nacimiento
↳↳↳↳ contact| *BaseContact* | No | Contacto con los datos básicos
↳↳↳↳↳ phone| *String* | No | Número de teléfono
↳↳↳↳↳ fax| *String* | No | Número de Fax
↳↳↳↳↳ email| *String* | No | Dirección de e-mail
↳↳↳↳↳ web| *Date* | No | Dirección de la página web
↳↳↳↳ address| *Address* | No | Información de Dirección
↳↳↳↳↳ countryCode| *String* | No | Código del país
↳↳↳↳↳ countryName| *String* | No | Nombre del país
↳↳↳↳↳ state| *String* | No | Estado
↳↳↳↳↳ county| *Date* | No | Condado
↳↳↳↳↳ province| *String* | No | Provincia
↳↳↳↳↳ locationCode| *String* | No | Código de la localidad, ciudad, zona rural
↳↳↳↳↳ locationName| *String* | No | Nombre de la localidad, ciudad, zona rural
↳↳↳↳↳ postalCode| *Date* | No | Código postal
↳↳↳↳ creditCard| *CreditCard* | No | Información de la tarjeta de crédito
↳↳↳↳↳ cardTypeCode| *String* | No | Código de la tarjeta de crédito
↳↳↳↳↳ cardTypeDescription| *String* | No | Nombre del tipo de tarjeta de crédito
↳↳↳↳↳ holder| *String* | Sí | Nombre del titular de la tarjeta
↳↳↳↳↳ number| *String* | Sí | Número de la tarjeta
↳↳↳↳↳ hashedValue| *String* | No | Número de la tarjeta
↳↳↳↳↳ seriesCode| *String* | No | CVC
↳↳↳↳↳ expiryDate| *Date* | Sí | Fecha de caducidad (dd/MM/yyy)
↳↳↳ prepaidCardDetail| *PrepaidCardDetail* | No | Detalle pago con tarjeta de prepago
↳↳↳↳ status| *String* | Sí | Estado del pago (Pending / Ok / Error / Cancelled / Inapplicable)
↳↳↳↳ systemCode| *String* | No | Identificador del sistema de pago
↳↳↳↳ card| *CreditCard* | Sí | Datos de la tarjeta prepago
↳↳↳↳↳ cardTypeCode| *String* | No | Código de la tarjeta de crédito
↳↳↳↳↳ cardTypeDescription| *String* | No | Nombre del tipo de tarjeta de crédito
↳↳↳↳↳ holder| *String* | Sí | Nombre del titular de la tarjeta
↳↳↳↳↳ number| *String* | Sí | Número de la tarjeta
↳↳↳↳↳ hashedValue| *String* | No | Número de la tarjeta
↳↳↳↳↳ seriesCode| *String* | No | CVC
↳↳↳↳↳ expiryDate| *Date* | Sí | Fecha de caducidad (dd/MM/yyy)
↳↳↳ warrantyCardDetail| *WarrantyCardDetail* | No | Detalle pago con tarjeta de garantía
↳↳↳↳ status| *String* | Sí | Estado del pago (Pending / Ok / Error / Cancelled / Inapplicable)
↳↳↳↳ systemCode| *String* | No | Identificador del sistema de pago
↳↳↳↳ card| *CreditCard* | Sí | Datos de la tarjeta de garantía
↳↳↳↳↳ cardTypeCode| *String* | No | Código de la tarjeta de crédito
↳↳↳↳↳ cardTypeDescription| *String* | No | Nombre del tipo de tarjeta de crédito
↳↳↳↳↳ holder| *String* | Sí | Nombre del titular de la tarjeta
↳↳↳↳↳ number| *String* | Sí | Número de la tarjeta
↳↳↳↳↳ hashedValue| *String* | No | Número de la tarjeta
↳↳↳↳↳ seriesCode| *String* | No | CVC
↳↳↳↳↳ expiryDate| *Date* | Sí | Fecha de caducidad (dd/MM/yyy)
↳ saleRules| **SaleRules** | No | Elemento que contiene las reglas de ventas cargadas en Hotetec, y que se han aplicado en la reserva.
↳↳ bookingRoom[]| *Room* | No | Elemento que contiene las reglas de venta aplicadas en una habitación en concreto.
↳↳↳ @id| *Integer* | Sí | Identificador de la habitación
↳↳↳ saleRulesByDay[]| *SaleRulesByDay* | Sí | Elemento que contiene un desglose de las reglas de venta aplicadas por día.
↳↳↳↳ day| *Date* | Sí | Día aplicado
↳↳↳↳ saleRule[]| *SaleRule* | No | Elemento que contiene una regla de venta aplicada en el día concreto.
↳↳↳↳↳ name| *String*| Sí | Nombre de la regla de venta.
↳↳↳↳↳ amount| *String*| No | Importe cargado en la regla de venta aplicada.
↳↳↳↳↳ percentage| *String*| No | Percentaje cargado en la regla de venta aplicada.

<aside class="notice">
<sup>1</sup>&nbsp;&nbsp;&nbsp; Nota: 
<ul>
   <li>La reserva revendida vendrá identificada con una propiedad a nivel de customData: *SUPPLIER.Tripresale.Resaled*</li>
</ul>
</aside>