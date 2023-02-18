# AWS CloudFormation User Guide

-----
*****Copyright &copy; Amazon Web Services, Inc. and/or its affiliates. All rights reserved.*****

-----
Amazon's trademarks and trade dress may not be used in
connection with any product or service that is not Amazon's,
in any manner that is likely to cause confusion among customers,
or in any manner that disparages or discredits Amazon. All other
trademarks not owned by Amazon are the property of their respective
owners, who may or may not be affiliated with, connected to, or
sponsored by Amazon.

-----
## Contents
+ [Amazon Connect resource type reference](AWS_Connect.md)
   + [AWS::Connect::ApprovedOrigin](aws-resource-connect-approvedorigin.md)
   + [AWS::Connect::ContactFlow](aws-resource-connect-contactflow.md)
   + [AWS::Connect::ContactFlowModule](aws-resource-connect-contactflowmodule.md)
   + [AWS::Connect::HoursOfOperation](aws-resource-connect-hoursofoperation.md)
      + [AWS::Connect::HoursOfOperation HoursOfOperationConfig](aws-properties-connect-hoursofoperation-hoursofoperationconfig.md)
      + [AWS::Connect::HoursOfOperation HoursOfOperationTimeSlice](aws-properties-connect-hoursofoperation-hoursofoperationtimeslice.md)
   + [AWS::Connect::Instance](aws-resource-connect-instance.md)
      + [AWS::Connect::Instance Attributes](aws-properties-connect-instance-attributes.md)
   + [AWS::Connect::InstanceStorageConfig](aws-resource-connect-instancestorageconfig.md)
      + [AWS::Connect::InstanceStorageConfig EncryptionConfig](aws-properties-connect-instancestorageconfig-encryptionconfig.md)
      + [AWS::Connect::InstanceStorageConfig KinesisFirehoseConfig](aws-properties-connect-instancestorageconfig-kinesisfirehoseconfig.md)
      + [AWS::Connect::InstanceStorageConfig KinesisStreamConfig](aws-properties-connect-instancestorageconfig-kinesisstreamconfig.md)
      + [AWS::Connect::InstanceStorageConfig KinesisVideoStreamConfig](aws-properties-connect-instancestorageconfig-kinesisvideostreamconfig.md)
      + [AWS::Connect::InstanceStorageConfig S3Config](aws-properties-connect-instancestorageconfig-s3config.md)
   + [AWS::Connect::IntegrationAssociation](aws-resource-connect-integrationassociation.md)
   + [AWS::Connect::PhoneNumber](aws-resource-connect-phonenumber.md)
   + [AWS::Connect::QuickConnect](aws-resource-connect-quickconnect.md)
      + [AWS::Connect::QuickConnect PhoneNumberQuickConnectConfig](aws-properties-connect-quickconnect-phonenumberquickconnectconfig.md)
      + [AWS::Connect::QuickConnect QueueQuickConnectConfig](aws-properties-connect-quickconnect-queuequickconnectconfig.md)
      + [AWS::Connect::QuickConnect QuickConnectConfig](aws-properties-connect-quickconnect-quickconnectconfig.md)
      + [AWS::Connect::QuickConnect UserQuickConnectConfig](aws-properties-connect-quickconnect-userquickconnectconfig.md)
   + [AWS::Connect::Rule](aws-resource-connect-rule.md)
      + [AWS::Connect::Rule Actions](aws-properties-connect-rule-actions.md)
      + [AWS::Connect::Rule EventBridgeAction](aws-properties-connect-rule-eventbridgeaction.md)
      + [AWS::Connect::Rule NotificationRecipientType](aws-properties-connect-rule-notificationrecipienttype.md)
      + [AWS::Connect::Rule Reference](aws-properties-connect-rule-reference.md)
      + [AWS::Connect::Rule RuleTriggerEventSource](aws-properties-connect-rule-ruletriggereventsource.md)
      + [AWS::Connect::Rule SendNotificationAction](aws-properties-connect-rule-sendnotificationaction.md)
      + [AWS::Connect::Rule TaskAction](aws-properties-connect-rule-taskaction.md)
   + [AWS::Connect::SecurityKey](aws-resource-connect-securitykey.md)
   + [AWS::Connect::TaskTemplate](aws-resource-connect-tasktemplate.md)
      + [AWS::Connect::TaskTemplate Constraints](aws-properties-connect-tasktemplate-constraints.md)
      + [AWS::Connect::TaskTemplate DefaultFieldValue](aws-properties-connect-tasktemplate-defaultfieldvalue.md)
      + [AWS::Connect::TaskTemplate Field](aws-properties-connect-tasktemplate-field.md)
      + [AWS::Connect::TaskTemplate FieldIdentifier](aws-properties-connect-tasktemplate-fieldidentifier.md)
      + [AWS::Connect::TaskTemplate InvisibleFieldInfo](aws-properties-connect-tasktemplate-invisiblefieldinfo.md)
      + [AWS::Connect::TaskTemplate ReadOnlyFieldInfo](aws-properties-connect-tasktemplate-readonlyfieldinfo.md)
      + [AWS::Connect::TaskTemplate RequiredFieldInfo](aws-properties-connect-tasktemplate-requiredfieldinfo.md)
   + [AWS::Connect::User](aws-resource-connect-user.md)
      + [AWS::Connect::User UserIdentityInfo](aws-properties-connect-user-useridentityinfo.md)
      + [AWS::Connect::User UserPhoneConfig](aws-properties-connect-user-userphoneconfig.md)
   + [AWS::Connect::UserHierarchyGroup](aws-resource-connect-userhierarchygroup.md)