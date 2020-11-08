---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 7e176ebe2185f2a8c049155e04197b333fabd83c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103714"
---
# <span data-ttu-id="eae9d-101">Remove-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="eae9d-101">Remove-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="eae9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eae9d-102">SYNOPSIS</span></span>
<span data-ttu-id="eae9d-103">CosmosDB Cassandra tablosunu siler.</span><span class="sxs-lookup"><span data-stu-id="eae9d-103">Deletes a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="eae9d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eae9d-104">SYNTAX</span></span>

### <span data-ttu-id="eae9d-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="eae9d-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eae9d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eae9d-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraTable -InputObject <PSCassandraTableGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eae9d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="eae9d-107">DESCRIPTION</span></span>
<span data-ttu-id="eae9d-108">**Remove-AzCosmosDBCassandraTable** , Cosmosdb Cassandra tablosunu silme.</span><span class="sxs-lookup"><span data-stu-id="eae9d-108">The **Remove-AzCosmosDBCassandraTable** delete a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="eae9d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eae9d-109">EXAMPLES</span></span>

### <span data-ttu-id="eae9d-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="eae9d-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroup} -AccountName {account} -KeyspaceName {keyspace} -Name {tableName}
```

<span data-ttu-id="eae9d-111">Cmdlet bool (ne zaman geçiş geçirilir) türünde, silme işlemi başarılıysa doğru olan bir nesneyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="eae9d-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="eae9d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eae9d-112">PARAMETERS</span></span>

### <span data-ttu-id="eae9d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eae9d-113">-AccountName</span></span>
<span data-ttu-id="eae9d-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="eae9d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="eae9d-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="eae9d-115">-Confirm</span></span>
<span data-ttu-id="eae9d-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eae9d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eae9d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eae9d-117">-DefaultProfile</span></span>
<span data-ttu-id="eae9d-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eae9d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eae9d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eae9d-119">-InputObject</span></span>
<span data-ttu-id="eae9d-120">Cassandra tablo nesnesi.</span><span class="sxs-lookup"><span data-stu-id="eae9d-120">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eae9d-121">-Anahtararalığı</span><span class="sxs-lookup"><span data-stu-id="eae9d-121">-KeyspaceName</span></span>
<span data-ttu-id="eae9d-122">Cassandra tuş alanı adı.</span><span class="sxs-lookup"><span data-stu-id="eae9d-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="eae9d-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="eae9d-123">-Name</span></span>
<span data-ttu-id="eae9d-124">Cassandra tablo adı.</span><span class="sxs-lookup"><span data-stu-id="eae9d-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="eae9d-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="eae9d-125">-PassThru</span></span>
<span data-ttu-id="eae9d-126">Kullanıcı çıktı almak isterse true olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="eae9d-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="eae9d-127">İşlem başarılı olduysa ve değilse hata atılır.</span><span class="sxs-lookup"><span data-stu-id="eae9d-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="eae9d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eae9d-128">-ResourceGroupName</span></span>
<span data-ttu-id="eae9d-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="eae9d-129">Name of resource group.</span></span>

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

### <span data-ttu-id="eae9d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eae9d-130">-WhatIf</span></span>
<span data-ttu-id="eae9d-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eae9d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eae9d-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eae9d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eae9d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eae9d-133">CommonParameters</span></span>
<span data-ttu-id="eae9d-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eae9d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eae9d-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="eae9d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eae9d-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eae9d-136">INPUTS</span></span>

### <span data-ttu-id="eae9d-137">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="eae9d-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="eae9d-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eae9d-138">OUTPUTS</span></span>

### <span data-ttu-id="eae9d-139">System. void</span><span class="sxs-lookup"><span data-stu-id="eae9d-139">System.Void</span></span>

### <span data-ttu-id="eae9d-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eae9d-140">System.Boolean</span></span>

## <span data-ttu-id="eae9d-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eae9d-141">NOTES</span></span>

## <span data-ttu-id="eae9d-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eae9d-142">RELATED LINKS</span></span>
