# Elastic Load Balancing AccessLoggingPolicy<a name="aws-properties-ec2-elb-accessloggingpolicy"></a>

The `AccessLoggingPolicy` property describes where and how access logs are stored for the [AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md) resource\.

## Syntax<a name="w3ab2c21c14d779b5"></a>

### JSON<a name="aws-properties-ec2-elb-accessloggingpolicy-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elb-accessloggingpolicy-emitinterval)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elb-accessloggingpolicy-enabled)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elb-accessloggingpolicy-s3bucketname)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elb-accessloggingpolicy-s3bucketprefix)" : String
}
```

### YAML<a name="aws-properties-ec2-elb-accessloggingpolicy-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elb-accessloggingpolicy-emitinterval): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elb-accessloggingpolicy-enabled): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elb-accessloggingpolicy-s3bucketname): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elb-accessloggingpolicy-s3bucketprefix): String
```

## Properties<a name="w3ab2c21c14d779b7"></a>

`EmitInterval`  
The interval for publishing access logs in minutes\. You can specify an interval of either 5 minutes or 60 minutes\.  
*Required: *No  
*Type*: Integer

`Enabled`  
Whether logging is enabled for the load balancer\.  
*Required: *Yes  
*Type*: Boolean

`S3BucketName`  
The name of an Amazon S3 bucket where access log files are stored\.  
*Required: *Yes  
*Type*: String

`S3BucketPrefix`  
A prefix for the all log object keys, such as `my-load-balancer-logs/prod`\. If you store log files from multiple sources in a single bucket, you can use a prefix to distinguish each log file and its source\.  
*Required: *No  
*Type*: String