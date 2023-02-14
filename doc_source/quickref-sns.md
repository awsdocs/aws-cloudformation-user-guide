# Amazon SNS template snippets<a name="quickref-sns"></a>

This example shows an Amazon SNS topic resource\. It requires a valid email address\.

## JSON<a name="quickref-sns-example-1.json"></a>

```
1. "MySNSTopic" : {
2.     "Type" : "AWS::SNS::Topic",
3.     "Properties" : {
4.         "Subscription" : [ {
5.             "Endpoint" : "add valid email address",
6.             "Protocol" : "email"
7.         } ]
8.     }
9. }
```

## YAML<a name="quickref-sns-example-1.yaml"></a>

```
1. MySNSTopic:
2.   Type: AWS::SNS::Topic
3.   Properties:
4.     Subscription:
5.     - Endpoint: "add valid email address"
6.       Protocol: email
```