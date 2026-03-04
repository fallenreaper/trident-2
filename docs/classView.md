# Class View

Definining Class Information initially was done in Figma which will be expanded upon.

## Figma Design

![Class class Image](./images/ClassView.png)

## Mermaid Designs

While the above Figma designs are useful and clean, they are not able to effectively track changes effectively if we want to change definitions over time. This is where Mermaid is more effective.

```mermaid
---
title: Class View
---
classDiagram
    User <-- UserCertification
    User <-- PayrollData
    User --> Company
    Shift --> Company
    Location --> Company
    Location --> Shift
    IncidentReport --> ShiftTasks
    ShiftPay --> Shift
    ShiftTask -- >Shift
    ShiftPay --> PayrollHistory
    class User {
        + int: userId
        + string: f_name
        + string: l_name
        + string: email
        + string: phoneNumber
        + Address: address
        + Datetime: creationDate
        + Datetime: lastLoginDate
    }
    class UserCertification{
        + int: userId
        + string: name
        + string: description
        + Datetime: completionDate
        + Datetime: renewalDate
        + getDocuments(): List~Document~
    }
    class Company {

    }
    class Shift {

    }
    class ShiftTasks {

    }
    class ShiftPay {

    }
    class Location {

    }
    class IncidentReport {

    }
    class PayrollData {

    }
    class PayrollHistory {

    }
```
