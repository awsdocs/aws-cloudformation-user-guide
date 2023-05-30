# AWS::Shield::ProtectionGroup<a name="aws-resource-shield-protectiongroup"></a>

Creates a grouping of protected resources so they can be handled as a collective\. This resource grouping improves the accuracy of detection and reduces false positives\. 

**Note**  
To configure this resource through AWS CloudFormation, you must be subscribed to AWS Shield Advanced\. You can subscribe through the [Shield Advanced console](https://console.aws.amazon.com/wafv2/shieldv2#/) and through the APIs\. For more information, see [Subscribe to AWS Shield Advanced](https://docs.aws.amazon.com/waf/latest/developerguide/enable-ddos-prem.html)\. 

## Syntax<a name="aws-resource-shield-protectiongroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-shield-protectiongroup-syntax.json"></a>

```
{
  "Type" : "AWS::Shield::ProtectionGroup",
  "Properties" : {
      "[Aggregation](#cfn-shield-protectiongroup-aggregation)" : String,
      "[Members](#cfn-shield-protectiongroup-members)" : [ String, ... ],
      "[Pattern](#cfn-shield-protectiongroup-pattern)" : String,
      "[ProtectionGroupId](#cfn-shield-protectiongroup-protectiongroupid)" : String,
      "[ResourceType](#cfn-shield-protectiongroup-resourcetype)" : String,
      "[Tags](#cfn-shield-protectiongroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-shield-protectiongroup-syntax.yaml"></a>

```
Type: AWS::Shield::ProtectionGroup
Properties: 
  [Aggregation](#cfn-shield-protectiongroup-aggregation): String
  [Members](#cfn-shield-protectiongroup-members): 
    - String
  [Pattern](#cfn-shield-protectiongroup-pattern): String
  [ProtectionGroupId](#cfn-shield-protectiongroup-protectiongroupid): String
  [ResourceType](#cfn-shield-protectiongroup-resourcetype): String
  [Tags](#cfn-shield-protectiongroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-shield-protectiongroup-properties"></a>

`Aggregation`  <a name="cfn-shield-protectiongroup-aggregation"></a>
Defines how AWS Shield combines resource data for the group in order to detect, mitigate, and report events\.  
+ Sum \- Use the total traffic across the group\. This is a good choice for most cases\. Examples include Elastic IP addresses for EC2 instances that scale manually or automatically\.
+ Mean \- Use the average of the traffic across the group\. This is a good choice for resources that share traffic uniformly\. Examples include accelerators and load balancers\.
+ Max \- Use the highest traffic from each resource\. This is useful for resources that don't share traffic and for resources that share that traffic in a non\-uniform way\. Examples include Amazon CloudFront distributions and origin resources for CloudFront distributions\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `MAX | MEAN | SUM`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Members`  <a name="cfn-shield-protectiongroup-members"></a>
The ARNs \(Amazon Resource Names\) of the resources to include in the protection group\. You must set this when you set `Pattern` to `ARBITRARY` and you must not set it for any other `Pattern` setting\.   
*Required*: No  
*Type*: List of String  
*Maximum*: `10000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Pattern`  <a name="cfn-shield-protectiongroup-pattern"></a>
The criteria to use to choose the protected resources for inclusion in the group\. You can include all resources that have protections, provide a list of resource ARNs \(Amazon Resource Names\), or include all resources of a specified resource type\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALL | ARBITRARY | BY_RESOURCE_TYPE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProtectionGroupId`  <a name="cfn-shield-protectiongroup-protectiongroupid"></a>
The name of the protection group\. You use this to identify the protection group in lists and to manage the protection group, for example to update, delete, or describe it\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `36`  
*Pattern*: `[a-zA-Z0-9\\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceType`  <a name="cfn-shield-protectiongroup-resourcetype"></a>
The resource type to include in the protection group\. All protected resources of this type are included in the protection group\. You must set this when you set `Pattern` to `BY_RESOURCE_TYPE` and you must not set it for any other `Pattern` setting\.   
*Required*: No  
*Type*: String  
*Allowed values*: `APPLICATION_LOAD_BALANCER | CLASSIC_LOAD_BALANCER | CLOUDFRONT_DISTRIBUTION | ELASTIC_IP_ALLOCATION | GLOBAL_ACCELERATOR | ROUTE_53_HOSTED_ZONE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-shield-protectiongroup-tags"></a>
Key:value pairs associated with an AWS resource\. The key:value pair can be anything you define\. Typically, the tag key represents a category \(such as "environment"\) and the tag value represents a specific value within that category \(such as "test," "development," or "production"\)\. You can add up to 50 tags to each AWS resource\.  
To modify tags on existing resources, use the AWS Shield Advanced APIs or command line interface\. With AWS CloudFormation, you can only add tags to resources during resource creation\. 
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-shield-protectiongroup-return-values"></a>

### Ref<a name="aws-resource-shield-protectiongroup-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the ARN \(Amazon Resource Name\) of the protection group\. 

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-shield-protectiongroup-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-shield-protectiongroup-return-values-fn--getatt-fn--getatt"></a>

`ProtectionGroupArn`  <a name="ProtectionGroupArn-fn::getatt"></a>
The ARN \(Amazon Resource Name\) of the new protection group\.

## Examples<a name="aws-resource-shield-protectiongroup--examples"></a>



### Create a protection group for all protected resources<a name="aws-resource-shield-protectiongroup--examples--Create_a_protection_group_for_all_protected_resources"></a>

The following shows an example protection group configuration for all protected resources\. 

#### YAML<a name="aws-resource-shield-protectiongroup--examples--Create_a_protection_group_for_all_protected_resources--yaml"></a>

```
Resources:
  ProtectionGroup:
    Type: AWS::Shield::ProtectionGroup
    Properties:
      ProtectionGroupId: 'ProtectionGroupForAllResources'
      Aggregation: SUM
      Pattern: ALL
```

#### JSON<a name="aws-resource-shield-protectiongroup--examples--Create_a_protection_group_for_all_protected_resources--json"></a>

```
{
    "Resources": {
        "ProtectionGroup": {
            "Type": "AWS::Shield::ProtectionGroup",
            "Properties": {
                "ProtectionGroupId": "ProtectionGroupForAllResources",
                "Aggregation": "SUM",
                "Pattern": "ALL"
            }
        }
    }
}
```

### Create a protection group for protected Elastic IP address resources<a name="aws-resource-shield-protectiongroup--examples--Create_a_protection_group_for_protected_Elastic_IP_address_resources"></a>

The following shows an example protection group configuration for all Elastic IP address resources that have AWS Shield Advanced protection\. 

#### YAML<a name="aws-resource-shield-protectiongroup--examples--Create_a_protection_group_for_protected_Elastic_IP_address_resources--yaml"></a>

```
Resources:
  ProtectionGroup:
    Type: AWS::Shield::ProtectionGroup
    Properties:
      ProtectionGroupId: 'ProtectionGroupForAllEIPResources'
      Aggregation: SUM
      Pattern: BY_RESOURCE_TYPE
      ResourceType: ELASTIC_IP_ALLOCATION
```

#### JSON<a name="aws-resource-shield-protectiongroup--examples--Create_a_protection_group_for_protected_Elastic_IP_address_resources--json"></a>

```
{
    "Resources": {
        "ProtectionGroup": {
            "Type": "AWS::Shield::ProtectionGroup",
            "Properties": {
                "ProtectionGroupId": "ProtectionGroupForAllEIPResources",
                "Aggregation": "SUM",
                "Pattern": "BY_RESOURCE_TYPE",
                "ResourceType": "ELASTIC_IP_ALLOCATION"
            }
        }
    }
}
```