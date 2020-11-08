---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: c6351fb39158f7389c0f491a813890373df82cc1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103772"
---
# <span data-ttu-id="4e598-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="4e598-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="4e598-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e598-102">SYNOPSIS</span></span>
<span data-ttu-id="4e598-103">Abonelik için bir güvenlik kişisi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4e598-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="4e598-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4e598-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e598-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4e598-105">DESCRIPTION</span></span>
<span data-ttu-id="4e598-106">Abonelik için bir güvenlik kişisi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4e598-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="4e598-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4e598-107">EXAMPLES</span></span>

### <span data-ttu-id="4e598-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4e598-108">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityContact -Name "default1" -Email "john@contoso.com" -Phone "214275-4038" -AlertAdmin -NotifyOnAlert

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/
                     default1
Name               : default1
Email              : john@contoso.com
Phone              : 214275-4038
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="4e598-109">Abonelik için bir güvenlik kişisi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4e598-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="4e598-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4e598-110">PARAMETERS</span></span>

### <span data-ttu-id="4e598-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="4e598-111">-AlertAdmin</span></span>
<span data-ttu-id="4e598-112">Yöneticilere uyarılar.</span><span class="sxs-lookup"><span data-stu-id="4e598-112">Alerts To Administrators.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e598-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e598-113">-DefaultProfile</span></span>
<span data-ttu-id="4e598-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4e598-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e598-115">-E-posta</span><span class="sxs-lookup"><span data-stu-id="4e598-115">-Email</span></span>
<span data-ttu-id="4e598-116">E-posta.</span><span class="sxs-lookup"><span data-stu-id="4e598-116">E-Mail.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e598-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="4e598-117">-Name</span></span>
<span data-ttu-id="4e598-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="4e598-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e598-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="4e598-119">-NotifyOnAlert</span></span>
<span data-ttu-id="4e598-120">Uyarı bildirimleri.</span><span class="sxs-lookup"><span data-stu-id="4e598-120">Alert Notifications.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e598-121">-Telefon</span><span class="sxs-lookup"><span data-stu-id="4e598-121">-Phone</span></span>
<span data-ttu-id="4e598-122">Telefon.</span><span class="sxs-lookup"><span data-stu-id="4e598-122">Phone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e598-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="4e598-123">-Confirm</span></span>
<span data-ttu-id="4e598-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4e598-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e598-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e598-125">-WhatIf</span></span>
<span data-ttu-id="4e598-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4e598-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e598-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4e598-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e598-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e598-128">CommonParameters</span></span>
<span data-ttu-id="4e598-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4e598-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e598-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e598-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e598-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4e598-131">INPUTS</span></span>

### <span data-ttu-id="4e598-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4e598-132">None</span></span>

## <span data-ttu-id="4e598-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4e598-133">OUTPUTS</span></span>

### <span data-ttu-id="4e598-134">Microsoft. Azure. Commands. Security. model. Securitcontacts. Pssecuritycontacts</span><span class="sxs-lookup"><span data-stu-id="4e598-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="4e598-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4e598-135">NOTES</span></span>

## <span data-ttu-id="4e598-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4e598-136">RELATED LINKS</span></span>
