---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBTable.md
ms.openlocfilehash: 9499933ef8e7b9e815d1438778a65f8abfdf7bff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097671"
---
# <span data-ttu-id="725ef-101">Set-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="725ef-101">Set-AzCosmosDBTable</span></span>

## <span data-ttu-id="725ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="725ef-102">SYNOPSIS</span></span>
<span data-ttu-id="725ef-103">CosmosDB tablosunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="725ef-103">Sets the CosmosDB Table.</span></span>

## <span data-ttu-id="725ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="725ef-104">SYNTAX</span></span>

### <span data-ttu-id="725ef-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="725ef-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="725ef-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="725ef-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBTable -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="725ef-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="725ef-107">DESCRIPTION</span></span>
<span data-ttu-id="725ef-108">**Set-AzCosmosDBTable** cmdlet 'i yeni bir tablo oluşturur ya da var olan tabloyu güncelleştirir, var olan tabloyu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="725ef-108">The **Set-AzCosmosDBTable** cmdlet creates a new Table or updates an existing Table, replacing the existing Table entirely.</span></span>

## <span data-ttu-id="725ef-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="725ef-109">EXAMPLES</span></span>

### <span data-ttu-id="725ef-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="725ef-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="725ef-111">Resource nesnesi tablonun _rid, _ts, _ ETag özelliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="725ef-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="725ef-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="725ef-112">PARAMETERS</span></span>

### <span data-ttu-id="725ef-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="725ef-113">-AccountName</span></span>
<span data-ttu-id="725ef-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="725ef-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="725ef-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="725ef-115">-Confirm</span></span>
<span data-ttu-id="725ef-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="725ef-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="725ef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="725ef-117">-DefaultProfile</span></span>
<span data-ttu-id="725ef-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="725ef-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="725ef-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="725ef-119">-InputObject</span></span>
<span data-ttu-id="725ef-120">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="725ef-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="725ef-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="725ef-121">-Name</span></span>
<span data-ttu-id="725ef-122">Tablonun adı.</span><span class="sxs-lookup"><span data-stu-id="725ef-122">Name of the Table.</span></span>

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

### <span data-ttu-id="725ef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="725ef-123">-ResourceGroupName</span></span>
<span data-ttu-id="725ef-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="725ef-124">Name of resource group.</span></span>

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

### <span data-ttu-id="725ef-125">-Üretim</span><span class="sxs-lookup"><span data-stu-id="725ef-125">-Throughput</span></span>
<span data-ttu-id="725ef-126">Tablonun üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="725ef-126">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="725ef-127">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="725ef-127">Default value is 400.</span></span>

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

### <span data-ttu-id="725ef-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="725ef-128">-WhatIf</span></span>
<span data-ttu-id="725ef-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="725ef-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="725ef-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="725ef-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="725ef-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="725ef-131">CommonParameters</span></span>
<span data-ttu-id="725ef-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="725ef-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="725ef-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="725ef-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="725ef-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="725ef-134">INPUTS</span></span>

### <span data-ttu-id="725ef-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="725ef-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="725ef-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="725ef-136">OUTPUTS</span></span>

### <span data-ttu-id="725ef-137">Microsoft. Azure. Commands. CosmosDB. modeller. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="725ef-137">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="725ef-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="725ef-138">NOTES</span></span>

## <span data-ttu-id="725ef-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="725ef-139">RELATED LINKS</span></span>
