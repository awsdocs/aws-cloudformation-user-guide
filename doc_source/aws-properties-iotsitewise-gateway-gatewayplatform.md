# AWS::IoTSiteWise::Gateway GatewayPlatform<a name="aws-properties-iotsitewise-gateway-gatewayplatform"></a>

Contains a gateway's platform information\.

## Syntax<a name="aws-properties-iotsitewise-gateway-gatewayplatform-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotsitewise-gateway-gatewayplatform-syntax.json"></a>

```
{
  "[Greengrass](#cfn-iotsitewise-gateway-gatewayplatform-greengrass)" : Greengrass,
  "[GreengrassV2](#cfn-iotsitewise-gateway-gatewayplatform-greengrassv2)" : GreengrassV2
}
```

### YAML<a name="aws-properties-iotsitewise-gateway-gatewayplatform-syntax.yaml"></a>

```
  [Greengrass](#cfn-iotsitewise-gateway-gatewayplatform-greengrass): 
    Greengrass
  [GreengrassV2](#cfn-iotsitewise-gateway-gatewayplatform-greengrassv2): 
    GreengrassV2
```

## Properties<a name="aws-properties-iotsitewise-gateway-gatewayplatform-properties"></a>

`Greengrass`  <a name="cfn-iotsitewise-gateway-gatewayplatform-greengrass"></a>
A gateway that runs on AWS IoT Greengrass\.  
*Required*: No  
*Type*: [Greengrass](aws-properties-iotsitewise-gateway-greengrass.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GreengrassV2`  <a name="cfn-iotsitewise-gateway-gatewayplatform-greengrassv2"></a>
A gateway that runs on AWS IoT Greengrass V2\.  
*Required*: No  
*Type*: [GreengrassV2](aws-properties-iotsitewise-gateway-greengrassv2.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)