# AWS Glue Connection ConnectionInput<a name="aws-properties-glue-connection-connectioninput"></a>

<a name="aws-properties-glue-connection-connectioninput-description"></a>The `ConnectionInput` property type specifies the AWS Glue connection to create\.

<a name="aws-properties-glue-connection-connectioninput-inheritance"></a> `ConnectionInput` is a property of the [AWS::Glue::Connection](aws-resource-glue-connection.md) resource\.

## Syntax<a name="aws-properties-glue-connection-connectioninput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-connection-connectioninput-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-connection-connectioninput-description)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-connection-connectioninput-connectiontype)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-connection-connectioninput-matchcriteria)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-connection-connectioninput-physicalconnectionrequirements)" : PhysicalConnectionRequirements,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-connection-connectioninput-connectionproperties)" : JSON object,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-connection-connectioninput-name)" : String
}
```

### YAML<a name="aws-properties-glue-connection-connectioninput-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-connection-connectioninput-description): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-connection-connectioninput-connectiontype): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-connection-connectioninput-matchcriteria): 
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-connection-connectioninput-physicalconnectionrequirements): 
  PhysicalConnectionRequirements
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-connection-connectioninput-connectionproperties): JSON object
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-connection-connectioninput-name): String
```

## Properties<a name="aws-properties-glue-connection-connectioninput-properties"></a>

For more information, see [ConnectionInput Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-connections.html#aws-glue-api-catalog-connections-ConnectionInput) in the *AWS Glue Developer Guide*\.

`Description`  
The description of the connection\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`ConnectionType`  
The type of the connection\. Valid values are `JDBC` or `SFTP`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`MatchCriteria`  
A list of UTF\-8 strings that specify the criteria that you can use in selecting this connection\.  
 *Required*: Yes  
 *Type*: List of String values  
 *Update requires*: No interruption 

`PhysicalConnectionRequirements`  
A map of physical connection requirements that are needed to make the connection, such as VPC and SecurityGroup\.  
 *Required*: Yes  
 *Type*:   
 *Update requires*: No interruption 

`ConnectionProperties`  
UTF\-8 string–to–UTF\-8 string key\-value pairs that specify the parameters for this connection\.  
 *Required*: Yes  
 *Type*: JSON object  
 *Update requires*: No interruption 

`Name`  
The name of the connection\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: Replacement 