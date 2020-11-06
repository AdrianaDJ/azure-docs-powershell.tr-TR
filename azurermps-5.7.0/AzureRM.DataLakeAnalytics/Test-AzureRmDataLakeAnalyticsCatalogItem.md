---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/test-azurermdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: deb93fb17c2c739dcf377665f8b2f604a2fb4847
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589811"
---
# <span data-ttu-id="52ffb-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="52ffb-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="52ffb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52ffb-102">SYNOPSIS</span></span>
<span data-ttu-id="52ffb-103">Katalog öğesinin varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="52ffb-103">Checks for the existence of a catalog item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52ffb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52ffb-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52ffb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="52ffb-105">DESCRIPTION</span></span>
<span data-ttu-id="52ffb-106">**Test-Azurermdatalakeanalyzer Tic,** bir Azure Data Lake Analytics Katalog öğesinin varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="52ffb-106">The **Test-AzureRmDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="52ffb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52ffb-107">EXAMPLES</span></span>

### <span data-ttu-id="52ffb-108">Örnek 1: bir katalog öğesinin var olup olmadığını test edin</span><span class="sxs-lookup"><span data-stu-id="52ffb-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="52ffb-109">Bu komut belirtilen bir şema öğesinin bulunup bulunmadığını sınar.</span><span class="sxs-lookup"><span data-stu-id="52ffb-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="52ffb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52ffb-110">PARAMETERS</span></span>

### <span data-ttu-id="52ffb-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="52ffb-111">-Account</span></span>
<span data-ttu-id="52ffb-112">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52ffb-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ffb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52ffb-113">-DefaultProfile</span></span>
<span data-ttu-id="52ffb-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="52ffb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52ffb-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="52ffb-115">-ItemType</span></span>
<span data-ttu-id="52ffb-116">Denetlenecek öğenin Katalog öğesi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="52ffb-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="52ffb-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="52ffb-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="52ffb-118">Veritabanı</span><span class="sxs-lookup"><span data-stu-id="52ffb-118">Database</span></span>
- <span data-ttu-id="52ffb-119">Şemayla</span><span class="sxs-lookup"><span data-stu-id="52ffb-119">Schema</span></span>
- <span data-ttu-id="52ffb-120">Derlemeyle</span><span class="sxs-lookup"><span data-stu-id="52ffb-120">Assembly</span></span>
- <span data-ttu-id="52ffb-121">Tablo</span><span class="sxs-lookup"><span data-stu-id="52ffb-121">Table</span></span>
- <span data-ttu-id="52ffb-122">Tablobölümü</span><span class="sxs-lookup"><span data-stu-id="52ffb-122">TablePartition</span></span>
- <span data-ttu-id="52ffb-123">Tablodeğerdenişlevi</span><span class="sxs-lookup"><span data-stu-id="52ffb-123">TableValuedFunction</span></span>
- <span data-ttu-id="52ffb-124">Tabloistatistikleri</span><span class="sxs-lookup"><span data-stu-id="52ffb-124">TableStatistics</span></span>
- <span data-ttu-id="52ffb-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="52ffb-125">ExternalDataSource</span></span>
- <span data-ttu-id="52ffb-126">Görünümünde</span><span class="sxs-lookup"><span data-stu-id="52ffb-126">View</span></span>
- <span data-ttu-id="52ffb-127">Anlatılan</span><span class="sxs-lookup"><span data-stu-id="52ffb-127">Procedure</span></span>
- <span data-ttu-id="52ffb-128">Gizlili</span><span class="sxs-lookup"><span data-stu-id="52ffb-128">Secret</span></span>
- <span data-ttu-id="52ffb-129">Sertifika</span><span class="sxs-lookup"><span data-stu-id="52ffb-129">Credential</span></span>
- <span data-ttu-id="52ffb-130">Tipte</span><span class="sxs-lookup"><span data-stu-id="52ffb-130">Types</span></span>

```yaml
Type: CatalogItemType
Parameter Sets: (All)
Aliases: 
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ffb-131">-Yol</span><span class="sxs-lookup"><span data-stu-id="52ffb-131">-Path</span></span>
<span data-ttu-id="52ffb-132">Getirilecek öğenin yolunu veya listedeki öğelerin üst öğesinin yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="52ffb-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

```yaml
Type: CatalogPathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ffb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52ffb-133">CommonParameters</span></span>
<span data-ttu-id="52ffb-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52ffb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52ffb-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52ffb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52ffb-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52ffb-136">INPUTS</span></span>

### <span data-ttu-id="52ffb-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="52ffb-137">None</span></span>
<span data-ttu-id="52ffb-138">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="52ffb-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="52ffb-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52ffb-139">OUTPUTS</span></span>

### <span data-ttu-id="52ffb-140">bool</span><span class="sxs-lookup"><span data-stu-id="52ffb-140">bool</span></span>
<span data-ttu-id="52ffb-141">Belirtilen katalog öğesinin var olup olmadığını belirten doğru veya yanlış.</span><span class="sxs-lookup"><span data-stu-id="52ffb-141">True or false indicating if the specified catalog item exists or not.</span></span>

## <span data-ttu-id="52ffb-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52ffb-142">NOTES</span></span>

## <span data-ttu-id="52ffb-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52ffb-143">RELATED LINKS</span></span>

[<span data-ttu-id="52ffb-144">Get-Azurermdatalakeanalyzer Tic, Alogıtem</span><span class="sxs-lookup"><span data-stu-id="52ffb-144">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Get-AzureRmDataLakeAnalyticsCatalogItem.md)


