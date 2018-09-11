# Amazon SNS Template Snippets<a name="quickref-sns"></a>

This example shows an Amazon SNS topic resource\. It requires a valid email address\.

## JSON<a name="quickref-sns-example-1.json"></a>

```
"MySNSTopic" : {
    "Type" : "AWS::SNS::Topic",
    "Properties" : {
        "Subscription" : [ {
            "Endpoint" : "add valid email address",
            "Protocol" : "email"
        } ]
    }
}
```

## YAML<a name="quickref-sns-example-1.yaml"></a>

```
MySNSTopic:
  Type: AWS::SNS::Topic
  Properties:
    Subscription:
    - Endpoint: "add valid email address"
      Protocol: email
```