---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 7e176ebe2185f2a8c049155e04197b333fabd83c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94275082"
---
# <span data-ttu-id="d494a-101">Remove-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="d494a-101">Remove-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="d494a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d494a-102">SYNOPSIS</span></span>
<span data-ttu-id="d494a-103">CosmosDB Cassandra tablosunu siler.</span><span class="sxs-lookup"><span data-stu-id="d494a-103">Deletes a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="d494a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d494a-104">SYNTAX</span></span>

### <span data-ttu-id="d494a-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d494a-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d494a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d494a-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraTable -InputObject <PSCassandraTableGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d494a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d494a-107">DESCRIPTION</span></span>
<span data-ttu-id="d494a-108">**Remove-AzCosmosDBCassandraTable** , Cosmosdb Cassandra tablosunu silme.</span><span class="sxs-lookup"><span data-stu-id="d494a-108">The **Remove-AzCosmosDBCassandraTable** delete a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="d494a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d494a-109">EXAMPLES</span></span>

### <span data-ttu-id="d494a-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d494a-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroup} -AccountName {account} -KeyspaceName {keyspace} -Name {tableName}
```

<span data-ttu-id="d494a-111">Cmdlet bool (ne zaman geçiş geçirilir) türünde, silme işlemi başarılıysa doğru olan bir nesneyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="d494a-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="d494a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d494a-112">PARAMETERS</span></span>

### <span data-ttu-id="d494a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d494a-113">-AccountName</span></span>
<span data-ttu-id="d494a-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="d494a-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d494a-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="d494a-115">-Confirm</span></span>
<span data-ttu-id="d494a-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d494a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d494a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d494a-117">-DefaultProfile</span></span>
<span data-ttu-id="d494a-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d494a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d494a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d494a-119">-InputObject</span></span>
<span data-ttu-id="d494a-120">Cassandra tablo nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d494a-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="d494a-121">-Anahtararalığı</span><span class="sxs-lookup"><span data-stu-id="d494a-121">-KeyspaceName</span></span>
<span data-ttu-id="d494a-122">Cassandra tuş alanı adı.</span><span class="sxs-lookup"><span data-stu-id="d494a-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="d494a-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="d494a-123">-Name</span></span>
<span data-ttu-id="d494a-124">Cassandra tablo adı.</span><span class="sxs-lookup"><span data-stu-id="d494a-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="d494a-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d494a-125">-PassThru</span></span>
<span data-ttu-id="d494a-126">Kullanıcı çıktı almak isterse true olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="d494a-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="d494a-127">İşlem başarılı olduysa ve değilse hata atılır.</span><span class="sxs-lookup"><span data-stu-id="d494a-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="d494a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d494a-128">-ResourceGroupName</span></span>
<span data-ttu-id="d494a-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d494a-129">Name of resource group.</span></span>

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

### <span data-ttu-id="d494a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d494a-130">-WhatIf</span></span>
<span data-ttu-id="d494a-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d494a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d494a-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d494a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d494a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d494a-133">CommonParameters</span></span>
<span data-ttu-id="d494a-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d494a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d494a-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d494a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d494a-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d494a-136">INPUTS</span></span>

### <span data-ttu-id="d494a-137">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="d494a-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="d494a-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d494a-138">OUTPUTS</span></span>

### <span data-ttu-id="d494a-139">System. void</span><span class="sxs-lookup"><span data-stu-id="d494a-139">System.Void</span></span>

### <span data-ttu-id="d494a-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d494a-140">System.Boolean</span></span>

## <span data-ttu-id="d494a-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d494a-141">NOTES</span></span>

## <span data-ttu-id="d494a-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d494a-142">RELATED LINKS</span></span>
