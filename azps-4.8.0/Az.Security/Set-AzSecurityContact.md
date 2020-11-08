---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: 504f07092a0a8e246e778421748f1cd807b04a77
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266358"
---
# <span data-ttu-id="172cb-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="172cb-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="172cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="172cb-102">SYNOPSIS</span></span>
<span data-ttu-id="172cb-103">Abonelik için bir güvenlik kişisi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="172cb-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="172cb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="172cb-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="172cb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="172cb-105">DESCRIPTION</span></span>
<span data-ttu-id="172cb-106">Abonelik için bir güvenlik kişisi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="172cb-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="172cb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="172cb-107">EXAMPLES</span></span>

### <span data-ttu-id="172cb-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="172cb-108">Example 1</span></span>
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

<span data-ttu-id="172cb-109">Abonelik için bir güvenlik kişisi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="172cb-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="172cb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="172cb-110">PARAMETERS</span></span>

### <span data-ttu-id="172cb-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="172cb-111">-AlertAdmin</span></span>
<span data-ttu-id="172cb-112">Yöneticilere uyarılar.</span><span class="sxs-lookup"><span data-stu-id="172cb-112">Alerts To Administrators.</span></span>

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

### <span data-ttu-id="172cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="172cb-113">-DefaultProfile</span></span>
<span data-ttu-id="172cb-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="172cb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="172cb-115">-E-posta</span><span class="sxs-lookup"><span data-stu-id="172cb-115">-Email</span></span>
<span data-ttu-id="172cb-116">E-posta.</span><span class="sxs-lookup"><span data-stu-id="172cb-116">E-Mail.</span></span>

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

### <span data-ttu-id="172cb-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="172cb-117">-Name</span></span>
<span data-ttu-id="172cb-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="172cb-118">Resource name.</span></span>

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

### <span data-ttu-id="172cb-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="172cb-119">-NotifyOnAlert</span></span>
<span data-ttu-id="172cb-120">Uyarı bildirimleri.</span><span class="sxs-lookup"><span data-stu-id="172cb-120">Alert Notifications.</span></span>

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

### <span data-ttu-id="172cb-121">-Telefon</span><span class="sxs-lookup"><span data-stu-id="172cb-121">-Phone</span></span>
<span data-ttu-id="172cb-122">Telefon.</span><span class="sxs-lookup"><span data-stu-id="172cb-122">Phone.</span></span>

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

### <span data-ttu-id="172cb-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="172cb-123">-Confirm</span></span>
<span data-ttu-id="172cb-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="172cb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="172cb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="172cb-125">-WhatIf</span></span>
<span data-ttu-id="172cb-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="172cb-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="172cb-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="172cb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="172cb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="172cb-128">CommonParameters</span></span>
<span data-ttu-id="172cb-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="172cb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="172cb-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="172cb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="172cb-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="172cb-131">INPUTS</span></span>

### <span data-ttu-id="172cb-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="172cb-132">None</span></span>

## <span data-ttu-id="172cb-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="172cb-133">OUTPUTS</span></span>

### <span data-ttu-id="172cb-134">Microsoft. Azure. Commands. Security. model. Securitcontacts. Pssecuritycontacts</span><span class="sxs-lookup"><span data-stu-id="172cb-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="172cb-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="172cb-135">NOTES</span></span>

## <span data-ttu-id="172cb-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="172cb-136">RELATED LINKS</span></span>
