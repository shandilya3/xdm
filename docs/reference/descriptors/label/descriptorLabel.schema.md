
# Label Descriptor Schema

```
https://ns.adobe.com/xdm/descriptors/descriptorLabel
```

Describes a label at the field level for a given class/fieldgroup/schema

| [Abstract](../../../abstract.md) | [Extensible](../../../extensions.md) | [Status](../../../status.md) | [Identifiable](../../../id.md) | [Custom Properties](../../../extensions.md) | [Additional Properties](../../../extensions.md) | Defined In |
|----------------------------------|--------------------------------------|------------------------------|--------------------------------|---------------------------------------------|-------------------------------------------------|------------|
| Can be instantiated | Yes | Stable | No | Forbidden | Permitted | [descriptors/label/descriptorLabel.schema.json](descriptors/label/descriptorLabel.schema.json) |
## Schema Hierarchy

* Label Descriptor `https://ns.adobe.com/xdm/descriptors/descriptorLabel`
  * [Schema Descriptor](../schemadescriptor.schema.md) `https://ns.adobe.com/xdm/common/descriptors/schemadescriptor`


## Label Descriptor Examples

```json
{
  "@type": "xdm:descriptorLabel",
  "xdm:sourceSchema": "https://ns.adobe.com/xdm/context/profile-work-details",
  "xdm:sourceVersion": 1,
  "xdm:sourceProperty": [
    "/workAddress",
    "/workEmail"
  ],
  "xdm:excludeProperty": [
    "/workAddress/street3",
    "/workAddress/street4",
    "/workEmail/status"
  ],
  "xdm:labels": [
    "sampleDUlELabelResourceID1",
    "sampleDUlELabelResourceID2",
    "sampleDUlELabelResourceID3",
    "sampleDUlELabelResourceID4"
  ]
}
```

```json
{
  "@type": "xdm:descriptorLabel",
  "xdm:sourceSchema": "https://ns.adobe.com/xdm/context/profile-privacy",
  "xdm:sourceVersion": 1,
  "xdm:excludeProperty": "/identityPrivacyInfo/identityIABConsent/consentTimestamp",
  "xdm:labels": [
    "sampleDUlELabelResourceID1",
    "sampleDUlELabelResourceID2",
    "sampleDUlELabelResourceID3",
    "sampleDUlELabelResourceID4"
  ]
}
```

```json
{
  "@type": "xdm:descriptorLabel",
  "xdm:sourceSchema": "https://ns.adobe.com/xdm/context/profile-privacy",
  "xdm:sourceVersion": 1,
  "xdm:sourceProperty": "/identityPrivacyInfo/identityIABConsent/consentTimestamp",
  "xdm:labels": [
    "sampleDUlELabelResourceID1",
    "sampleDUlELabelResourceID2",
    "sampleDUlELabelResourceID3",
    "sampleDUlELabelResourceID4"
  ]
}
```


# Label Descriptor Properties

| Property | Type | Required | Defined by |
|----------|------|----------|------------|
| [@id](#id) | `string` | Optional | [Schema Descriptor](../schemadescriptor.schema.md#id) |
| [@type](#type) | `const` | Optional | Label Descriptor (this schema) |
| [xdm:excludeProperty](#xdmexcludeproperty) | complex | Optional | Label Descriptor (this schema) |
| [xdm:labels](#xdmlabels) | `string[]` | Optional | Label Descriptor (this schema) |
| [xdm:sourceItem](#xdmsourceitem) | complex | Optional | [Schema Descriptor](../schemadescriptor.schema.md#xdmsourceitem) |
| [xdm:sourceProperty](#xdmsourceproperty) | complex | Optional | [Schema Descriptor](../schemadescriptor.schema.md#xdmsourceproperty) |
| [xdm:sourceSchema](#xdmsourceschema) | `string` | Optional | [Schema Descriptor](../schemadescriptor.schema.md#xdmsourceschema) |
| [xdm:sourceVersion](#xdmsourceversion) | `number` | Optional | [Schema Descriptor](../schemadescriptor.schema.md#xdmsourceversion) |
| `*` | any | Additional | this schema *allows* additional properties |

## @id
### Identifier

The unique identifier for the schema descriptor. This property is required when the descriptor is defined outside of the applicable schema, but is optional when applied via 'meta:descriptors'.

`@id`
* is optional
* type: `string`
* defined in [Schema Descriptor](../schemadescriptor.schema.md#id)

### @id Type


`string`
* format: `uri-reference` – URI Reference (according to [RFC3986](https://tools.ietf.org/html/rfc3986))






## @type


`@type`
* is optional
* type: `const`
* defined in this schema

The value of this property **must** be equal to:

```json
"xdm:descriptorLabel"
```





## xdm:excludeProperty
### Exclude Property

When present, the property of the source schema to which this descriptor excludes. This value is a JSON Pointer, applied to an instance of an object described by `xdm:sourceSchema`.

`xdm:excludeProperty`
* is optional
* type: complex
* defined in this schema

### xdm:excludeProperty Type


**One** of the following *conditions* need to be fulfilled.


#### Condition 1


`string`



#### Condition 2


Array type: 

All items must be of the type:
`string`










## xdm:labels
### Labels

When present, it allows an array of labels. Values are resources IDs

`xdm:labels`
* is optional
* type: `string[]`

* defined in this schema

### xdm:labels Type


Array type: `string[]`

All items must be of the type:
`string`









## xdm:sourceItem
### Source Item

When present, the selector used to match a specific item in the array pointed to by `sourceProperty`.

`xdm:sourceItem`
* is optional
* type: complex
* defined in [Schema Descriptor](../schemadescriptor.schema.md#xdmsourceitem)

### xdm:sourceItem Type


**One** of the following *conditions* need to be fulfilled.


#### Condition 1



#### Condition 2



#### Condition 3



#### Condition 4







## xdm:sourceProperty
### Source Property

When present, the property of the source schema to which this descriptor applies. This value is a JSON Pointer, applied to an instance of an object described by `xdm:sourceSchema`.

`xdm:sourceProperty`
* is optional
* type: complex
* defined in [Schema Descriptor](../schemadescriptor.schema.md#xdmsourceproperty)

### xdm:sourceProperty Type


**One** of the following *conditions* need to be fulfilled.


#### Condition 1


`string`



#### Condition 2


Array type: 

All items must be of the type:
`string`










## xdm:sourceSchema
### Source Schema

The source schema this descriptor applies to. This property is required when the descriptor is defined outside of the applicable schema, but is optional when applied via 'meta:descriptors'

`xdm:sourceSchema`
* is optional
* type: `string`
* defined in [Schema Descriptor](../schemadescriptor.schema.md#xdmsourceschema)

### xdm:sourceSchema Type


`string`
* format: `uri` – Uniformous Resource Identifier (according to [RFC3986](http://tools.ietf.org/html/rfc3986))






## xdm:sourceVersion
### Source Version

Major version being referenced.

`xdm:sourceVersion`
* is optional
* type: `number`
* defined in [Schema Descriptor](../schemadescriptor.schema.md#xdmsourceversion)

### xdm:sourceVersion Type


`number`





