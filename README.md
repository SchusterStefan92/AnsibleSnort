
# Launch EC2-instances and install Snort and Filebeat with Ansible

My project for the lecture "Software Development for Cloud Computing"

----------------
This repo contains several ansible playbooks, which help to setup a Snort IDS in AWS.
The first playbook launches ec2-instances with the aws-cli.
We can afterwards install Snort on these newly launched instances, mainly by compiling snort by source.
The last playbook downloads and installs filebeat, which will forward the alerts to a centrally managed Logstash/ELK-Instance.

For further information check the blog.md file.

------------------------

## Step by Step 

1. Setup your Logstash-Elasticsearch-Kibana server
3. Create certificates for ssl between filebeat and logstash 
4. Create a folder in FilebeatFiles called ssl and insert your certificates, which will be used for our secure communication
5. Export your AWS credentials <br>
    export AWS_ACCESS_KEY_ID="you_access_key_id" <br>
    export AWS_SECRET_ACCESS_KEY="your_secret_key" <br>
6. Update the playbooks variables according to your use-case
7. Start the playbooks

---------------

## What this is not

1. A correctly configured snort ruleset - everything, that I added were some dummy files
2. Enterprise-Level Playbooks

--------------
### License
[GNU GENERAL PUBLIC LICENSE Version 3](https://[link](https://www.gnu.org/licenses/gpl-3.0))

