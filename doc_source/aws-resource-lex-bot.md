# AWS::Lex::Bot<a name="aws-resource-lex-bot"></a>

**Note**  
Amazon Lex V2 is the only supported version in AWS CloudFormation\.

Specifies an Amazon Lex conversational bot\. 

You must configure an intent based on the `AMAZON.FallbackIntent` built\-in intent\. If you don't add one, creating the bot will fail\.

## Syntax<a name="aws-resource-lex-bot-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lex-bot-syntax.json"></a>

```
{
  "Type" : "AWS::Lex::Bot",
  "Properties" : {
      "[AutoBuildBotLocales](#cfn-lex-bot-autobuildbotlocales)" : Boolean,
      "[BotFileS3Location](#cfn-lex-bot-botfiles3location)" : S3Location,
      "[BotLocales](#cfn-lex-bot-botlocales)" : [ BotLocale, ... ],
      "[BotTags](#cfn-lex-bot-bottags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[DataPrivacy](#cfn-lex-bot-dataprivacy)" : DataPrivacy,
      "[Description](#cfn-lex-bot-description)" : String,
      "[IdleSessionTTLInSeconds](#cfn-lex-bot-idlesessionttlinseconds)" : Integer,
      "[Name](#cfn-lex-bot-name)" : String,
      "[RoleArn](#cfn-lex-bot-rolearn)" : String,
      "[TestBotAliasSettings](#cfn-lex-bot-testbotaliassettings)" : TestBotAliasSettings,
      "[TestBotAliasTags](#cfn-lex-bot-testbotaliastags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-lex-bot-syntax.yaml"></a>

```
Type: AWS::Lex::Bot
Properties: 
  [AutoBuildBotLocales](#cfn-lex-bot-autobuildbotlocales): Boolean
  [BotFileS3Location](#cfn-lex-bot-botfiles3location): 
    S3Location
  [BotLocales](#cfn-lex-bot-botlocales): 
    - BotLocale
  [BotTags](#cfn-lex-bot-bottags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [DataPrivacy](#cfn-lex-bot-dataprivacy): 
    DataPrivacy
  [Description](#cfn-lex-bot-description): String
  [IdleSessionTTLInSeconds](#cfn-lex-bot-idlesessionttlinseconds): Integer
  [Name](#cfn-lex-bot-name): String
  [RoleArn](#cfn-lex-bot-rolearn): String
  [TestBotAliasSettings](#cfn-lex-bot-testbotaliassettings): 
    TestBotAliasSettings
  [TestBotAliasTags](#cfn-lex-bot-testbotaliastags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-lex-bot-properties"></a>

`AutoBuildBotLocales`  <a name="cfn-lex-bot-autobuildbotlocales"></a>
Indicates whether Amazon Lex V2 should automatically build the locales for the bot after a change\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BotFileS3Location`  <a name="cfn-lex-bot-botfiles3location"></a>
The Amazon S3 location of files used to import a bot\. The files must be in the import format specified in [JSON format for importing and exporting](https://docs.aws.amazon.com/lexv2/latest/dg/import-export-format.html) in the *Amazon Lex developer guide\.*  
*Required*: No  
*Type*: [S3Location](aws-properties-lex-bot-s3location.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BotLocales`  <a name="cfn-lex-bot-botlocales"></a>
A list of locales for the bot\.  
*Required*: No  
*Type*: List of [BotLocale](aws-properties-lex-bot-botlocale.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BotTags`  <a name="cfn-lex-bot-bottags"></a>
A list of tags to add to the bot\. You can only add tags when you import a bot\. You can't use the `UpdateBot` operation to update tags\. To update tags, use the `TagResource` operation\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataPrivacy`  <a name="cfn-lex-bot-dataprivacy"></a>
Property description not available\.  
*Required*: Yes  
*Type*: [DataPrivacy](aws-properties-lex-bot-dataprivacy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-lex-bot-description"></a>
The description of the version\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdleSessionTTLInSeconds`  <a name="cfn-lex-bot-idlesessionttlinseconds"></a>
The time, in seconds, that Amazon Lex should keep information about a user's conversation with the bot\.   
A user interaction remains active for the amount of time specified\. If no conversation occurs during this time, the session expires and Amazon Lex deletes any data provided before the timeout\.  
You can specify between 60 \(1 minute\) and 86,400 \(24 hours\) seconds\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-lex-bot-name"></a>
The name of the bot locale\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-lex-bot-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role used to build and run the bot\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TestBotAliasSettings`  <a name="cfn-lex-bot-testbotaliassettings"></a>
Specifies configuration settings for the alias used to test the bot\. If the `TestBotAliasSettings` property is not specified, the settings are configured with default values\.  
*Required*: No  
*Type*: [TestBotAliasSettings](aws-properties-lex-bot-testbotaliassettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TestBotAliasTags`  <a name="cfn-lex-bot-testbotaliastags"></a>
A list of tags to add to the test alias for a bot\. You can only add tags when you import a bot\. You can't use the `UpdateAlias` operation to update tags\. To update tags on the test alias, use the `TagResource` operation\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-lex-bot-return-values"></a>

### Fn::GetAtt<a name="aws-resource-lex-bot-return-values-fn--getatt"></a>

#### <a name="aws-resource-lex-bot-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the bot\.

`Id`  <a name="Id-fn::getatt"></a>
The unique identifier of the bot\.

## Examples<a name="aws-resource-lex-bot--examples"></a>



### Order flowers example bot<a name="aws-resource-lex-bot--examples--Order_flowers_example_bot"></a>

The example creates a bot to order flowers\. It is the same as the example bot that you can create using the console\. 

#### YAML<a name="aws-resource-lex-bot--examples--Order_flowers_example_bot--yaml"></a>

```
# The OrderFlower bot consists of the following:
# 1. IAM role that is used by the bot at runtime
# 2. Inline Bot
# 3. Bot Version
# 4. Alias
Resources:
  # 1. IAM Role used by the Lex service to make runtime calls
  BotRuntimeRole:
    Type: AWS::IAM::Role
    Properties:
      AssumeRolePolicyDocument:
        Version: "2012-10-17"
        Statement:
          - Effect: Allow
            Principal:
              Service:
                - lexv2.amazonaws.com
            Action:
              - "sts:AssumeRole"
      Path: "/"
      Policies:
        - PolicyName: LexRuntimeRolePolicy
          PolicyDocument:
            Version: 2012-10-17
            Statement:
              - Effect: Allow
                Action:
                  - "polly:SynthesizeSpeech"
                  - "comprehend:DetectSentiment"
                Resource: "*"
 
  # 2. Inline bot definition that depends on the IAM role.
  # The bot definition consists of combining all the child resources into one CFN resource.
  # This includes Locales, Intents, Slots, and SlotTypes.
  OrderFlowersTemplateBot:
    DependsOn: BotRuntimeRole
    Type: AWS::Lex::Bot
    Properties:
      Name: "OrderFlowersWithCFN"
      RoleArn: !GetAtt BotRuntimeRole.Arn
      DataPrivacy:
        ChildDirected: false
      IdleSessionTTLInSeconds: 300
      Description: "How to create a OrderFlowers bot with CFN"
      # We provide a setting that allows you to auto build the locales provided.
      # Locale builds are also kicked off if you attempt to create a bot version 
      # that depends on an unbuilt locale.
      AutoBuildBotLocales: false
      BotLocales:
        - LocaleId: "en_US"
          Description: "Book a trip bot Locale"
          NluConfidenceThreshold: 0.40
          VoiceSettings:
            VoiceId: "Ivy"
          SlotTypes:
            - Name: "FlowerTypes"
              Description: "Slot Type description"
              SlotTypeValues:
                - SampleValue:
                    Value: lilies
                - SampleValue:
                    Value: roses
                - SampleValue:
                    Value: tulips
              ValueSelectionSetting:
                ResolutionStrategy: ORIGINAL_VALUE
          Intents:
            - Name: "OrderFlowers"
              Description: "Intent to order a bouquet of flowers for pick up"
              SampleUtterances:
                - Utterance: "I would like to pick up flowers"
                - Utterance: "I would like to order some flowers"
              IntentConfirmationSetting:
                PromptSpecification:
                  MessageGroupsList:
                    - Message:
                        PlainTextMessage:
                          Value: "Okay, your {FlowerType} will be ready for pickup by {PickupTime} on {PickupDate}.  Does this sound okay?"
                  MaxRetries: 3
                  AllowInterrupt: false
                DeclinationResponse:
                  MessageGroupsList:
                    - Message:
                        PlainTextMessage:
                          Value: "Okay, I will not place your order."
                  AllowInterrupt: false
              SlotPriorities:
                - Priority: 2
                  SlotName: PickupDate
                - Priority: 1
                  SlotName: FlowerType
                - Priority: 3
                  SlotName: PickupTime
              Slots:
                - Name: "FlowerType"
                  Description: "something"
                  SlotTypeName: "FlowerTypes"
                  ValueElicitationSetting:
                    SlotConstraint: "Required"
                    PromptSpecification:
                      MessageGroupsList:
                        - Message:
                            PlainTextMessage:
                              Value: "What type of flowers would you like to order?"
                      MaxRetries: 3
                      AllowInterrupt: false
                - Name: "PickupDate"
                  Description: "something"
                  SlotTypeName: "AMAZON.Date"
                  ValueElicitationSetting:
                    SlotConstraint: "Required"
                    PromptSpecification:
                      MessageGroupsList:
                        - Message:
                            PlainTextMessage:
                              Value: "What day do you want the {FlowerType} to be picked up?"
                      MaxRetries: 3
                      AllowInterrupt: false
                - Name: "PickupTime"
                  Description: "something"
                  SlotTypeName: "AMAZON.Time"
                  ValueElicitationSetting:
                    SlotConstraint: "Required"
                    PromptSpecification:
                      MessageGroupsList:
                        - Message:
                            PlainTextMessage:
                              Value: "At what time do you want the {FlowerType} to be picked up?"
                      MaxRetries: 3
                      AllowInterrupt: false
            - Name: "FallbackIntent"
              Description: "Default intent when no other intent matches"
              ParentIntentSignature: "AMAZON.FallbackIntent"
 
  # 3. Define a bot version that depends on the DRAFT version of the Lex Bot.
  OrderFlowersTemplateBotVersionWithCFN:
    DependsOn: OrderFlowersTemplateBot
    Type: AWS::Lex::BotVersion
    Properties:
      BotId: !Ref OrderFlowersTemplateBot
      BotVersionLocaleSpecification:
        - LocaleId: en_US
          BotVersionLocaleDetails:
            SourceBotVersion: DRAFT
      Description: OrderFlowers Version
 
  # 4. Define the alias by providing the bot version created by the 
  #    AWS::Lex::BotVersion resource above.
  FirstBotAliasWithCFN:
    DependsOn: OrderFlowersTemplateBotVersionWithCFN
    Type: AWS::Lex::BotAlias
    Properties:
      BotId: !Ref OrderFlowersTemplateBot
      BotAliasName: "OrderFlowersVersion1Alias"
      BotVersion: !GetAtt OrderFlowersTemplateBotVersionWithCFN.BotVersion
      SentimentAnalysisSettings:
        DetectSentiment: true
```

### Book trip example bot<a name="aws-resource-lex-bot--examples--Book_trip_example_bot"></a>

The example creates a bot to book hotel rooms and rental cars\. It is the same as the example bot that you can create using the console\. 

#### YAML<a name="aws-resource-lex-bot--examples--Book_trip_example_bot--yaml"></a>

```
# The BookTrip bot consists of the following:
# 1. IAM role that is used by the bot at runtime
# 2. Inline Bot
# 3. Bot Version
# 4. Alias
Resources:
  # 1. IAM Role used by the Lex service to make runtime calls
  BotRuntimeRole:
    Type: AWS::IAM::Role
    Properties:
      AssumeRolePolicyDocument:
        Version: "2012-10-17"
        Statement:
          - Effect: Allow
            Principal:
              Service:
                - lexv2.amazonaws.com
            Action:
              - "sts:AssumeRole"
      Path: "/"
      Policies:
        - PolicyName: LexRuntimeRolePolicy
          PolicyDocument:
            Version: 2012-10-17
            Statement:
              - Effect: Allow
                Action:
                  - "polly:SynthesizeSpeech"
                  - "comprehend:DetectSentiment"
                Resource: "*"
 
  # 2. Inline bot definition which depends on the IAM role
  # The bot definition consists of combining all the child resources into one CFN resource.
  # This includes Locales, Intents, Slots, and SlotTypes.
  BookTripTemplateBot:
    DependsOn: BotRuntimeRole
    Type: AWS::Lex::Bot
    Properties:
      Name: "BookTripWithCFN"
      RoleArn: !GetAtt BotRuntimeRole.Arn
      DataPrivacy:
        ChildDirected: false
      IdleSessionTTLInSeconds: 300
      Description: "How to create a BookTrip bot with CFN"
      # Provide a setting that allows you to either auto build the locales provided.
      # Locale builds are also kicked off if you attempt to create a bot version 
      # that depends on an unbuilt locale.
      AutoBuildBotLocales: false
      BotLocales:
        - LocaleId: "en_US"
          Description: "Book a trip bot Locale"
          NluConfidenceThreshold: 0.40
          VoiceSettings:
            VoiceId: "Ivy"
          SlotTypes:
            - Name: "CarTypeValues"
              Description: "Slot Type description"
              SlotTypeValues:
                - SampleValue:
                    Value: economy
                - SampleValue:
                    Value: standard
                - SampleValue:
                    Value: midsize
                - SampleValue:
                    Value: full size
                - SampleValue:
                    Value: luxury
                - SampleValue:
                    Value: minivan
              ValueSelectionSetting:
                ResolutionStrategy: ORIGINAL_VALUE
            - Name: "RoomTypeValues"
              Description: "Slot Type description"
              SlotTypeValues:
                - SampleValue:
                    Value: queen
                - SampleValue:
                    Value: king
                - SampleValue:
                    Value: deluxe
              ValueSelectionSetting:
                ResolutionStrategy: ORIGINAL_VALUE
          Intents:
            - Name: "BookCar"
              Description: "Intent to book a car on StayBooker"
              SampleUtterances:
                - Utterance: "Book a car"
                - Utterance: "Reserve a car"
                - Utterance: "Make a car reservation"
              SlotPriorities:
                - Priority: 4
                  SlotName: DriverAge
                - Priority: 1
                  SlotName: PickUpCity
                - Priority: 3
                  SlotName: ReturnDate
                - Priority: 5
                  SlotName: CarType
                - Priority: 2
                  SlotName: PickUpDate 
              IntentConfirmationSetting:
                PromptSpecification:
                  MessageGroupsList:
                    - Message:
                        PlainTextMessage:
                          Value: "Okay, I have you down for a {CarType} rental in {PickUpCity} from {PickUpDate} to {ReturnDate}.  Should I book the reservation?"
                  MaxRetries: 3
                  AllowInterrupt: false
                DeclinationResponse:
                  MessageGroupsList:
                    - Message:
                        PlainTextMessage:
                          Value: "Okay, I have cancelled your reservation in progress."
                  AllowInterrupt: false
              Slots:
                - Name: "PickUpCity"
                  Description: "something"
                  SlotTypeName: "AMAZON.City"
                  ValueElicitationSetting:
                    SlotConstraint: "Required"
                    PromptSpecification:
                      MessageGroupsList:
                        - Message:
                            PlainTextMessage:
                              Value: "In what city do you need to rent a car?"
                      MaxRetries: 3
                      AllowInterrupt: false
                - Name: "PickUpDate"
                  Description: "something"
                  SlotTypeName: "AMAZON.Date"
                  ValueElicitationSetting:
                    SlotConstraint: "Required"
                    PromptSpecification:
                      MessageGroupsList:
                        - Message:
                            PlainTextMessage:
                              Value: "What day do you want to start your rental?"
                      MaxRetries: 3
                      AllowInterrupt: false
                - Name: "ReturnDate"
                  Description: "something"
                  SlotTypeName: "AMAZON.Date"
                  ValueElicitationSetting:
                    SlotConstraint: "Required"
                    PromptSpecification:
                      MessageGroupsList:
                        - Message:
                            PlainTextMessage:
                              Value: "What day do you want to return the car?"
                      MaxRetries: 3
                      AllowInterrupt: false
                - Name: "DriverAge"
                  Description: "something"
                  SlotTypeName: "AMAZON.Number"
                  ValueElicitationSetting:
                    SlotConstraint: "Required"
                    PromptSpecification:
                      MessageGroupsList:
                        - Message:
                            PlainTextMessage:
                              Value: "How old is the driver for this rental?"
                      MaxRetries: 3
                      AllowInterrupt: false
                - Name: "CarType"
                  Description: "something"
                  SlotTypeName: "CarTypeValues"
                  ValueElicitationSetting:
                    SlotConstraint: "Required"
                    PromptSpecification:
                      MessageGroupsList:
                        - Message:
                            PlainTextMessage:
                              Value: "What type of car would you like to rent?  Our most popular options are economy, midsize, and luxury"
                      MaxRetries: 3
                      AllowInterrupt: false
            # We expect developers to provide the FallbackIntent when generating their bot.
            # The service will throw an exception if it isn't provided.
            - Name: "BookHotel"
              Description: "Intent to book a hotel on StayBooker"
              SampleUtterances:
                - Utterance: "Book a hotel"
                - Utterance: "I want a make hotel reservations"
                - Utterance: "Book a {Nights} night stay in {Location}"
              IntentConfirmationSetting:
                PromptSpecification:
                  MessageGroupsList:
                    - Message:
                        PlainTextMessage:
                          Value: "Okay, I have you down for a {Nights} night stay in {Location} starting {CheckInDate}.  Shall I book the reservation?"
                  MaxRetries: 3
                  AllowInterrupt: false
                DeclinationResponse:
                  MessageGroupsList:
                    - Message:
                        PlainTextMessage:
                          Value: "Okay, I have cancelled your reservation in progress."
                  AllowInterrupt: true
              SlotPriorities:
                - Priority: 4
                  SlotName: RoomType
                - Priority: 1
                  SlotName: Location
                - Priority: 3
                  SlotName: Nights
                - Priority: 2
                  SlotName: CheckInDate 
              Slots:
                - Name: "Location"
                  Description: "something"
                  SlotTypeName: "AMAZON.City"
                  ValueElicitationSetting:
                    SlotConstraint: "Required"
                    PromptSpecification:
                      MessageGroupsList:
                        - Message:
                            PlainTextMessage:
                              Value: "What city will you be staying in?"
                      MaxRetries: 3
                      AllowInterrupt: false
                - Name: "CheckInDate"
                  Description: "something"
                  SlotTypeName: "AMAZON.Date"
                  ValueElicitationSetting:
                    SlotConstraint: "Required"
                    PromptSpecification:
                      MessageGroupsList:
                        - Message:
                            PlainTextMessage:
                              Value: "What day do you want to check in?"
                      MaxRetries: 3
                      AllowInterrupt: false
                - Name: "Nights"
                  Description: "something"
                  SlotTypeName: "AMAZON.Number"
                  ValueElicitationSetting:
                    SlotConstraint: "Required"
                    PromptSpecification:
                      MessageGroupsList:
                        - Message:
                            PlainTextMessage:
                              Value: "How many nights will you be staying?"
                      MaxRetries: 3
                      AllowInterrupt: false
                - Name: "RoomType"
                  Description: "something"
                  SlotTypeName: "RoomTypeValues"
                  ValueElicitationSetting:
                    SlotConstraint: "Required"
                    PromptSpecification:
                      MessageGroupsList:
                        - Message:
                            PlainTextMessage:
                              Value: "What type of room would you like, queen, king or deluxe?"
                      MaxRetries: 3
                      AllowInterrupt: false
            - Name: "FallbackIntent"
              Description: "Default intent when no other intent matches"
              ParentIntentSignature: "AMAZON.FallbackIntent"
 
  # 3. Define a bot version which depends on the DRAFT version of the Lex Bot
  BookTripBotVersionWithCFN:
    DependsOn: BookTripTemplateBot
    Type: AWS::Lex::BotVersion
    Properties:
      BotId: !Ref BookTripTemplateBot
      BotVersionLocaleSpecification:
        - LocaleId: en_US
          BotVersionLocaleDetails:
            SourceBotVersion: DRAFT
      Description: BookTrip Version
 
  # 4. We define the alias by providing the bot version created by the AWS::Lex::BotVersion resource above
  FirstBotAliasWithCFN:
    DependsOn: BookTripBotVersionWithCFN
    Type: AWS::Lex::BotAlias
    Properties:
      BotId: !Ref BookTripTemplateBot
      BotAliasName: "BookTripVersion1Alias"
      # Remove BotAliasLocaleSettings if you aren't concerned with Lambda setup.
      # If you are you can modify the LambdaArn below to get started.
      # BotAliasLocaleSettings:
      #   - LocaleId: en_US
      #     BotAliasLocaleSetting:
      #       Enabled: false
      #       CodeHookSpecification: 
      #         LambdaCodeHook:
      #           CodeHookInterfaceVersion: "1.0"
      #           LambdaArn: "arn:aws:lambda:us-east-1:111111111111:function:ReplaceWithYourOwnLambda"
      BotVersion: !GetAtt BookTripBotVersionWithCFN.BotVersion
      SentimentAnalysisSettings:
        DetectSentiment: true
```