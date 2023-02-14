# AWS::RedshiftServerless::Workgroup<a name="aws-resource-redshiftserverless-workgroup"></a>

The collection of compute resources in Amazon Redshift Serverless\.

## Syntax<a name="aws-resource-redshiftserverless-workgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-redshiftserverless-workgroup-syntax.json"></a>

```
{
  "Type" : "AWS::RedshiftServerless::Workgroup",
  "Properties" : {
      "[BaseCapacity](#cfn-redshiftserverless-workgroup-basecapacity)" : Integer,
      "[ConfigParameters](#cfn-redshiftserverless-workgroup-configparameters)" : [ ConfigParameter, ... ],
      "[EnhancedVpcRouting](#cfn-redshiftserverless-workgroup-enhancedvpcrouting)" : Boolean,
      "[NamespaceName](#cfn-redshiftserverless-workgroup-namespacename)" : String,
      "[PubliclyAccessible](#cfn-redshiftserverless-workgroup-publiclyaccessible)" : Boolean,
      "[SecurityGroupIds](#cfn-redshiftserverless-workgroup-securitygroupids)" : [ String, ... ],
      "[SubnetIds](#cfn-redshiftserverless-workgroup-subnetids)" : [ String, ... ],
      "[Tags](#cfn-redshiftserverless-workgroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[WorkgroupName](#cfn-redshiftserverless-workgroup-workgroupname)" : String
    }
}
```

### YAML<a name="aws-resource-redshiftserverless-workgroup-syntax.yaml"></a>

```
Type: AWS::RedshiftServerless::Workgroup
Properties: 
  [BaseCapacity](#cfn-redshiftserverless-workgroup-basecapacity): Integer
  [ConfigParameters](#cfn-redshiftserverless-workgroup-configparameters): 
    - ConfigParameter
  [EnhancedVpcRouting](#cfn-redshiftserverless-workgroup-enhancedvpcrouting): Boolean
  [NamespaceName](#cfn-redshiftserverless-workgroup-namespacename): String
  [PubliclyAccessible](#cfn-redshiftserverless-workgroup-publiclyaccessible): Boolean
  [SecurityGroupIds](#cfn-redshiftserverless-workgroup-securitygroupids): 
    - String
  [SubnetIds](#cfn-redshiftserverless-workgroup-subnetids): 
    - String
  [Tags](#cfn-redshiftserverless-workgroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [WorkgroupName](#cfn-redshiftserverless-workgroup-workgroupname): String
```

## Properties<a name="aws-resource-redshiftserverless-workgroup-properties"></a>

`BaseCapacity`  <a name="cfn-redshiftserverless-workgroup-basecapacity"></a>
The base compute capacity of the workgroup in Redshift Processing Units \(RPUs\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConfigParameters`  <a name="cfn-redshiftserverless-workgroup-configparameters"></a>
A list of parameters to set for finer control over a database\. Available options are `datestyle`, `enable_user_activity_logging`, `query_group`, `search_path`, and `max_query_execution_time`\.  
*Required*: No  
*Type*: List of [ConfigParameter](aws-properties-redshiftserverless-workgroup-configparameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnhancedVpcRouting`  <a name="cfn-redshiftserverless-workgroup-enhancedvpcrouting"></a>
The value that specifies whether to enable enhanced virtual private cloud \(VPC\) routing, which forces Amazon Redshift Serverless to route traffic through your VPC\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NamespaceName`  <a name="cfn-redshiftserverless-workgroup-namespacename"></a>
The namespace the workgroup is associated with\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PubliclyAccessible`  <a name="cfn-redshiftserverless-workgroup-publiclyaccessible"></a>
A value that specifies whether the workgroup can be accessible from a public network\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIds`  <a name="cfn-redshiftserverless-workgroup-securitygroupids"></a>
A list of security group IDs to associate with the workgroup\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-redshiftserverless-workgroup-subnetids"></a>
A list of subnet IDs the workgroup is associated with\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-redshiftserverless-workgroup-tags"></a>
The map of the key\-value pairs used to tag the workgroup\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WorkgroupName`  <a name="cfn-redshiftserverless-workgroup-workgroupname"></a>
The name of the workgroup\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-redshiftserverless-workgroup-return-values"></a>

### Ref<a name="aws-resource-redshiftserverless-workgroup-return-values-ref"></a>

When the logical ID of this resource is provided to the Ref intrinsic function, Ref returns the WorkgroupName, such as `sample-workgroup.` For more information about using the Ref function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.