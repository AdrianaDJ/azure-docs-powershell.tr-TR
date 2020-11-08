---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
ms.openlocfilehash: 7fba74a3778df0c8c26ed4b581e5d2777ff75029
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098066"
---
# <span data-ttu-id="195a8-101">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="195a8-101">Update-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="195a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="195a8-102">SYNOPSIS</span></span>
<span data-ttu-id="195a8-103">Bir yönlendirme kuralını yuvaya güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="195a8-103">Update a routing Rule to the Slot.</span></span>

## <span data-ttu-id="195a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="195a8-104">SYNTAX</span></span>

```
Update-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="195a8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="195a8-105">DESCRIPTION</span></span>
<span data-ttu-id="195a8-106">**Update-AzWebAppTrafficRouting** cmdlet 'ı bir Azure Web App yuvası için yönlendirme kuralı yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="195a8-106">The **Update-AzWebAppTrafficRouting** cmdlet updates the routing rule configuration for an Azure Web App Slot.</span></span>

## <span data-ttu-id="195a8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="195a8-107">EXAMPLES</span></span>

### <span data-ttu-id="195a8-108">Örnek 1 üretim akışını STG yuvasına aktarmak için bir yönlendirme kuralı traffice</span><span class="sxs-lookup"><span data-stu-id="195a8-108">Example 1 Update a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
- RoutingRule @{AtionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="195a8-109">Bu komut, üretim akışını STG yuvasına aktarmak için bir yönlendirme kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="195a8-109">This command updates a routing rule to transfer 15% of production traffic to Stg slot.</span></span>

### <span data-ttu-id="195a8-110">Örnek 2 50% ile STG yuva aralıklarını artımlı şekilde% ile %90 arasında aktarmak için bir yönlendirme kuralı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="195a8-110">Example 2 Update a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="195a8-111">Bu komut, 50% 90 ile STG yuva aralıklarına artımlı bir şekilde üretim traffice aktarmak için bir yönlendirme kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="195a8-111">This command Updates a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="195a8-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="195a8-112">PARAMETERS</span></span>

### <span data-ttu-id="195a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="195a8-113">-DefaultProfile</span></span>
<span data-ttu-id="195a8-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="195a8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="195a8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="195a8-115">-ResourceGroupName</span></span>
<span data-ttu-id="195a8-116">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="195a8-116">ResourceGroupName</span></span>
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

### <span data-ttu-id="195a8-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="195a8-117">-RoutingRule</span></span>
<span data-ttu-id="195a8-118">Web uygulaması yönlendirme kuralı.</span><span class="sxs-lookup"><span data-stu-id="195a8-118">Web App RoutingRule.</span></span>
<span data-ttu-id="195a8-119">Örnek:-RoutingRule @ {Actionanabilgisayaradı = $slot. DefaultHostName; ReroutePercentage = $ReroutePercentage; Name = $slotName}</span><span class="sxs-lookup"><span data-stu-id="195a8-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195a8-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="195a8-120">-WebAppName</span></span>
<span data-ttu-id="195a8-121">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="195a8-121">WebApp Name</span></span>

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

### <span data-ttu-id="195a8-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="195a8-122">-Confirm</span></span>
<span data-ttu-id="195a8-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="195a8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="195a8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="195a8-124">-WhatIf</span></span>
<span data-ttu-id="195a8-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="195a8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="195a8-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="195a8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="195a8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="195a8-127">CommonParameters</span></span>
<span data-ttu-id="195a8-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="195a8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="195a8-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="195a8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="195a8-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="195a8-130">INPUTS</span></span>

### <span data-ttu-id="195a8-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="195a8-131">None</span></span>

## <span data-ttu-id="195a8-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="195a8-132">OUTPUTS</span></span>

### <span data-ttu-id="195a8-133">Microsoft. Azure. Management. Web sitesi. modeller. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="195a8-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="195a8-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="195a8-134">NOTES</span></span>

## <span data-ttu-id="195a8-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="195a8-135">RELATED LINKS</span></span>

[<span data-ttu-id="195a8-136">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="195a8-136">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="195a8-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="195a8-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="195a8-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="195a8-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)