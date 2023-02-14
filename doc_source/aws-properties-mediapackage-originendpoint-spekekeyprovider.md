# AWS::MediaPackage::OriginEndpoint SpekeKeyProvider<a name="aws-properties-mediapackage-originendpoint-spekekeyprovider"></a>

Keyprovider settings for DRM\.

## Syntax<a name="aws-properties-mediapackage-originendpoint-spekekeyprovider-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-originendpoint-spekekeyprovider-syntax.json"></a>

```
{
  "[CertificateArn](#cfn-mediapackage-originendpoint-spekekeyprovider-certificatearn)" : String,
  "[ResourceId](#cfn-mediapackage-originendpoint-spekekeyprovider-resourceid)" : String,
  "[RoleArn](#cfn-mediapackage-originendpoint-spekekeyprovider-rolearn)" : String,
  "[SystemIds](#cfn-mediapackage-originendpoint-spekekeyprovider-systemids)" : [ String, ... ],
  "[Url](#cfn-mediapackage-originendpoint-spekekeyprovider-url)" : String
}
```

### YAML<a name="aws-properties-mediapackage-originendpoint-spekekeyprovider-syntax.yaml"></a>

```
  [CertificateArn](#cfn-mediapackage-originendpoint-spekekeyprovider-certificatearn): String
  [ResourceId](#cfn-mediapackage-originendpoint-spekekeyprovider-resourceid): String
  [RoleArn](#cfn-mediapackage-originendpoint-spekekeyprovider-rolearn): String
  [SystemIds](#cfn-mediapackage-originendpoint-spekekeyprovider-systemids): 
    - String
  [Url](#cfn-mediapackage-originendpoint-spekekeyprovider-url): String
```

## Properties<a name="aws-properties-mediapackage-originendpoint-spekekeyprovider-properties"></a>

`CertificateArn`  <a name="cfn-mediapackage-originendpoint-spekekeyprovider-certificatearn"></a>
The Amazon Resource Name \(ARN\) for the certificate that you imported to AWS Certificate Manager to add content key encryption to this endpoint\. For this feature to work, your DRM key provider must support content key encryption\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceId`  <a name="cfn-mediapackage-originendpoint-spekekeyprovider-resourceid"></a>
Unique identifier for this endpoint, as it is configured in the key provider service\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-mediapackage-originendpoint-spekekeyprovider-rolearn"></a>
The ARN for the IAM role that's granted by the key provider to provide access to the key provider API\. This role must have a trust policy that allows AWS Elemental MediaPackage to assume the role, and it must have a sufficient permissions policy to allow access to the specific key retrieval URL\. Valid format: arn:aws:iam::\{accountID\}:role/\{name\}   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SystemIds`  <a name="cfn-mediapackage-originendpoint-spekekeyprovider-systemids"></a>
List of unique identifiers for the DRM systems to use, as defined in the CPIX specification\.   
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Url`  <a name="cfn-mediapackage-originendpoint-spekekeyprovider-url"></a>
URL for the key provider’s key retrieval API endpoint\. Must start with https://\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)