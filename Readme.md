* AWS Organization-level compliance system using Config + StackSets to automatically detect and remediate non-compliant resources across all accounts in the Organisation.


As organizations grow, managing compliance manually across multiple AWS accounts becomes increasingly difficult. Security standards, governance requirements, and operational policies need to be enforced consistently across the entire organization to reduce risk and maintain compliance.

This solution leverages AWS Config and CloudFormation StackSets to automatically deploy and enforce compliance controls across all accounts within an AWS Organization. New accounts can automatically inherit the same governance framework without requiring manual configuration.

The stack is designed to be flexible and customizable, supporting resource exclusions, inclusion or exclusion of global resource types, service-specific recording overrides, and custom recording frequencies. This allows organizations to tailor monitoring and compliance controls based on their requirements.

In addition, the solution integrates with Amazon SNS to send email notifications whenever non-compliant resources are detected, providing near real-time visibility into compliance violations across the organization. AWS Config data and compliance snapshots are also delivered to Amazon S3 for centralized storage, auditing, and reporting purposes.

The framework can be extended further by attaching remediation actions, such as terminating non-compliant resources, invoking AWS Lambda functions, or triggering AWS Systems Manager Automation documents, enabling automated enforcement of organizational security policies.


Key capabilities:

* Centralized compliance monitoring

   ** Track all AWS resources across multiple accounts

   ** Detect non-compliant resources in real time

 

* Organization-wide enforcement using StackSets 

   ** Automatically deploy Config rules to every account in AWS Organization

   ** Ensure consistent governance across all environments (dev/stage/prod) 



* Automated remediation 

  ** Trigger actions when non-compliance is detected

  ** Example: terminate non-compliant EC2 instances 

  ** or invoke custom remediation workflows using Lambda / SSM



* Scalable governance model

  ** Add new Config rules over time without redesigning architecture

  ** Policies evolve with organizational security requirements



* Outcome:

This creates a self-healing, policy-driven cloud environment where compliance is continuously enforced rather than manually audited.


* Architecture

![alt text](<Screenshot 2026-06-01 202254.png>)