---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: d19acf8bb97f3b84b3cd831e4cf91397231f4b08
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109475"
---
# <span data-ttu-id="561ed-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="561ed-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="561ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="561ed-102">SYNOPSIS</span></span>
<span data-ttu-id="561ed-103">Azure ExpressRoutePortIdentity oluşturur.</span><span class="sxs-lookup"><span data-stu-id="561ed-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="561ed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="561ed-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="561ed-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="561ed-105">DESCRIPTION</span></span>
<span data-ttu-id="561ed-106">**Yeni-AzExpressRoutePortIdentity** cmdlet 'i yerel bir Azure ExpressRoutePort Identity nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="561ed-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="561ed-107">**New-azexpressrouteport** veya **set-azexpressrouteport** kullanarak Azure expressrouteport 'a atayın.</span><span class="sxs-lookup"><span data-stu-id="561ed-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="561ed-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="561ed-108">EXAMPLES</span></span>

### <span data-ttu-id="561ed-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="561ed-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="561ed-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="561ed-110">PARAMETERS</span></span>

### <span data-ttu-id="561ed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="561ed-111">-DefaultProfile</span></span>
<span data-ttu-id="561ed-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="561ed-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="561ed-113">-Useratandidentityıd</span><span class="sxs-lookup"><span data-stu-id="561ed-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="561ed-114">ExpressRoutePort 'a atanacak Kullanıcı tarafından atanan kimliğin RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="561ed-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="561ed-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="561ed-115">-Confirm</span></span>
<span data-ttu-id="561ed-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="561ed-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="561ed-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="561ed-117">-WhatIf</span></span>
<span data-ttu-id="561ed-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="561ed-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="561ed-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="561ed-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="561ed-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="561ed-120">CommonParameters</span></span>
<span data-ttu-id="561ed-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="561ed-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="561ed-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="561ed-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="561ed-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="561ed-123">INPUTS</span></span>

### <span data-ttu-id="561ed-124">System. String</span><span class="sxs-lookup"><span data-stu-id="561ed-124">System.String</span></span>

## <span data-ttu-id="561ed-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="561ed-125">OUTPUTS</span></span>

### <span data-ttu-id="561ed-126">Microsoft. Azure. Commands. Network. model. Psmanagedserviceıdentity</span><span class="sxs-lookup"><span data-stu-id="561ed-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="561ed-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="561ed-127">NOTES</span></span>

## <span data-ttu-id="561ed-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="561ed-128">RELATED LINKS</span></span>
[<span data-ttu-id="561ed-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="561ed-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="561ed-130">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="561ed-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="561ed-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="561ed-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)