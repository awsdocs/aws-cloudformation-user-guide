# AWS::CustomerProfiles::ObjectType<a name="aws-resource-customerprofiles-objecttype"></a>

Specifies an Amazon Connect Customer Profiles Object Type Mapping\.

## Syntax<a name="aws-resource-customerprofiles-objecttype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-customerprofiles-objecttype-syntax.json"></a>

```
{
  "Type" : "AWS::CustomerProfiles::ObjectType",
  "Properties" : {
      "[AllowProfileCreation](#cfn-customerprofiles-objecttype-allowprofilecreation)" : Boolean,
      "[Description](#cfn-customerprofiles-objecttype-description)" : String,
      "[DomainName](#cfn-customerprofiles-objecttype-domainname)" : String,
      "[EncryptionKey](#cfn-customerprofiles-objecttype-encryptionkey)" : String,
      "[ExpirationDays](#cfn-customerprofiles-objecttype-expirationdays)" : Integer,
      "[Fields](#cfn-customerprofiles-objecttype-fields)" : [ FieldMap, ... ],
      "[Keys](#cfn-customerprofiles-objecttype-keys)" : [ KeyMap, ... ],
      "[ObjectTypeName](#cfn-customerprofiles-objecttype-objecttypename)" : String,
      "[Tags](#cfn-customerprofiles-objecttype-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TemplateId](#cfn-customerprofiles-objecttype-templateid)" : String
    }
}
```

### YAML<a name="aws-resource-customerprofiles-objecttype-syntax.yaml"></a>

```
Type: AWS::CustomerProfiles::ObjectType
Properties: 
  [AllowProfileCreation](#cfn-customerprofiles-objecttype-allowprofilecreation): Boolean
  [Description](#cfn-customerprofiles-objecttype-description): String
  [DomainName](#cfn-customerprofiles-objecttype-domainname): String
  [EncryptionKey](#cfn-customerprofiles-objecttype-encryptionkey): String
  [ExpirationDays](#cfn-customerprofiles-objecttype-expirationdays): Integer
  [Fields](#cfn-customerprofiles-objecttype-fields): 
    - FieldMap
  [Keys](#cfn-customerprofiles-objecttype-keys): 
    - KeyMap
  [ObjectTypeName](#cfn-customerprofiles-objecttype-objecttypename): String
  [Tags](#cfn-customerprofiles-objecttype-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TemplateId](#cfn-customerprofiles-objecttype-templateid): String
```

## Properties<a name="aws-resource-customerprofiles-objecttype-properties"></a>

`AllowProfileCreation`  <a name="cfn-customerprofiles-objecttype-allowprofilecreation"></a>
Indicates whether a profile should be created when data is received if one doesn’t exist for an object of this type\. The default is `FALSE`\. If the AllowProfileCreation flag is set to `FALSE`, then the service tries to fetch a standard profile and associate this object with the profile\. If it is set to `TRUE`, and if no match is found, then the service creates a new standard profile\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-customerprofiles-objecttype-description"></a>
The description of the profile object type mapping\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainName`  <a name="cfn-customerprofiles-objecttype-domainname"></a>
The unique name of the domain\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EncryptionKey`  <a name="cfn-customerprofiles-objecttype-encryptionkey"></a>
The customer\-provided key to encrypt the profile object that will be created in this profile object type mapping\. If not specified the system will use the encryption key of the domain\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExpirationDays`  <a name="cfn-customerprofiles-objecttype-expirationdays"></a>
The number of days until the data of this type expires\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Fields`  <a name="cfn-customerprofiles-objecttype-fields"></a>
A list of field definitions for the object type mapping\.  
*Required*: No  
*Type*: List of [FieldMap](aws-properties-customerprofiles-objecttype-fieldmap.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Keys`  <a name="cfn-customerprofiles-objecttype-keys"></a>
A list of keys that can be used to map data to the profile or search for the profile\.  
*Required*: No  
*Type*: List of [KeyMap](aws-properties-customerprofiles-objecttype-keymap.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObjectTypeName`  <a name="cfn-customerprofiles-objecttype-objecttypename"></a>
The name of the profile object type\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-customerprofiles-objecttype-tags"></a>
The tags used to organize, track, or control access for this resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateId`  <a name="cfn-customerprofiles-objecttype-templateid"></a>
A unique identifier for the template mapping\. This can be used instead of specifying the Keys and Fields properties directly\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-customerprofiles-objecttype-return-values"></a>

### Ref<a name="aws-resource-customerprofiles-objecttype-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the DomainName and the ObjectTypeName of the object type\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-customerprofiles-objecttype-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-customerprofiles-objecttype-return-values-fn--getatt-fn--getatt"></a>

`CreatedAt`  <a name="CreatedAt-fn::getatt"></a>
The timestamp of when the object type was created\.

`LastUpdatedAt`  <a name="LastUpdatedAt-fn::getatt"></a>
The timestamp of when the object type was most recently edited\.

## Examples<a name="aws-resource-customerprofiles-objecttype--examples"></a>

The following example creates a object type if Domain existed\.

### <a name="aws-resource-customerprofiles-objecttype--examples--"></a>

#### YAML<a name="aws-resource-customerprofiles-objecttype--examples----yaml"></a>

```
Type: "AWS::CustomerProfiles::ObjectType"
Properties: 
    DomainName: "ExampleDomain" 
    ObjectTypeName: "ExampleObjectType"
    AllowProfileCreation: false 
    Description: "Description Example" 
    ExpirationDays: 1 
    Fields: 
      - Name: "email" 
        ObjectTypeField: 
          Source: "_source.email" 
          Target: "_profile.BusinessEmail"
          ContentType: "EMAIL_ADDRESS" 
    Keys: 
      - Name: "_email" 
        ObjectTypeKeyList: 
          - FieldNames: 
            - "email" 
            StandardIdentifiers: 
              - "PROFILE" 
              - "UNIQUE"
```

#### JSON<a name="aws-resource-customerprofiles-objecttype--examples----json"></a>

```
"Type": "AWS::CustomerProfiles::ObjectType", 
"Properties": { 
    "DomainName": "ExampleDomain",
    "ObjectTypeName": "ExampleObjectType", 
    "AllowProfileCreation": false, 
    "Description": "Description Example", 
    "ExpirationDays": 1, 
    "Fields": [{ 
        "Name": "email",
        "ObjectTypeField": { 
            "Source": "_source.email", 
            "Target": "_profile.BusinessEmail",
            "ContentType": "EMAIL_ADDRESS" 
        } 
    }], 
    "Keys": [{ 
        "Name": "_email", 
        "ObjectTypeKeyList": [{
            "FieldNames": [ "email" ], 
            "StandardIdentifiers": [ "PROFILE", "UNIQUE" ] 
        }] 
    }]
}
```