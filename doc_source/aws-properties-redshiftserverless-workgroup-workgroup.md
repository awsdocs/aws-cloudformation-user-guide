# AWS::RedshiftServerless::Workgroup Workgroup<a name="aws-properties-redshiftserverless-workgroup-workgroup"></a>

The collection of computing resources from which an endpoint is created\.

## Syntax<a name="aws-properties-redshiftserverless-workgroup-workgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-redshiftserverless-workgroup-workgroup-syntax.json"></a>

```
{
  "[BaseCapacity](#cfn-redshiftserverless-workgroup-workgroup-basecapacity)" : Integer,
  "[ConfigParameters](#cfn-redshiftserverless-workgroup-workgroup-configparameters)" : [ ConfigParameter, ... ],
  "[CreationDate](#cfn-redshiftserverless-workgroup-workgroup-creationdate)" : String,
  "[Endpoint](#cfn-redshiftserverless-workgroup-workgroup-endpoint)" : Endpoint,
  "[EnhancedVpcRouting](#cfn-redshiftserverless-workgroup-workgroup-enhancedvpcrouting)" : Boolean,
  "[NamespaceName](#cfn-redshiftserverless-workgroup-workgroup-namespacename)" : String,
  "[PubliclyAccessible](#cfn-redshiftserverless-workgroup-workgroup-publiclyaccessible)" : Boolean,
  "[SecurityGroupIds](#cfn-redshiftserverless-workgroup-workgroup-securitygroupids)" : [ String, ... ],
  "[Status](#cfn-redshiftserverless-workgroup-workgroup-status)" : String,
  "[SubnetIds](#cfn-redshiftserverless-workgroup-workgroup-subnetids)" : [ String, ... ],
  "[WorkgroupArn](#cfn-redshiftserverless-workgroup-workgroup-workgrouparn)" : String,
  "[WorkgroupId](#cfn-redshiftserverless-workgroup-workgroup-workgroupid)" : String,
  "[WorkgroupName](#cfn-redshiftserverless-workgroup-workgroup-workgroupname)" : String
}
```

### YAML<a name="aws-properties-redshiftserverless-workgroup-workgroup-syntax.yaml"></a>

```
  [BaseCapacity](#cfn-redshiftserverless-workgroup-workgroup-basecapacity): Integer
  [ConfigParameters](#cfn-redshiftserverless-workgroup-workgroup-configparameters): 
    - ConfigParameter
  [CreationDate](#cfn-redshiftserverless-workgroup-workgroup-creationdate): String
  [Endpoint](#cfn-redshiftserverless-workgroup-workgroup-endpoint): 
    Endpoint
  [EnhancedVpcRouting](#cfn-redshiftserverless-workgroup-workgroup-enhancedvpcrouting): Boolean
  [NamespaceName](#cfn-redshiftserverless-workgroup-workgroup-namespacename): String
  [PubliclyAccessible](#cfn-redshiftserverless-workgroup-workgroup-publiclyaccessible): Boolean
  [SecurityGroupIds](#cfn-redshiftserverless-workgroup-workgroup-securitygroupids): 
    - String
  [Status](#cfn-redshiftserverless-workgroup-workgroup-status): String
  [SubnetIds](#cfn-redshiftserverless-workgroup-workgroup-subnetids): 
    - String
  [WorkgroupArn](#cfn-redshiftserverless-workgroup-workgroup-workgrouparn): String
  [WorkgroupId](#cfn-redshiftserverless-workgroup-workgroup-workgroupid): String
  [WorkgroupName](#cfn-redshiftserverless-workgroup-workgroup-workgroupname): String
```

## Properties<a name="aws-properties-redshiftserverless-workgroup-workgroup-properties"></a>

`BaseCapacity`  <a name="cfn-redshiftserverless-workgroup-workgroup-basecapacity"></a>
The base data warehouse capacity of the workgroup in Redshift Processing Units \(RPUs\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConfigParameters`  <a name="cfn-redshiftserverless-workgroup-workgroup-configparameters"></a>
An array of parameters to set for advanced control over a database\. The options are `auto_mv`, `datestyle`, `enable_case_sensitivity_identifier`, `enable_user_activity_logging`, `query_group`, , `search_path`, and query monitoring metrics that let you define performance boundaries\. For more information about query monitoring rules and available metrics, see [ Query monitoring metrics for Amazon Redshift Serverless](https://docs.aws.amazon.com/redshift/latest/dg/cm-c-wlm-query-monitoring-rules.html#cm-c-wlm-query-monitoring-metrics-serverless)\.  
*Required*: No  
*Type*: List of [ConfigParameter](aws-properties-redshiftserverless-workgroup-configparameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CreationDate`  <a name="cfn-redshiftserverless-workgroup-workgroup-creationdate"></a>
The creation date of the workgroup\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Endpoint`  <a name="cfn-redshiftserverless-workgroup-workgroup-endpoint"></a>
The endpoint that is created from the workgroup\.  
*Required*: No  
*Type*: [Endpoint](aws-properties-redshiftserverless-workgroup-endpoint.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnhancedVpcRouting`  <a name="cfn-redshiftserverless-workgroup-workgroup-enhancedvpcrouting"></a>
The value that specifies whether to enable enhanced virtual private cloud \(VPC\) routing, which forces Amazon Redshift Serverless to route traffic through your VPC\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NamespaceName`  <a name="cfn-redshiftserverless-workgroup-workgroup-namespacename"></a>
The namespace the workgroup is associated with\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PubliclyAccessible`  <a name="cfn-redshiftserverless-workgroup-workgroup-publiclyaccessible"></a>
A value that specifies whether the workgroup can be accessible from a public network  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIds`  <a name="cfn-redshiftserverless-workgroup-workgroup-securitygroupids"></a>
An array of security group IDs to associate with the workgroup\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-redshiftserverless-workgroup-workgroup-status"></a>
The status of the workgroup\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-redshiftserverless-workgroup-workgroup-subnetids"></a>
An array of subnet IDs the workgroup is associated with\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WorkgroupArn`  <a name="cfn-redshiftserverless-workgroup-workgroup-workgrouparn"></a>
The Amazon Resource Name \(ARN\) that links to the workgroup\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WorkgroupId`  <a name="cfn-redshiftserverless-workgroup-workgroup-workgroupid"></a>
The unique identifier of the workgroup\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WorkgroupName`  <a name="cfn-redshiftserverless-workgroup-workgroup-workgroupname"></a>
The name of the workgroup\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)