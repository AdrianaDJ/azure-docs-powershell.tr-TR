---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/add-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 1f2fe13567bd17170fd73854ce5554a693210c7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588957"
---
# <span data-ttu-id="3289f-101">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="3289f-101">Add-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="3289f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3289f-102">SYNOPSIS</span></span>
<span data-ttu-id="3289f-103">Data Lake Analytics hesabına veri kaynağı ekler.</span><span class="sxs-lookup"><span data-stu-id="3289f-103">Adds a data source to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3289f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3289f-104">SYNTAX</span></span>

### <span data-ttu-id="3289f-105">AddDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3289f-105">AddDataLakeStorageAccount</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3289f-106">AddBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3289f-106">AddBlobStorageAccount</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3289f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3289f-107">DESCRIPTION</span></span>
<span data-ttu-id="3289f-108">**Add-Azurermdatalakeanalizleri** , bir Azure Data Lake Analytics hesabına veri kaynağı ekler.</span><span class="sxs-lookup"><span data-stu-id="3289f-108">The **Add-AzureRmDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="3289f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3289f-109">EXAMPLES</span></span>

### <span data-ttu-id="3289f-110">Örnek 1: hesaba veri kaynağı ekleme</span><span class="sxs-lookup"><span data-stu-id="3289f-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="3289f-111">Bu komut, Data Lake Analytics hesabına bir Data Lake Store veri kaynağı ekler.</span><span class="sxs-lookup"><span data-stu-id="3289f-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="3289f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3289f-112">PARAMETERS</span></span>

### <span data-ttu-id="3289f-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="3289f-113">-AccessKey</span></span>
<span data-ttu-id="3289f-114">Eklenecek Azure Blob depolama hesabının erişim anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3289f-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

```yaml
Type: String
Parameter Sets: AddBlobStorageAccount
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3289f-115">-Hesap</span><span class="sxs-lookup"><span data-stu-id="3289f-115">-Account</span></span>
<span data-ttu-id="3289f-116">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3289f-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="3289f-117">-Blob</span><span class="sxs-lookup"><span data-stu-id="3289f-117">-Blob</span></span>
<span data-ttu-id="3289f-118">Eklenecek Azure Blob depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3289f-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

```yaml
Type: String
Parameter Sets: AddBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3289f-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3289f-119">-DataLakeStore</span></span>
<span data-ttu-id="3289f-120">Eklenecek Azure Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3289f-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

```yaml
Type: String
Parameter Sets: AddDataLakeStorageAccount
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3289f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3289f-121">-DefaultProfile</span></span>
<span data-ttu-id="3289f-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3289f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3289f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3289f-123">-ResourceGroupName</span></span>
<span data-ttu-id="3289f-124">Data Lake Analytics hesabının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3289f-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3289f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3289f-125">CommonParameters</span></span>
<span data-ttu-id="3289f-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3289f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3289f-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3289f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3289f-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3289f-128">INPUTS</span></span>

### <span data-ttu-id="3289f-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3289f-129">None</span></span>
<span data-ttu-id="3289f-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="3289f-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3289f-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3289f-131">OUTPUTS</span></span>

### <span data-ttu-id="3289f-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3289f-132">None</span></span>

## <span data-ttu-id="3289f-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3289f-133">NOTES</span></span>

## <span data-ttu-id="3289f-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3289f-134">RELATED LINKS</span></span>

[<span data-ttu-id="3289f-135">Remove-Azurermdatalakeanalyzer Ticsdatasource</span><span class="sxs-lookup"><span data-stu-id="3289f-135">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="3289f-136">Set-Azurermdatalakeanalyzer Ticsdatasource</span><span class="sxs-lookup"><span data-stu-id="3289f-136">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


