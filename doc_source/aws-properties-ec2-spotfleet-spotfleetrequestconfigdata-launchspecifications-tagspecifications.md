# Amazon Elastic Compute Cloud SpotFleet SpotFleetTagSpecification<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-tagspecifications"></a>

`SpotFleetTagSpecification` is a property of the [Amazon Elastic Compute Cloud SpotFleet LaunchSpecifications](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications.md) property that specifies the tags for a Spot fleet resource\.

## Syntax<a name="w3ab2c21c14d822b5"></a>

### JSON<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-tagspecifications-syntax.json"></a>

```
{
  "[ResourceType](#cfn-ec2-spotfleet-spotfleettagspecification-resourcetype)" : String,
  "[Tags](#cfn-ec2-spotfleet-spotfleettagspecification-tags)" : [ Resource Tag, ... ]
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-tagspecifications-syntax.yaml"></a>

```
[ResourceType](#cfn-ec2-spotfleet-spotfleettagspecification-resourcetype): String
[Tags](#cfn-ec2-spotfleet-spotfleettagspecification-tags):
    - Resource Tag
```

## Properties<a name="w3ab2c21c14d822b7"></a>

`ResourceType`  <a name="cfn-ec2-spotfleet-spotfleettagspecification-resourcetype"></a>
The type of resource\.   
For valid resource types, see [SpotFleetTagSpecification](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_SpotFleetTagSpecification.html) operation in the *Amazon EC2 API Reference*  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Tags`  <a name="cfn-ec2-spotfleet-spotfleettagspecification-tags"></a>
Specifies an arbitrary set of tags \(key–value pairs\) to associate with this spot fleet\. Use tags to manage your resources\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)