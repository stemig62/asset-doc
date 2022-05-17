**Formly**

Il componete Formly è documentato : [qui](https://formly.dev/guide/getting-started).

La modellazione corrente, descritta in seguito deve essere usata per adattarsi al componente.

per una semplice form, il modello è costituito da questa struttura

{
  "dataOut": null,
  "schemaVersion": null,
  "creationUser": null,
  "treeUUID": null,
  "import_id": null,
  "columndefsCrossCommission": true,
  "creationDate": "2019-07-30T13:46:27.000Z",
  "columndefsCommission": "2200001",
  "version": "AX__fzbbKx9K-N9kvEsw",
  "tags": null,
  "schemaCode": "schema",
  "previousVersion": "AXF4AksYmb61S4JIKjer",
  "model": {
    "schema": {
      "type": "object",
      "title": "",
      "properties": {
        "code": {
          "check": true,
          "title": "Codice",
          "type": "string"
        },
        "position_geo": {
          "enableFiltering": true,
          "check": true,
          "title": "Posizione",
          "type": "geopoint",
          "enableSorting": true
        },
        "description": {
          "check": true,
          "title": "Descrizione",
          "type": "string"
        }
      },
      "required": [
        "code",
        "description"
      ]
    },
    "code": "aeroporto",
    "form": [
      {
        "type": "fieldset",
        "items": [
          {
            "tabs": [
              {
                "title": "Dati Base",
                "items": [
                  {
                    "title": "Codice",
                    "type": "text",
                    "key": [
                      "code"
                    ],
                    "required": true
                  },
                  {
                    "title": "Descrizione",
                    "type": "text",
                    "key": [
                      "description"
                    ],
                    "required": true
                  },
                  {
                    "title": "Posizione",
                    "type": "geopoint",
                    "key": [
                      "position_geo"
                    ]
                  }
                ]
              }
            ],
            "type": "tabs"
          }
        ]
      }
    ],
    "columndefsCrossCommission": false,
    "description": "Aeroporto",
    "history": true,
    "drawingManagement": true,
    "columndefsCommission": "1900013",
    "columnDefs": [
      {
        "field": "code",
        "name": "Codice"
      },
      {
        "field": "description",
        "name": "Descrizione"
      },
      {
        "field": "position_geo",
        "name": "Posizione"
      }
    ],
    "commissionDependent": true,
    "attachmentManagement": true
  },
  "commission": null,
  "UUID": "aeroporto",
  "user": "polist",
  "dataIn": "2022-04-06T15:30:01.000Z",
  "customer": null,
  "parents": null
}

dove, al di là degli auto esplicativi nome di campo, troviamo tre strutture:

1) la definizione delle intestazioni delle colonne della tabella di filtro:

    "columnDefs": [
      {
        "field": "code",
        "name": "Codice"
      },
      {
        "field": "description",
        "name": "Descrizione"
      },
      {
        "field": "position_geo",
        "name": "Posizione"
      }
    ],

in cui:
"field" indica il metadato della variabile che indica un generico codice
"name" il titolo dell'intestazione

2) gli attributi che descrivono il tipo di oggetto nominato in "description" sono descritti nella sezione "properties"
( )

    "description": "Aeroporto",
    "history": true,
    "drawingManagement": true,
    "columndefsCommission": "1900013",
    "columnDefs": [
     "properties": {
        "code": {
          "check": true,
          "title": "Codice",
          "type": "string"
        },
        "position_geo": {
          "enableFiltering": true,
          "check": true,
          "title": "Posizione",
          "type": "geopoint",
          "enableSorting": true
        },
        "description": {
          "check": true,
          "title": "Descrizione",
          "type": "string"
        }
      },
