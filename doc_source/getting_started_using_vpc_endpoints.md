# Using Cloud Directory Interface VPC Endpoints<a name="getting_started_using_vpc_endpoints"></a>

If you use Amazon Virtual Private Cloud \(Amazon VPC\) to host your AWS resources, you can establish a private connection between your VPC and Cloud Directory\. You can use this connection to enable Cloud Directory to communicate with your resources on your VPC without going through the public internet\.

Amazon VPC is an AWS service that you can use to launch AWS resources in a virtual network that you define\. With a VPC, you have control over your network settings, such as the IP address range, subnets, route tables, and network gateways\. To connect your VPC to Cloud Directory, you define an *interface VPC endpoint* for Cloud Directory\. The endpoint provides reliable, scalable connectivity to Cloud Directory without requiring an internet gateway, network address translation \(NAT\) instance, or VPN connection\. For more information, see [What Is Amazon VPC?](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Introduction.html) in the *Amazon VPC User Guide*\.

Interface VPC endpoints are powered by AWS PrivateLink, an AWS technology that enables private communication between AWS services using an elastic network interface with private IP addresses\. For more information, see [AWS PrivateLink for AWS Services](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Introduction.html#what-is-privatelink)\.

The following steps are for users of Amazon VPC\. For more information, see [Getting Started with Amazon VPC](https://docs.aws.amazon.com/vpc/latest/userguide/GetStarted.html) in the *Amazon VPC User Guide*\.

## Availability<a name="vpc_endpoints_availability"></a>

Cloud Directory currently supports VPC endpoints in the following Regions:
+ US East \(Ohio\)
+ US East \(N\. Virginia\)
+ US West \(Oregon\)
+ Asia Pacific \(Singapore\)
+ Asia Pacific \(Sydney\)
+ Canada \(Central\)
+ EU \(Frankfurt\)
+ EU \(Ireland\)
+ EU \(London\)

## Create a VPC for Cloud Directory<a name="vpc_endpoints_create"></a>

To start using Cloud Directory with your VPC, use the Amazon VPC console to create an interface VPC endpoint for Cloud Directory\. For detailed instructions, see the procedure "To create an interface endpoint to an AWS server using the console" in [Creating an Interface Endpoint](https://docs.aws.amazon.com/vpc/latest/userguide/vpce-interface.html#create-interface-endpoint) within the *Amazon VPC User Guide*\. When you get to the step in the procedure that asks to select a **Service Name**, choose **`com.amazonaws.region.clouddirectory`** to create a VPC endpoint for Cloud Directory operations\.

For general information, see [What is Amazon VPC](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html) in the *Amazon VPC User Guide*\.