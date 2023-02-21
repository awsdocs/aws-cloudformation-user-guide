# AWS::AppRunner::Service IngressConfiguration<a name="aws-properties-apprunner-service-ingressconfiguration"></a>

Network configuration settings for inbound network traffic\.

## Syntax<a name="aws-properties-apprunner-service-ingressconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apprunner-service-ingressconfiguration-syntax.json"></a>

```
{
  "[IsPubliclyAccessible](#cfn-apprunner-service-ingressconfiguration-ispubliclyaccessible)" : Boolean
}
```

### YAML<a name="aws-properties-apprunner-service-ingressconfiguration-syntax.yaml"></a>

```
  [IsPubliclyAccessible](#cfn-apprunner-service-ingressconfiguration-ispubliclyaccessible): Boolean
```

## Properties<a name="aws-properties-apprunner-service-ingressconfiguration-properties"></a>

`IsPubliclyAccessible`  <a name="cfn-apprunner-service-ingressconfiguration-ispubliclyaccessible"></a>
Specifies whether your App Runner service is publicly accessible\. To make the service publicly accessible set it to `True`\. To make the service privately accessible, from only within an Amazon VPC set it to `False`\.   
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)