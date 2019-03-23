Make sure you create the destination directory (code below assumes /home/cif/CIF_DATA).

You can run the below commands as a cron job to auto update contens.

# To get ipv4 based indicators
cif --itype ipv4 --fields itype,tlp,group,firstdetecttime,lastdetecttime,indicator,cc,asn,confidence,tags,description,rdata,provider,altid,altid_tlp --tags phishing,botnet,whitelist,scanner,bruteforce,blacklist,dns,malware,feodo,c2,Malware,wannacry,phishing,botnet,suspicious,spam,spammers,botnet,ssl,tor,zeus -f csv > /home/cif/CIF_DATA/ipv4.csv

# To get fqdn based indicators
cif --itype fqdn --fields itype,tlp,group,firstdetecttime,lastdetecttime,indicator,cc,asn,confidence,tags,description,rdata,provider,altid,altid_tlp --tags phishing,botnet,whitelist,scanner,bruteforce,blacklist,dns,malware,feodo,c2,Malware,wannacry,phishing,botnet,suspicious,spam,spammers,botnet,ssl,tor,zeus -f csv > /home/cif/CIF_DATA/fqdn.csv

# To get url based indicators
cif --itype url --fields itype,tlp,group,firsttime,lasttime,indicator,cc,asn,confidence,tags,description,rdata,provider,altid,altid_tlp --tags phishing,botnet,whitelist,scanner,bruteforce,blacklist,dns,malware,feodo,c2,Malware,wannacry,phishing,botnet,suspicious,spam,spammers,botnet,ssl,tor,zeus -f csv > /home/cif/CIF_DATA/url.csv

# To get sha1 based indicators
cif --itype sha1 --fields itype,tlp,group,firsttime,lasttime,indicator,cc,asn,confidence,tags,description,rdata,provider,altid,altid_tlp --tags phishing,botnet,whitelist,scanner,bruteforce,blacklist,dns,malware,feodo,c2,Malware,wannacry,phishing,botnet,suspicious,spam,spammers,botnet,ssl,tor,zeus -f csv > /home/cif/CIF_DATA/sha1.csv

# To get sha256 based indicators
cif --itype sha256 --fields itype,tlp,group,firsttime,lasttime,indicator,cc,asn,confidence,tags,description,rdata,provider,altid,altid_tlp --tags phishing,botnet,whitelist,scanner,bruteforce,blacklist,dns,malware,feodo,c2,Malware,wannacry,phishing,botnet,suspicious,spam,spammers,botnet,ssl,tor,zeus -f csv > /home/cif/CIF_DATA/sha256.csv

# To get sha512 based indicators
cif --itype sha512 --fields itype,tlp,group,firsttime,lasttime,indicator,cc,asn,confidence,tags,description,rdata,provider,altid,altid_tlp --tags phishing,botnet,whitelist,scanner,bruteforce,blacklist,dns,malware,feodo,c2,Malware,wannacry,phishing,botnet,suspicious,spam,spammers,botnet,ssl,tor,zeus -f csv > /home/cif/CIF_DATA/sha512.csv

# To get md5 based indicators
cif --itype md5 --fields itype,tlp,group,firsttime,lasttime,indicator,cc,asn,confidence,tags,description,rdata,provider,altid,altid_tlp --tags phishing,botnet,whitelist,scanner,bruteforce,blacklist,dns,malware,feodo,c2,Malware,wannacry,phishing,botnet,suspicious,spam,spammers,botnet,ssl,tor,zeus -f csv > /home/cif/CIF_DATA/md5.csv

# To get email based indicators
cif --itype email --fields itype,tlp,group,firsttime,lasttime,indicator,cc,asn,confidence,tags,description,rdata,provider,altid,altid_tlp --tags phishing,botnet,whitelist,scanner,bruteforce,blacklist,dns,malware,feodo,c2,Malware,wannacry,phishing,botnet,suspicious,spam,spammers,botnet,ssl,tor,zeus -f csv > /home/cif/CIF_DATA/email.csv
