---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 258db8a7dc1d771b73ea4c4fa373b1861847b820
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763768"
---
# <span data-ttu-id="c8433-101">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="c8433-101">Set-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="c8433-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8433-102">SYNOPSIS</span></span>
<span data-ttu-id="c8433-103">Veri Lake Analytics hesabının veri kaynağının ayrıntılarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c8433-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8433-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c8433-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8433-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c8433-105">DESCRIPTION</span></span>
<span data-ttu-id="c8433-106">**Set-Azurermdatalakeanalizleri** , Azure Data Lake Analytics hesabının veri kaynağının ayrıntılarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c8433-106">The **Set-AzureRmDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="c8433-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c8433-107">EXAMPLES</span></span>

### <span data-ttu-id="c8433-108">Örnek 1: veri kaynağının erişim anahtarını değiştirme</span><span class="sxs-lookup"><span data-stu-id="c8433-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="c8433-109">Bu komut, Azure Blob depolama veri kaynağı için depolanan erişim tuşunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c8433-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="c8433-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c8433-110">PARAMETERS</span></span>

### <span data-ttu-id="c8433-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="c8433-111">-AccessKey</span></span>
<span data-ttu-id="c8433-112">Azure Blob depolama veri kaynağının yeni erişim anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8433-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="c8433-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="c8433-113">-Account</span></span>
<span data-ttu-id="c8433-114">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8433-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="c8433-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="c8433-115">-Blob</span></span>
<span data-ttu-id="c8433-116">Azure Blob depolama veri kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8433-116">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="c8433-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8433-117">-ResourceGroupName</span></span>
<span data-ttu-id="c8433-118">Data Lake Analytics hesabının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8433-118">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="c8433-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8433-119">-DefaultProfile</span></span>
<span data-ttu-id="c8433-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c8433-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8433-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8433-121">CommonParameters</span></span>
<span data-ttu-id="c8433-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c8433-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8433-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8433-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8433-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c8433-124">INPUTS</span></span>

## <span data-ttu-id="c8433-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c8433-125">OUTPUTS</span></span>

### <span data-ttu-id="c8433-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c8433-126">None</span></span>

## <span data-ttu-id="c8433-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c8433-127">NOTES</span></span>

## <span data-ttu-id="c8433-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c8433-128">RELATED LINKS</span></span>

[<span data-ttu-id="c8433-129">Add-Azurermdatalakeanalyzer Ticsdatasource</span><span class="sxs-lookup"><span data-stu-id="c8433-129">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="c8433-130">Remove-Azurermdatalakeanalyzer Ticsdatasource</span><span class="sxs-lookup"><span data-stu-id="c8433-130">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)


