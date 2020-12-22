# AWS::IoTSiteWise::Gateway Greengrass<a name="aws-properties-iotsitewise-gateway-greengrass"></a>

Contains details for a gateway that runs on AWS IoT Greengrass\. To create a gateway that runs on AWS IoT Greengrass, you must add the IoT SiteWise connector to a Greengrass group and deploy it\. Your Greengrass group must also have permissions to upload data to AWS IoT SiteWise\. For more information, see [Ingesting data using a gateway](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/gateway-connector.html) in the *AWS IoT SiteWise User Guide*\.

## Syntax<a name="aws-properties-iotsitewise-gateway-greengrass-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotsitewise-gateway-greengrass-syntax.json"></a>

```
{
  "[GroupArn](#cfn-iotsitewise-gateway-greengrass-grouparn)" : String
}
```

### YAML<a name="aws-properties-iotsitewise-gateway-greengrass-syntax.yaml"></a>

```
  [GroupArn](#cfn-iotsitewise-gateway-greengrass-grouparn): String
```

## Properties<a name="aws-properties-iotsitewise-gateway-greengrass-properties"></a>

`GroupArn`  <a name="cfn-iotsitewise-gateway-greengrass-grouparn"></a>
The [ARN](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) of the Greengrass group\. For more information about how to find a group's ARN, see [ListGroups](https://docs.aws.amazon.com/greengrass/latest/apireference/listgroups-get.html) and [GetGroup](https://docs.aws.amazon.com/greengrass/latest/apireference/getgroup-get.html) in the *AWS IoT Greengrass API Reference*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)