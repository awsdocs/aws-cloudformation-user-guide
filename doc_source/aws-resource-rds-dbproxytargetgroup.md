# AWS::RDS::DBProxyTargetGroup<a name="aws-resource-rds-dbproxytargetgroup"></a>

**Note**  
This is prerelease documentation for the RDS Database Proxy feature in preview release\. It is subject to change\.

The `AWS::RDS::DBProxyTargetGroup` resource represents a set of RDS DB instances, Aurora DB clusters, or both that a proxy can connect to\. Currently, each target group is associated with exactly one RDS DB instance or Aurora DB cluster\.

This data type is used as a response element in the `DescribeDBProxyTargetGroups` action\.

For information about RDS Proxy for Amazon RDS, see [ Managing Connections with Amazon RDS Proxy](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/rds-proxy.html) in the *Amazon RDS User Guide*\.

For information about RDS Proxy for Amazon Aurora, see [ Managing Connections with Amazon RDS Proxy](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/rds-proxy.html) in the *Amazon Aurora User Guide*\.

## Syntax<a name="aws-resource-rds-dbproxytargetgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-dbproxytargetgroup-syntax.json"></a>

```
{
  "Type" : "AWS::RDS::DBProxyTargetGroup",
  "Properties" : {
      "[ConnectionPoolConfigurationInfo](#cfn-rds-dbproxytargetgroup-connectionpoolconfigurationinfo)" : [ConnectionPoolConfigurationInfoFormat](aws-properties-rds-dbproxytargetgroup-connectionpoolconfigurationinfoformat.md),
      "[DBClusterIdentifiers](#cfn-rds-dbproxytargetgroup-dbclusteridentifiers)" : [ String, ... ],
      "[DBInstanceIdentifiers](#cfn-rds-dbproxytargetgroup-dbinstanceidentifiers)" : [ String, ... ],
      "[DBProxyName](#cfn-rds-dbproxytargetgroup-dbproxyname)" : String
    }
}
```

### YAML<a name="aws-resource-rds-dbproxytargetgroup-syntax.yaml"></a>

```
Type: AWS::RDS::DBProxyTargetGroup
Properties: 
  [ConnectionPoolConfigurationInfo](#cfn-rds-dbproxytargetgroup-connectionpoolconfigurationinfo): 
    [ConnectionPoolConfigurationInfoFormat](aws-properties-rds-dbproxytargetgroup-connectionpoolconfigurationinfoformat.md)
  [DBClusterIdentifiers](#cfn-rds-dbproxytargetgroup-dbclusteridentifiers): 
    - String
  [DBInstanceIdentifiers](#cfn-rds-dbproxytargetgroup-dbinstanceidentifiers): 
    - String
  [DBProxyName](#cfn-rds-dbproxytargetgroup-dbproxyname): String
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
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-rds-dbproxytargetgroup-return-values"></a>

### Ref<a name="aws-resource-rds-dbproxytargetgroup-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-rds-dbproxytargetgroup-return-values-fn--getatt"></a>

#### <a name="aws-resource-rds-dbproxytargetgroup-return-values-fn--getatt-fn--getatt"></a>

`TargetGroupArn`  <a name="TargetGroupArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) representing the target group\.

`TargetGroupName`  <a name="TargetGroupName-fn::getatt"></a>
The identifier for the target group\. This name must be unique for all target groups owned by your AWS account in the specified AWS Region\.