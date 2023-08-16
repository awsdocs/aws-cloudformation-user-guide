# AWS::RDS::DBCluster ReadEndpoint<a name="aws-properties-rds-dbcluster-readendpoint"></a>

The `ReadEndpoint` return value specifies the reader endpoint for the DB cluster\.

The reader endpoint for a DB cluster load\-balances connections across the Aurora Replicas that are available in a DB cluster\. As clients request new connections to the reader endpoint, Aurora distributes the connection requests among the Aurora Replicas in the DB cluster\. This functionality can help balance your read workload across multiple Aurora Replicas in your DB cluster\.

If a failover occurs, and the Aurora Replica that you are connected to is promoted to be the primary instance, your connection is dropped\. To continue sending your read workload to other Aurora Replicas in the cluster, you can then reconnect to the reader endpoint\.

For more information about Aurora endpoints, see [Amazon Aurora connection management](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Overview.Endpoints.html) in the *Amazon Aurora User Guide*\.

## Syntax<a name="aws-properties-rds-dbcluster-readendpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rds-dbcluster-readendpoint-syntax.json"></a>

```
{
  "[Address](#cfn-rds-dbcluster-readendpoint-address)" : String
}
```

### YAML<a name="aws-properties-rds-dbcluster-readendpoint-syntax.yaml"></a>

```
  [Address](#cfn-rds-dbcluster-readendpoint-address): String
```

## Properties<a name="aws-properties-rds-dbcluster-readendpoint-properties"></a>

`Address`  <a name="cfn-rds-dbcluster-readendpoint-address"></a>
The host address of the reader endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)