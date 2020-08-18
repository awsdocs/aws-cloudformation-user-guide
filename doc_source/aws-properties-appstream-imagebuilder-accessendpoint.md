# AWS::AppStream::ImageBuilder AccessEndpoint<a name="aws-properties-appstream-imagebuilder-accessendpoint"></a>

Describes an interface VPC endpoint \(interface endpoint\) that lets you create a private connection between the virtual private cloud \(VPC\) that you specify and AppStream 2\.0\. When you specify an interface endpoint for a stack, users of the stack can connect to AppStream 2\.0 only through that endpoint\. When you specify an interface endpoint for an image builder, administrators can connect to the image builder only through that endpoint\.

## Syntax<a name="aws-properties-appstream-imagebuilder-accessendpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appstream-imagebuilder-accessendpoint-syntax.json"></a>

```
{
  "[EndpointType](#cfn-appstream-imagebuilder-accessendpoint-endpointtype)" : String,
  "[VpceId](#cfn-appstream-imagebuilder-accessendpoint-vpceid)" : String
}
```

### YAML<a name="aws-properties-appstream-imagebuilder-accessendpoint-syntax.yaml"></a>

```
  [EndpointType](#cfn-appstream-imagebuilder-accessendpoint-endpointtype): String
  [VpceId](#cfn-appstream-imagebuilder-accessendpoint-vpceid): String
```

## Properties<a name="aws-properties-appstream-imagebuilder-accessendpoint-properties"></a>

`EndpointType`  <a name="cfn-appstream-imagebuilder-accessendpoint-endpointtype"></a>
The type of interface endpoint\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `STREAMING`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpceId`  <a name="cfn-appstream-imagebuilder-accessendpoint-vpceid"></a>
The identifier \(ID\) of the VPC in which the interface endpoint is used\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)