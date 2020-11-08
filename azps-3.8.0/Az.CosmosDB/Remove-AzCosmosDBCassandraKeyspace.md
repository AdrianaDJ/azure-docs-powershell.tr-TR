---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 7f6cae6a3187bf4393ea4fb592123c1833a18ebb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103713"
---
# <span data-ttu-id="d8f94-101">Remove-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="d8f94-101">Remove-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="d8f94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8f94-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f94-103">CosmosDB Cassandra anahtar uzayını siler.</span><span class="sxs-lookup"><span data-stu-id="d8f94-103">Deletes a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="d8f94-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8f94-104">SYNTAX</span></span>

### <span data-ttu-id="d8f94-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8f94-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8f94-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8f94-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -InputObject <PSCassandraKeyspaceGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8f94-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8f94-107">DESCRIPTION</span></span>
<span data-ttu-id="d8f94-108">**Remove-AzCosmosDBCassandraKeyspace** cmdlet 'i var olan cosmosdb</span><span class="sxs-lookup"><span data-stu-id="d8f94-108">The **Remove-AzCosmosDBCassandraKeyspace** cmdlet deletes an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="d8f94-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8f94-109">EXAMPLES</span></span>

### <span data-ttu-id="d8f94-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d8f94-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {keyspaceName}
```

<span data-ttu-id="d8f94-111">Cmdlet, silme işlemi başarılı olmuşsa, bool (ne zaman geçiş geçirildiğinde) türünde bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="d8f94-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true if the delete was successful.</span></span>

## <span data-ttu-id="d8f94-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8f94-112">PARAMETERS</span></span>

### <span data-ttu-id="d8f94-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d8f94-113">-AccountName</span></span>
<span data-ttu-id="d8f94-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="d8f94-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d8f94-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="d8f94-115">-Confirm</span></span>
<span data-ttu-id="d8f94-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d8f94-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8f94-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f94-117">-DefaultProfile</span></span>
<span data-ttu-id="d8f94-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8f94-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8f94-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8f94-119">-InputObject</span></span>
<span data-ttu-id="d8f94-120">Cassandra keyspace nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d8f94-120">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8f94-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="d8f94-121">-Name</span></span>
<span data-ttu-id="d8f94-122">Cassandra tuş alanı adı.</span><span class="sxs-lookup"><span data-stu-id="d8f94-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="d8f94-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d8f94-123">-PassThru</span></span>
<span data-ttu-id="d8f94-124">Kullanıcı çıktı almak isterse true olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="d8f94-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="d8f94-125">İşlem başarılı olduysa ve değilse hata atılır.</span><span class="sxs-lookup"><span data-stu-id="d8f94-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="d8f94-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8f94-126">-ResourceGroupName</span></span>
<span data-ttu-id="d8f94-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d8f94-127">Name of resource group.</span></span>

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

### <span data-ttu-id="d8f94-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8f94-128">-WhatIf</span></span>
<span data-ttu-id="d8f94-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d8f94-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8f94-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d8f94-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8f94-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f94-131">CommonParameters</span></span>
<span data-ttu-id="d8f94-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8f94-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f94-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d8f94-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f94-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8f94-134">INPUTS</span></span>

### <span data-ttu-id="d8f94-135">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="d8f94-135">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="d8f94-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8f94-136">OUTPUTS</span></span>

### <span data-ttu-id="d8f94-137">System. void</span><span class="sxs-lookup"><span data-stu-id="d8f94-137">System.Void</span></span>

### <span data-ttu-id="d8f94-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d8f94-138">System.Boolean</span></span>

## <span data-ttu-id="d8f94-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8f94-139">NOTES</span></span>

## <span data-ttu-id="d8f94-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8f94-140">RELATED LINKS</span></span>
