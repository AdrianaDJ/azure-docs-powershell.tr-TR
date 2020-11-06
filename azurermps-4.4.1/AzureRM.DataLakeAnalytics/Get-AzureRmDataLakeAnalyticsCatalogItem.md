---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: b12b09c686a2e0a5fcd85854551608b16cb43d3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594294"
---
# <span data-ttu-id="58f46-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="58f46-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="58f46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58f46-102">SYNOPSIS</span></span>
<span data-ttu-id="58f46-103">Veri Lake Analytics Katalog öğesi veya öğe türleri alır.</span><span class="sxs-lookup"><span data-stu-id="58f46-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58f46-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="58f46-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58f46-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="58f46-105">DESCRIPTION</span></span>
<span data-ttu-id="58f46-106">**Get-Azurermdatalakeanalizleri** , belirtilen Azure Data Lake Analytics Katalog öğesini alır veya belirtilen türde katalog öğelerini alır.</span><span class="sxs-lookup"><span data-stu-id="58f46-106">The **Get-AzureRmDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="58f46-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="58f46-107">EXAMPLES</span></span>

### <span data-ttu-id="58f46-108">Örnek 1: belirli bir veritabanı alma</span><span class="sxs-lookup"><span data-stu-id="58f46-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="58f46-109">Bu komut belirtilen veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="58f46-109">This command gets the specified database.</span></span>

### <span data-ttu-id="58f46-110">Örnek 2: belirtilen veritabanı ve şemada tablolar alma</span><span class="sxs-lookup"><span data-stu-id="58f46-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="58f46-111">Bu komut, belirtilen veritabanındaki tabloların listesini alır.</span><span class="sxs-lookup"><span data-stu-id="58f46-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="58f46-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="58f46-112">PARAMETERS</span></span>

### <span data-ttu-id="58f46-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="58f46-113">-Account</span></span>
<span data-ttu-id="58f46-114">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="58f46-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="58f46-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="58f46-115">-ItemType</span></span>
<span data-ttu-id="58f46-116">Getirilen veya listelenen öğelerin Katalog öğesi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="58f46-116">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="58f46-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="58f46-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="58f46-118">Veritabanı</span><span class="sxs-lookup"><span data-stu-id="58f46-118">Database</span></span>
- <span data-ttu-id="58f46-119">Şemayla</span><span class="sxs-lookup"><span data-stu-id="58f46-119">Schema</span></span>
- <span data-ttu-id="58f46-120">Derlemeyle</span><span class="sxs-lookup"><span data-stu-id="58f46-120">Assembly</span></span>
- <span data-ttu-id="58f46-121">Tablo</span><span class="sxs-lookup"><span data-stu-id="58f46-121">Table</span></span>
- <span data-ttu-id="58f46-122">Tablodeğerdenişlevi</span><span class="sxs-lookup"><span data-stu-id="58f46-122">TableValuedFunction</span></span>
- <span data-ttu-id="58f46-123">Tabloistatistikleri</span><span class="sxs-lookup"><span data-stu-id="58f46-123">TableStatistics</span></span>
- <span data-ttu-id="58f46-124">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="58f46-124">ExternalDataSource</span></span>
- <span data-ttu-id="58f46-125">Görünümünde</span><span class="sxs-lookup"><span data-stu-id="58f46-125">View</span></span>
- <span data-ttu-id="58f46-126">Anlatılan</span><span class="sxs-lookup"><span data-stu-id="58f46-126">Procedure</span></span>
- <span data-ttu-id="58f46-127">Gizlili</span><span class="sxs-lookup"><span data-stu-id="58f46-127">Secret</span></span>
- <span data-ttu-id="58f46-128">Sertifika</span><span class="sxs-lookup"><span data-stu-id="58f46-128">Credential</span></span>
- <span data-ttu-id="58f46-129">Tipte</span><span class="sxs-lookup"><span data-stu-id="58f46-129">Types</span></span>
- <span data-ttu-id="58f46-130">Tablobölümü</span><span class="sxs-lookup"><span data-stu-id="58f46-130">TablePartition</span></span>

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

### <span data-ttu-id="58f46-131">-Yol</span><span class="sxs-lookup"><span data-stu-id="58f46-131">-Path</span></span>
<span data-ttu-id="58f46-132">Alınacak öğenin birden çok parçalı yolunu veya listedeki öğelerin üst öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="58f46-132">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="58f46-133">Yolun bölümleri noktayla ayrılmalıdır (.).</span><span class="sxs-lookup"><span data-stu-id="58f46-133">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="58f46-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58f46-134">-DefaultProfile</span></span>
<span data-ttu-id="58f46-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="58f46-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58f46-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58f46-136">CommonParameters</span></span>
<span data-ttu-id="58f46-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="58f46-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58f46-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58f46-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58f46-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="58f46-139">INPUTS</span></span>

## <span data-ttu-id="58f46-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="58f46-140">OUTPUTS</span></span>

### <span data-ttu-id="58f46-141">CatalogItem</span><span class="sxs-lookup"><span data-stu-id="58f46-141">CatalogItem</span></span>
<span data-ttu-id="58f46-142">Belirtilen katalog öğesi.</span><span class="sxs-lookup"><span data-stu-id="58f46-142">The specified catalog item.</span></span>

### <span data-ttu-id="58f46-143">Listeniz<CatalogItem></span><span class="sxs-lookup"><span data-stu-id="58f46-143">List<CatalogItem></span></span>
<span data-ttu-id="58f46-144">İlgili kapsayıcının altındaki belirtilen Katalog öğelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="58f46-144">The list of the specified catalog items underneath their corresponding container.</span></span>

## <span data-ttu-id="58f46-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="58f46-145">NOTES</span></span>

## <span data-ttu-id="58f46-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="58f46-146">RELATED LINKS</span></span>

[<span data-ttu-id="58f46-147">Test-Azurermdatalakeanalyzer Tic, Alogıtem</span><span class="sxs-lookup"><span data-stu-id="58f46-147">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Test-AzureRmDataLakeAnalyticsCatalogItem.md)


