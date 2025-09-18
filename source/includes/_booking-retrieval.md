# BookingRetrieval

> Ejemplo BookingRetrievalRequest para recuperar una reserva en particular
&nbsp;&nbsp;<span class="postman-button">[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/495ff7995b655b745365)</span>

````xml
<?xml version="1.0" encoding="UTF-8"?>
<BookingRetrievalRequest>
    <credentials>
        <systemCode>SFO</systemCode>
        <vendorCode>FOO</vendorCode>
        <user>BAR</user>
        <password>FOOBAR</password>
    </credentials>   
    <hotelCode>1234</hotelCode>
    <reference>EPL10032017140800-SALE</reference>
</BookingRetrievalRequest>
````

````json
{
  "BookingRetrievalRequest": {
    "credentials": {
      "systemCode": "SFO",
      "vendorCode": "FOO",
      "user": "BAR",
      "password": "FOOBAR"
    },
    "hotelCode": "1234",
    "reference": "EPL10032017140800-SALE"
  }
}
````

> Ejemplo BookingRetrievalRequest para recuperar una reserva a partir del localizador externo
&nbsp;&nbsp;<span class="postman-button">[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/495ff7995b655b745365)</span>

````xml
<?xml version="1.0" encoding="UTF-8"?>
<BookingRetrievalRequest>
    <credentials>
        <systemCode>SFO</systemCode>
        <vendorCode>FOO</vendorCode>
        <user>BAR</user>
        <password>FOOBAR</password>
    </credentials>   
    <hotelCode>1234</hotelCode>
    <clientReference>23564378</clientReference>
</BookingRetrievalRequest>
````

````json
{
  "BookingRetrievalRequest": {
    "credentials": {
      "systemCode": "SFO",
      "vendorCode": "FOO",
      "user": "BAR",
      "password": "FOOBAR"
    },
    "hotelCode": "1234",
    "clientReference": "23564378"
  }
}
````

> Ejemplo BookingRetrievalRequest para para recuperar las reservas de un hotel en un determinado rango de fechas (creadas, canceladas o modificadas)
&nbsp;&nbsp;<span class="postman-button">[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/495ff7995b655b745365)</span>

````xml
<?xml version="1.0" encoding="UTF-8"?>
<BookingRetrievalRequest>
    <credentials>
        <systemCode>SFO</systemCode>
        <vendorCode>FOO</vendorCode>
        <user>BAR</user>
        <password>FOOBAR</password>
    </credentials>   
    <hotelCode>1234</hotelCode>
    <dateFrom>10/03/2017 14:30</dateFrom>
    <dateTo>10/03/2017 15:00</dateTo>
</BookingRetrievalRequest>
````

````json
{
  "BookingRetrievalRequest": {
    "credentials": {
      "systemCode": "SFO",
      "vendorCode": "FOO",
      "user": "BAR",
      "password": "FOOBAR"
    },
    "hotelCode": "1234",
    "dateFrom": "10/03/2017 14:30",
    "dateTo": "10/03/2017 15:00"
  }
}
````

> Ejemplo respuesta BookingRetrievalResponse procesada correctamente
La reserva recuperada contiene dos habitaciones: 1 doble + 1 individual

