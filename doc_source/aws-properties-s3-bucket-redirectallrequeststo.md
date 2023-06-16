# AWS::S3::Bucket RedirectAllRequestsTo<a name="aws-properties-s3-bucket-redirectallrequeststo"></a>

Specifies the redirect behavior of all requests to a website endpoint of an Amazon S3 bucket\.

## Syntax<a name="aws-properties-s3-bucket-redirectallrequeststo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-redirectallrequeststo-syntax.json"></a>

```
{
  "[HostName](#cfn-s3-bucket-redirectallrequeststo-hostname)" : String,
  "[Protocol](#cfn-s3-bucket-redirectallrequeststo-protocol)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-redirectallrequeststo-syntax.yaml"></a>

```
  [HostName](#cfn-s3-bucket-redirectallrequeststo-hostname): String
  [Protocol](#cfn-s3-bucket-redirectallrequeststo-protocol): String
```

## Properties<a name="aws-properties-s3-bucket-redirectallrequeststo-properties"></a>

`HostName`  <a name="cfn-s3-bucket-redirectallrequeststo-hostname"></a>
Name of the host where requests are redirected\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-s3-bucket-redirectallrequeststo-protocol"></a>
Protocol to use when redirecting requests\. The default is the protocol that is used in the original request\.  
*Required*: No  
*Type*: String  
*Allowed values*: `http | https`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)