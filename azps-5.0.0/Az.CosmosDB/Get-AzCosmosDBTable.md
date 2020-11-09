---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: d405c081ab1f848e25b67de4ec100f40b40fb4c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321646"
---
# <span data-ttu-id="3b131-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="3b131-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="3b131-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b131-102">SYNOPSIS</span></span>
<span data-ttu-id="3b131-103">CosmosDB tablosu alır.</span><span class="sxs-lookup"><span data-stu-id="3b131-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="3b131-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b131-104">SYNTAX</span></span>

### <span data-ttu-id="3b131-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3b131-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b131-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b131-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b131-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b131-107">DESCRIPTION</span></span>
<span data-ttu-id="3b131-108">**Get-AzCosmosDBTable** cmdlet 'i var olan bir tabloyu alır.</span><span class="sxs-lookup"><span data-stu-id="3b131-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="3b131-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b131-109">EXAMPLES</span></span>

### <span data-ttu-id="3b131-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3b131-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="3b131-111">Resource nesnesi tablonun _rid, _ts, _ ETag özelliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="3b131-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="3b131-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b131-112">PARAMETERS</span></span>

### <span data-ttu-id="3b131-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3b131-113">-AccountName</span></span>
<span data-ttu-id="3b131-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="3b131-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3b131-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b131-115">-DefaultProfile</span></span>
<span data-ttu-id="3b131-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3b131-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b131-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="3b131-117">-Name</span></span>
<span data-ttu-id="3b131-118">Tablonun adı.</span><span class="sxs-lookup"><span data-stu-id="3b131-118">Name of the Table.</span></span>

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

### <span data-ttu-id="3b131-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3b131-119">-ParentObject</span></span>
<span data-ttu-id="3b131-120">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="3b131-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b131-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b131-121">-ResourceGroupName</span></span>
<span data-ttu-id="3b131-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3b131-122">Name of resource group.</span></span>

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

### <span data-ttu-id="3b131-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b131-123">CommonParameters</span></span>
<span data-ttu-id="3b131-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b131-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b131-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3b131-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b131-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b131-126">INPUTS</span></span>

### <span data-ttu-id="3b131-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3b131-127">None</span></span>

## <span data-ttu-id="3b131-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b131-128">OUTPUTS</span></span>

### <span data-ttu-id="3b131-129">Microsoft. Azure. Commands. CosmosDB. modeller. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="3b131-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="3b131-130">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="3b131-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="3b131-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b131-131">NOTES</span></span>

## <span data-ttu-id="3b131-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b131-132">RELATED LINKS</span></span>
