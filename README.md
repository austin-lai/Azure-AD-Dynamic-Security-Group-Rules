# Azure AD Dynamic Security Group - Rules

> Austin Lai | March 13th, 2022

---

<!-- Description -->

A collection of Azure AD Dynamic Security Group - Rules for your reference.

<!-- /Description -->

## Table of Contents

<!-- TOC -->

- [Azure AD Dynamic Security Group - Rules](#azure-ad-dynamic-security-group---rules)
    - [Table of Contents](#table-of-contents)
    - [Dynamic Security Group - Rules](#dynamic-security-group---rules)
        - [**Account Activate or Enabled**](#account-activate-or-enabled)
        - [**Include user base on location**](#include-user-base-on-location)
        - [**Example of a dynamic security group - rules**](#example-of-a-dynamic-security-group---rules)

<!-- /TOC -->

## Dynamic Security Group - Rules

### **Account Activate or Enabled**

```
(user.accountEnabled -eq True)
```

### **Include user base on location**

```
(user.usageLocation -eq "US")

OR

(user.usageLocation -eq "Japan")
```

### **Example of a dynamic security group - rules**

```
user.accountEnabled -eq True and ( user.usageLocation -eq "US" or user.companyName -contains "XXXYYYZZZ" ) and ( user.mail -contains "XXXYYYZZZ.com" and user.mail -notIn ["user1@XXXYYYZZZ.com","user2@XXXYYYZZZ.com"] and user.mail -notIn ["notifications@XXXYYYZZZ.com"])
```

<br />

---

> Do let me know any command or step can be improve or you have any question you can contact me via THM message or write down comment below or via FB
