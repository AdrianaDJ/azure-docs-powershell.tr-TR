---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 19b8b5a00e5bcb75b90a91097316dc065afa025b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761104"
---
# <span data-ttu-id="24c4a-101">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="24c4a-101">Add-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="24c4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="24c4a-103">Data Lake Analytics hesabına veri kaynağı ekler.</span><span class="sxs-lookup"><span data-stu-id="24c4a-103">Adds a data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="24c4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24c4a-104">SYNTAX</span></span>

### <span data-ttu-id="24c4a-105">AddDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="24c4a-105">AddDataLakeStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24c4a-106">AddBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="24c4a-106">AddBlobStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24c4a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="24c4a-107">DESCRIPTION</span></span>
<span data-ttu-id="24c4a-108">**Add-Azdatalakeanaliz Ticsdatasource** cmdlet 'ı bir Azure Data Lake Analytics hesabına veri kaynağı ekler.</span><span class="sxs-lookup"><span data-stu-id="24c4a-108">The **Add-AzDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="24c4a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24c4a-109">EXAMPLES</span></span>

### <span data-ttu-id="24c4a-110">Örnek 1: hesaba veri kaynağı ekleme</span><span class="sxs-lookup"><span data-stu-id="24c4a-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="24c4a-111">Bu komut, Data Lake Analytics hesabına bir Data Lake Store veri kaynağı ekler.</span><span class="sxs-lookup"><span data-stu-id="24c4a-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="24c4a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24c4a-112">PARAMETERS</span></span>

### <span data-ttu-id="24c4a-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="24c4a-113">-AccessKey</span></span>
<span data-ttu-id="24c4a-114">Eklenecek Azure Blob depolama hesabının erişim anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24c4a-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddBlobStorageAccount
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24c4a-115">-Hesap</span><span class="sxs-lookup"><span data-stu-id="24c4a-115">-Account</span></span>
<span data-ttu-id="24c4a-116">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24c4a-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="24c4a-117">-Blob</span><span class="sxs-lookup"><span data-stu-id="24c4a-117">-Blob</span></span>
<span data-ttu-id="24c4a-118">Eklenecek Azure Blob depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24c4a-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24c4a-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="24c4a-119">-DataLakeStore</span></span>
<span data-ttu-id="24c4a-120">Eklenecek Azure Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24c4a-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddDataLakeStorageAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24c4a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24c4a-121">-DefaultProfile</span></span>
<span data-ttu-id="24c4a-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="24c4a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24c4a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24c4a-123">-ResourceGroupName</span></span>
<span data-ttu-id="24c4a-124">Data Lake Analytics hesabının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24c4a-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24c4a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c4a-125">CommonParameters</span></span>
<span data-ttu-id="24c4a-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24c4a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c4a-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24c4a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c4a-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24c4a-128">INPUTS</span></span>

### <span data-ttu-id="24c4a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="24c4a-129">System.String</span></span>

## <span data-ttu-id="24c4a-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24c4a-130">OUTPUTS</span></span>

### <span data-ttu-id="24c4a-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="24c4a-131">System.Object</span></span>
## <span data-ttu-id="24c4a-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24c4a-132">NOTES</span></span>

## <span data-ttu-id="24c4a-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24c4a-133">RELATED LINKS</span></span>

[<span data-ttu-id="24c4a-134">Remove-Azdatalakeanaliz Ticsdatasource</span><span class="sxs-lookup"><span data-stu-id="24c4a-134">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="24c4a-135">Set-Azdatalakeanaliz Ticsdatasource</span><span class="sxs-lookup"><span data-stu-id="24c4a-135">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