````xml
<?xml version="1.0" encoding="UTF-8"?>
<BookingRetrievalResponse>
	<sessionId>SUP#FOO#123456789</sessionId>
	<booking>
		<reference>EPL10032017140800-SALE</reference>
		<creationDate>10/03/2017 14:15</creationDate>
		<modificationDate>10/03/2017 14:17</modificationDate>
		<country>ES</country>
		<checkIn>15/04/2017</checkIn>
		<checkOut>18/04/2017</checkOut>
        <numPax>4</numPax>
		<status>Confirmed</status>
		<amount>550.00</amount>
		<amountToInvoice>625.25</amountToInvoice>
		<bookingClient>
			<clientCode>EPL</clientCode>
			<clientName>Europlayas</clientName>
			<fiscalClientName>Europlayas S.L.</fiscalClientName>
			<addressClient>Parc Bit, 14</addressClient>
			<postalClientCode>07001</postalClientCode>
			<countryClient>ES</countryClient>
			<cifClient>A00000000</cifClient>
			<emailClient>europlayas@test.com</emailClient>
			<clientReference>AA45645D55</clientReference>
		</bookingClient>
		<endCustomer>
			<name>Elena Ballester</name>
			<firstName>Elena</firstName>
			<lastName>Ballester</lastName>
			<mail>elena_ballester1234@mail.com</mail>
			<phone>003466667788</phone>
			<document>
				<typeDocument>Passport</typeDocument>
				<numberDocument>A123456789</numberDocument>
			</document>
			<labels>
                <label>ORO</label>
                <label>REPETIDOR</label>
            </labels>
			<language>ES</language>
		</endCustomer>
		<commission>
			<serviceCommission>
				<serviceId>1</serviceId>
				<commissionAmount>0</commissionAmount>
				<commissionPercentage>0</commissionPercentage>
			</serviceCommission>
			<serviceCommission>
				<serviceId>2</serviceId>
				<commissionAmount>0</commissionAmount>
				<commissionPercentage>0</commissionPercentage>
			</serviceCommission>
		</commission>
		<hotelCode>1234</hotelCode>
		<currencyCode>EUR</currencyCode>
		<bookingRoom id="1">
			<checkIn>15/04/2017</checkIn>
			<checkOut>17/04/2017</checkOut>
			<status>Confirmed</status>
			<roomCode>DBL#STD</roomCode>
			<internalRoomName>Nombre interno de la habitacion DBL#STD</internalRoomName>
			<mealPlanCode>BB</mealPlanCode>
			<amount>350.00</amount>
			<totalRoomAmount>350.00</totalRoomAmount>
			<commissionRoomAmount>0.0</commissionRoomAmount>
			<netRoomAmount>350.00</netRoomAmount>
			<amountRoomToInvoice>350.00</amountRoomToInvoice>
			<roomRateDay>
				<day>15/04/2017</day>
				<rateCode>BASE</rateCode>
				<rateName>BASE VERANO</rateName>
				<internalRateName>BASEVER</internalRateName>
				<amount>116.67</amount>
			</roomRateDay>
			<roomRateDay>
				<day>16/04/2017</day>
				<rateCode>BASE</rateCode>
				<rateName>BASE VERANO</rateName>
				<internalRateName>BASEVER</internalRateName>
				<amount>116.67</amount>
			</roomRateDay>
			<roomRateDay>
				<day>17/04/2017</day>
				<rateCode>BASE</rateCode>
				<rateName>BASE VERANO</rateName>
				<internalRateName>BASEVER</internalRateName>
				<amount>116.67</amount>
			</roomRateDay>
			<guest id="1">
				<type>Adult</type>
				<name>Juan Ballester</name>
				<firstName>Juan</firstName>
				<lastName>Ballester</lastName>
				<birthDate>19/06/1993</birthDate>
				<amount>175.00</amount>
				<age>33</age>
			</guest>
			<guest id="2">
				<type>Adult</type>
				<name>Elena Ballester</name>
				<firstName>Elena</firstName>
				<lastName>Ballester</lastName>
				<birthDate>23/08/1993</birthDate>
				<amount>175.00</amount>
				<age>33</age>
			</guest>
			<numPax>2</numPax>
			<cancellationData>
				<cancelPenaltyPolicy id="5">
					<date>18/05/2023 00:00</date>
					<timeRelevant>false</timeRelevant>
					<amount>625.25</amount>
				</cancelPenaltyPolicy>
			</cancellationData>
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
					<key>PriceType</key>
					<value>PVP</value>
				</customData>
				<customData>
					<key>ClientType</key>
					<value>A</value>
				</customData>
			</extraCustomData>
		</bookingRoom>
		<bookingRoom id="2">
			<checkIn>15/04/2017</checkIn>
			<checkOut>17/04/2017</checkOut>
			<status>Confirmed</status>
			<roomCode>SGL#STD</roomCode>
			<totalRoomAmount>150.00</totalRoomAmount>
			<commissionRoomAmount>0.0</commissionRoomAmount>
			<netRoomAmount>150.00</netRoomAmount>
			<amountRoomToInvoice>150.00</amountRoomToInvoice>
			<internalRoomName>Nombre interno de la habitacion SGL#STD</internalRoomName>
			<mealPlanCode>BB</mealPlanCode>
			<amount>150.00</amount>
			<roomRateDay>
				<day>15/04/2017</day>
				<rateCode>BASE</rateCode>
				<rateName>BASE VERANO</rateName>
				<internalRateName>BASEVER</internalRateName>
				<amount>50.00</amount>
			</roomRateDay>
			<roomRateDay>
				<day>16/04/2017</day>
				<rateCode>BASE</rateCode>
				<rateName>BASE VERANO</rateName>
				<internalRateName>BASEVER</internalRateName>
				<amount>50.00</amount>
			</roomRateDay>
			<roomRateDay>
				<day>17/04/2017</day>
				<rateCode>BASE</rateCode>
				<rateName>BASE VERANO</rateName>
				<internalRateName>BASEVER</internalRateName>
				<amount>50.00</amount>
			</roomRateDay>
			<guest id="3">
				<type>Adult</type>
				<name>Elena Ballester</name>
				<firstName>Elena</firstName>
				<lastName>Ballester</lastName>
				<birthDate>23/08/1993</birthDate>
				<gender>Female</gender>
				<amount>100.00</amount>
				<age>33</age>
			</guest>
			<guest id="4">
				<type>Child</type>
				<name>Maria Ballester</name>
				<firstName>Maria</firstName>
				<lastName>Maria</lastName>
				<birthDate>25/03/2015</birthDate>
				<gender>Female</gender>
				<amount>50.00</amount>
				<age>33</age>
			</guest>
			<numPax>2</numPax>
		</bookingRoom>
		<bookingSupplement>
			<code>[EtT]Supplement(PpT)DEMOHTT@30621@20054@1@EUR</code>
			<name>PARK - 1</name>
			<typeSupplement>SalePolicy</typeSupplement>
			<internalTypeSupplement>SPS</internalTypeSupplement>
			<description>Suplemento Parking toda la estancia</description>
			<checkIn>15/04/2017</checkIn>
			<checkOut>17/04/2017</checkOut>
			<bookingRoomId>1</bookingRoomId>
			<amount>50.00</amount>
			<mandatory>true</mandatory>
		</bookingSupplement>
		<bookingSupplement>
            <code>[EtT]Supplement(PpT)TESTHTT@53089@21599@1@EUR</code>
            <name>TEST 2 - 1</name>
            <typeSupplement>Optional</typeSupplement>
            <internalTypeSupplement>ESP</internalTypeSupplement>
            <bookingRoomId>1</bookingRoomId>
            <amount>10.0</amount>
            <commissionSupplementAmount>0.0</commissionSupplementAmount>
            <netSupplementAmount>10.0</netSupplementAmount>
            <mandatory>false</mandatory>
        </bookingSupplement>
		<remark>
			<code>Informative</code>
			<from>Hotel</from>
			<to>Client</to>
			<text>Piscina cerrada hasta el 15/04/2017</text>
		</remark>
		<remark>
			<code>Informative</code>
			<from>Client</from>
			<to>Hotel</to>
			<bookingRoomId>2</bookingRoomId>
			<text>Por favor, habitaciones no fumadores</text>
		</remark>
		<remark>
			<code>ArrivalTime</code>
			<from>Client</from>
			<to>Hotel</to>
			<text>12:00</text>
		</remark>
		<bookingPayment>
			<modality>Establishment</modality>
			<internalModalityName>Descripcion interna modalidad de pago</internalModalityName>
			<type>PrepaidCard</type>
			<otaType>PC</otaType>
			<description>Tarjeta de prepago</description>
			<status>Pending</status>
		</bookingPayment>
		    <paymentCardDetail>
		    <holder>John Smith</holder>
		    <number>cust_677b20db-a28b-4e2a-b3e0-da8c19e2fec3#1DCA3173-9DD0-4F2D-8420-266808C0A4EB</number>
		    <expiryDate>01/10/2027</expiryDate>
        </paymentCardDetail>
		<paymentDetail>
			<action>Charge</action>
			<paymentStatus>Ok</paymentStatus>
			<type>ExternalManaged</type>
			<method>Card</method>
			<date>24/01/2019 17:18</date>
			<amount>2635.663</amount>
			<cardDetail>
                <card>
                    <holder>John Smith</holder>
                    <number>5004</number>
                    <expiryDate>01/10/2027</expiryDate>
                </card>
                <systemCode>PNN</systemCode>
                <reference>677b20db-a28b-4e2a-b3e0-da8c19e2fec3</reference>
                <authorizedCode>075128</authorizedCode>
            </cardDetail>
			<breakdown>
				<bookingRoomId>1</bookingRoomId>
				<amount>350.0</amount>
			</breakdown>
			<breakdown>
				<bookingRoomId>2</bookingRoomId>
				<amount>150.0</amount>
			</breakdown>
		</paymentDetail>
		<paymentDetail>
			<action>Charge</action>
			<paymentStatus>Pending</paymentStatus>
			<type>PrepaidCard</type>
			<method>Card</method>
			<otaType>PC</otaType>
			<date>23/07/2019 09:42</date>
			<amount>2635.66</amount>
			<prepaidCardDetail>
				<status>Pending</status>
				<card>
					<cardTypeCode>Visa</cardTypeCode>
					<holder>Elena Ballester</holder>
					<number>4111111111111111</number>
					<expiryDate>01/01/2020</expiryDate>
					<securityCode>123</securityCode>
				</card>
			</prepaidCardDetail>
			<breakdown>
				<bookingRoomId>1</bookingRoomId>
				<amount>350.0</amount>
			</breakdown>
			<breakdown>
				<bookingRoomId>2</bookingRoomId>
				<amount>150.0</amount>
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
				<key>PriceType</key>
				<value>PVP</value>
			</customData>
			<customData>
				<key>ClientType</key>
				<value>A</value>
			</customData>
		</extraCustomData>
		<saleRules>
			<bookingRoom id="1">
				<saleRulesByDay>
					<day>27/11/2024</day>
					<saleRule>
						<name>EBB PLAYA SUMMER 0.7</name>
						<percentage>-18.0</percentage>
					</saleRule>
				</saleRulesByDay>
			</bookingRoom>
        </saleRules>
	</booking>
