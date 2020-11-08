---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 3fa4a8c1868673b4ce9bc630a70e02bb92a55fda
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268809"
---
# <span data-ttu-id="082d3-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="082d3-101">New-AzSearchService</span></span>

## <span data-ttu-id="082d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="082d3-102">SYNOPSIS</span></span>
<span data-ttu-id="082d3-103">Azure Search hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="082d3-103">Creates an Azure Search service.</span></span>

## <span data-ttu-id="082d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="082d3-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="082d3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="082d3-105">DESCRIPTION</span></span>
<span data-ttu-id="082d3-106">**New-Azaramahizmeti** cmdlet 'i belirtilen parametrelerle bir Azure Arama hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="082d3-106">The **New-AzSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="082d3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="082d3-107">EXAMPLES</span></span>

### <span data-ttu-id="082d3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="082d3-108">Example 1</span></span>
```powershell
PS C:\> New-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -Sku "Standard" -Location "West US" -PartitionCount 1 -ReplicaCount 1 -HostingMode Default -Force


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Tags              :
```

<span data-ttu-id="082d3-109">Komut bir Azure Arama hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="082d3-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="082d3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="082d3-110">PARAMETERS</span></span>

### <span data-ttu-id="082d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="082d3-111">-DefaultProfile</span></span>
<span data-ttu-id="082d3-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="082d3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="082d3-113">-Hostingmodu</span><span class="sxs-lookup"><span data-stu-id="082d3-113">-HostingMode</span></span>
<span data-ttu-id="082d3-114">Arama hizmeti barındırma modu.</span><span class="sxs-lookup"><span data-stu-id="082d3-114">Search Service hosting mode.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSHostingMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, HighDensity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="082d3-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="082d3-115">-Location</span></span>
<span data-ttu-id="082d3-116">Arama hizmeti konumu.</span><span class="sxs-lookup"><span data-stu-id="082d3-116">Search Service location.</span></span>

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

### <span data-ttu-id="082d3-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="082d3-117">-Name</span></span>
<span data-ttu-id="082d3-118">Arama hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="082d3-118">Search Service name.</span></span>

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

### <span data-ttu-id="082d3-119">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="082d3-119">-PartitionCount</span></span>
<span data-ttu-id="082d3-120">Arama hizmeti bölüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="082d3-120">Search Service partition count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="082d3-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="082d3-121">-ReplicaCount</span></span>
<span data-ttu-id="082d3-122">Arama hizmeti kopya sayısı.</span><span class="sxs-lookup"><span data-stu-id="082d3-122">Search Service replica count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="082d3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="082d3-123">-ResourceGroupName</span></span>
<span data-ttu-id="082d3-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="082d3-124">Resource Group name.</span></span>

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

### <span data-ttu-id="082d3-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="082d3-125">-Sku</span></span>
<span data-ttu-id="082d3-126">Arama hizmeti SKU 'Su.</span><span class="sxs-lookup"><span data-stu-id="082d3-126">Search Service Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard, Standard2, Standard3

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="082d3-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="082d3-127">-Confirm</span></span>
<span data-ttu-id="082d3-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="082d3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="082d3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="082d3-129">-WhatIf</span></span>
<span data-ttu-id="082d3-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="082d3-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="082d3-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="082d3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="082d3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="082d3-132">CommonParameters</span></span>
<span data-ttu-id="082d3-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="082d3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="082d3-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="082d3-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="082d3-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="082d3-135">INPUTS</span></span>

### <span data-ttu-id="082d3-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="082d3-136">None</span></span>

## <span data-ttu-id="082d3-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="082d3-137">OUTPUTS</span></span>

### <span data-ttu-id="082d3-138">Microsoft. Azure. Commands. Management. Search. model. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="082d3-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="082d3-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="082d3-139">NOTES</span></span>

## <span data-ttu-id="082d3-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="082d3-140">RELATED LINKS</span></span>

[<span data-ttu-id="082d3-141">Get-Azaramahizmeti</span><span class="sxs-lookup"><span data-stu-id="082d3-141">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="082d3-142">Set-Azaramahizmeti</span><span class="sxs-lookup"><span data-stu-id="082d3-142">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="082d3-143">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="082d3-143">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)