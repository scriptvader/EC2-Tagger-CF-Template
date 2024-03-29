# EC2-Tagger-CF-Template
This cloud formation template automatically adds specified tags to newly created EC2 instances.
Especially useful to force EC2 instances in an environment to always have certain tags.

## Description
This AWS CloudFormation Template deploys a Lambda function triggered by an EventBridge rule that detects instance creation.

<img width="700" alt="image" src="https://github.com/scriptvader/EC2-Tagger-CF-Template/assets/28531392/d36e7809-1fda-4169-a49a-3473f80fe6ee">

The template takes in the tag key and values as parameters. Any number of tags, one or more can be passed. 

For more than one tag, the keys and values should be passed as comma seperated values.
The number and order of the keys and values should be the same.

For example the following set ok keys and values...

* Keys: ID, Region, Fruit
* Values: 117, London, Apple

...will create the tags

* ID: 117
* Region: London
* Fruit: Apple

The code will fail if the size of both lists do not match.

## AWS Resource Costs

As with most AWS services you will incur costs for usage. For this CloudFormation template the resources that incur costs are as follows

* Pricing:
  * <a href="https://aws.amazon.com/lambda/pricing/">Lambda pricing</a>
  * <a href="https://aws.amazon.com/eventbridge/pricing/">EventBridge pricing</a>