</BookingRetrievalResponse>
````

````json
{
  "BookingRetrievalResponse": {
    "sessionId": "SUP#FOO#123456789",
    "booking": {
      "reference": "EPL10032017140800-SALE",
      "creationDate": "10/03/2017 14:15",
      "modificationDate": "10/03/2017 14:17",
      "country": "ES",
      "checkIn": "15/04/2017",
      "checkOut": "18/04/2017",
      "numPax":  "4",
      "status": "Confirmed",
      "amount": 550,
      "amountToInvoice": 625.25,
      "bookingClient": {
        "clientCode": "EPL",
        "clientName": "Europlayas",
        "fiscalClientName": "Europlayas S.L.",
        "addressClient": "Parc Bit, 14",
        "postalClientCode": 7001,
        "countryClient": "ES",
        "cifClient": "A00000000",
        "emailClient": "europlayas@test.com",
        "clientReference": "AA45645D55"
      },
      "endCustomer": {
        "name": "Elena Ballester",
        "firstName": "Elena",
        "lastName": "Ballester",
        "mail": "elena_ballester1234@mail.com",
        "phone": 3466667788,
        "document": {
          "typeDocument": "Passport",
          "numberDocument": "A123456789"
        },
        "labels": {
          "label": [
            "ORO",
            "REPETIDOR"
          ]
        },
        "language": "ES"
      },
      "commission": {
        "serviceCommission": [
          {
            "serviceId": 1,
            "commissionAmount": 0,
            "commissionPercentage": 0
          },
          {
            "serviceId": 2,
            "commissionAmount": 0,
            "commissionPercentage": 0
          }
        ]
      },
      "hotelCode": 1234,
      "currencyCode": "EUR",
      "bookingRoom": [
        {
          "checkIn": "15/04/2017",
          "checkOut": "17/04/2017",
          "status": "Confirmed",
          "roomCode": "DBL#STD",
          "internalRoomName": "Nombre interno de la habitacion DBL#STD",
          "mealPlanCode": "BB",
          "amount": 350,
          "totalRoomAmount": 350,
          "commissionRoomAmount": 0,
          "netRoomAmount": 350,
          "amountRoomToInvoice": 350,
          "roomRateDay": [
            {
              "day": "15/04/2017",
              "rateCode": "BASE",
              "rateName": "BASE VERANO",
              "internalRateName": "BASEVER",
              "amount": 116.67
            },
            {
              "day": "16/04/2017",
              "rateCode": "BASE",
              "rateName": "BASE VERANO",
              "internalRateName": "BASEVER",
              "amount": 116.67
            },
            {
              "day": "17/04/2017",
              "rateCode": "BASE",
              "rateName": "BASE VERANO",
              "internalRateName": "BASEVER",
              "amount": 116.67
            }
          ],
          "guest": [
            {
              "type": "Adult",
              "name": "Juan Ballester",
              "firstName": "Juan",
              "lastName": "Ballester",
              "birthDate": "19/06/1993",
              "amount": 175,
              "age": 33
            },
            {
              "type": "Adult",
              "name": "Elena Ballester",
              "firstName": "Elena",
              "lastName": "Ballester",
              "birthDate": "23/08/1993",
              "amount": 175,
              "age": 33
            }
          ],
          "numPax":  "2",
          "cancellationData": {
            "cancelPenaltyPolicy": {
              "date": "18/05/2023 00:00",
              "timeRelevant": false,
              "amount": 625.25
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
                "key": "PriceType",
                "value": "PVP"
              },
              {
                "key": "ClientType",
                "value": "A"
              }
            ]
          }
        },
        {
          "checkIn": "15/04/2017",
          "checkOut": "17/04/2017",
          "status": "Confirmed",
          "roomCode": "SGL#STD",
          "totalRoomAmount": 150,
          "commissionRoomAmount": 0,
          "netRoomAmount": 150,
          "amountRoomToInvoice": 150,
          "internalRoomName": "Nombre interno de la habitacion SGL#STD",
          "mealPlanCode": "BB",
          "amount": 150,
          "roomRateDay": [
            {
              "day": "15/04/2017",
              "rateCode": "BASE",
              "rateName": "BASE VERANO",
              "internalRateName": "BASEVER",
              "amount": 50
            },
            {
              "day": "16/04/2017",
              "rateCode": "BASE",
              "rateName": "BASE VERANO",
              "internalRateName": "BASEVER",
              "amount": 50
            },
            {
              "day": "17/04/2017",
              "rateCode": "BASE",
              "rateName": "BASE VERANO",
              "internalRateName": "BASEVER",
              "amount": 50
            }
          ],
          "guest": [
            {
              "type": "Adult",
              "name": "Elena Ballester",
              "firstName": "Elena",
              "lastName": "Ballester",
              "birthDate": "23/08/1993",
              "gender": "Female",
              "amount": 100,
              "age": 33
            },
            {
              "type": "Child",
              "name": "Maria Ballester",
              "firstName": "Maria",
              "lastName": "Maria",
              "birthDate": "25/03/2015",
              "gender": "Female",
              "amount": 50,
              "age": 33
            }
          ]
        }
      ],
      "numPax":  "2",
      "bookingSupplement": [
        {
          "code": "[EtT]Supplement(PpT)DEMOHTT@30621@20054@1@EUR",
          "name": "PARK - 1",
          "typeSupplement": "SalePolicy",
          "internalTypeSupplement": "SPS",
          "description": "Suplemento Parking toda la estancia",
          "checkIn": "15/04/2017",
          "checkOut": "17/04/2017",
          "bookingRoomId": 1,
          "amount": 50,
          "mandatory": true
        },
        {
          "code": "[EtT]Supplement(PpT)TESTHTT@53089@21599@1@EUR",
          "name": "TEST 2 - 1",
          "typeSupplement": "Optional",
          "internalTypeSupplement": "ESP",
          "bookingRoomId": 1,
          "amount": 10,
          "commissionSupplementAmount": 0,
          "netSupplementAmount": 10,
          "mandatory": false
        }
      ],
      "remark": [
        {
          "code": "Informative",
          "from": "Hotel",
          "to": "Client",
          "text": "Piscina cerrada hasta el 15/04/2017"
        },
        {
          "code": "Informative",
          "from": "Client",
          "to": "Hotel",
          "bookingRoomId": 2,
          "text": "Por favor, habitaciones no fumadores"
        },
        {
          "code": "ArrivalTime",
          "from": "Client",
          "to": "Hotel",
          "text": "12:00"
        }
      ],
      "bookingPayment": {
        "modality": "Establishment",
        "internalModalityName": "Descripcion interna modalidad de pago",
        "type": "PrepaidCard",
        "otaType": "PC",
        "description": "Tarjeta de prepago",
        "status": "Pending"
      },
      "paymentCardDetail": {
        "holder": "John Smith",
        "number": "cust_677b20db-a28b-4e2a-b3e0-da8c19e2fec3#1DCA3173-9DD0-4F2D-8420-266808C0A4EB",
        "expiryDate": "01/10/2027"
      },
      "paymentDetail": [
        {
          "action": "Charge",
          "paymentStatus": "Ok",
          "type": "ExternalManaged",
		  "method": "Card",
          "date": "24/01/2019 17:18",
          "amount": 2635.663,
          "cardDetail": {
            "card": {
              "holder": "John Smith",
              "number": 5004,
              "expiryDate": "01/10/2027"
            },
            "systemCode": "PNN",
            "reference": "677b20db-a28b-4e2a-b3e0-da8c19e2fec3",
            "authorizedCode": 75128
          },
          "breakdown": [
            {
              "bookingRoomId": 1,
              "amount": 350
            },
            {
              "bookingRoomId": 2,
              "amount": 150
            }
          ]
        },
        {
          "action": "Charge",
          "paymentStatus": "Pending",
          "type": "PrepaidCard",
		  "method": "Card",
          "otaType": "PC",
          "date": "23/07/2019 09:42",
          "amount": 2635.66,
          "prepaidCardDetail": {
            "status": "Pending",
            "card": {
              "cardTypeCode": "Visa",
              "holder": "Elena Ballester",
              "number": 4111111111111111,
              "expiryDate": "01/01/2020",
              "securityCode": 123
            }
          },
          "breakdown": [
            {
              "bookingRoomId": 1,
              "amount": 350
            },
            {
              "bookingRoomId": 2,
              "amount": 150
            }
          ]
        }
      ],
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
            "key": "PriceType",
            "value": "PVP"
          },
          {
            "key": "ClientType",
            "value": "A"
          }
        ]
      },
      "saleRules": {
        "bookingRoom": {
          "saleRulesByDay": {
            "day": "27/11/2024",
            "saleRule": {
              "name": "EBB PLAYA SUMMER 0.7",
              "percentage": -18
            }
          }
        }
      }
    }
  }
}
````

