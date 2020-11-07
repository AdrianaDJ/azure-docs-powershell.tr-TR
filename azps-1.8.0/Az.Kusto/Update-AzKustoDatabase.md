---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: 05d01d776f03ec3bbfe4e9bf6bd438ba8f002afb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916124"
---
# <span data-ttu-id="9b280-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="9b280-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="9b280-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b280-102">SYNOPSIS</span></span>
<span data-ttu-id="9b280-103">Var olan kusto veritabanını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="9b280-103">Update an existing Kusto database.</span></span>

## <span data-ttu-id="9b280-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9b280-104">SYNTAX</span></span>

### <span data-ttu-id="9b280-105">Binaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9b280-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b280-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="9b280-106">ByResourceId</span></span>
```
Update-AzKustoDatabase [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b280-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9b280-107">ByInputObject</span></span>
```
Update-AzKustoDatabase [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>]
 [-InputObject] <PSKustoDatabase> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b280-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9b280-108">DESCRIPTION</span></span>
<span data-ttu-id="9b280-109">Var olan kusto veritabanını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="9b280-109">Update an existing Kusto database.</span></span>

## <span data-ttu-id="9b280-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9b280-110">EXAMPLES</span></span>

### <span data-ttu-id="9b280-111">Örnek 1-varolan veritabanını adla güncelleyin</span><span class="sxs-lookup"><span data-stu-id="9b280-111">Example 1 - Update an existing database by name</span></span>

```
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase -SoftDeletePeriodInDays 5

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 5
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="9b280-112">Yukarıdaki komut, "mykustodatabase" kaynak grubunda bulunan "mykustocluster" kümesinde "" kusto veritabanının yumuşak silme dönemini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9b280-112">The above command updates the soft deletion period of the Kusto database "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="9b280-113">Örnek 2-varolan bir veritabanını boruları kullanarak güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="9b280-113">Example 2 - Update an existing database by piping</span></span>

```
PS C:\> PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase | Update-AzKustoDatabase -SoftDeletePeriodInDays 5

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 5
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="9b280-114">Yukarıdaki komut, cmdlet 'i kullanarak "mykustodatabase" kaynak grubunda yer alan "mykustocluster" kümesinde bulunan "" kusto veritabanını alır `Get-AzKustoDatabase` ve sonra da `Update-AzKustoDatabase` veritabanının yumuşak silme süresini beş güne güncellemesine yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="9b280-114">The above command gets the Kusto database "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoDatabase` cmdlet, and then pipes the result to `Update-AzKustoDatabase` to update the database's soft deletion period to five days.</span></span>

## <span data-ttu-id="9b280-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9b280-115">PARAMETERS</span></span>

### <span data-ttu-id="9b280-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9b280-116">-ClusterName</span></span>
<span data-ttu-id="9b280-117">Veritabanının bulunduğu kümenin adı</span><span class="sxs-lookup"><span data-stu-id="9b280-117">Name of cluster under which the database exists</span></span>

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

### <span data-ttu-id="9b280-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b280-118">-DefaultProfile</span></span>
<span data-ttu-id="9b280-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9b280-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b280-120">-HotCachePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="9b280-120">-HotCachePeriodInDays</span></span>
<span data-ttu-id="9b280-121">Hızlı sorgularda verilerin önbellekte tutulması gereken gün sayısı</span><span class="sxs-lookup"><span data-stu-id="9b280-121">The number of days that data should be kept in cache for fast queries</span></span>

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

### <span data-ttu-id="9b280-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b280-122">-InputObject</span></span>
<span data-ttu-id="9b280-123">Kusto veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9b280-123">Kusto database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b280-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="9b280-124">-Name</span></span>
<span data-ttu-id="9b280-125">Güncelleştirilecek veritabanının adı</span><span class="sxs-lookup"><span data-stu-id="9b280-125">Name of the database to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b280-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b280-126">-ResourceGroupName</span></span>
<span data-ttu-id="9b280-127">Kümenin bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9b280-127">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="9b280-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9b280-128">-ResourceId</span></span>
<span data-ttu-id="9b280-129">Kusto veritabanı RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="9b280-129">Kusto database ResourceID.</span></span>

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

### <span data-ttu-id="9b280-130">-SoftDeletePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="9b280-130">-SoftDeletePeriodInDays</span></span>
<span data-ttu-id="9b280-131">Sorguların erişilebilir olması bitmeden önce tutulacağı gün sayısı</span><span class="sxs-lookup"><span data-stu-id="9b280-131">The number of days that data should be kept before it stops being accessible to queries</span></span>

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

### <span data-ttu-id="9b280-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="9b280-132">-Confirm</span></span>
<span data-ttu-id="9b280-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9b280-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b280-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b280-134">-WhatIf</span></span>
<span data-ttu-id="9b280-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9b280-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b280-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9b280-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b280-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b280-137">CommonParameters</span></span>
<span data-ttu-id="9b280-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9b280-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b280-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b280-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b280-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9b280-140">INPUTS</span></span>

### <span data-ttu-id="9b280-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9b280-141">System.String</span></span>

### <span data-ttu-id="9b280-142">Microsoft. Azure. Commands. kusto. modeller. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="9b280-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="9b280-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9b280-143">OUTPUTS</span></span>

### <span data-ttu-id="9b280-144">Microsoft. Azure. Commands. kusto. modeller. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="9b280-144">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="9b280-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9b280-145">NOTES</span></span>

## <span data-ttu-id="9b280-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9b280-146">RELATED LINKS</span></span>