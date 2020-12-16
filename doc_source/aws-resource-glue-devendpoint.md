# AWS::Glue::DevEndpoint<a name="aws-resource-glue-devendpoint"></a>

The `AWS::Glue::DevEndpoint` resource specifies a development endpoint where a developer can remotely debug ETL scripts for AWS Glue\. For more information, see [DevEndpoint Structure](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-dev-endpoint.html#aws-glue-api-jobs-dev-endpoint-DevEndpoint) in the AWS Glue Developer Guide\.

## Syntax<a name="aws-resource-glue-devendpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-devendpoint-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::DevEndpoint",
  "Properties" : {
      "[Arguments](#cfn-glue-devendpoint-arguments)" : Json,
      "[EndpointName](#cfn-glue-devendpoint-endpointname)" : String,
      "[ExtraJarsS3Path](#cfn-glue-devendpoint-extrajarss3path)" : String,
      "[ExtraPythonLibsS3Path](#cfn-glue-devendpoint-extrapythonlibss3path)" : String,
      "[GlueVersion](#cfn-glue-devendpoint-glueversion)" : String,
      "[NumberOfNodes](#cfn-glue-devendpoint-numberofnodes)" : Integer,
      "[NumberOfWorkers](#cfn-glue-devendpoint-numberofworkers)" : Integer,
      "[PublicKey](#cfn-glue-devendpoint-publickey)" : String,
      "[PublicKeys](#cfn-glue-devendpoint-publickeys)" : [ String, ... ],
      "[RoleArn](#cfn-glue-devendpoint-rolearn)" : String,
      "[SecurityConfiguration](#cfn-glue-devendpoint-securityconfiguration)" : String,
      "[SecurityGroupIds](#cfn-glue-devendpoint-securitygroupids)" : [ String, ... ],
      "[SubnetId](#cfn-glue-devendpoint-subnetid)" : String,
      "[Tags](#cfn-glue-devendpoint-tags)" : Json,
      "[WorkerType](#cfn-glue-devendpoint-workertype)" : String
    }
}
```

### YAML<a name="aws-resource-glue-devendpoint-syntax.yaml"></a>

```
Type: AWS::Glue::DevEndpoint
Properties: 
  [Arguments](#cfn-glue-devendpoint-arguments): Json
  [EndpointName](#cfn-glue-devendpoint-endpointname): String
  [ExtraJarsS3Path](#cfn-glue-devendpoint-extrajarss3path): String
  [ExtraPythonLibsS3Path](#cfn-glue-devendpoint-extrapythonlibss3path): String
  [GlueVersion](#cfn-glue-devendpoint-glueversion): String
  [NumberOfNodes](#cfn-glue-devendpoint-numberofnodes): Integer
  [NumberOfWorkers](#cfn-glue-devendpoint-numberofworkers): Integer
  [PublicKey](#cfn-glue-devendpoint-publickey): String
  [PublicKeys](#cfn-glue-devendpoint-publickeys): 
    - String
  [RoleArn](#cfn-glue-devendpoint-rolearn): String
  [SecurityConfiguration](#cfn-glue-devendpoint-securityconfiguration): String
  [SecurityGroupIds](#cfn-glue-devendpoint-securitygroupids): 
    - String
  [SubnetId](#cfn-glue-devendpoint-subnetid): String
  [Tags](#cfn-glue-devendpoint-tags): Json
  [WorkerType](#cfn-glue-devendpoint-workertype): String
```

## Properties<a name="aws-resource-glue-devendpoint-properties"></a>

`Arguments`  <a name="cfn-glue-devendpoint-arguments"></a>
A map of arguments used to configure the `DevEndpoint`\.  
Valid arguments are:  
+ `"--enable-glue-datacatalog": ""`
+ `"GLUE_PYTHON_VERSION": "3"`
+ `"GLUE_PYTHON_VERSION": "2"`
You can specify a version of Python support for development endpoints by using the `Arguments` parameter in the `CreateDevEndpoint` or `UpdateDevEndpoint` APIs\. If no arguments are provided, the version defaults to Python 2\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

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

`GlueVersion`  <a name="cfn-glue-devendpoint-glueversion"></a>
Glue version determines the versions of Apache Spark and Python that AWS Glue supports\. The Python version indicates the version supported for running your ETL scripts on development endpoints\.   
For more information about the available AWS Glue versions and corresponding Spark and Python versions, see [Glue version](https://docs.aws.amazon.com/glue/latest/dg/add-job.html) in the developer guide\.  
Development endpoints that are created without specifying a Glue version default to Glue 0\.9\.  
You can specify a version of Python support for development endpoints by using the `Arguments` parameter in the `CreateDevEndpoint` or `UpdateDevEndpoint` APIs\. If no arguments are provided, the version defaults to Python 2\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumberOfNodes`  <a name="cfn-glue-devendpoint-numberofnodes"></a>
The number of AWS Glue Data Processing Units \(DPUs\) allocated to this `DevEndpoint`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumberOfWorkers`  <a name="cfn-glue-devendpoint-numberofworkers"></a>
The number of workers of a defined `workerType` that are allocated to the development endpoint\.  
The maximum number of workers you can define are 299 for `G.1X`, and 149 for `G.2X`\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PublicKey`  <a name="cfn-glue-devendpoint-publickey"></a>
The public key to be used by this `DevEndpoint` for authentication\. This attribute is provided for backward compatibility because the recommended attribute to use is public keys\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PublicKeys`  <a name="cfn-glue-devendpoint-publickeys"></a>
A list of public keys to be used by the `DevEndpoints` for authentication\. Using this attribute is preferred over a single public key because the public keys allow you to have a different private key per client\.  
If you previously created an endpoint with a public key, you must remove that key to be able to set a list of public keys\. Call the `UpdateDevEndpoint` API operation with the public key content in the `deletePublicKeys` attribute, and the list of new keys in the `addPublicKeys` attribute\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-glue-devendpoint-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role used in this `DevEndpoint`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityConfiguration`  <a name="cfn-glue-devendpoint-securityconfiguration"></a>
The name of the `SecurityConfiguration` structure to be used with this `DevEndpoint`\.  
*Required*: No  
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

`Tags`  <a name="cfn-glue-devendpoint-tags"></a>
The tags to use with this DevEndpoint\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WorkerType`  <a name="cfn-glue-devendpoint-workertype"></a>
The type of predefined worker that is allocated to the development endpoint\. Accepts a value of Standard, G\.1X, or G\.2X\.  
+ For the `Standard` worker type, each worker provides 4 vCPU, 16 GB of memory and a 50GB disk, and 2 executors per worker\.
+ For the `G.1X` worker type, each worker maps to 1 DPU \(4 vCPU, 16 GB of memory, 64 GB disk\), and provides 1 executor per worker\. We recommend this worker type for memory\-intensive jobs\.
+ For the `G.2X` worker type, each worker maps to 2 DPU \(8 vCPU, 32 GB of memory, 128 GB disk\), and provides 1 executor per worker\. We recommend this worker type for memory\-intensive jobs\.
Known issue: when a development endpoint is created with the `G.2X` `WorkerType` configuration, the Spark drivers for the development endpoint will run on 4 vCPU, 16 GB of memory, and a 64 GB disk\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-glue-devendpoint-return-values"></a>

### Ref<a name="aws-resource-glue-devendpoint-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the endpoint name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See also<a name="aws-resource-glue-devendpoint--seealso"></a>
+  [DevEndpoint Structure](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-dev-endpoint.html#aws-glue-api-jobs-dev-endpoint-DevEndpoint) in the *AWS Glue Developer Guide* 

