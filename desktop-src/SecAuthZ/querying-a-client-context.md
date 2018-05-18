---
Description: 'Applications can call the AuthzGetInformationFromContext function to query information about an existing client context.'
ms.assetid: '32655e54-499e-439e-8d4f-f2b4eaa0b184'
title: Querying a Client Context
---

# Querying a Client Context

Applications can call the [**AuthzGetInformationFromContext**](authzgetinformationfromcontext.md) function to query information about an existing client context.

The *InfoClass* parameter of the [**AuthzGetInformationFromContext**](authzgetinformationfromcontext.md) function takes a value from the [**AUTHZ\_CONTEXT\_INFORMATION\_CLASS**](authz-context-information-class.md) enumeration that specifies what type of information the function queries.

Security attribute variables must be present in the client context if referred to in a conditional expression; otherwise, the conditional expression term referencing them will be evaluated as unknown. For more information on conditional expressions, see the [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md) topic.

## Example

The following example queries the client context created in the example from [Initializing a Client Context](initializing-a-client-context.md) to retrieve the list of [**SIDs**](sid.md) of groups associated with that client context.


```C++
BOOL GetGroupsFromContext(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{

    DWORD                cbSize = 0;
    PTOKEN_GROUPS        pTokenGroups=NULL;
    LPTSTR                StringSid = NULL;
    BOOL                bResult = FALSE;
    int i = 0;

    //Call the AuthzGetInformationFromContext function with a NULL output buffer to get the required buffer size.
    AuthzGetInformationFromContext(hClientContext, AuthzContextInfoGroupsSids, 0, &amp;cbSize, NULL);
    
        
    

    //Allocate the buffer for the TOKEN_GROUPS structure.
    pTokenGroups = (PTOKEN_GROUPS)malloc(cbSize);
    if (!pTokenGroups)
        return FALSE;

    //Get the SIDs of groups associated with the client context. 
    if(!AuthzGetInformationFromContext(hClientContext, AuthzContextInfoGroupsSids, cbSize, &amp;cbSize, pTokenGroups))
    {    
        printf_s("AuthzGetInformationFromContext failed with %d\n", GetLastError);
        free(pTokenGroups);
        return FALSE;
    }

    //Enumerate and display the group SIDs.
    for (i=pTokenGroups->GroupCount-1; i >= 0; --i)
    {
        //Convert a SID to a string.
        if(!ConvertSidToStringSid(
            pTokenGroups->Groups[i].Sid,
            &amp;StringSid
            ))
        {
            LocalFree(StringSid);
            return FALSE;
        }


        wprintf_s(L"%s \n", StringSid);
        
    }

    free(pTokenGroups);

    return TRUE;
}
```



## Related topics

<dl> <dt>

[Adding SIDs to a Client Context](adding-sids-to-a-client-context.md)
</dt> <dt>

[Caching Access Checks](caching-access-checks.md)
</dt> <dt>

[Checking Access with Authz API](checking-access-with-authz-api.md)
</dt> <dt>

[How AccessCheck Works](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[Initializing a Client Context](initializing-a-client-context.md)
</dt> <dt>

[Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 


