Role Name
=========

NodeJS and MongoDB Setup

Requirements
------------

- You must have [ansible](https://www.ansible.com/) installed.
- You must have [aws-cli](https://aws.amazon.com/cli/?nc1=h_ls) installed.
- You must [configure your aws-cli](http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html)


Usage
-----

To run this playbook you should do like the following:

    cd ansible
    ansible-playbook main.yml -i ec2.py --private-key=<ec2_private_key> [-e key=value] #list of variables

    
Playbook Variables
------------------

    aws_ec2_name: The Tag Name of AWS EC2 Machine


Example of Usage with Variables
-------------------------------
    ansible-playbook main.yml -i ec2.py --private-key=<ec2_private_key> -e -e aws_ec2_name=foo