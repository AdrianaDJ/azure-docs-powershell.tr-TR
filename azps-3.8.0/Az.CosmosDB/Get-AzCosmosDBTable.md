---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: 7fb12f7413a0452a3e74f6fa03aa9a391dcacd26
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104882"
---
# <span data-ttu-id="47287-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="47287-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="47287-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47287-102">SYNOPSIS</span></span>
<span data-ttu-id="47287-103">CosmosDB tablosu alır.</span><span class="sxs-lookup"><span data-stu-id="47287-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="47287-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47287-104">SYNTAX</span></span>

### <span data-ttu-id="47287-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="47287-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47287-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47287-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47287-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="47287-107">DESCRIPTION</span></span>
<span data-ttu-id="47287-108">**Get-AzCosmosDBTable** cmdlet 'i var olan bir tabloyu alır.</span><span class="sxs-lookup"><span data-stu-id="47287-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="47287-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47287-109">EXAMPLES</span></span>

### <span data-ttu-id="47287-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="47287-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="47287-111">Resource nesnesi tablonun _rid, _ts, _ ETag özelliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="47287-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="47287-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47287-112">PARAMETERS</span></span>

### <span data-ttu-id="47287-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="47287-113">-AccountName</span></span>
<span data-ttu-id="47287-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="47287-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="47287-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47287-115">-DefaultProfile</span></span>
<span data-ttu-id="47287-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="47287-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47287-117">-Ayrıntılı</span><span class="sxs-lookup"><span data-stu-id="47287-117">-Detailed</span></span>
<span data-ttu-id="47287-118">Sağlanmışsa, cmdlet, ilgili üretilen iş değerini içeren tabloyu döndürür.</span><span class="sxs-lookup"><span data-stu-id="47287-118">If provided then, the cmdlet returns the Table with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47287-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47287-119">-InputObject</span></span>
<span data-ttu-id="47287-120">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="47287-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47287-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="47287-121">-Name</span></span>
<span data-ttu-id="47287-122">Tablonun adı.</span><span class="sxs-lookup"><span data-stu-id="47287-122">Name of the Table.</span></span>

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

### <span data-ttu-id="47287-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47287-123">-ResourceGroupName</span></span>
<span data-ttu-id="47287-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="47287-124">Name of resource group.</span></span>

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

### <span data-ttu-id="47287-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47287-125">CommonParameters</span></span>
<span data-ttu-id="47287-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47287-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47287-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="47287-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47287-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47287-128">INPUTS</span></span>

### <span data-ttu-id="47287-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="47287-129">None</span></span>

## <span data-ttu-id="47287-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47287-130">OUTPUTS</span></span>

### <span data-ttu-id="47287-131">Microsoft. Azure. Commands. CosmosDB. modeller. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="47287-131">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="47287-132">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="47287-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="47287-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47287-133">NOTES</span></span>

## <span data-ttu-id="47287-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47287-134">RELATED LINKS</span></span>
