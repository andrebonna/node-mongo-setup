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
    project_folder: Name of the project folder
    src_project_path: Path of the source project folder # /home/user/project_folder
    dest_project_path: Path of the destination project folder # Ex: /home/ubuntu
    main_js: Ex: index #Optional
    main_file: Ex: "index.js" #Optional

Example of Usage with Variables
-------------------------------
    ansible-playbook main.yml -i ec2.py --private-key=<ec2_private_key> -e -e aws_ec2_name=foo