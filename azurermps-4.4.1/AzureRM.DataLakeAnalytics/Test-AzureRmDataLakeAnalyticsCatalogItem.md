---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 249ef7ae66436d4bf82b3b038aa8b1201f68110e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763123"
---
# <span data-ttu-id="d172c-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="d172c-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="d172c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d172c-102">SYNOPSIS</span></span>
<span data-ttu-id="d172c-103">Katalog öğesinin varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="d172c-103">Checks for the existence of a catalog item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d172c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d172c-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d172c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d172c-105">DESCRIPTION</span></span>
<span data-ttu-id="d172c-106">**Test-Azurermdatalakeanalyzer Tic,** bir Azure Data Lake Analytics Katalog öğesinin varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="d172c-106">The **Test-AzureRmDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="d172c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d172c-107">EXAMPLES</span></span>

### <span data-ttu-id="d172c-108">Örnek 1: bir katalog öğesinin var olup olmadığını test edin</span><span class="sxs-lookup"><span data-stu-id="d172c-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="d172c-109">Bu komut belirtilen bir şema öğesinin bulunup bulunmadığını sınar.</span><span class="sxs-lookup"><span data-stu-id="d172c-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="d172c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d172c-110">PARAMETERS</span></span>

### <span data-ttu-id="d172c-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="d172c-111">-Account</span></span>
<span data-ttu-id="d172c-112">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d172c-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="d172c-113">-ItemType</span><span class="sxs-lookup"><span data-stu-id="d172c-113">-ItemType</span></span>
<span data-ttu-id="d172c-114">Denetlenecek öğenin Katalog öğesi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d172c-114">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="d172c-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d172c-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d172c-116">Veritabanı</span><span class="sxs-lookup"><span data-stu-id="d172c-116">Database</span></span>
- <span data-ttu-id="d172c-117">Şemayla</span><span class="sxs-lookup"><span data-stu-id="d172c-117">Schema</span></span>
- <span data-ttu-id="d172c-118">Derlemeyle</span><span class="sxs-lookup"><span data-stu-id="d172c-118">Assembly</span></span>
- <span data-ttu-id="d172c-119">Tablo</span><span class="sxs-lookup"><span data-stu-id="d172c-119">Table</span></span>
- <span data-ttu-id="d172c-120">Tablobölümü</span><span class="sxs-lookup"><span data-stu-id="d172c-120">TablePartition</span></span>
- <span data-ttu-id="d172c-121">Tablodeğerdenişlevi</span><span class="sxs-lookup"><span data-stu-id="d172c-121">TableValuedFunction</span></span>
- <span data-ttu-id="d172c-122">Tabloistatistikleri</span><span class="sxs-lookup"><span data-stu-id="d172c-122">TableStatistics</span></span>
- <span data-ttu-id="d172c-123">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="d172c-123">ExternalDataSource</span></span>
- <span data-ttu-id="d172c-124">Görünümünde</span><span class="sxs-lookup"><span data-stu-id="d172c-124">View</span></span>
- <span data-ttu-id="d172c-125">Anlatılan</span><span class="sxs-lookup"><span data-stu-id="d172c-125">Procedure</span></span>
- <span data-ttu-id="d172c-126">Gizlili</span><span class="sxs-lookup"><span data-stu-id="d172c-126">Secret</span></span>
- <span data-ttu-id="d172c-127">Sertifika</span><span class="sxs-lookup"><span data-stu-id="d172c-127">Credential</span></span>
- <span data-ttu-id="d172c-128">Tipte</span><span class="sxs-lookup"><span data-stu-id="d172c-128">Types</span></span>

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

### <span data-ttu-id="d172c-129">-Yol</span><span class="sxs-lookup"><span data-stu-id="d172c-129">-Path</span></span>
<span data-ttu-id="d172c-130">Getirilecek öğenin yolunu veya listedeki öğelerin üst öğesinin yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d172c-130">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d172c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d172c-131">-DefaultProfile</span></span>
<span data-ttu-id="d172c-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d172c-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d172c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d172c-133">CommonParameters</span></span>
<span data-ttu-id="d172c-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d172c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d172c-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d172c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d172c-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d172c-136">INPUTS</span></span>

## <span data-ttu-id="d172c-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d172c-137">OUTPUTS</span></span>

### <span data-ttu-id="d172c-138">bool</span><span class="sxs-lookup"><span data-stu-id="d172c-138">bool</span></span>
<span data-ttu-id="d172c-139">Belirtilen katalog öğesinin var olup olmadığını belirten doğru veya yanlış.</span><span class="sxs-lookup"><span data-stu-id="d172c-139">True or false indicating if the specified catalog item exists or not.</span></span>

## <span data-ttu-id="d172c-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d172c-140">NOTES</span></span>

## <span data-ttu-id="d172c-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d172c-141">RELATED LINKS</span></span>

[<span data-ttu-id="d172c-142">Get-Azurermdatalakeanalyzer Tic, Alogıtem</span><span class="sxs-lookup"><span data-stu-id="d172c-142">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Get-AzureRmDataLakeAnalyticsCatalogItem.md)


