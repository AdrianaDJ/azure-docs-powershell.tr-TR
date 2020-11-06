---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 8aae62ccbf79f2b3c59f6009aa5233daf00853fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592000"
---
# <span data-ttu-id="15fe2-101">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="15fe2-101">Set-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="15fe2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15fe2-102">SYNOPSIS</span></span>
<span data-ttu-id="15fe2-103">Veri Lake Analytics hesabının veri kaynağının ayrıntılarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="15fe2-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15fe2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15fe2-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15fe2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="15fe2-105">DESCRIPTION</span></span>
<span data-ttu-id="15fe2-106">**Set-Azurermdatalakeanalizleri** , Azure Data Lake Analytics hesabının veri kaynağının ayrıntılarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="15fe2-106">The **Set-AzureRmDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="15fe2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15fe2-107">EXAMPLES</span></span>

### <span data-ttu-id="15fe2-108">Örnek 1: veri kaynağının erişim anahtarını değiştirme</span><span class="sxs-lookup"><span data-stu-id="15fe2-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="15fe2-109">Bu komut, Azure Blob depolama veri kaynağı için depolanan erişim tuşunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="15fe2-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="15fe2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15fe2-110">PARAMETERS</span></span>

### <span data-ttu-id="15fe2-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="15fe2-111">-AccessKey</span></span>
<span data-ttu-id="15fe2-112">Azure Blob depolama veri kaynağının yeni erişim anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15fe2-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fe2-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="15fe2-113">-Account</span></span>
<span data-ttu-id="15fe2-114">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15fe2-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="15fe2-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="15fe2-115">-Blob</span></span>
<span data-ttu-id="15fe2-116">Azure Blob depolama veri kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15fe2-116">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fe2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15fe2-117">-DefaultProfile</span></span>
<span data-ttu-id="15fe2-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="15fe2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15fe2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15fe2-119">-ResourceGroupName</span></span>
<span data-ttu-id="15fe2-120">Data Lake Analytics hesabının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15fe2-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="15fe2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15fe2-121">CommonParameters</span></span>
<span data-ttu-id="15fe2-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15fe2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15fe2-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15fe2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15fe2-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15fe2-124">INPUTS</span></span>

### <span data-ttu-id="15fe2-125">System. String</span><span class="sxs-lookup"><span data-stu-id="15fe2-125">System.String</span></span>

## <span data-ttu-id="15fe2-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15fe2-126">OUTPUTS</span></span>

### <span data-ttu-id="15fe2-127">System. void</span><span class="sxs-lookup"><span data-stu-id="15fe2-127">System.Void</span></span>

## <span data-ttu-id="15fe2-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15fe2-128">NOTES</span></span>

## <span data-ttu-id="15fe2-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15fe2-129">RELATED LINKS</span></span>

[<span data-ttu-id="15fe2-130">Add-Azurermdatalakeanalyzer Ticsdatasource</span><span class="sxs-lookup"><span data-stu-id="15fe2-130">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="15fe2-131">Remove-Azurermdatalakeanalyzer Ticsdatasource</span><span class="sxs-lookup"><span data-stu-id="15fe2-131">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)


