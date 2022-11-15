# Classic Architecture

Keywords: storage, route & vpc

## EBS General Purpose SSD (gp2) storage vs. EBS Provision IOPS SSD (io1) storage

## AWS

### SSD

1. 一個是適用於交易工作負載的 SSD 支援儲存，如資料庫、虛擬桌面和開機磁碟區
2. 適用於您最嚴苛交易應用程式 (如 SAP HANA、Microsoft SQL Server 和 IBM DB2) 的最高效能 EBS 磁碟區 (io2 和 io1)
3. 可平衡交易應用程式 (如虛擬桌面、測試和開發環境及互動式遊戲應用程式) 價格和效能的一般用途 SSD 磁碟區 (gp3 和 gp2)

### HDD

1. 適用於輸送量密集型工作負載的 HDD 支援儲存，如 MapReduce 和日誌處理。
2. HDD 型磁碟區包含適用於經常存取、輸送量密集型工作負載的輸送量最佳化 HDD (st1)，以及適用於較不常存取資料的最低成本冷 HDD (sc1)。

### IOPS vs. throughput vs. latency

`#Measuring Storage Performance`

1. IOPS
    1. Input/Output operations per second
    2. Measures the number of storage transactions processed through a system each second. This metric is a great way to __measure smaller data objects like web traffic logs__.
2. throughput
    1. mount of data able to flow through a point in the data path over a given time
    2. Best storage metric when measuring data that needs to be streamed rapidly, such as images and video files.
3. latency
    1. the time required for a sub-system to process a single data request or transaction
4. IOPS vs. throughput
    1. throughput is the actual measurement of read/write bits per second that are transferred over a network.
* Doc: [storage-performance-metrics](https://www.parkplacetechnologies.com/blog/storage-performance-metrics/)

## SAML, IAM, identity federation

1. integrate AWS IAM with an on-premise LDAP (Lightweight Directory Access Protocol) directory service
* Doc: [Providing access to externally authenticated users (identity federation)](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_common-scenarios_federated-users.html)

### SAML
1. SAML 是 Security Assertion Markup Language
2. 是指在身分識別資訊提供者（Identity Provider，IdP）與服務提供者（Service Provider，SP）之間傳送驗證以及授權資料的一種公開標準。
* Doc: [what-is-saml](https://hennge.com/tw/blog/what-is-saml.html)
* Doc: [Azure auth-saml](https://learn.microsoft.com/zh-tw/azure/active-directory/fundamentals/auth-saml)

### LDAP

1. 輕型目錄存取協定（英文：Lightweight Directory Access Protocol，縮寫：LDAP，/ˈɛldæp/）是一個開放的，中立的，工業標準的應用協定，通過IP協定提供存取控制和維護分散式資訊的目錄資訊。
* Doc: [輕型目錄存取協定](https://zh.wikipedia.org/zh-tw/%E8%BD%BB%E5%9E%8B%E7%9B%AE%E5%BD%95%E8%AE%BF%E9%97%AE%E5%8D%8F%E8%AE%AE)

## EC2

You have an environment that consists of a public subnet using Amazon VPC and 3 instances that are running in this subnet. These three instances can successfully commnuicate with other hosts on the internet. You launch a fourth instance in the same subnet, using the same AMI and security group configuration you used for the others, but find that this instance cannot be accessed from the internet. What should you do to enable internet access?

## AWS VPN