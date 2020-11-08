---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
ms.openlocfilehash: efc177e5255f4325fc2ecbfe88e94bb32708c45a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267838"
---
# <span data-ttu-id="a37a4-101">Update-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="a37a4-101">Update-AzCosmosDBTable</span></span>

## <span data-ttu-id="a37a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a37a4-102">SYNOPSIS</span></span>
<span data-ttu-id="a37a4-103">CosmosDB tablosunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a37a4-103">Updates the CosmosDB Table.</span></span> <span data-ttu-id="a37a4-104">Var olan tabloyu okuyarak bir istemci tarafı düzeltme eki işlemi gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="a37a4-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="a37a4-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a37a4-105">SYNTAX</span></span>

### <span data-ttu-id="a37a4-106">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a37a4-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a37a4-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a37a4-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a37a4-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a37a4-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a37a4-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="a37a4-109">DESCRIPTION</span></span>
<span data-ttu-id="a37a4-110">CosmosDB tablosunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a37a4-110">Updates the CosmosDB Table.</span></span> <span data-ttu-id="a37a4-111">Var olan tabloyu okuyarak bir istemci tarafı düzeltme eki işlemi gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="a37a4-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="a37a4-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a37a4-112">EXAMPLES</span></span>

### <span data-ttu-id="a37a4-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a37a4-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName Throughput 800

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="a37a4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a37a4-114">PARAMETERS</span></span>

### <span data-ttu-id="a37a4-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a37a4-115">-AccountName</span></span>
<span data-ttu-id="a37a4-116">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="a37a4-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a37a4-117">-Otomatik ölçek Maxüretilen Iş</span><span class="sxs-lookup"><span data-stu-id="a37a4-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="a37a4-118">Otomatik ölçeklendirme etkinleştirilirse maksimum üretilen Iş değeri.</span><span class="sxs-lookup"><span data-stu-id="a37a4-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="a37a4-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="a37a4-119">-Confirm</span></span>
<span data-ttu-id="a37a4-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a37a4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a37a4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a37a4-121">-DefaultProfile</span></span>
<span data-ttu-id="a37a4-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a37a4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a37a4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a37a4-123">-InputObject</span></span>
<span data-ttu-id="a37a4-124">Tablo nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a37a4-124">Table Object.</span></span>

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

### <span data-ttu-id="a37a4-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="a37a4-125">-Name</span></span>
<span data-ttu-id="a37a4-126">Tablonun adı.</span><span class="sxs-lookup"><span data-stu-id="a37a4-126">Name of the Table.</span></span>

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

### <span data-ttu-id="a37a4-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a37a4-127">-ParentObject</span></span>
<span data-ttu-id="a37a4-128">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="a37a4-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="a37a4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a37a4-129">-ResourceGroupName</span></span>
<span data-ttu-id="a37a4-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a37a4-130">Name of resource group.</span></span>

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

### <span data-ttu-id="a37a4-131">-Üretim</span><span class="sxs-lookup"><span data-stu-id="a37a4-131">-Throughput</span></span>
<span data-ttu-id="a37a4-132">Tablonun üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="a37a4-132">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="a37a4-133">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="a37a4-133">Default value is 400.</span></span>

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

### <span data-ttu-id="a37a4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a37a4-134">-WhatIf</span></span>
<span data-ttu-id="a37a4-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a37a4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a37a4-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a37a4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a37a4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a37a4-137">CommonParameters</span></span>
<span data-ttu-id="a37a4-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a37a4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a37a4-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a37a4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a37a4-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a37a4-140">INPUTS</span></span>

### <span data-ttu-id="a37a4-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="a37a4-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="a37a4-142">Microsoft. Azure. Commands. CosmosDB. modeller. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="a37a4-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="a37a4-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a37a4-143">OUTPUTS</span></span>

### <span data-ttu-id="a37a4-144">Microsoft. Azure. Commands. CosmosDB. modeller. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="a37a4-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="a37a4-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="a37a4-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="a37a4-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a37a4-146">NOTES</span></span>

## <span data-ttu-id="a37a4-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a37a4-147">RELATED LINKS</span></span>
