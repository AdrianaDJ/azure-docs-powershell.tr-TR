---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
ms.openlocfilehash: 8a3949397b12b54062c5cc68f367187f691fb02d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322741"
---
# <span data-ttu-id="030f3-101">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="030f3-101">Add-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="030f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="030f3-102">SYNOPSIS</span></span>
<span data-ttu-id="030f3-103">Yuvaya bir yönlendirme kuralı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="030f3-103">Add a routing Rule to the Slot.</span></span>

## <span data-ttu-id="030f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="030f3-104">SYNTAX</span></span>

```
Add-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="030f3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="030f3-105">DESCRIPTION</span></span>
<span data-ttu-id="030f3-106">**Add-AzWebAppTrafficRouting** cmdlet 'ı bir Azure Web App yuvasına yönlendirme kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="030f3-106">The **Add-AzWebAppTrafficRouting** cmdlet adds a Routing rule to an Azure Web App Slot.</span></span>

## <span data-ttu-id="030f3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="030f3-107">EXAMPLES</span></span>

### <span data-ttu-id="030f3-108">Örnek 1 traffice üretim akışını STG yuvasına aktarmak için bir yönlendirme kuralı ekleyin</span><span class="sxs-lookup"><span data-stu-id="030f3-108">Example 1 Add a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="030f3-109">Bu komut, STG yuvasına üretim traffice %15 aktarmak için bir yönlendirme kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="030f3-109">This command adds a routing rule to transfer 15% of production traffice to  Stg slot</span></span>

### <span data-ttu-id="030f3-110">Örnek 2 50% ile STG yuva aralıklarına artımlı şekilde% ile %90 arasındaki bir yönlendirme kuralı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="030f3-110">Example 2 Add a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="030f3-111">Bu komut, 50% 90 ile STG yuva aralıklarına artımlı bir şekilde üretim traffice aktarmak için bir yönlendirme kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="030f3-111">This command adds a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="030f3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="030f3-112">PARAMETERS</span></span>

### <span data-ttu-id="030f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="030f3-113">-DefaultProfile</span></span>
<span data-ttu-id="030f3-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="030f3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="030f3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="030f3-115">-ResourceGroupName</span></span>
<span data-ttu-id="030f3-116">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="030f3-116">Resource Group Name</span></span>

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

### <span data-ttu-id="030f3-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="030f3-117">-RoutingRule</span></span>
<span data-ttu-id="030f3-118">Web uygulaması yönlendirme kuralı.</span><span class="sxs-lookup"><span data-stu-id="030f3-118">Web App RoutingRule.</span></span>
<span data-ttu-id="030f3-119">Örnek:-RoutingRule @ {Actionanabilgisayaradı = $slot. DefaultHostName; ReroutePercentage = $ReroutePercentage; Name = $slotName}</span><span class="sxs-lookup"><span data-stu-id="030f3-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

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

### <span data-ttu-id="030f3-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="030f3-120">-WebAppName</span></span>
<span data-ttu-id="030f3-121">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="030f3-121">WebApp Name</span></span>

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

### <span data-ttu-id="030f3-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="030f3-122">-Confirm</span></span>
<span data-ttu-id="030f3-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="030f3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="030f3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="030f3-124">-WhatIf</span></span>
<span data-ttu-id="030f3-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="030f3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="030f3-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="030f3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="030f3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="030f3-127">CommonParameters</span></span>
<span data-ttu-id="030f3-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="030f3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="030f3-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="030f3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="030f3-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="030f3-130">INPUTS</span></span>

### <span data-ttu-id="030f3-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="030f3-131">None</span></span>

## <span data-ttu-id="030f3-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="030f3-132">OUTPUTS</span></span>

### <span data-ttu-id="030f3-133">Microsoft. Azure. Management. Web sitesi. modeller. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="030f3-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="030f3-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="030f3-134">NOTES</span></span>

## <span data-ttu-id="030f3-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="030f3-135">RELATED LINKS</span></span>
[<span data-ttu-id="030f3-136">Güncelleştirme-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="030f3-136">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="030f3-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="030f3-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="030f3-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="030f3-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
