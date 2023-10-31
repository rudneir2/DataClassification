# WAF20 - Data Classification (draft)

**NOTE:** 
This content below is supposed to be part of the WAF 20 document, to be embedded in the chapter "WAF>Recommendations>SE:03 Data Classification".

[https://review.learn.microsoft.com/en-us/azure/well-architected/security/networking?branch=collab-waf-2-0-1](https://review.learn.microsoft.com/en-us/azure/well-architected/security/data-classification?branch=release-waf-2-0-1)

## Introduction / Use case

Well Architected Framework **Data Classification** provides recommendations for categorizing data based on criteria set by your company according to the sensitive, type of data and compliance required.

Data used by Company's workload may be stored in different resources, regardless the security, performance, scalability or capacity, that your company stabilish for your data.
The diagram below show some of the common examples where you may have data stored and used by different workoads, accessed by different systems and personas, such as your employees, customers and the bad actors, trying to compromise your data.

**NOTE**
It is out of scope for this article to explain:
- how different disk storage technologies works
- database technologies works
- all security solution available for disk storage such as file, blobs and databases

<<diagram image goes here>>

Let's consider the following in the diagram:

1. It is common companies protect their data stored on databases and disks, so only few users, as Administrators and Database administrator may have access to it. Then, it is usual that common users or customer's final clients have access only to layers that are exposed to the internet, such as Web Applications or Jump Servers.
2. Then, those Web Applications finally communicate with the database servers or data stored on disks, such as object storage or file servers.
3. There are some companies that build their business continuity, as high availabilit or disaster recovery, for their database between on-premises environment and the public cloud, so you need to take care of your data in both sites.
4. There are also scenarios where Remote administrators have to access Jump servers on the cloud, or sometimes a specific workload directly on the Virtual Machines.
5. Those VMs then communicate with the database, such as datawarehouse, relational database, no-sql DB or storage behind it.
6. in small companies or non critical workloads, companies may store data directly in disk VMs, that is not recommended. So, in somehow, you will need to take care of those data as well.
7. in hybrid environment, different personas, such as external developers, remote admins, remote employees, may access workloads on-premises through different means such as VPNs, RDPs, SSH, etc, that then will connect in different data storage technologies.
8. as on the public cloud, those servers may connect to important data, that need to be classified and protected, such as file servers, object storages, and different types of databases, such as relational, no-SQL and datawarehouse.

**Azure Security services has many security services that protect Storage services mentioned above, and also security solutions for different types of database technologies, not only for transactional databases, but also for analytical and big data solution. It is out of scope, covering those solutions, but you may find more about in this link **putlinkhere**.**

9. Microsoft Purview Compliance provides a solution to classify files and emails (not covered in this article), that helps in your data classification.
10. Microsoft Defender for Cloud provides a solution that helps your company to track compliance in your environment, including many of your services used to store data, mentioned in these use cases above.

The above examples are only a few of the common scenario found in many companies so you may have a better understand of the recommendations found in this article.

**NOTE:**
If you'd like to understand more about any solution described in the diagram, including acronyms, please refer to this table of contents, from the Baseline chapter.
(table to be built)

In the following content, you will find more details about **Data Classification** that you will be able to apply in your environment for a better Security posture.

**from this point on, we could add the current draft content for Data Classification **
