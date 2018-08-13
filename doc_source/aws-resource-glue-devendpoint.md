# AWS::Glue::DevEndpoint<a name="aws-resource-glue-devendpoint"></a>

The `AWS::Glue::DevEndpoint` resource specifies a development endpoint where a developer can remotely debug ETL scripts for AWS Glue\. For more information, see [DevEndpoint Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-dev-endpoint.html#aws-glue-api-jobs-dev-endpoint-DevEndpoint) in the *AWS Glue Developer Guide*\. 

**Topics**
+ [Syntax](#aws-resource-glue-devendpoint-syntax)
+ [Properties](#aws-resource-glue-devendpoint-properties)
+ [See Also](#aws-resource-glue-devendpoint-seealso)

## Syntax<a name="aws-resource-glue-devendpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-devendpoint-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::DevEndpoint",
  "Properties" : {
    "[EndpointName](#cfn-glue-devendpoint-endpointname)" : String,
    "[ExtraJarsS3Path](#cfn-glue-devendpoint-extrajarss3path)" : String,
    "[ExtraPythonLibsS3Path](#cfn-glue-devendpoint-extrapythonlibss3path)" : String,
    "[NumberOfNodes](#cfn-glue-devendpoint-numberofnodes)" : Integer,
    "[PublicKey](#cfn-glue-devendpoint-publickey)" : String,
    "[RoleArn](#cfn-glue-devendpoint-rolearn)" : String,
    "[SecurityGroupIds](#cfn-glue-devendpoint-securitygroupids)" : [ String, ... ],
    "[SubnetId](#cfn-glue-devendpoint-subnetid)" : String
  }
}
```

### YAML<a name="aws-resource-glue-devendpoint-syntax.yaml"></a>

```
Type: "AWS::Glue::DevEndpoint"
Properties:
  [EndpointName](#cfn-glue-devendpoint-endpointname): String
  [ExtraJarsS3Path](#cfn-glue-devendpoint-extrajarss3path): String
  [ExtraPythonLibsS3Path](#cfn-glue-devendpoint-extrapythonlibss3path): String
  [NumberOfNodes](#cfn-glue-devendpoint-numberofnodes): Integer
  [PublicKey](#cfn-glue-devendpoint-publickey): String
  [RoleArn](#cfn-glue-devendpoint-rolearn): String
  [SecurityGroupIds](#cfn-glue-devendpoint-securitygroupids): 
    - String
  [SubnetId](#cfn-glue-devendpoint-subnetid): String
```

## Properties<a name="aws-resource-glue-devendpoint-properties"></a>

`EndpointName`  <a name="cfn-glue-devendpoint-endpointname"></a>
The name of the endpoint\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ExtraJarsS3Path`  <a name="cfn-glue-devendpoint-extrajarss3path"></a>
The path to one or more Java Jars in an Amazon S3 bucket to load in your endpoint\.  
You can currently use only pure Java/Scala libraries on a DevEndpoint\.
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ExtraPythonLibsS3Path`  <a name="cfn-glue-devendpoint-extrapythonlibss3path"></a>
The path to one or more Python libraries in an Amazon S3 bucket to load in your endpoint\.  
You can currently use only pure Python libraries on a DevEndpoint\. Libraries that rely on C extensions, such as the [pandas](http://pandas.pydata.org/) Python data analysis library, aren't supported yet\.
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`NumberOfNodes`  <a name="cfn-glue-devendpoint-numberofnodes"></a>
The number of nodes that the endpoint uses\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`PublicKey`  <a name="cfn-glue-devendpoint-publickey"></a>
The public key for the endpoint to use for authentication\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RoleArn`  <a name="cfn-glue-devendpoint-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role for the endpoint\. It must match the AWS ARN string pattern: `arn:aws:iam::\d{12}:role/.*`  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SecurityGroupIds`  <a name="cfn-glue-devendpoint-securitygroupids"></a>
A list of UTF\-8 strings that specify the security group IDs for the endpoint\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SubnetId`  <a name="cfn-glue-devendpoint-subnetid"></a>
The subnet ID for the endpoint\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-resource-glue-devendpoint-seealso"></a>
+ [DevEndpoint Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-dev-endpoint.html#aws-glue-api-jobs-dev-endpoint-DevEndpoint) in the *AWS Glue Developer Guide* 