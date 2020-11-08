---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 2879923b38b6813213fe6819f84fa55a593f6930
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266620"
---
# <span data-ttu-id="a52d4-101">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="a52d4-101">Test-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="a52d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a52d4-102">SYNOPSIS</span></span>
<span data-ttu-id="a52d4-103">Katalog öğesinin varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="a52d4-103">Checks for the existence of a catalog item.</span></span>

## <span data-ttu-id="a52d4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a52d4-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a52d4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a52d4-105">DESCRIPTION</span></span>
<span data-ttu-id="a52d4-106">**Test-Azdatalakeanalizleri Ticdağırırgıtem** cmdlet 'i, bir Azure Data Lake Analytics Katalog öğesinin varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="a52d4-106">The **Test-AzDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="a52d4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a52d4-107">EXAMPLES</span></span>

### <span data-ttu-id="a52d4-108">Örnek 1: bir katalog öğesinin var olup olmadığını test edin</span><span class="sxs-lookup"><span data-stu-id="a52d4-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="a52d4-109">Bu komut belirtilen bir şema öğesinin bulunup bulunmadığını sınar.</span><span class="sxs-lookup"><span data-stu-id="a52d4-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="a52d4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a52d4-110">PARAMETERS</span></span>

### <span data-ttu-id="a52d4-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="a52d4-111">-Account</span></span>
<span data-ttu-id="a52d4-112">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a52d4-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="a52d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a52d4-113">-DefaultProfile</span></span>
<span data-ttu-id="a52d4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a52d4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a52d4-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="a52d4-115">-ItemType</span></span>
<span data-ttu-id="a52d4-116">Denetlenecek öğenin Katalog öğesi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a52d4-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="a52d4-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a52d4-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a52d4-118">Veritabanı</span><span class="sxs-lookup"><span data-stu-id="a52d4-118">Database</span></span>
- <span data-ttu-id="a52d4-119">Şemayla</span><span class="sxs-lookup"><span data-stu-id="a52d4-119">Schema</span></span>
- <span data-ttu-id="a52d4-120">Derlemeyle</span><span class="sxs-lookup"><span data-stu-id="a52d4-120">Assembly</span></span>
- <span data-ttu-id="a52d4-121">Tablo</span><span class="sxs-lookup"><span data-stu-id="a52d4-121">Table</span></span>
- <span data-ttu-id="a52d4-122">Tablobölümü</span><span class="sxs-lookup"><span data-stu-id="a52d4-122">TablePartition</span></span>
- <span data-ttu-id="a52d4-123">Tablodeğerdenişlevi</span><span class="sxs-lookup"><span data-stu-id="a52d4-123">TableValuedFunction</span></span>
- <span data-ttu-id="a52d4-124">Tabloistatistikleri</span><span class="sxs-lookup"><span data-stu-id="a52d4-124">TableStatistics</span></span>
- <span data-ttu-id="a52d4-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="a52d4-125">ExternalDataSource</span></span>
- <span data-ttu-id="a52d4-126">Görünümünde</span><span class="sxs-lookup"><span data-stu-id="a52d4-126">View</span></span>
- <span data-ttu-id="a52d4-127">Anlatılan</span><span class="sxs-lookup"><span data-stu-id="a52d4-127">Procedure</span></span>
- <span data-ttu-id="a52d4-128">Gizlili</span><span class="sxs-lookup"><span data-stu-id="a52d4-128">Secret</span></span>
- <span data-ttu-id="a52d4-129">Sertifika</span><span class="sxs-lookup"><span data-stu-id="a52d4-129">Credential</span></span>
- <span data-ttu-id="a52d4-130">Tipte</span><span class="sxs-lookup"><span data-stu-id="a52d4-130">Types</span></span>

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

### <span data-ttu-id="a52d4-131">-Yol</span><span class="sxs-lookup"><span data-stu-id="a52d4-131">-Path</span></span>
<span data-ttu-id="a52d4-132">Getirilecek öğenin yolunu veya listedeki öğelerin üst öğesinin yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a52d4-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

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

### <span data-ttu-id="a52d4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a52d4-133">CommonParameters</span></span>
<span data-ttu-id="a52d4-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a52d4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a52d4-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a52d4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a52d4-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a52d4-136">INPUTS</span></span>

### <span data-ttu-id="a52d4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a52d4-137">System.String</span></span>

### <span data-ttu-id="a52d4-138">Microsoft. Azure. Commands. DataLakeAnalytics. modeller. Datalakeanalizleri Ticsenums + Catalogıtemtype</span><span class="sxs-lookup"><span data-stu-id="a52d4-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="a52d4-139">Microsoft. Azure. Commands. DataLakeAnalytics. model. Catalogpathınstance</span><span class="sxs-lookup"><span data-stu-id="a52d4-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="a52d4-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a52d4-140">OUTPUTS</span></span>

### <span data-ttu-id="a52d4-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a52d4-141">System.Boolean</span></span>

## <span data-ttu-id="a52d4-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a52d4-142">NOTES</span></span>

## <span data-ttu-id="a52d4-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a52d4-143">RELATED LINKS</span></span>

[<span data-ttu-id="a52d4-144">Get-azdatalakeanalyzer ticdağır</span><span class="sxs-lookup"><span data-stu-id="a52d4-144">Get-AzDataLakeAnalyticsCatalogItem</span></span>](./Get-AzDataLakeAnalyticsCatalogItem.md)


