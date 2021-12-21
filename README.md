# Secureworks Taegis Log4j / Log4shell Analysis 

A collection of released technical information from [Secureworks](https://secureworks.com) surrounding the exploitation of CVE-2021-44228, known as the log4j / log4shell vulnerability. 

The analysis here originates from our flagship security platform, [Taegis](https://www.secureworks.com/products/taegis/xdr), which collects security related events from a wide reaching set of visibility points from network devices, endpoint agents, and cloud service providers. Given the variety and scale of our Taegis customer base, we can provide insight into log4j exploitation attempts observed in-the-wild. 

## Description of taegis-log4j-ip-analysis.tsv

Some of the observed log4j-related events within Taegis exhibit characteristics beyond the security community’s vulnerability scans or exploratory research activities. For example, Taegis-observed log4j exploitation attempts include encoded commands to download malicious initial access scripts, jumpstart crypto-miners, exfiltrate credentials found on the target, record confirmed vulnerable status for later exploitation, or include carefully crafted data to initiate remote shells. 

To aid in the collective defense of all of our networks, and in the spirit of responding to emergencies as a global security community, we are releasing IP addresses that exhibit malicious characteristics beyond the normal scanning and research traffic.

The data released contains a set of columns, as follows:
1. _JNDI Referenced Suspicious IP_: The public IP exhibiting suspicious behavior.
2. _Suspicious Behavior_: A brief description of that suspicious behavior beyond typical scanning or exploratory research.
3. _Example Command/Download_: Specific jdni payload examples from observed in-the-wild exploitation attempts. In many cases, we have redacted information seen within “< … >” markers to protect the identity of victims or other sensitive information. 
4. _Count of IP seen with …_: A set of columns showing the magnitude of observed exploitation attempts within Taegis associated with the suspicious IP where it exhibited specific payload categories. Such as base64 encoding a curl download and execution, or initiating a remote shell directly from jdni, or several other categories we have annotated. 
