# AWS::Lightsail::Container<a name="aws-resource-lightsail-container"></a>

The `AWS::Lightsail::Container` resource specifies a container service\.

A Lightsail container service is a compute resource to which you can deploy containers\.

## Syntax<a name="aws-resource-lightsail-container-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lightsail-container-syntax.json"></a>

```
{
  "Type" : "AWS::Lightsail::Container",
  "Properties" : {
      "[ContainerServiceDeployment](#cfn-lightsail-container-containerservicedeployment)" : ContainerServiceDeployment,
      "[IsDisabled](#cfn-lightsail-container-isdisabled)" : Boolean,
      "[Power](#cfn-lightsail-container-power)" : String,
      "[PublicDomainNames](#cfn-lightsail-container-publicdomainnames)" : [ PublicDomainName, ... ],
      "[Scale](#cfn-lightsail-container-scale)" : Integer,
      "[ServiceName](#cfn-lightsail-container-servicename)" : String,
      "[Tags](#cfn-lightsail-container-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-lightsail-container-syntax.yaml"></a>

```
Type: AWS::Lightsail::Container
Properties: 
  [ContainerServiceDeployment](#cfn-lightsail-container-containerservicedeployment): 
    ContainerServiceDeployment
  [IsDisabled](#cfn-lightsail-container-isdisabled): Boolean
  [Power](#cfn-lightsail-container-power): String
  [PublicDomainNames](#cfn-lightsail-container-publicdomainnames): 
    - PublicDomainName
  [Scale](#cfn-lightsail-container-scale): Integer
  [ServiceName](#cfn-lightsail-container-servicename): String
  [Tags](#cfn-lightsail-container-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-lightsail-container-properties"></a>

`ContainerServiceDeployment`  <a name="cfn-lightsail-container-containerservicedeployment"></a>
An object that describes the current container deployment of the container service\.  
*Required*: No  
*Type*: [ContainerServiceDeployment](aws-properties-lightsail-container-containerservicedeployment.md)  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`IsDisabled`  <a name="cfn-lightsail-container-isdisabled"></a>
A Boolean value indicating whether the container service is disabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Power`  <a name="cfn-lightsail-container-power"></a>
The power specification of the container service\.  
The power specifies the amount of RAM, the number of vCPUs, and the base price of the container service\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `large | medium | micro | nano | small | xlarge`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PublicDomainNames`  <a name="cfn-lightsail-container-publicdomainnames"></a>
The public domain name of the container service, such as `example.com` and `www.example.com`\.  
You can specify up to four public domain names for a container service\. The domain names that you specify are used when you create a deployment with a container that is configured as the public endpoint of your container service\.  
If you don't specify public domain names, then you can use the default domain of the container service\.  
You must create and validate an SSL/TLS certificate before you can use public domain names with your container service\. Use the [AWS::Lightsail::Certificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-certificate.html) resource to create a certificate for the public domain names that you want to use with your container service\.
*Required*: No  
*Type*: List of [PublicDomainName](aws-properties-lightsail-container-publicdomainname.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scale`  <a name="cfn-lightsail-container-scale"></a>
The scale specification of the container service\.  
The scale specifies the allocated compute nodes of the container service\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceName`  <a name="cfn-lightsail-container-servicename"></a>
The name of the container service\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-lightsail-container-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html) in the *AWS CloudFormation User Guide*\.  
The `Value` of `Tags` is optional for Lightsail resources\.
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-lightsail-container-return-values"></a>

### Ref<a name="aws-resource-lightsail-container-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a unique identifier for this resource\.

### Fn::GetAtt<a name="aws-resource-lightsail-container-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-lightsail-container-return-values-fn--getatt-fn--getatt"></a>

`ContainerArn`  <a name="ContainerArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the container\.

`Url`  <a name="Url-fn::getatt"></a>
The publicly accessible URL of the container service\.  
If no public endpoint is specified in the current deployment, this URL returns a 404 response\.

## Remarks<a name="aws-resource-lightsail-container--remarks"></a>

*Container deployment failures*

The stack will drift if the deployment to your `ContainerService` fails\. This is because the template will have a different deployment compared to the container service\.