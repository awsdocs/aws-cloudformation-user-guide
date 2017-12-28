# AWS::Glue::DevEndpoint<a name="aws-resource-glue-devendpoint"></a>

The `AWS::Glue::DevEndpoint` resource specifies a development endpoint where a developer can remotely debug ETL scripts for AWS Glue\. For more information, see [DevEndpoint Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-dev-endpoint.html#aws-glue-api-jobs-dev-endpoint-DevEndpoint) in the *AWS Glue Developer Guide*\. 


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
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-devendpoint-endpointname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-devendpoint-extrajarss3path)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-devendpoint-extrapythonlibss3path)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-devendpoint-numberofnodes)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-devendpoint-publickey)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-devendpoint-rolearn)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-devendpoint-securitygroupids)" : [ String, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-devendpoint-subnetid)" : String
  }
}
```

### YAML<a name="aws-resource-glue-devendpoint-syntax.yaml"></a>

```
Type: "AWS::Glue::DevEndpoint"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-devendpoint-endpointname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-devendpoint-extrajarss3path): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-devendpoint-extrapythonlibss3path): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-devendpoint-numberofnodes): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-devendpoint-publickey): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-devendpoint-rolearn): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-devendpoint-securitygroupids): 
    - String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-devendpoint-subnetid): String
```

## Properties<a name="aws-resource-glue-devendpoint-properties"></a>

`EndpointName`  
The name of the endpoint\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: Replacement 

`ExtraJarsS3Path`  
The path to one or more Java Jars in an Amazon S3 bucket to load in your endpoint\.  
You can currently use only pure Java/Scala libraries on a DevEndpoint\.
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`ExtraPythonLibsS3Path`  
The path to one or more Python libraries in an Amazon S3 bucket to load in your endpoint\.  
You can currently use only pure Python libraries on a DevEndpoint\. Libraries that rely on C extensions, such as the [pandas](http://pandas.pydata.org/) Python data analysis library, aren't supported yet\.
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`NumberOfNodes`  
The number of nodes that the endpoint uses\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: No interruption 

`PublicKey`  
The public key for the endpoint to use for authentication\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`RoleArn`  
The Amazon Resource Name \(ARN\) of the IAM role for the endpoint\. It must match the AWS ARN string pattern: `arn:aws:iam::\d{12}:role/.*`  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`SecurityGroupIds`  
A list of UTF\-8 strings that specify the security group IDs for the endpoint\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: No interruption 

`SubnetId`  
The subnet ID for the endpoint\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

## See Also<a name="aws-resource-glue-devendpoint-seealso"></a>

+ [DevEndpoint Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-dev-endpoint.html#aws-glue-api-jobs-dev-endpoint-DevEndpoint) in the *AWS Glue Developer Guide* 