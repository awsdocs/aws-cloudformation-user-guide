# AWS::EC2::TrafficMirrorFilter<a name="aws-resource-ec2-trafficmirrorfilter"></a>

Specifies a Traffic Mirror filter\.

A Traffic Mirror filter is a set of rules that defines the traffic to mirror\.

By default, no traffic is mirrored\. To mirror traffic, use [AWS::EC2::TrafficMirrorFilterRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-trafficmirrorfilterrule.html) to add Traffic Mirror rules to the filter\. The rules you add define what traffic gets mirrored\.

## Syntax<a name="aws-resource-ec2-trafficmirrorfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-trafficmirrorfilter-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::TrafficMirrorFilter",
  "Properties" : {
      "[Description](#cfn-ec2-trafficmirrorfilter-description)" : String,
      "[NetworkServices](#cfn-ec2-trafficmirrorfilter-networkservices)" : [ String, ... ],
      "[Tags](#cfn-ec2-trafficmirrorfilter-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-trafficmirrorfilter-syntax.yaml"></a>

```
Type: AWS::EC2::TrafficMirrorFilter
Properties: 
  [Description](#cfn-ec2-trafficmirrorfilter-description): String
  [NetworkServices](#cfn-ec2-trafficmirrorfilter-networkservices): 
    - String
  [Tags](#cfn-ec2-trafficmirrorfilter-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-trafficmirrorfilter-properties"></a>

`Description`  <a name="cfn-ec2-trafficmirrorfilter-description"></a>
The description of the Traffic Mirror filter\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetworkServices`  <a name="cfn-ec2-trafficmirrorfilter-networkservices"></a>
The network service traffic that is associated with the Traffic Mirror filter\.  
Valid values are `amazon-dns`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ec2-trafficmirrorfilter-tags"></a>
The tags to assign to a Traffic Mirror filter\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-trafficmirrorfilter-return-values"></a>

### Ref<a name="aws-resource-ec2-trafficmirrorfilter-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the Traffic Mirror filter\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-trafficmirrorfilter--examples"></a>

### Create a Traffic Mirror Filter<a name="aws-resource-ec2-trafficmirrorfilter--examples--Create_a_Traffic_Mirror_Filter"></a>

This is a filter that you can use when you create a traffic mirror session\. This filter also configures mirroring of Amazon DNS network services\.

#### JSON<a name="aws-resource-ec2-trafficmirrorfilter--examples--Create_a_Traffic_Mirror_Filter--json"></a>

```
{
  "SampleTrafficMirrorFilter": {
    "Type": "AWS::EC2::TrafficMirrorFilter",
    "Properties": {
      "Description": "Example traffic mirror filter",
      "NetworkServices": [
        "amazon-dns"
      ],
      "Tags": [
        {
          "Key": "Name",
          "Value": "SampleFilter"
        }
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-ec2-trafficmirrorfilter--examples--Create_a_Traffic_Mirror_Filter--yaml"></a>

```
SampleTrafficMirrorFilter:
  Type: "AWS::EC2::TrafficMirrorFilter"
  Properties:
    Description: "Example traffic mirror filter"
    NetworkServices:
      - "amazon-dns"
    Tags:
    - Key: "Name"
      Value: "SampleFilter"
```

## See also<a name="aws-resource-ec2-trafficmirrorfilter--seealso"></a>
+ [Traffic Mirror Filters and Filter Rules](https://docs.aws.amazon.com/vpc/latest/mirroring/traffic-mirroring-how-it-works.html#traffic-mirroring-filters) in *Traffic Mirroring*
+ [CreateTrafficMirrorFilter](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateTrafficMirrorFilter.html) in the *Amazon EC2 API Reference*

