I need a quick clarification on the CrowdStrike health dashboard request. From my understanding, this looks more aligned with SRE scope rather than CD-TOOLS, as it involves endpoint health monitoring and integrations. Can you please confirm whether we should take this up under CD-TOOLS or route it to the SRE team / check with the CD-TOOLS owner first?


I also wanted to check if we have an existing document or defined process that clearly outlines what falls under the CD-TOOLS scope and what doesn’t. Recently, we’ve been receiving many new types of requests where the scope isn’t very clear at our level, and we often need to reach out to SMEs each time for confirmation. Having a centralized doc or decision framework would really help streamline this and reduce back-and-forth. If something already exists, could you please share it? Otherwise, happy to help contribute towards creating one.



Nagaraju and I had a call with Ken today. Below are the MOM (Minutes of Meeting):

Ken shared complete details on how we should handle this type of request. Thanks to Ken for clearly explaining the approach.

Currently, there is no defined process or documentation. Ken mentioned that he will prepare and share the documentation soon. We will follow the same for this case and for future requests.”


--------------


Title:
Implement Host Monitoring Automation Using Terraform

Description:
We have developed automation code in Terraform to enable host monitoring across multiple hosts. This solution addresses the requirements raised in the user ticket and is documented in the project wiki. The automation ensures consistent monitoring setup and reduces manual intervention.

Acceptance Criteria:

Terraform code is deployed and successfully configures monitoring for all specified hosts.
Monitoring setup is verified for each host.
Documentation is updated in the wiki, including setup steps and troubleshooting guidelines.
All requirements from the user ticket are addressed.
References:

[Link to Wiki Documentation]
[Link to User Ticket]
Notes:

Multiple hosts are included in the scope as per the user request.
Please refer to the wiki for detailed implementation steps and host list.
