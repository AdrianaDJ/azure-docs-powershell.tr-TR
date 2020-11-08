---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: fb0e73d338c54b93626ee3a5ee78bbbe4adca884
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097850"
---
# <span data-ttu-id="2f584-101">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="2f584-101">Get-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="2f584-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f584-102">SYNOPSIS</span></span>
<span data-ttu-id="2f584-103">Veri Lake Analytics Katalog öğesi veya öğe türleri alır.</span><span class="sxs-lookup"><span data-stu-id="2f584-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

## <span data-ttu-id="2f584-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f584-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f584-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f584-105">DESCRIPTION</span></span>
<span data-ttu-id="2f584-106">**Get-Azdatalakeanaliz Ticdağlı Alogıtem** , belirtilen Azure Data Lake Analytics Katalog öğesini alır veya belirtilen türde katalog öğelerini alır.</span><span class="sxs-lookup"><span data-stu-id="2f584-106">The **Get-AzDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="2f584-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f584-107">EXAMPLES</span></span>

### <span data-ttu-id="2f584-108">Örnek 1: belirli bir veritabanı alma</span><span class="sxs-lookup"><span data-stu-id="2f584-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="2f584-109">Bu komut belirtilen veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="2f584-109">This command gets the specified database.</span></span>

### <span data-ttu-id="2f584-110">Örnek 2: belirtilen veritabanı ve şemada tablolar alma</span><span class="sxs-lookup"><span data-stu-id="2f584-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="2f584-111">Bu komut, belirtilen veritabanındaki tabloların listesini alır.</span><span class="sxs-lookup"><span data-stu-id="2f584-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="2f584-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f584-112">PARAMETERS</span></span>

### <span data-ttu-id="2f584-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="2f584-113">-Account</span></span>
<span data-ttu-id="2f584-114">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f584-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f584-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f584-115">-DefaultProfile</span></span>
<span data-ttu-id="2f584-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2f584-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f584-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="2f584-117">-ItemType</span></span>
<span data-ttu-id="2f584-118">Getirilen veya listelenen öğelerin Katalog öğesi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f584-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="2f584-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="2f584-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2f584-120">Veritabanı</span><span class="sxs-lookup"><span data-stu-id="2f584-120">Database</span></span>
- <span data-ttu-id="2f584-121">Şemayla</span><span class="sxs-lookup"><span data-stu-id="2f584-121">Schema</span></span>
- <span data-ttu-id="2f584-122">Derlemeyle</span><span class="sxs-lookup"><span data-stu-id="2f584-122">Assembly</span></span>
- <span data-ttu-id="2f584-123">Tablo</span><span class="sxs-lookup"><span data-stu-id="2f584-123">Table</span></span>
- <span data-ttu-id="2f584-124">Tablodeğerdenişlevi</span><span class="sxs-lookup"><span data-stu-id="2f584-124">TableValuedFunction</span></span>
- <span data-ttu-id="2f584-125">Tabloistatistikleri</span><span class="sxs-lookup"><span data-stu-id="2f584-125">TableStatistics</span></span>
- <span data-ttu-id="2f584-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="2f584-126">ExternalDataSource</span></span>
- <span data-ttu-id="2f584-127">Görünümünde</span><span class="sxs-lookup"><span data-stu-id="2f584-127">View</span></span>
- <span data-ttu-id="2f584-128">Anlatılan</span><span class="sxs-lookup"><span data-stu-id="2f584-128">Procedure</span></span>
- <span data-ttu-id="2f584-129">Gizlili</span><span class="sxs-lookup"><span data-stu-id="2f584-129">Secret</span></span>
- <span data-ttu-id="2f584-130">Sertifika</span><span class="sxs-lookup"><span data-stu-id="2f584-130">Credential</span></span>
- <span data-ttu-id="2f584-131">Tipte</span><span class="sxs-lookup"><span data-stu-id="2f584-131">Types</span></span>
- <span data-ttu-id="2f584-132">Tablobölümü</span><span class="sxs-lookup"><span data-stu-id="2f584-132">TablePartition</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType
Parameter Sets: (All)
Aliases:
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f584-133">-Yol</span><span class="sxs-lookup"><span data-stu-id="2f584-133">-Path</span></span>
<span data-ttu-id="2f584-134">Alınacak öğenin birden çok parçalı yolunu veya listedeki öğelerin üst öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f584-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="2f584-135">Yolun bölümleri noktayla ayrılmalıdır (.).</span><span class="sxs-lookup"><span data-stu-id="2f584-135">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f584-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f584-136">CommonParameters</span></span>
<span data-ttu-id="2f584-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f584-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f584-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f584-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f584-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f584-139">INPUTS</span></span>

### <span data-ttu-id="2f584-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2f584-140">System.String</span></span>

### <span data-ttu-id="2f584-141">Microsoft. Azure. Commands. DataLakeAnalytics. modeller. Datalakeanalizleri Ticsenums + Catalogıtemtype</span><span class="sxs-lookup"><span data-stu-id="2f584-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="2f584-142">Microsoft. Azure. Commands. DataLakeAnalytics. model. Catalogpathınstance</span><span class="sxs-lookup"><span data-stu-id="2f584-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="2f584-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f584-143">OUTPUTS</span></span>

### <span data-ttu-id="2f584-144">Microsoft. Azure. Management. DataLake. Analytics. modeller. CatalogItem</span><span class="sxs-lookup"><span data-stu-id="2f584-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span></span>

## <span data-ttu-id="2f584-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f584-145">NOTES</span></span>

## <span data-ttu-id="2f584-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f584-146">RELATED LINKS</span></span>

[<span data-ttu-id="2f584-147">Test-Azdatalakeanaliz Ticdağlı Alogıtem</span><span class="sxs-lookup"><span data-stu-id="2f584-147">Test-AzDataLakeAnalyticsCatalogItem</span></span>](./Test-AzDataLakeAnalyticsCatalogItem.md)

