---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: ed039eefe46a1527948e7fffc3030f209a91b0c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096609"
---
# <span data-ttu-id="4dbae-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="4dbae-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="4dbae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dbae-102">SYNOPSIS</span></span>
<span data-ttu-id="4dbae-103">Var olan bir kümede yeni bir kusto veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4dbae-103">Creates a new Kusto database in an existing cluster.</span></span>

## <span data-ttu-id="4dbae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4dbae-104">SYNTAX</span></span>

### <span data-ttu-id="4dbae-105">Binaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4dbae-105">ByNameAndResourceGroup (Default)</span></span>
```
New-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dbae-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="4dbae-106">ByResourceId</span></span>
```
New-AzKustoDatabase -Name <String> -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32>
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dbae-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4dbae-107">ByInputObject</span></span>
```
New-AzKustoDatabase -Name <String> -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32>
 [-InputObject] <PSKustoCluster> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4dbae-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4dbae-108">DESCRIPTION</span></span>
<span data-ttu-id="4dbae-109">Var olan bir kümede yeni bir kusto veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4dbae-109">Creates a new Kusto database in an existing cluster.</span></span>

## <span data-ttu-id="4dbae-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4dbae-110">EXAMPLES</span></span>

### <span data-ttu-id="4dbae-111">Örnek 1-adla yeni bir kusto veritabanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="4dbae-111">Example 1 - Create a new Kusto database by name</span></span>

```
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase -SoftDeletePeriodInDays 4 -HotCachePeriodInDays 2

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 4
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="4dbae-112">Yukarıdaki komut, "mykustodatabase" adlı yeni bir kusto veritabanını, "testrg" kaynak grubunda bulunan "mykustocluster" adında oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4dbae-112">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "mykustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="4dbae-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4dbae-113">PARAMETERS</span></span>

### <span data-ttu-id="4dbae-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4dbae-114">-ClusterName</span></span>
<span data-ttu-id="4dbae-115">Veritabanını oluşturmak istediğiniz kümenin adı.</span><span class="sxs-lookup"><span data-stu-id="4dbae-115">Name of cluster under which you want to create the database.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dbae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dbae-116">-DefaultProfile</span></span>
<span data-ttu-id="4dbae-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4dbae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dbae-118">-HotCachePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="4dbae-118">-HotCachePeriodInDays</span></span>
<span data-ttu-id="4dbae-119">Hızlı sorgularda önbellekte tutulması gereken verilerin gün sayısı.</span><span class="sxs-lookup"><span data-stu-id="4dbae-119">The number of days of data that should be kept in cache for fast queries.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dbae-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4dbae-120">-InputObject</span></span>
<span data-ttu-id="4dbae-121">Kusto küme nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4dbae-121">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4dbae-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="4dbae-122">-Name</span></span>
<span data-ttu-id="4dbae-123">Oluşturulacak veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="4dbae-123">Name of the database to be created.</span></span>

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

### <span data-ttu-id="4dbae-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dbae-124">-ResourceGroupName</span></span>
<span data-ttu-id="4dbae-125">Kümenin bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4dbae-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dbae-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4dbae-126">-ResourceId</span></span>
<span data-ttu-id="4dbae-127">Kusto küme RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="4dbae-127">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dbae-128">-SoftDeletePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="4dbae-128">-SoftDeletePeriodInDays</span></span>
<span data-ttu-id="4dbae-129">Sorguların erişilebilir olmasını durdurmadan önce tutulacağı gün sayısı.</span><span class="sxs-lookup"><span data-stu-id="4dbae-129">The number of days data should be kept before it stops being accessible to queries.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dbae-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="4dbae-130">-Confirm</span></span>
<span data-ttu-id="4dbae-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4dbae-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dbae-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dbae-132">-WhatIf</span></span>
<span data-ttu-id="4dbae-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4dbae-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dbae-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4dbae-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dbae-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dbae-135">CommonParameters</span></span>
<span data-ttu-id="4dbae-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4dbae-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dbae-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dbae-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dbae-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4dbae-138">INPUTS</span></span>

### <span data-ttu-id="4dbae-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4dbae-139">System.String</span></span>

### <span data-ttu-id="4dbae-140">Microsoft. Azure. Commands. kusto. modeller. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="4dbae-140">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="4dbae-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4dbae-141">OUTPUTS</span></span>

### <span data-ttu-id="4dbae-142">Microsoft. Azure. Commands. kusto. modeller. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="4dbae-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="4dbae-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4dbae-143">NOTES</span></span>

## <span data-ttu-id="4dbae-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4dbae-144">RELATED LINKS</span></span>