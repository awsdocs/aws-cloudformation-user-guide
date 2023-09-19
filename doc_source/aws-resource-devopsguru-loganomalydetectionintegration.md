# AWS::DevOpsGuru::LogAnomalyDetectionIntegration<a name="aws-resource-devopsguru-loganomalydetectionintegration"></a>

 Information about the integration of DevOps Guru with CloudWatch log groups for log anomaly detection\.

## Syntax<a name="aws-resource-devopsguru-loganomalydetectionintegration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-devopsguru-loganomalydetectionintegration-syntax.json"></a>

```
{
  "Type" : "AWS::DevOpsGuru::LogAnomalyDetectionIntegration
}
```

### YAML<a name="aws-resource-devopsguru-loganomalydetectionintegration-syntax.yaml"></a>

```
Type: AWS::DevOpsGuru::LogAnomalyDetectionIntegration
```

## Return values<a name="aws-resource-devopsguru-loganomalydetectionintegration-return-values"></a>

### Ref<a name="aws-resource-devopsguru-loganomalydetectionintegration-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the user account ID\. For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

### Fn::GetAtt<a name="aws-resource-devopsguru-loganomalydetectionintegration-return-values-fn--getatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. For more information about using `Fn::GetAtt`, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\. 

#### <a name="aws-resource-devopsguru-loganomalydetectionintegration-return-values-fn--getatt-fn--getatt"></a>

`AccountId`  <a name="AccountId-fn::getatt"></a>
 The account ID associated with the integration of DevOps Guru with CloudWatch log groups for log anomaly detection\.