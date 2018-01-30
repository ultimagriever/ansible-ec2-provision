# AWS Provisioner

This [Ansible](https://docs.ansible.com) playbook was
created to provision a fully secure, fault-tolerant
[Amazon Web Services](https://aws.amazon.com) environment
to host and deploy your NodeJS/MongoDB apps. This provisioner
creates the following resources on your account (therefore,
you need an IAM user with said create/attach privileges):

* [Elastic Compute Cloud (EC2)](https://aws.amazon.com/ec2)
* [Simple Storage Service (S3)](https://aws.amazon.com/s3)
* [Elastic Block Store (EBS)](https://aws.amazon.com/ebs)
* [Virtual Private Cloud (VPC)](https://aws.amazon.com/vpc)
* [CloudFront](https://aws.amazon.com/cloudfront)
* [Route 53](https://aws.amazon.com/route53)
* [Elastic Load Balancing (ELB)](https://aws.amazon.com/elasticloadbalancing)
* [CodeDeploy](https://aws.amazon.com/codedeploy)
* [Identity and Access Management (IAM)](https://aws.amazon.com/iam)

**Important**: running this playbook against your AWS
account might incur charges related to each product's
pricing, regardless of Free Tier usage.

## Control Machine Configuration

To run this playbook, you need to install the [AWS CLI](https://aws.amazon.com/cli)
and configure your environment.

```bash
# Set your AWS Access Key/Secret Key
aws configure

# Run the Ansible playbook
AWS_PROFILE=default ansible-playbook playbook.yml -i hosts
```