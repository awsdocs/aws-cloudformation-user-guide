# AWS::RDS::DBProxyTargetGroup<a name="aws-resource-rds-dbproxytargetgroup"></a>

The `AWS::RDS::DBProxyTargetGroup` resource represents a set of RDS DB instances, Aurora DB clusters, or both that a proxy can connect to\. Currently, each target group is associated with exactly one RDS DB instance or Aurora DB cluster\.

This data type is used as a response element in the `DescribeDBProxyTargetGroups` action\.

For information about RDS Proxy for Amazon RDS, see [ Managing Connections with Amazon RDS Proxy](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/rds-proxy.html) in the *Amazon RDS User Guide*\.

For information about RDS Proxy for Amazon Aurora, see [ Managing Connections with Amazon RDS Proxy](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/rds-proxy.html) in the *Amazon Aurora User Guide*\.

For a sample template that creates a DB proxy and registers a DB instance, see [ Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbproxy.html#aws-resource-rds-dbproxy--examples) in AWS::RDS::DBProxy\.

**Note**  
Limitations apply to RDS Proxy, including DB engine version limitations and AWS Region limitations\.  
For information about limitations that apply to RDS Proxy for Amazon RDS, see [ Limitations for RDS Proxy](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/rds-proxy.html#rds-proxy.limitations) in the *Amazon RDS User Guide*\.  
For information about that apply to RDS Proxy for Amazon Aurora, see [ Limitations for RDS Proxy](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/rds-proxy.html#rds-proxy.limitations) in the *Amazon Aurora User Guide*\.

## Syntax<a name="aws-resource-rds-dbproxytargetgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-dbproxytargetgroup-syntax.json"></a>

```
{
  "Type" : "AWS::RDS::DBProxyTargetGroup",
  "Properties" : {
      "[ConnectionPoolConfigurationInfo](#cfn-rds-dbproxytargetgroup-connectionpoolconfigurationinfo)" : ConnectionPoolConfigurationInfoFormat,
      "[DBClusterIdentifiers](#cfn-rds-dbproxytargetgroup-dbclusteridentifiers)" : [ String, ... ],
      "[DBInstanceIdentifiers](#cfn-rds-dbproxytargetgroup-dbinstanceidentifiers)" : [ String, ... ],
      "[DBProxyName](#cfn-rds-dbproxytargetgroup-dbproxyname)" : String,
      "[TargetGroupName](#cfn-rds-dbproxytargetgroup-targetgroupname)" : String
    }
}
```

### YAML<a name="aws-resource-rds-dbproxytargetgroup-syntax.yaml"></a>

```
Type: AWS::RDS::DBProxyTargetGroup
Properties: 
  [ConnectionPoolConfigurationInfo](#cfn-rds-dbproxytargetgroup-connectionpoolconfigurationinfo): 
    ConnectionPoolConfigurationInfoFormat
  [DBClusterIdentifiers](#cfn-rds-dbproxytargetgroup-dbclusteridentifiers): 
    - String
  [DBInstanceIdentifiers](#cfn-rds-dbproxytargetgroup-dbinstanceidentifiers): 
    - String
  [DBProxyName](#cfn-rds-dbproxytargetgroup-dbproxyname): String
  [TargetGroupName](#cfn-rds-dbproxytargetgroup-targetgroupname): String
```

## Properties<a name="aws-resource-rds-dbproxytargetgroup-properties"></a>

`ConnectionPoolConfigurationInfo`  <a name="cfn-rds-dbproxytargetgroup-connectionpoolconfigurationinfo"></a>
Settings that control the size and behavior of the connection pool associated with a `DBProxyTargetGroup`\.   
*Required*: No  
*Type*: [ConnectionPoolConfigurationInfoFormat](aws-properties-rds-dbproxytargetgroup-connectionpoolconfigurationinfoformat.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DBClusterIdentifiers`  <a name="cfn-rds-dbproxytargetgroup-dbclusteridentifiers"></a>
One or more DB cluster identifiers\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DBInstanceIdentifiers`  <a name="cfn-rds-dbproxytargetgroup-dbinstanceidentifiers"></a>
One or more DB instance identifiers\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DBProxyName`  <a name="cfn-rds-dbproxytargetgroup-dbproxyname"></a>
The identifier of the `DBProxy` that is associated with the `DBProxyTargetGroup`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TargetGroupName`  <a name="cfn-rds-dbproxytargetgroup-targetgroupname"></a>
The identifier for the target group\.  
Currently, this property must be set to `default`\.
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-rds-dbproxytargetgroup-return-values"></a>

### Ref<a name="aws-resource-rds-dbproxytargetgroup-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the target group\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-rds-dbproxytargetgroup-return-values-fn--getatt"></a>

#### <a name="aws-resource-rds-dbproxytargetgroup-return-values-fn--getatt-fn--getatt"></a>

`TargetGroupArn`  <a name="TargetGroupArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) representing the target group\.