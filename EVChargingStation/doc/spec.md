Entity: EVChargingStation  
=========================  
[Open License](https://github.com/smart-data-models//dataModel.Transportation/blob/master/EVChargingStation/LICENSE.md)  
[document generated automatically](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
Global description: **EV Charging Station**  

## List of properties  

- `acceptedPaymentMethod`: Type(s) of charge when using this station. Enum:'ByBankTransferInAdvance, ByInvoice, Cash, CheckInAdvance, COD, DirectDebit, GoogleCheckout, PayPal, PaySwarm'  - `address`: The mailing address  - `allowedVehicleType`: Vehicle type(s) which can be charged. Enum:'bicycle, bus, car, caravan, motorcycle, motorscooter, truck'   - `alternateName`: An alternative name for this item  - `amperage`: The total amperage offered by the charging station.  - `areaServed`: The geographic area where a service or offered item is provided  - `availableCapacity`: The number of vehicles which currently can be charged. It must lower or equal than `capacity`.  - `capacity`: The total number of vehicles which can be charged at the same time. The total number of sockets can be higher.   - `chargeType`: Type(s) of charge when using this station. Enum:'annualPayment, flat, free, monthlyPayment, other'  - `contactPoint`: Charging station contact point  - `dataProvider`: A sequence of characters identifying the provider of the harmonised data entity.  - `dateCreated`: Entity creation timestamp. This will usually be allocated by the storage platform.  - `dateModified`: Timestamp of the last modification of the entity. This will usually be allocated by the storage platform.  - `description`: A description of this item  - `id`: Unique identifier of the entity  - `location`: Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon  - `name`: The name of this item.  - `network`: The name of the Network, with that the operator cooperates.   - `openingHours`: Opening hours of the charging station.   - `operator`: Charging station's operator.   - `owner`: A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)  - `seeAlso`: list of uri pointing to additional resources about the item  - `socketNumber`: The total number of sockets offered by this charging station  - `socketType`: The type of sockets offered by this station. Enum:'Caravan_Mains_Socket, CHAdeMO, CCS/SAE, Dual_CHAdeMO, Dual_J-1772, Dual_Mennekes, J-1772, Mennekes, Other, Tesla, Type2, Type3, Wall_Euro'  - `source`: A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object.  - `status`: Status of the charging station. Enum:'almostEmpty, almostFull, empty, full, outOfService, withIncidence, working'. Or any other application-specific.  - `type`: NGSI Entity type. It has to be EVChargingStation  - `voltage`: The total voltage offered by the charging station    
Required properties  
- `allowedVehicleType`  - `capacity`  - `id`  - `socketType`  - `type`    
A public charging station supplying energy to electrical vehicles. The charge time depends on the maximum power output of the station, the number of vehicles currently charging and the current battery level.  
## Data Model description of properties  
Sorted alphabetically (click for details)  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
EVChargingStation:    
  description: 'EV Charging Station'    
  properties:    
    acceptedPaymentMethod:    
      description: 'Type(s) of charge when using this station. Enum:''ByBankTransferInAdvance, ByInvoice, Cash, CheckInAdvance, COD, DirectDebit, GoogleCheckout, PayPal, PaySwarm'''    
      items:    
        enum:    
          - ByBankTransferInAdvance    
          - ByInvoice    
          - Cash    
          - CheckInAdvance    
          - COD    
          - DirectDebit    
          - GoogleCheckout    
          - PayPal    
          - PaySwarm    
        type: string    
      minItems: 1    
      type: Property    
      uniqueItems: true    
      x-ngsi:    
        model: https://schema.org/Text    
    address:    
      description: 'The mailing address'    
      properties:    
        addressCountry:    
          description: 'Property. The country. For example, Spain. Model:''https://schema.org/addressCountry'''    
          type: string    
        addressLocality:    
          description: 'Property. The locality in which the street address is, and which is in the region. Model:''https://schema.org/addressLocality'''    
          type: string    
        addressRegion:    
          description: 'Property. The region in which the locality is, and which is in the country. Model:''https://schema.org/addressRegion'''    
          type: string    
        postOfficeBoxNumber:    
          description: 'Property. The post office box number for PO box addresses. For example, 03578. Model:''https://schema.org/postOfficeBoxNumber'''    
          type: string    
        postalCode:    
          description: 'Property. The postal code. For example, 24004. Model:''https://schema.org/https://schema.org/postalCode'''    
          type: string    
        streetAddress:    
          description: 'Property. The street address. Model:''https://schema.org/streetAddress'''    
          type: string    
      type: Property    
      x-ngsi:    
        model: https://schema.org/address    
    allowedVehicleType:    
      description: 'Vehicle type(s) which can be charged. Enum:''bicycle, bus, car, caravan, motorcycle, motorscooter, truck'' '    
      items:    
        enum:    
          - bicycle    
          - bus    
          - car    
          - caravan    
          - motorcycle    
          - motorscooter    
          - truck    
        type: string    
      minItems: 1    
      type: Property    
      uniqueItems: true    
      x-ngsi:    
        model: http://schema.org/Text    
    alternateName:    
      description: 'An alternative name for this item'    
      type: Property    
    amperage:    
      description: 'The total amperage offered by the charging station.'    
      minimum: 0    
      type: Property    
      x-ngsi:    
        model: http://schema.org/Number    
        units: 'Ampers (A)'    
    areaServed:    
      description: 'The geographic area where a service or offered item is provided'    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Text    
    availableCapacity:    
      description: 'The number of vehicles which currently can be charged. It must lower or equal than `capacity`.'    
      minimum: 0    
      type: Property    
      x-ngsi:    
        model: http://schema.org/Number    
    capacity:    
      description: 'The total number of vehicles which can be charged at the same time. The total number of sockets can be higher. '    
      minimum: 1    
      type: Property    
      x-ngsi:    
        model: http://schema.org/Number    
    chargeType:    
      description: 'Type(s) of charge when using this station. Enum:''annualPayment, flat, free, monthlyPayment, other'''    
      items:    
        enum:    
          - annualPayment    
          - flat    
          - free    
          - monthlyPayment    
          - other    
        type: string    
      minItems: 1    
      type: Property    
      uniqueItems: true    
      x-ngsi:    
        model: https://schema.org/Text    
    contactPoint:    
      description: 'Charging station contact point'    
      type: Property    
      x-ngsi:    
        model: https://schema.org/contactPoint.    
    dataProvider:    
      description: 'A sequence of characters identifying the provider of the harmonised data entity.'    
      type: Property    
    dateCreated:    
      description: 'Entity creation timestamp. This will usually be allocated by the storage platform.'    
      format: date-time    
      type: Property    
    dateModified:    
      description: 'Timestamp of the last modification of the entity. This will usually be allocated by the storage platform.'    
      format: date-time    
      type: Property    
    description:    
      description: 'A description of this item'    
      type: Property    
    id:    
      anyOf: &evchargingstation_-_properties_-_owner_-_items_-_anyof    
        - description: 'Property. Identifier format of any NGSI entity'    
          maxLength: 256    
          minLength: 1    
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
          type: string    
        - description: 'Property. Identifier format of any NGSI entity'    
          format: uri    
          type: string    
      description: 'Unique identifier of the entity'    
      type: Property    
    location:    
      description: 'Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon'    
      oneOf:    
        - description: 'Geoproperty. Geojson reference to the item. Point'    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                type: number    
              minItems: 2    
              type: array    
            type:    
              enum:    
                - Point    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON Point'    
          type: object    
        - description: 'Geoproperty. Geojson reference to the item. LineString'    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  type: number    
                minItems: 2    
                type: array    
              minItems: 2    
              type: array    
            type:    
              enum:    
                - LineString    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON LineString'    
          type: object    
        - description: 'Geoproperty. Geojson reference to the item. Polygon'    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  items:    
                    type: number    
                  minItems: 2    
                  type: array    
                minItems: 4    
                type: array    
              type: array    
            type:    
              enum:    
                - Polygon    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON Polygon'    
          type: object    
        - description: 'Geoproperty. Geojson reference to the item. MultiPoint'    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  type: number    
                minItems: 2    
                type: array    
              type: array    
            type:    
              enum:    
                - MultiPoint    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON MultiPoint'    
          type: object    
        - description: 'Geoproperty. Geojson reference to the item. MultiLineString'    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  items:    
                    type: number    
                  minItems: 2    
                  type: array    
                minItems: 2    
                type: array    
              type: array    
            type:    
              enum:    
                - MultiLineString    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON MultiLineString'    
          type: object    
        - description: 'Geoproperty. Geojson reference to the item. MultiLineString'    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  items:    
                    items:    
                      type: number    
                    minItems: 2    
                    type: array    
                  minItems: 4    
                  type: array    
                type: array    
              type: array    
            type:    
              enum:    
                - MultiPolygon    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON MultiPolygon'    
          type: object    
      type: Geoproperty    
    name:    
      description: 'The name of this item.'    
      type: Property    
    network:    
      description: 'The name of the Network, with that the operator cooperates. '    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Text    
    openingHours:    
      description: 'Opening hours of the charging station. '    
      type: Property    
      x-ngsi:    
        model: http://schema.org/openingHours    
    operator:    
      description: 'Charging station''s operator. '    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Text    
    owner:    
      description: 'A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)'    
      items:    
        anyOf: *evchargingstation_-_properties_-_owner_-_items_-_anyof    
        description: 'Property. Unique identifier of the entity'    
      type: Property    
    seeAlso:    
      description: 'list of uri pointing to additional resources about the item'    
      oneOf:    
        - items:    
            format: uri    
            type: string    
          minItems: 1    
          type: array    
        - format: uri    
          type: string    
      type: Property    
    socketNumber:    
      description: 'The total number of sockets offered by this charging station'    
      minimum: 1    
      type: Property    
      x-ngsi:    
        model: http://schema.org/Number.    
    socketType:    
      description: 'The type of sockets offered by this station. Enum:''Caravan_Mains_Socket, CHAdeMO, CCS/SAE, Dual_CHAdeMO, Dual_J-1772, Dual_Mennekes, J-1772, Mennekes, Other, Tesla, Type2, Type3, Wall_Euro'''    
      items:    
        enum:    
          - Caravan_Mains_Socket    
          - CHAdeMO    
          - CCS/SAE    
          - Dual_CHAdeMO    
          - Dual_J-1772    
          - Dual_Mennekes    
          - J-1772    
          - Mennekes    
          - Other    
          - Tesla    
          - Type2    
          - Type3    
          - Wall_Euro    
        type: string    
      minItems: 1    
      type: Property    
      uniqueItems: true    
      x-ngsi:    
        model: http://schema.org/Text    
    source:    
      description: 'A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object.'    
      type: Property    
    status:    
      description: 'Status of the charging station. Enum:''almostEmpty, almostFull, empty, full, outOfService, withIncidence, working''. Or any other application-specific.'    
      enum:    
        - almostEmpty    
        - almostFull    
        - empty    
        - full    
        - outOfService    
        - withIncidence    
        - working    
      type: Property    
      x-ngsi:    
        model: http://schema.org/Text    
    type:    
      description: 'NGSI Entity type. It has to be EVChargingStation'    
      enum:    
        - EVChargingStation    
      type: Property    
    voltage:    
      description: 'The total voltage offered by the charging station'    
      minimum: 0    
      type: Property    
      x-ngsi:    
        model: http://schema.org/Number    
        units: 'Volts (V)'    
  required:    
    - id    
    - type    
    - socketType    
    - capacity    
    - allowedVehicleType    
  type: object    
```  
</details>    
## Example payloads    
#### EVChargingStation NGSI-v2 key-values Example    
Here is an example of a EVChargingStation in JSON-LD format as key-values. This is compatible with NGSI-v2 when  using `options=keyValues` and returns the context data of an individual entity.  
```json  
{  
  "id": "urn:ngsi-ld:EVChargingStation:ValladolI+D_Covaresa",  
  "type": "EVChargingStation",  
  "name": "Agencia de Innovación",  
  "location": {  
    "coordinates": [-4.747901, 41.618265],  
    "type": "Point"  
  },  
  "capacity": 2,  
  "socketType": ["Wall_Euro"],  
  "address": {  
    "streetAddress": "Paseo de Zorrilla, 191",  
    "addressLocality": "Valladolid",  
    "addressCountry": "España"  
  },  
  "contactPoint": {  
    "email": "vehiculoelectrico@ava.es"  
  },  
  "operator": "Iberdrola",  
  "allowedVehicleType": ["car"],  
  "chargeType": ["free"],  
  "source": "https://openchargemap.org/"  
}  
```  
#### EVChargingStation NGSI-v2 normalized Example    
Here is an example of a EVChargingStation in JSON-LD format as normalized. This is compatible with NGSI-v2 when not using options and returns the context data of an individual entity.  
```json  
{  
  "id": "urn:ngsi-ld:EVChargingStation:ValladolI+D_Covaresa",  
  "type": "EVChargingStation",  
  "socketType": {  
    "value": ["Wall_Euro"]  
  },  
  "capacity": {  
    "value": 2  
  },  
  "name": {  
    "value": "Agencia de Innovaci\u00f3n"  
  },  
  "allowedVehicleType": {  
    "value": ["car"]  
  },  
  "source": {  
    "value": "https://openchargemap.org/"  
  },  
  "location": {  
    "type": "geo:json",  
    "value": {  
      "type": "Point",  
      "coordinates": [-4.747901, 41.618265]  
    }  
  },  
  "chargeType": {  
    "value": ["free"]  
  },  
  "address": {  
    "type": "PostalAddress",  
    "value": {  
      "addressLocality": "Valladolid",  
      "addressCountry": "Espa\u00f1a",  
      "streetAddress": "Paseo de Zorrilla, 191"  
    }  
  },  
  "operator": {  
    "value": "Iberdrola"  
  },  
  "contactPoint": {  
    "value": {  
      "email": "vehiculoelectrico@ava.es"  
    }  
  }  
}  
```  
#### EVChargingStation NGSI-LD key-values Example    
Here is an example of a EVChargingStation in JSON-LD format as key-values. This is compatible with NGSI-LD when  using `options=keyValues` and returns the context data of an individual entity.  
```json  
{  
  "id": "urn:ngsi-ld:EVChargingStation:ValladolI+D_Covaresa",  
  "type": "EVChargingStation",  
  "socketType": {  
    "type": "Property",  
    "value": [  
      "Wall_Euro"  
    ]  
  },  
  "capacity": {  
    "type": "Property",  
    "value": 2  
  },  
  "name": {  
    "type": "Property",  
    "value": "Agencia de Innovaci\u00f3n"  
  },  
  "allowedVehicleType": {  
    "type": "Property",  
    "value": [  
      "car"  
    ]  
  },  
  "source": {  
    "type": "Property",  
    "value": "https://openchargemap.org/"  
  },  
  "location": {  
    "type": "GeoProperty",  
    "value": {  
      "type": "Point",  
      "coordinates": [  
        -4.747901,  
        41.618265  
      ]  
    }  
  },  
  "chargeType": {  
    "type": "Property",  
    "value": [  
      "free"  
    ]  
  },  
  "address": {  
    "type": "Property",  
    "value": {  
      "addressLocality": "Valladolid",  
      "addressCountry": "Espa\u00f1a",  
      "streetAddress": "Paseo de Zorrilla, 191",  
      "type": "PostalAddress"  
    }  
  },  
  "operator": {  
    "type": "Property",  
    "value": "Iberdrola"  
  },  
  "contactPoint": {  
    "type": "Property",  
    "value": {  
      "email": "vehiculoelectrico@ava.es"  
    }  
  },  
  "@context": [  
    "https://smartdatamodels.org/context.jsonld",  
    "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context.jsonld"  
  ]  
}  
```  
#### EVChargingStation NGSI-LD normalized Example    
Here is an example of a EVChargingStation in JSON-LD format as normalized. This is compatible with NGSI-LD when not using options and returns the context data of an individual entity.  
```json  
{  
  "@context": [  
    "https://smartdatamodels.org/context.jsonld",  
    "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context.jsonld"  
  ],  
  "address": {  
    "addressCountry": "Espa\u00f1a",  
    "addressLocality": "Valladolid",  
    "streetAddress": "Paseo de Zorrilla, 191",  
    "type": "PostalAddress"  
  },  
  "allowedVehicleType": [  
    "car"  
  ],  
  "capacity": 2,  
  "chargeType": [  
    "free"  
  ],  
  "contactPoint": {  
    "email": "vehiculoelectrico@ava.es"  
  },  
  "id": "urn:ngsi-ld:EVChargingStation:ValladolI+D_Covaresa",  
  "location": {  
    "coordinates": [  
      -4.747901,  
      41.618265  
    ],  
    "type": "Point"  
  },  
  "name": "Agencia de Innovaci\u00f3n",  
  "operator": "Iberdrola",  
  "socketType": [  
    "Wall_Euro"  
  ],  
  "source": "https://openchargemap.org/",  
  "type": "EVChargingStation"  
}  
```  
