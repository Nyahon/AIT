#AIT - présentation AWS glacier & Arq

##AWS Glacier

### 1. concept

The data are stored in archive form and are contained in vaults. Vaults are accesible to add/modify/delete through the AWS SDK. 

---

###2. informations

* *archives*

  * max. 40 TB per archive (any type file)

  * immutable

* *vaults*

  * max 1000 per account

* *storage costs*

  * $0.0045 per GB / Month

* *data upload*

  * $0.06 per 1,000 Requests

* *data retrieval*

  | Type                    | Availability                         | Cost                                       |
  | ----------------------- | ------------------------------------ | ------------------------------------------ |
  | Expedited (On-demand)   | 1-5 minutes **as possible** (<250MB) | \$0.03/GB +  \$0.012/request.              |
  | Expedited (provisioned) | 1-5 minutes **guaranteed** (<250MB)  | \$0.03/GB +  \$0.012/request + $100/month. |
  | Standard                | 3-5 hours                            | \$0.01/GB +  \$0.05/1000 requests.         |
  | Bulk                    | 5-12 hours                           | \$0.0025/GB +  \$0.025/1000 requests.      |

---

###3. features

* *Range retrievals*
  * allow retrieval of a partial archive based on range given by the user.
* *Select*
  * allows queries to run directly on data stored in Amazon Glacier without having to retreive the entire archive.
* *Vault policy*
  * Allow to tune policies by individual vaults (like WORM - write once read many)
* *Access control*
* *Audit logs*
* *Vault inventory*
  * Glacier maintain a list of all files on vaults. Update once a day.
* *AWS Management Console*
  * an easy-to-use web interface that provides the capability to create 
    vaults, configure vault-level access permissions, and set up SNS 
    notifications for data retrieval.
* *Encryption by default*
* *AWS SDK*
  * Low-level API
  * High-level API