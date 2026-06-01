* AWS Organization-level compliance system using Config + StackSets to automatically detect and remediate non-compliant resources across all accounts in the Organisation.



This solution is designed for organization-wide cloud governance and compliance at scale using AWS Config and CloudFormation StackSets.

With AWS Config rules deployed via CloudFormation StackSets, we can automatically enforce compliance policies across all accounts in an AWS Organization including newly added accounts without manual intervention.



With growing AWS accounts and evolving security requirements, we cannot realistically monitor and audit every resource manually. This solution provides organization-wide visibility and automated compliance enforcement, ensuring all accounts follow the same security and governance standards.



The solution is designed to be flexible and customizable. It supports resource exclusions, inclusion or exclusion of global resource types, service-specific recording overrides, and custom recording frequencies. This allows organizations to tailor AWS Config monitoring based on their operational, compliance, and cost requirements while maintaining a consistent governance framework.



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