Mensaje utilizado para recuperación de reservas. Se puede recuperar una reserva en particular (filtrando por reference),
o bien las reservas de un hotel creadas, canceladas o modificadas dentro de un rango de fechas.

### BookingRetrievalRequest

Mensaje petición de recuperación de reservas
 
Elemento | Tipo | Obl? |  Descripción
--------- | ----------- | ----------- | -----------
credentials | **Credentials** | Sí |Credenciales de autenticación del usuario (Ver Autenticación)
reference | *String* | No<sup>1</sup> | Localizador de la reserva
clientReference | *String* | No<sup>1</sup> | Localizador externo de la reserva
hotelCode | *Integer* | Sí | Código de hotel
dateFrom | *DateTime* | No<sup>1</sup> | Fecha desde. Devolverá todas las reservas que se hayan creado, cancelado o modificado a partir de esta fecha (dd/MM/yyy HH:mm)
dateTo | *DateTime* | No<sup>1</sup> | Fecha hasta. Devolverá todas las reservas que se hayan creado, cancelado o modificado hasta esta fecha (dd/MM/yyy HH:mm)
notificationStatus | *Enum* | No<sup>1</sup> | Filtro por estado de notificación de reserva (Delivered: Notificada / UnDelivered: No notificada) No<sup>2</sup>

