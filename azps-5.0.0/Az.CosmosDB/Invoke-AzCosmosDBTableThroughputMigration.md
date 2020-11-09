---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbtablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
ms.openlocfilehash: 009048c5f37936d469fe88c5e75cab8270efa81c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321606"
---
# <span data-ttu-id="8df0d-101">Invoke-AzCosmosDBTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="8df0d-101">Invoke-AzCosmosDBTableThroughputMigration</span></span>

## <span data-ttu-id="8df0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8df0d-102">SYNOPSIS</span></span>
<span data-ttu-id="8df0d-103">Otomatik ölçeklendirme çıkışını elle üretilen işleme geçirmek için bunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="8df0d-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="8df0d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8df0d-104">SYNTAX</span></span>

### <span data-ttu-id="8df0d-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8df0d-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8df0d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8df0d-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8df0d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8df0d-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -InputObject <PSTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8df0d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8df0d-108">DESCRIPTION</span></span>
<span data-ttu-id="8df0d-109">ThroughpyteType paramter, geçiş yapmak istediğiniz üretimi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="8df0d-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="8df0d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8df0d-110">EXAMPLES</span></span>

### <span data-ttu-id="8df0d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8df0d-111">Example 1</span></span>
```powershell
PS C:\>
      $NewTable =  New-AzCosmosDBTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```


## <span data-ttu-id="8df0d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8df0d-112">PARAMETERS</span></span>

### <span data-ttu-id="8df0d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8df0d-113">-AccountName</span></span>
<span data-ttu-id="8df0d-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="8df0d-114">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df0d-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="8df0d-115">-Confirm</span></span>
<span data-ttu-id="8df0d-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8df0d-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df0d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8df0d-117">-DefaultProfile</span></span>
<span data-ttu-id="8df0d-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8df0d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df0d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8df0d-119">-InputObject</span></span>
<span data-ttu-id="8df0d-120">Tablo nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8df0d-120">Table Object.</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8df0d-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="8df0d-121">-Name</span></span>
<span data-ttu-id="8df0d-122">Tablonun adı.</span><span class="sxs-lookup"><span data-stu-id="8df0d-122">Name of the Table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df0d-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8df0d-123">-ParentObject</span></span>
<span data-ttu-id="8df0d-124">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="8df0d-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8df0d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8df0d-125">-ResourceGroupName</span></span>
<span data-ttu-id="8df0d-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8df0d-126">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df0d-127">-Throughınputtype</span><span class="sxs-lookup"><span data-stu-id="8df0d-127">-ThroughputType</span></span>
<span data-ttu-id="8df0d-128">Geçirilecek aktarım türü.</span><span class="sxs-lookup"><span data-stu-id="8df0d-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="8df0d-129">Olası değerler: otomatik ölçeklendirme, El Ile.</span><span class="sxs-lookup"><span data-stu-id="8df0d-129">Possible values are: Autoscale, Manual.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df0d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8df0d-130">-WhatIf</span></span>
<span data-ttu-id="8df0d-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8df0d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8df0d-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8df0d-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df0d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8df0d-133">CommonParameters</span></span>
<span data-ttu-id="8df0d-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8df0d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8df0d-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8df0d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8df0d-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8df0d-136">INPUTS</span></span>

### <span data-ttu-id="8df0d-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="8df0d-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="8df0d-138">Microsoft. Azure. Commands. CosmosDB. modeller. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="8df0d-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="8df0d-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8df0d-139">OUTPUTS</span></span>

### <span data-ttu-id="8df0d-140">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="8df0d-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="8df0d-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8df0d-141">NOTES</span></span>

## <span data-ttu-id="8df0d-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8df0d-142">RELATED LINKS</span></span>
