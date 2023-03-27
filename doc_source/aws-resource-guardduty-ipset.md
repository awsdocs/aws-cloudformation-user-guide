# AWS::GuardDuty::IPSet<a name="aws-resource-guardduty-ipset"></a>

The `AWS::GuardDuty::IPSet` resource specifies a new `IPSet`\. An `IPSet` is a list of trusted IP addresses from which secure communication is allowed with AWS infrastructure and applications\.

## Syntax<a name="aws-resource-guardduty-ipset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-guardduty-ipset-syntax.json"></a>

```
{
  "Type" : "AWS::GuardDuty::IPSet",
  "Properties" : {
      "[Activate](#cfn-guardduty-ipset-activate)" : Boolean,
      "[DetectorId](#cfn-guardduty-ipset-detectorid)" : String,
      "[Format](#cfn-guardduty-ipset-format)" : String,
      "[Location](#cfn-guardduty-ipset-location)" : String,
      "[Name](#cfn-guardduty-ipset-name)" : String,
      "[Tags](#cfn-guardduty-ipset-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-guardduty-ipset-syntax.yaml"></a>

```
Type: AWS::GuardDuty::IPSet
Properties: 
  [Activate](#cfn-guardduty-ipset-activate): Boolean
  [DetectorId](#cfn-guardduty-ipset-detectorid): String
  [Format](#cfn-guardduty-ipset-format): String
  [Location](#cfn-guardduty-ipset-location): String
  [Name](#cfn-guardduty-ipset-name): String
  [Tags](#cfn-guardduty-ipset-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-guardduty-ipset-properties"></a>

`Activate`  <a name="cfn-guardduty-ipset-activate"></a>
Indicates whether or not GuardDuty uses the `IPSet`\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DetectorId`  <a name="cfn-guardduty-ipset-detectorid"></a>
The unique ID of the detector of the GuardDuty account that you want to create an IPSet for\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `300`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Format`  <a name="cfn-guardduty-ipset-format"></a>
The format of the file that contains the IPSet\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALIEN_VAULT | FIRE_EYE | OTX_CSV | PROOF_POINT | STIX | TXT`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Location`  <a name="cfn-guardduty-ipset-location"></a>
The URI of the file that contains the IPSet\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `300`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-guardduty-ipset-name"></a>
The user\-friendly name to identify the IPSet\.  
 Allowed characters are alphanumeric, whitespace, dash \(\-\), and underscores \(\_\)\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `300`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-guardduty-ipset-tags"></a>
The tags to be added to a new IP set resource\. Each tag consists of a key and an optional value, both of which you define\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-guardduty-ipset-return-values"></a>

### Ref<a name="aws-resource-guardduty-ipset-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the unique ID of the `IPSet`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-guardduty-ipset--examples"></a>



### Declare an IPSet Resource<a name="aws-resource-guardduty-ipset--examples--Declare_an_IPSet_Resource"></a>

The following example shows how to declare a GuardDuty `IPSet` resource:

#### JSON<a name="aws-resource-guardduty-ipset--examples--Declare_an_IPSet_Resource--json"></a>

```
"myipset": {
    "Type" : "AWS::GuardDuty::IPSet",
    "Properties" : {
        "Activate" : True,
        "DetectorId" : "12abc34d567e8f4912ab3d45e67891f2",
        "Format" : "TXT",
        "Location" : "https://s3-us-west-2.amazonaws.com/mybucket/myipset.txt",
        "Name" : "MyIPSet"
    }
}
```

#### YAML<a name="aws-resource-guardduty-ipset--examples--Declare_an_IPSet_Resource--yaml"></a>

```
myipset:
    Type: AWS::GuardDuty::IPSet
    Properties:
        Activate: True
        DetectorId: "12abc34d567e8f4912ab3d45e67891f2"
        Format: "TXT"
        Location: "https://s3-us-west-2.amazonaws.com/mybucket/myipset.txt"
        Name: "MyIPSet"
```