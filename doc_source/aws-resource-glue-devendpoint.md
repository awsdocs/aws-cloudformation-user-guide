# AWS::Glue::DevEndpoint<a name="aws-resource-glue-devendpoint"></a>

The `AWS::Glue::DevEndpoint` resource specifies a development endpoint where a developer can remotely debug ETL scripts for AWS Glue\. For more information, see [DevEndpoint Structure](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-dev-endpoint.html#aws-glue-api-jobs-dev-endpoint-DevEndpoint) in the AWS Glue Developer Guide\.

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
Type: AWS::Glue::DevEndpoint
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
The name of the `DevEndpoint`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ExtraJarsS3Path`  <a name="cfn-glue-devendpoint-extrajarss3path"></a>
The path to one or more Java `.jar` files in an S3 bucket that should be loaded in your `DevEndpoint`\.  
You can only use pure Java/Scala libraries with a `DevEndpoint`\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExtraPythonLibsS3Path`  <a name="cfn-glue-devendpoint-extrapythonlibss3path"></a>
The paths to one or more Python libraries in an Amazon S3 bucket that should be loaded in your `DevEndpoint`\. Multiple values must be complete paths separated by a comma\.  
You can only use pure Python libraries with a `DevEndpoint`\. Libraries that rely on C extensions, such as the [pandas](http://pandas.pydata.org/) Python data analysis library, are not currently supported\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumberOfNodes`  <a name="cfn-glue-devendpoint-numberofnodes"></a>
The number of AWS Glue Data Processing Units \(DPUs\) allocated to this `DevEndpoint`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PublicKey`  <a name="cfn-glue-devendpoint-publickey"></a>
The public key to be used by this `DevEndpoint` for authentication\. This attribute is provided for backward compatibility because the recommended attribute to use is public keys\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-glue-devendpoint-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role used in this `DevEndpoint`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIds`  <a name="cfn-glue-devendpoint-securitygroupids"></a>
A list of security group identifiers used in this `DevEndpoint`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetId`  <a name="cfn-glue-devendpoint-subnetid"></a>
The subnet ID for this `DevEndpoint`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-glue-devendpoint-return-values"></a>

### Ref<a name="aws-resource-glue-devendpoint-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the endpoint name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See Also<a name="aws-resource-glue-devendpoint--seealso"></a>
+  [DevEndpoint Structure](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-dev-endpoint.html#aws-glue-api-jobs-dev-endpoint-DevEndpoint) in the *AWS Glue Developer Guide* 