<aside class="notice">
<sup>1</sup>&nbsp;&nbsp;&nbsp;Si no se informa localizador de la reserva (reference), es obligatorio filtrar por fechas y/o estado de notificación (dateFrom/dateTo y/o notificationStatus)
</aside>

<aside class="notice">
<sup>2</sup>&nbsp;&nbsp;&nbsp;Si no se informa, se devolverán todas las reservas sea cual sea su estado. Una reserva se marca como notificada cuando se entrega vía PUSH o bien se devuelve en alguna respuesta BookingRetrievalResponse.
</aside>

### BookingRetrievalResponse

Mensaje respuesta de recuperación de reservas

Elemento | Tipo | Obl? | Descripción
--------- | ----------- | ----------- | -----------
sessionId | *String* | Sí|Identificador de la sesión que ha procesado la transacción
booking[] | **Booking** | No | Información de una reserva de hotel
↳ reference| *String* | Sí | Localizador de la reserva
↳ creationDate| *DateTime* | Sí | Fecha de creación de la reserva (dd/MM/yyy HH:mm)
↳ modificationDate| *DateTime* | No | Fecha de creación de la reserva (dd/MM/yyyy HH:mm). Sólo viene informado cuando es una modificación de reserva
↳ cancellationDate| *DateTime* | No | Fecha de cancelación de la reserva (dd/MM/yyyy HH:mm). Sólo viene informado cuando es una cancelación de reserva
↳ country| *String* | No | Código del país de origen de la reserva (2 letter ISO 3166). Sólo vendrá informado en la reservas propias de Hotetec
↳ checkIn| *Date* | Sí | Fecha de entrada (dd/MM/yyy)
↳ checkOut| *Date* | Sí | Fecha de salida (dd/MM/yyy)
↳ numPax| *Integer* | Sí | Número de pasajeros total de la reserva
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
↳↳ language| *String* | No | Idioma del cliente
↳↳ address| *String* | No | Dirección indicada para el cliente
↳↳ document| **Document** | No | Información referente al documento de identificación de la persona de contacto
↳↳↳ typeDocument| *String* | No | Tipo de documento (DNI, NIE, Passport o IdentityCard)
↳↳↳ numberDocument| *String* | No | Número de documento
↳↳ labels| **Labels** | No | Información referente a las etiquetas asignadas a la persona de contacto
↳↳↳ label[]| *String* | No | Etiqueta asignada a la persona de contacto. Estas etiquetas se definen en el apartado CRM del backOffice de Hotetec.
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
↳↳ internalRoomName | *String* | No | Nombre interno de la habitación
↳↳ mealPlanCode| *String* | Sí | Código de régimen alimenticio
↳↳ amount| *Double* | Sí | Importe de la habitación reservada (#.##)
↳↳ totalRoomAmount| *Double* | No | Coste de la habitación: Precio Hab x Noches + Suplementos Obligatorios (#.##)
↳↳ commissionRoomAmount| *Double* | No | Comisión de la habitación: Coste de la habitación * Porcentaje comisión (#.##)
↳↳ netRoomAmount| *Double* | No | Coste neto de la habitación: Coste de la habitación - Comisión habitación (#.##)
↳↳ amountRoomToInvoice| *Double* | No | Coste a facturar de la habitación: Amount - porcentaje de comisión (#.##)
↳↳ roomRateDay[]| **RoomRateDay** | Sí | Desglose de reserva por día, informando la tarifa y precio correspondiente a cada día de la estancia
↳↳↳ day| *Date* | Sí | Día de la estancia (dd/MM/yyy)
↳↳↳ rateCode| *String* | No | Código de tarifa
↳↳↳ rateName| *String* | No | Nombre de la tarifa
↳↳↳ internalRateName| *String* | No | Nombre interno de la tarifa
↳↳↳ amount| *String* | Sí | Importe del día
↳↳ guest[]| **Guest** | Sí | Pasajero de la reserva
↳↳↳ @id| *Integer* | Sí | Identificador del pasajero
↳↳↳ name| *String* | Sí | Nombre del pasajero. Si el nombre no ha sido informado en la reserva, se substituirá por el nombre de la persona de contacto
↳↳↳ gender| *String* | No | Género del pasajero ('Male': Hombre, 'Female': Mujer y 'Undefined': Indefinido). 
↳↳↳ type| *Enum* | Sí | Tipo (Adult, Child, Baby)
↳↳↳ amount| *Double* | Sí | Importe correspondiente al pasajero
↳↳↳ birthDate| *Date* | No | Fecha de nacimiento
↳↳↳ nationality[]| *String* | No | Nacionalidad del huésped. Se incorpora el código ISO-3166. Ejemplo: <nationality>España (ES)</nationality>.
↳↳↳ document[]| *Document* | No | Información relativa a los documentos aportados por el huésped
↳↳↳ age| *String* | No | Edad del huésped
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
↳↳ numPax| *Integer* | Sí | Número de pasajeros de la habitación
↳↳↳ cancelPenaltyPolicy[]| *CancelPenaltyPolicy* | Sí | Gasto de cancelación aplicable a partir de una fecha de cancelación
↳↳↳↳ @id| *Integer* | Sí | Identificador del gasto de cancelación
↳↳↳↳ date| *Calendar* | Sí | Elemento que contiene la fecha a partir de la cual se aplican los gastos de cancelación
↳↳↳↳ timeRelevant| *Boolean* | Sí | Elemento que indica si las horas en la fecha de cancelación son relevantes o se debe tomar sólo la fecha como dato significativo
↳↳↳↳ amount| *Double* | Sí | Importe que se aplicará al cancelar la habitación
↳↳↳↳ description| *String* | No | Descripción de los gastos de cancelación
↳ extraCustomData | **ExtraCustomData** | No | Indica diversos aspectos de la reserva que no tienen cabida en el formato básico de la reserva.
↳↳ customData[] | *CustomData* | No | Valor de la reserva que no tiene cabida en el formato básico de la misma.
↳↳↳ key | *String* | Sí | Clave que referencia el valor. Ver apartado de ExtraCustomData de la documentación para ver los posibles valores.
↳↳↳ value | *String* | Sí | Valor de la reserva referenciado por el campo 'Key'.
↳ bookingSupplement[]| **BookingSupplement** | No | Información de suplemento reservado
↳↳ code| *String* | No | Código del suplemento opcional reservado. Sólo se informará si se dispone del mismo, lo cual será siempre en las reservas internas, y de forma opcional en las externas.
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
↳ remark| **Remark** | No | Notas de la reserva
↳↳ code| *Enum* | Si | Código de la nota (ArrivalTime, Attachment, Informative, Warning, General)
↳↳ from| *Enum* | Si | Indica quien notifica la nota (Hotel, Client)
↳↳ to| *Enum* | Si | Indica para quien es la nota (Hotel, Client)
↳↳ bookingRoomId| *String* | No | Indica a que habitación hace referencia la nota
↳↳ text| *String* | Si | Texto de la nota
↳↳ customerReference| *String* | No | Referencia del cliente
↳ bookingPayment| **BookingPayment** | No | Información del último pago de la reserva<sup>1</sup>
↳↳ modality| *Enum* | Sí | Modalidad de pago (Establishment / Inmediate / Deferred / CancelPenalty / Instalment / ExternManagement)
↳↳ internalModalityName| *String* | No | Descripcion interna de la modalidad de pago
↳↳ type| *Enum* | Sí | Tipo de pago (BankTransfer / Card / VirtualCard / PrepaidCard / WarrantyCard / Cash / Cheque / Credit / Voucher / ExternalManaged / PinPad)
↳↳ otaType| *Enum* | No | Tipo de pago OTA (PA: Agency prepaid/PC: Customer prepaid/PD: Customer payment/PB: Voucher Payment/FC: Credit invoice/PM: Loyalty points + money PU: Loyalty Points/SC: By contract/SD: OTA Virtual card/NN: TPV pending/AW: Prepaid TPV with AMEX/VW: Prepaid TPV NO AMEX)
↳↳ status| *Enum* | Sí | Estado de pago (Pending / Ok / Error / Cancelled / Inapplicable)
↳↳ description| *String* | No | Contiene el nombre comercial asignado a a la modalidad de pago
↳ paymentCardDetail| **PaymentCardDetail** | No | Detalles de la tarjeta que ha realizado el último pago (sólo viene informado si bookingPayment.type es Card, PrepaidCard, VirtualCard o WarrantyCard)
↳↳ holder| *String* | Sí | Nombre del titular de la tarjeta
↳↳ number| *String* | Sí | Número de la tarjeta tokenizado
↳↳ expiryDate| *Date* | Sí | Fecha de caducidad (dd/MM/yyy)
↳↳ securityCode| *String* | No | Código de seguridad (cvc2)
↳ paymentDetail[]| **PaymentDetail** | No | Log con todos los pagos realizados en la reserva
↳↳ action| *String* | Sí | Tipo de operación (charge / refund)
↳↳ paymentStatus| *String* | Sí | Estado del pago (Pending / Ok / Error / Cancelled / Inapplicable)
↳↳ type| *String* | Sí | Código del tipo de pago (Establishment / Inmediate / Deferred / CancelPenalty / Instalment / ExternManagement)
↳↳ method| *String* | No | Código del método de pago que se usará en el sistema externo (Card / ApplePay / GooglePay / PayPal / ExternalWebsite / Bizum)
↳↳ otaType| *Enum* | No | Tipo de pago OTA (PA: Agency prepaid/PC: Customer prepaid/PD: Customer payment/PB: Voucher Payment/FC: Credit invoice/PM: Loyalty points + money PU: Loyalty Points/SC: By contract/SD: OTA Virtual card/NN: TPV pending/AW: Prepaid TPV with AMEX/VW: Prepaid TPV NO AMEX)
↳↳ date| *Calendar* | Sí | Fecha de la transacción
↳↳ amount| *Double* | Sí | Importe (#.##)
↳↳↳ breakdown[]| **Breakdown** | No | Desglose de pago por habitación
↳↳↳↳ bookingRoomId| *Integer* | Sí | Id de referencia a la habitacion 
↳↳↳↳ amount| *Double* | Sí | Importe del pago (#.##)
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
↳ extraCustomData | **ExtraCustomData** | No | Indica diversos aspectos de la reserva que no tienen cabida en el formato básico de la reserva.
↳↳ customData[] | *CustomData* | No | Valor de la reserva que no tiene cabida en el formato básico de la misma.
↳↳↳ key | *String* | Sí | Clave que referencia el valor. Ver apartado de ExtraCustomData de la documentación para ver los posibles valores.
↳↳↳ value | *String* | Sí | Valor de la reserva referenciado por el campo 'Key'.
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
<sup>1</sup>&nbsp;&nbsp;&nbsp; Ejemplos: 
<ul>
   <li>Pago con tarjeta de garantía, pendiente de cobro, a cobrar en establecimiento. modality: Establishment, type: WarrantyCard, status: Pending</li>
   <li>Pago inmediato, cobrado a traves de una pasarela de pago externa. modality: Inmediate, type: ExternalManaged, status: Ok</li>
   <li>Pago a crédito, acordado con la agencia. modality: ExternManagement, type: Credit, status: Inapplicable</li>
</ul>
</aside>
