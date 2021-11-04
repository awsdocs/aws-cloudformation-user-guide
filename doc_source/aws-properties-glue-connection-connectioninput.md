# AWS::Glue::Connection ConnectionInput<a name="aws-properties-glue-connection-connectioninput"></a>

A structure that is used to specify a connection to create or update\.

## Syntax<a name="aws-properties-glue-connection-connectioninput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-connection-connectioninput-syntax.json"></a>

```
{
  "[ConnectionProperties](#cfn-glue-connection-connectioninput-connectionproperties)" : Json,
  "[ConnectionType](#cfn-glue-connection-connectioninput-connectiontype)" : String,
  "[Description](#cfn-glue-connection-connectioninput-description)" : String,
  "[MatchCriteria](#cfn-glue-connection-connectioninput-matchcriteria)" : [ String, ... ],
  "[Name](#cfn-glue-connection-connectioninput-name)" : String,
  "[PhysicalConnectionRequirements](#cfn-glue-connection-connectioninput-physicalconnectionrequirements)" : PhysicalConnectionRequirements
}
```

### YAML<a name="aws-properties-glue-connection-connectioninput-syntax.yaml"></a>

```
  [ConnectionProperties](#cfn-glue-connection-connectioninput-connectionproperties): Json
  [ConnectionType](#cfn-glue-connection-connectioninput-connectiontype): String
  [Description](#cfn-glue-connection-connectioninput-description): String
  [MatchCriteria](#cfn-glue-connection-connectioninput-matchcriteria): 
    - String
  [Name](#cfn-glue-connection-connectioninput-name): String
  [PhysicalConnectionRequirements](#cfn-glue-connection-connectioninput-physicalconnectionrequirements): 
    PhysicalConnectionRequirements
```

## Properties<a name="aws-properties-glue-connection-connectioninput-properties"></a>

`ConnectionProperties`  <a name="cfn-glue-connection-connectioninput-connectionproperties"></a>
These key\-value pairs define parameters for the connection\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectionType`  <a name="cfn-glue-connection-connectioninput-connectiontype"></a>
The type of the connection\. Currently, these types are supported:  
+ `JDBC` \- Designates a connection to a database through Java Database Connectivity \(JDBC\)\.
+ `KAFKA` \- Designates a connection to an Apache Kafka streaming platform\.
+ `MONGODB` \- Designates a connection to a MongoDB document database\.
+ `NETWORK` \- Designates a network connection to a data source within an Amazon Virtual Private Cloud environment \(Amazon VPC\)\.
SFTP is not supported\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-glue-connection-connectioninput-description"></a>
The description of the connection\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MatchCriteria`  <a name="cfn-glue-connection-connectioninput-matchcriteria"></a>
A list of criteria that can be used in selecting this connection\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-glue-connection-connectioninput-name"></a>
The name of the connection\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PhysicalConnectionRequirements`  <a name="cfn-glue-connection-connectioninput-physicalconnectionrequirements"></a>
A map of physical connection requirements, such as virtual private cloud \(VPC\) and `SecurityGroup`, that are needed to successfully make this connection\.  
*Required*: No  
*Type*: [PhysicalConnectionRequirements](aws-properties-glue-connection-physicalconnectionrequirements.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)