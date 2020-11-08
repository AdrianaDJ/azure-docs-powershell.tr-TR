---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 3fa4a8c1868673b4ce9bc630a70e02bb92a55fda
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279149"
---
# <span data-ttu-id="957b9-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="957b9-101">New-AzSearchService</span></span>

## <span data-ttu-id="957b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="957b9-102">SYNOPSIS</span></span>
<span data-ttu-id="957b9-103">Azure Search hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="957b9-103">Creates an Azure Search service.</span></span>

## <span data-ttu-id="957b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="957b9-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="957b9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="957b9-105">DESCRIPTION</span></span>
<span data-ttu-id="957b9-106">**New-Azaramahizmeti** cmdlet 'i belirtilen parametrelerle bir Azure Arama hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="957b9-106">The **New-AzSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="957b9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="957b9-107">EXAMPLES</span></span>

### <span data-ttu-id="957b9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="957b9-108">Example 1</span></span>
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

<span data-ttu-id="957b9-109">Komut bir Azure Arama hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="957b9-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="957b9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="957b9-110">PARAMETERS</span></span>

### <span data-ttu-id="957b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="957b9-111">-DefaultProfile</span></span>
<span data-ttu-id="957b9-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="957b9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="957b9-113">-Hostingmodu</span><span class="sxs-lookup"><span data-stu-id="957b9-113">-HostingMode</span></span>
<span data-ttu-id="957b9-114">Arama hizmeti barındırma modu.</span><span class="sxs-lookup"><span data-stu-id="957b9-114">Search Service hosting mode.</span></span>

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

### <span data-ttu-id="957b9-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="957b9-115">-Location</span></span>
<span data-ttu-id="957b9-116">Arama hizmeti konumu.</span><span class="sxs-lookup"><span data-stu-id="957b9-116">Search Service location.</span></span>

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

### <span data-ttu-id="957b9-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="957b9-117">-Name</span></span>
<span data-ttu-id="957b9-118">Arama hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="957b9-118">Search Service name.</span></span>

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

### <span data-ttu-id="957b9-119">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="957b9-119">-PartitionCount</span></span>
<span data-ttu-id="957b9-120">Arama hizmeti bölüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="957b9-120">Search Service partition count.</span></span>

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

### <span data-ttu-id="957b9-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="957b9-121">-ReplicaCount</span></span>
<span data-ttu-id="957b9-122">Arama hizmeti kopya sayısı.</span><span class="sxs-lookup"><span data-stu-id="957b9-122">Search Service replica count.</span></span>

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

### <span data-ttu-id="957b9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="957b9-123">-ResourceGroupName</span></span>
<span data-ttu-id="957b9-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="957b9-124">Resource Group name.</span></span>

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

### <span data-ttu-id="957b9-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="957b9-125">-Sku</span></span>
<span data-ttu-id="957b9-126">Arama hizmeti SKU 'Su.</span><span class="sxs-lookup"><span data-stu-id="957b9-126">Search Service Sku.</span></span>

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

### <span data-ttu-id="957b9-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="957b9-127">-Confirm</span></span>
<span data-ttu-id="957b9-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="957b9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="957b9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="957b9-129">-WhatIf</span></span>
<span data-ttu-id="957b9-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="957b9-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="957b9-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="957b9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="957b9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="957b9-132">CommonParameters</span></span>
<span data-ttu-id="957b9-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="957b9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="957b9-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="957b9-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="957b9-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="957b9-135">INPUTS</span></span>

### <span data-ttu-id="957b9-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="957b9-136">None</span></span>

## <span data-ttu-id="957b9-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="957b9-137">OUTPUTS</span></span>

### <span data-ttu-id="957b9-138">Microsoft. Azure. Commands. Management. Search. model. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="957b9-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="957b9-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="957b9-139">NOTES</span></span>

## <span data-ttu-id="957b9-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="957b9-140">RELATED LINKS</span></span>

[<span data-ttu-id="957b9-141">Get-Azaramahizmeti</span><span class="sxs-lookup"><span data-stu-id="957b9-141">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="957b9-142">Set-Azaramahizmeti</span><span class="sxs-lookup"><span data-stu-id="957b9-142">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="957b9-143">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="957b9-143">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)