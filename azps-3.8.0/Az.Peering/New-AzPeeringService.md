---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
ms.openlocfilehash: 60772963530d14eeb93f2f28fbf5e067ac5833ab
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104473"
---
# <span data-ttu-id="60933-101">New-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="60933-101">New-AzPeeringService</span></span>

## <span data-ttu-id="60933-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60933-102">SYNOPSIS</span></span>
<span data-ttu-id="60933-103">Yeni bir eşleme hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="60933-103">Creates a new peering service.</span></span>

## <span data-ttu-id="60933-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="60933-104">SYNTAX</span></span>

```
New-AzPeeringService [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeeringServiceProvider] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60933-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="60933-105">DESCRIPTION</span></span>
<span data-ttu-id="60933-106">Eşleme hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="60933-106">Creates peering service.</span></span>

## <span data-ttu-id="60933-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="60933-107">EXAMPLES</span></span>

### <span data-ttu-id="60933-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="60933-108">Example 1</span></span>
```powershell
PS C:\> New-AzPeeringService -ResourceGroupName $resourceGroup -Name $name -Location $loc -PeeringServiceProvider $provider

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="60933-109">Sağlayıcı ve eşleme konumu içeren bir eşleme hizmeti nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="60933-109">Creates a peering service object with provider and peering location.</span></span> <span data-ttu-id="60933-110">İle birlikte kullanın `Get-AzPeeringServiceProvider` ve `Get-AzPeeringServiceLocation`</span><span class="sxs-lookup"><span data-stu-id="60933-110">Use in conjuction with `Get-AzPeeringServiceProvider` and `Get-AzPeeringServiceLocation`</span></span>

## <span data-ttu-id="60933-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="60933-111">PARAMETERS</span></span>

### <span data-ttu-id="60933-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="60933-112">-AsJob</span></span>
<span data-ttu-id="60933-113">Arka planda çalışır.</span><span class="sxs-lookup"><span data-stu-id="60933-113">Run in the background.</span></span>

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

### <span data-ttu-id="60933-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60933-114">-DefaultProfile</span></span>
<span data-ttu-id="60933-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="60933-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60933-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="60933-116">-Name</span></span>
<span data-ttu-id="60933-117">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="60933-117">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60933-118">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="60933-118">-PeeringLocation</span></span>
<span data-ttu-id="60933-119">Azure bölgesinden farklı fiziksel konum.</span><span class="sxs-lookup"><span data-stu-id="60933-119">The Physical Location Different from Azure Region.</span></span> <span data-ttu-id="60933-120">Get-AzPeeringServiceLocation [-Country <country> ] kullanın</span><span class="sxs-lookup"><span data-stu-id="60933-120">Use Get-AzPeeringServiceLocation [-Country <country>]</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60933-121">-PeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="60933-121">-PeeringServiceProvider</span></span>
<span data-ttu-id="60933-122">Eşleme hizmeti sağlayıcısının adı.</span><span class="sxs-lookup"><span data-stu-id="60933-122">The peering service provider name.</span></span>
<span data-ttu-id="60933-123">Liste için Get-AzPeeringServiceProvider cmdlet 'ini kullanma</span><span class="sxs-lookup"><span data-stu-id="60933-123">Use Get-AzPeeringServiceProvider cmdlet for a list</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60933-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60933-124">-ResourceGroupName</span></span>
<span data-ttu-id="60933-125">Var olan kaynak grubu adını oluştur veya kullan.</span><span class="sxs-lookup"><span data-stu-id="60933-125">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60933-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="60933-126">-Tag</span></span>
<span data-ttu-id="60933-127">Microsoft InputObject hizmetiyle ilişkilendirilecek Etiketler.</span><span class="sxs-lookup"><span data-stu-id="60933-127">The tags to associate with the Microsoft InputObject Service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60933-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="60933-128">-Confirm</span></span>
<span data-ttu-id="60933-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="60933-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60933-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60933-130">-WhatIf</span></span>
<span data-ttu-id="60933-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="60933-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60933-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="60933-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60933-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60933-133">CommonParameters</span></span>
<span data-ttu-id="60933-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="60933-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60933-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="60933-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60933-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="60933-136">INPUTS</span></span>

### <span data-ttu-id="60933-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="60933-137">None</span></span>

## <span data-ttu-id="60933-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="60933-138">OUTPUTS</span></span>

### <span data-ttu-id="60933-139">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60933-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="60933-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="60933-140">NOTES</span></span>

## <span data-ttu-id="60933-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="60933-141">RELATED LINKS</span></span>
