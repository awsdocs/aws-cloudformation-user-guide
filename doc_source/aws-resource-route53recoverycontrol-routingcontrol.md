# AWS::Route53RecoveryControl::RoutingControl<a name="aws-resource-route53recoverycontrol-routingcontrol"></a>

Defines a routing control\. To get or update the routing control state, see the Recovery Cluster \(data plane\) API actions for Amazon Route 53 Application Recovery Controller\.

## Syntax<a name="aws-resource-route53recoverycontrol-routingcontrol-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53recoverycontrol-routingcontrol-syntax.json"></a>

```
{
  "Type" : "AWS::Route53RecoveryControl::RoutingControl",
  "Properties" : {
      "[ClusterArn](#cfn-route53recoverycontrol-routingcontrol-clusterarn)" : String,
      "[ControlPanelArn](#cfn-route53recoverycontrol-routingcontrol-controlpanelarn)" : String,
      "[Name](#cfn-route53recoverycontrol-routingcontrol-name)" : String
    }
}
```

### YAML<a name="aws-resource-route53recoverycontrol-routingcontrol-syntax.yaml"></a>

```
Type: AWS::Route53RecoveryControl::RoutingControl
Properties: 
  [ClusterArn](#cfn-route53recoverycontrol-routingcontrol-clusterarn): String
  [ControlPanelArn](#cfn-route53recoverycontrol-routingcontrol-controlpanelarn): String
  [Name](#cfn-route53recoverycontrol-routingcontrol-name): String
```

## Properties<a name="aws-resource-route53recoverycontrol-routingcontrol-properties"></a>

`ClusterArn`  <a name="cfn-route53recoverycontrol-routingcontrol-clusterarn"></a>
The Amazon Resource Name \(ARN\) of the cluster that includes the routing control\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ControlPanelArn`  <a name="cfn-route53recoverycontrol-routingcontrol-controlpanelarn"></a>
The Amazon Resource Name \(ARN\) of the control panel that includes the routing control\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-route53recoverycontrol-routingcontrol-name"></a>
The name of the routing control\. You can use any non\-white space character in the name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-route53recoverycontrol-routingcontrol-return-values"></a>

### Ref<a name="aws-resource-route53recoverycontrol-routingcontrol-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `RoutingControlArn` object\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-route53recoverycontrol-routingcontrol-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-route53recoverycontrol-routingcontrol-return-values-fn--getatt-fn--getatt"></a>

`RoutingControlArn`  <a name="RoutingControlArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the routing control\.

`Status`  <a name="Status-fn::getatt"></a>
The deployment status of the routing control\. Status can be one of the following: PENDING, DEPLOYED, PENDING\_DELETION\.