# AWS::EC2::LaunchTemplate CapacityReservationPreference<a name="aws-properties-ec2-launchtemplate-capacityreservationpreference"></a>

Indicates the instance's Capacity Reservation preferences\. This is a string value\. Possible preferences include the following:
+  `open` \- The instance can run in any `open` Capacity Reservation that has matching attributes \(instance type, platform, Availability Zone\)\.
+  `none` \- The instance avoids running in a Capacity Reservation even if one is available\. The instance runs in On\-Demand capacity\.

`CapacityReservationPreference` is a property of the [Amazon EC2 LaunchTemplate CapacityReservationSpecification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata-capacityreservationspecification.html) property type\.
