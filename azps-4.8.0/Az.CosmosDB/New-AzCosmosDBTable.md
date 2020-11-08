---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
ms.openlocfilehash: 41494f860eea0ad811e9066d1fa8a45032b2317d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268041"
---
# <span data-ttu-id="652ed-101">New-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="652ed-101">New-AzCosmosDBTable</span></span>

## <span data-ttu-id="652ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="652ed-102">SYNOPSIS</span></span>
<span data-ttu-id="652ed-103">Yeni bir CosmosDB tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="652ed-103">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="652ed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="652ed-104">SYNTAX</span></span>

### <span data-ttu-id="652ed-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="652ed-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="652ed-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="652ed-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="652ed-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="652ed-107">DESCRIPTION</span></span>
<span data-ttu-id="652ed-108">Yeni bir CosmosDB tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="652ed-108">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="652ed-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="652ed-109">EXAMPLES</span></span>

### <span data-ttu-id="652ed-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="652ed-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="652ed-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="652ed-111">PARAMETERS</span></span>

### <span data-ttu-id="652ed-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="652ed-112">-AccountName</span></span>
<span data-ttu-id="652ed-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="652ed-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="652ed-114">-Otomatik ölçek Maxüretilen Iş</span><span class="sxs-lookup"><span data-stu-id="652ed-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="652ed-115">Otomatik ölçeklendirme etkinleştirilirse maksimum üretilen Iş değeri.</span><span class="sxs-lookup"><span data-stu-id="652ed-115">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652ed-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="652ed-116">-Confirm</span></span>
<span data-ttu-id="652ed-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="652ed-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="652ed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="652ed-118">-DefaultProfile</span></span>
<span data-ttu-id="652ed-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="652ed-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="652ed-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="652ed-120">-Name</span></span>
<span data-ttu-id="652ed-121">Tablonun adı.</span><span class="sxs-lookup"><span data-stu-id="652ed-121">Name of the Table.</span></span>

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

### <span data-ttu-id="652ed-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="652ed-122">-ParentObject</span></span>
<span data-ttu-id="652ed-123">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="652ed-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="652ed-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="652ed-124">-ResourceGroupName</span></span>
<span data-ttu-id="652ed-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="652ed-125">Name of resource group.</span></span>

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

### <span data-ttu-id="652ed-126">-Üretim</span><span class="sxs-lookup"><span data-stu-id="652ed-126">-Throughput</span></span>
<span data-ttu-id="652ed-127">Tablonun üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="652ed-127">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="652ed-128">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="652ed-128">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652ed-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="652ed-129">-WhatIf</span></span>
<span data-ttu-id="652ed-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="652ed-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="652ed-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="652ed-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="652ed-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="652ed-132">CommonParameters</span></span>
<span data-ttu-id="652ed-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="652ed-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="652ed-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="652ed-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="652ed-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="652ed-135">INPUTS</span></span>

### <span data-ttu-id="652ed-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="652ed-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="652ed-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="652ed-137">OUTPUTS</span></span>

### <span data-ttu-id="652ed-138">Microsoft. Azure. Commands. CosmosDB. modeller. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="652ed-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="652ed-139">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="652ed-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="652ed-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="652ed-140">NOTES</span></span>

## <span data-ttu-id="652ed-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="652ed-141">RELATED LINKS</span></span>
