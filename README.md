Role Name
=========

Wordpress Setup

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

    title: #Title of wordpress installation
    admin_name: #Admin Username
    admin_password: #Admin User password
    admin_email: #Admin User Email
    
    db_name: #Database name
    db_user: #Database User
    db_password: #Database User password
    db_host: #Optional
    domain: #Domain name WITHOUT WWW
    aws_ec2_name: The Tag Name of AWS EC2 Machine


Example of Usage with Variables
-------------------------------
    ansible-playbook main.yml -i ec2.py --private-key=<ec2_private_key> -e title=foo -e admin_name=foo -e admin_password=foo -e admin_email:foo@foo.com -e db_name=foo -e db_user=foo -e db_password=foo -e domain=foo.com -e aws_ec2_name=foo