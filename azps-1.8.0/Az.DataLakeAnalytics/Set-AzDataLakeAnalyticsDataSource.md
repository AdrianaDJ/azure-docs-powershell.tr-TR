---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 8fece6d480ee2210ff66256e02baaf6a11f9c1f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916951"
---
# <span data-ttu-id="958ac-101">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="958ac-101">Set-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="958ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="958ac-102">SYNOPSIS</span></span>
<span data-ttu-id="958ac-103">Veri Lake Analytics hesabının veri kaynağının ayrıntılarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="958ac-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="958ac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="958ac-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="958ac-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="958ac-105">DESCRIPTION</span></span>
<span data-ttu-id="958ac-106">**Set-Azdatalakeanaliz Ticsdatasource** cmdlet 'i, bir Azure Data Lake Analytics hesabının veri kaynağının ayrıntılarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="958ac-106">The **Set-AzDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="958ac-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="958ac-107">EXAMPLES</span></span>

### <span data-ttu-id="958ac-108">Örnek 1: veri kaynağının erişim anahtarını değiştirme</span><span class="sxs-lookup"><span data-stu-id="958ac-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="958ac-109">Bu komut, Azure Blob depolama veri kaynağı için depolanan erişim tuşunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="958ac-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="958ac-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="958ac-110">PARAMETERS</span></span>

### <span data-ttu-id="958ac-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="958ac-111">-AccessKey</span></span>
<span data-ttu-id="958ac-112">Azure Blob depolama veri kaynağının yeni erişim anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="958ac-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="958ac-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="958ac-113">-Account</span></span>
<span data-ttu-id="958ac-114">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="958ac-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="958ac-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="958ac-115">-Blob</span></span>
<span data-ttu-id="958ac-116">Azure Blob depolama veri kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="958ac-116">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="958ac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="958ac-117">-DefaultProfile</span></span>
<span data-ttu-id="958ac-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="958ac-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="958ac-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="958ac-119">-ResourceGroupName</span></span>
<span data-ttu-id="958ac-120">Data Lake Analytics hesabının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="958ac-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="958ac-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="958ac-121">CommonParameters</span></span>
<span data-ttu-id="958ac-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="958ac-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="958ac-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="958ac-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="958ac-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="958ac-124">INPUTS</span></span>

### <span data-ttu-id="958ac-125">System. String</span><span class="sxs-lookup"><span data-stu-id="958ac-125">System.String</span></span>

## <span data-ttu-id="958ac-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="958ac-126">OUTPUTS</span></span>

### <span data-ttu-id="958ac-127">System. void</span><span class="sxs-lookup"><span data-stu-id="958ac-127">System.Void</span></span>

## <span data-ttu-id="958ac-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="958ac-128">NOTES</span></span>

## <span data-ttu-id="958ac-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="958ac-129">RELATED LINKS</span></span>

[<span data-ttu-id="958ac-130">Add-Azdatalakeçözümlerken</span><span class="sxs-lookup"><span data-stu-id="958ac-130">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="958ac-131">Remove-Azdatalakeanaliz Ticsdatasource</span><span class="sxs-lookup"><span data-stu-id="958ac-131">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)


