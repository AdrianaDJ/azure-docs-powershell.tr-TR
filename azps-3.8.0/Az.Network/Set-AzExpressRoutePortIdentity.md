---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
ms.openlocfilehash: af04f3540aaf0ec90432c3b1262b45ef9ef1c2cd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096812"
---
# <span data-ttu-id="5cf07-101">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5cf07-101">Set-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="5cf07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cf07-102">SYNOPSIS</span></span>
<span data-ttu-id="5cf07-103">ExpressRoutePort 'a atanan bir kimliği güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5cf07-103">Updates a identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="5cf07-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5cf07-104">SYNTAX</span></span>

```
Set-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cf07-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5cf07-105">DESCRIPTION</span></span>
<span data-ttu-id="5cf07-106">**Set-AzExpressRoutePortIdentity** cmdlet 'i yerel bir Azure ExpressRoutePort nesnesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5cf07-106">The **Set-AzExpressRoutePortIdentity** cmdlet updates a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="5cf07-107">**Set-AzExpressRoutePort** kullanarak expressrouteport 'a atayın.</span><span class="sxs-lookup"><span data-stu-id="5cf07-107">Use **Set-AzExpressRoutePort** to assign it to ExpressRoutePort.</span></span>

## <span data-ttu-id="5cf07-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5cf07-108">EXAMPLES</span></span>

### <span data-ttu-id="5cf07-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5cf07-109">Example 1</span></span>
```powershell
PS C:\>$exrport = Get-AzExpressRoutePort -Name $portName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$exrPortIdentity = Set-AzExpressRoutePortIdentity -UserAssignedIdentity $identity.Id -ExpressRoutePort $exrPort
PS C:\>$updatedExrPort = Set-AzExpressRoutePort -ExpressRoutePort $exrPort
```

## <span data-ttu-id="5cf07-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5cf07-110">PARAMETERS</span></span>

### <span data-ttu-id="5cf07-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cf07-111">-DefaultProfile</span></span>
<span data-ttu-id="5cf07-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5cf07-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cf07-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="5cf07-113">-ExpressRoutePort</span></span>
<span data-ttu-id="5cf07-114">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="5cf07-114">The ExpressRoutePort</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cf07-115">-Useratandidentityıd</span><span class="sxs-lookup"><span data-stu-id="5cf07-115">-UserAssignedIdentityId</span></span>
<span data-ttu-id="5cf07-116">ExpressRoutePort 'a atanacak Kullanıcı tarafından atanan kimliğin RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="5cf07-116">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="5cf07-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="5cf07-117">-Confirm</span></span>
<span data-ttu-id="5cf07-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5cf07-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cf07-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cf07-119">-WhatIf</span></span>
<span data-ttu-id="5cf07-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5cf07-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cf07-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5cf07-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cf07-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cf07-122">CommonParameters</span></span>
<span data-ttu-id="5cf07-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5cf07-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cf07-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cf07-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cf07-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5cf07-125">INPUTS</span></span>

### <span data-ttu-id="5cf07-126">Microsoft. Azure. Commands. Network. model. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="5cf07-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="5cf07-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5cf07-127">System.String</span></span>

## <span data-ttu-id="5cf07-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5cf07-128">OUTPUTS</span></span>

### <span data-ttu-id="5cf07-129">Microsoft. Azure. Commands. Network. model. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="5cf07-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="5cf07-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5cf07-130">NOTES</span></span>

## <span data-ttu-id="5cf07-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5cf07-131">RELATED LINKS</span></span>
[<span data-ttu-id="5cf07-132">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5cf07-132">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="5cf07-133">Yeni-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5cf07-133">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="5cf07-134">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5cf07-134">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)
