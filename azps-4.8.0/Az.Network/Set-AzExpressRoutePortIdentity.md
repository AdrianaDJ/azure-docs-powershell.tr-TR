---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
ms.openlocfilehash: af04f3540aaf0ec90432c3b1262b45ef9ef1c2cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274785"
---
# <span data-ttu-id="4aa7e-101">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="4aa7e-101">Set-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="4aa7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aa7e-102">SYNOPSIS</span></span>
<span data-ttu-id="4aa7e-103">ExpressRoutePort 'a atanan bir kimliği güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4aa7e-103">Updates a identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="4aa7e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4aa7e-104">SYNTAX</span></span>

```
Set-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4aa7e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4aa7e-105">DESCRIPTION</span></span>
<span data-ttu-id="4aa7e-106">**Set-AzExpressRoutePortIdentity** cmdlet 'i yerel bir Azure ExpressRoutePort nesnesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4aa7e-106">The **Set-AzExpressRoutePortIdentity** cmdlet updates a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="4aa7e-107">**Set-AzExpressRoutePort** kullanarak expressrouteport 'a atayın.</span><span class="sxs-lookup"><span data-stu-id="4aa7e-107">Use **Set-AzExpressRoutePort** to assign it to ExpressRoutePort.</span></span>

## <span data-ttu-id="4aa7e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4aa7e-108">EXAMPLES</span></span>

### <span data-ttu-id="4aa7e-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4aa7e-109">Example 1</span></span>
```powershell
PS C:\>$exrport = Get-AzExpressRoutePort -Name $portName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$exrPortIdentity = Set-AzExpressRoutePortIdentity -UserAssignedIdentity $identity.Id -ExpressRoutePort $exrPort
PS C:\>$updatedExrPort = Set-AzExpressRoutePort -ExpressRoutePort $exrPort
```

## <span data-ttu-id="4aa7e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4aa7e-110">PARAMETERS</span></span>

### <span data-ttu-id="4aa7e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aa7e-111">-DefaultProfile</span></span>
<span data-ttu-id="4aa7e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4aa7e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4aa7e-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4aa7e-113">-ExpressRoutePort</span></span>
<span data-ttu-id="4aa7e-114">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4aa7e-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="4aa7e-115">-Useratandidentityıd</span><span class="sxs-lookup"><span data-stu-id="4aa7e-115">-UserAssignedIdentityId</span></span>
<span data-ttu-id="4aa7e-116">ExpressRoutePort 'a atanacak Kullanıcı tarafından atanan kimliğin RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="4aa7e-116">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="4aa7e-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="4aa7e-117">-Confirm</span></span>
<span data-ttu-id="4aa7e-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4aa7e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4aa7e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aa7e-119">-WhatIf</span></span>
<span data-ttu-id="4aa7e-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4aa7e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aa7e-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4aa7e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4aa7e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aa7e-122">CommonParameters</span></span>
<span data-ttu-id="4aa7e-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4aa7e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aa7e-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aa7e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aa7e-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4aa7e-125">INPUTS</span></span>

### <span data-ttu-id="4aa7e-126">Microsoft. Azure. Commands. Network. model. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4aa7e-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="4aa7e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4aa7e-127">System.String</span></span>

## <span data-ttu-id="4aa7e-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4aa7e-128">OUTPUTS</span></span>

### <span data-ttu-id="4aa7e-129">Microsoft. Azure. Commands. Network. model. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4aa7e-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="4aa7e-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4aa7e-130">NOTES</span></span>

## <span data-ttu-id="4aa7e-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4aa7e-131">RELATED LINKS</span></span>
[<span data-ttu-id="4aa7e-132">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="4aa7e-132">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="4aa7e-133">Yeni-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="4aa7e-133">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="4aa7e-134">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="4aa7e-134">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)
