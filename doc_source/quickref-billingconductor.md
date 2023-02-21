# AWS Billing Console template snippets<a name="quickref-billingconductor"></a>

This example creates one pricing plan with a 10% global markup pricing rule\. This pricing plan is attached to the billing group\. The billing group also has two custom line items which applies a $10 charge and a 10% charge on top of the billing group total cost\.

## JSON<a name="quickref-billingconductor-example-1.json"></a>

```
 1. {
 2.    "Parameters": {
 3.       "LinkedAccountIds": {
 4.          "Type": "ListNumber"
 5.       },
 6.       "PrimaryAccountId": {
 7.          "Type": "Number"
 8.       }
 9.    },
10.    "Resources": {
11.       "TestPricingRule": {
12.          "Type": "AWS::BillingConductor::PricingRule",
13.          "Properties": {
14.             "Name": "TestPricingRule",
15.             "Description": "Test pricing rule created through Cloudformation. Mark everything by 10%.",
16.             "Type": "MARKUP",
17.             "Scope": "GLOBAL",
18.             "ModifierPercentage": 10
19.          }
20.       },
21.       "TestPricingPlan": {
22.          "Type": "AWS::BillingConductor::PricingPlan",
23.          "Properties": {
24.             "Name": "TestPricingPlan",
25.             "Description": "Test pricing plan created through Cloudformation.",
26.             "PricingRuleArns": [
27.                {"Fn::GetAtt": ["TestPricingRule", "Arn"]}
28.             ]
29.          }
30.       },
31.       "TestBillingGroup": {
32.          "Type": "AWS::BillingConductor::BillingGroup",
33.          "Properties": {
34.             "Name": "TestBillingGroup",
35.             "Description": "Test billing group created through Cloudformation with 1 linked account. The linked account is also the primary account.",
36.             "PrimaryAccountId": {
37.                "Ref": "PrimaryAccountId"
38.             },
39.             "AccountGrouping": {
40.                "LinkedAccountIds": null
41.             },
42.             "ComputationPreference": {
43.                "PricingPlanArn": {
44.                  "Fn::GetAtt": ["TestPricingPlan", "Arn"]
45.                }
46.             }
47.          }
48.       },
49.       "TestFlatCustomLineItem": {
50.          "Type": "AWS::BillingConductor::CustomLineItem",
51.          "Properties": {
52.             "Name": "TestFlatCustomLineItem",
53.             "Description": "Test flat custom line item created through Cloudformation for a $10 charge.",
54.             "BillingGroupArn": {
55.               "Fn::GetAtt": ["TestBillingGroup", "Arn"]
56.             },
57.             "CustomLineItemChargeDetails": {
58.                "Flat": {
59.                   "ChargeValue": 10
60.                },
61.                "Type": "FEE"
62.             }
63.          }
64.       },
65.       "TestPercentageCustomLineItem": {
66.          "Type": "AWS::BillingConductor::CustomLineItem",
67.          "Properties": {
68.             "Name": "TestPercentageCustomLineItem",
69.             "Description": "Test percentage custom line item created through Cloudformation for a %10 additional charge on the overall total bill of the billing group.",
70.             "BillingGroupArn": {
71.               "Fn::GetAtt": ["TestBillingGroup", "Arn"]
72.             },
73.             "CustomLineItemChargeDetails": {
74.                "Percentage": {
75.                   "PercentageValue": 10,
76.                   "ChildAssociatedResources": [
77.                      {"Fn::GetAtt": ["TestBillingGroup", "Arn"]}
78.                   ]
79.                },
80.                "Type": "FEE"
81.             }
82.          }
83.       }
84.    }
85. }
```

## YAML<a name="quickref-sns-example-1.yaml"></a>

```
 1. Parameters:
 2.   LinkedAccountIds:
 3.     Type: ListNumber
 4.   PrimaryAccountId:
 5.     Type: Number
 6. Resources:
 7.   TestPricingRule:
 8.     Type: 'AWS::BillingConductor::PricingRule'
 9.     Properties:
10.       Name: 'TestPricingRule'
11.       Description: 'Test pricing rule created through Cloudformation. Mark everything by 10%.'
12.       Type: 'MARKUP'
13.       Scope: 'GLOBAL'
14.       ModifierPercentage: 10
15.   TestPricingPlan:
16.     Type: 'AWS::BillingConductor::PricingPlan'
17.     Properties:
18.       Name: 'TestPricingPlan'
19.       Description: 'Test pricing plan created through Cloudformation.'
20.       PricingRuleArns:
21.         - !GetAtt TestPricingRule.Arn
22.   TestBillingGroup:
23.     Type: 'AWS::BillingConductor::BillingGroup'
24.     Properties:
25.       Name: 'TestBillingGroup'
26.       Description: 'Test billing group created through Cloudformation with 1 linked account. The linked account is also the primary account.'
27.       PrimaryAccountId: !Ref PrimaryAccountId
28.       AccountGrouping:
29.         LinkedAccountIds: !Ref LinkedAccountIds
30.       ComputationPreference:
31.         PricingPlanArn: !GetAtt TestPricingPlan.Arn
32.   TestFlatCustomLineItem:
33.     Type: 'AWS::BillingConductor::CustomLineItem'
34.     Properties:
35.       Name: 'TestFlatCustomLineItem'
36.       Description: 'Test flat custom line item created through Cloudformation for a $10 charge.'
37.       BillingGroupArn: !GetAtt TestBillingGroup.Arn
38.       CustomLineItemChargeDetails:
39.         Flat:
40.           ChargeValue: 10
41.         Type: 'FEE'
42.   TestPercentageCustomLineItem:
43.     Type: 'AWS::BillingConductor::CustomLineItem'
44.     Properties:
45.       Name: 'TestPercentageCustomLineItem'
46.       Description: 'Test percentage custom line item created through Cloudformation for a %10 additional charge on the overall total bill of the billing group.'
47.       BillingGroupArn: !GetAtt TestBillingGroup.Arn
48.       CustomLineItemChargeDetails:
49.         Percentage:
50.           PercentageValue: 10
51.           ChildAssociatedResources:
52.             - !GetAtt TestBillingGroup.Arn
53.         Type: 'FEE'
```