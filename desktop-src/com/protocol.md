---
title: Protocol
description: Indicates that this OLE 2 class is insertable in OLE 1 containers.
ms.assetid: 'a53a1edf-f374-4cbf-8050-7cde45284157'
keywords: ["Protocol registry key COM"]
---

# Protocol

Indicates that this OLE 2 class is insertable in OLE 1 containers.

## Registry Entry

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Protocol
         StdFileEditing
            Server = path
            Verb
               0 = verb1
               1 = verb2
               ...
```

## Remarks

The **StdFileEditing** entry specifies OLE 1 compatibility information. It should be present only if objects of this class are insertable in OLE 1 containers.

**Server** specifies the full path to the OLE 2 server application and **Verb** specifies the verbs. Verb 0 is the primary verb and additional verbs must be numbered consecutively.

 

 



