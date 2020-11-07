---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 2f6dfae3d13a6de57a7dc04367ec2886be78f5f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593273"
---
# <span data-ttu-id="951aa-101">Get-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="951aa-101">Get-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="951aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="951aa-102">SYNOPSIS</span></span>
<span data-ttu-id="951aa-103">Data Lake Analytics veri kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="951aa-103">Gets a Data Lake Analytics data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="951aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="951aa-104">SYNTAX</span></span>

### <span data-ttu-id="951aa-105">GetAllDataSources (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="951aa-105">GetAllDataSources (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="951aa-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="951aa-106">GetDataLakeStoreAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="951aa-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="951aa-107">GetBlobStorageAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="951aa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="951aa-108">DESCRIPTION</span></span>
<span data-ttu-id="951aa-109">**Get-Azurermdatalakeanalizleri** , bir Azure Data Lake Analytics veri kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="951aa-109">The **Get-AzureRmDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="951aa-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="951aa-110">EXAMPLES</span></span>

### <span data-ttu-id="951aa-111">Örnek 1: hesaptan veri kaynağı alma</span><span class="sxs-lookup"><span data-stu-id="951aa-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="951aa-112">Bu komut, Data Lake Analytics hesabından ContosoAdls adlı bir Data Lake Store veri kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="951aa-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="951aa-113">Örnek 2: veri Lake Analytics hesabındaki veri Lake Store hesaplarının listesini alma</span><span class="sxs-lookup"><span data-stu-id="951aa-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="951aa-114">Bu komut, veri Lake Analytics hesabındaki tüm Data Lake Store hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="951aa-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="951aa-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="951aa-115">PARAMETERS</span></span>

### <span data-ttu-id="951aa-116">-Hesap</span><span class="sxs-lookup"><span data-stu-id="951aa-116">-Account</span></span>
<span data-ttu-id="951aa-117">Bu cmdlet 'in veri kaynaklarını aldığı Data Lake Analytics hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="951aa-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="951aa-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="951aa-118">-Blob</span></span>
<span data-ttu-id="951aa-119">Azure Blob depolama veri kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="951aa-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="951aa-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="951aa-120">-DataLakeStore</span></span>
<span data-ttu-id="951aa-121">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="951aa-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDataLakeStoreAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="951aa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="951aa-122">-DefaultProfile</span></span>
<span data-ttu-id="951aa-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="951aa-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="951aa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="951aa-124">-ResourceGroupName</span></span>
<span data-ttu-id="951aa-125">Veri kaynağını içeren kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="951aa-125">Specifies the resource group name that contains the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="951aa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="951aa-126">CommonParameters</span></span>
<span data-ttu-id="951aa-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="951aa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="951aa-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="951aa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="951aa-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="951aa-129">INPUTS</span></span>

### <span data-ttu-id="951aa-130">System. String</span><span class="sxs-lookup"><span data-stu-id="951aa-130">System.String</span></span>

## <span data-ttu-id="951aa-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="951aa-131">OUTPUTS</span></span>

### <span data-ttu-id="951aa-132">Microsoft. Azure. Commands. DataLakeAnalytics. model. Psstorageaccountınfo</span><span class="sxs-lookup"><span data-stu-id="951aa-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span></span>

### <span data-ttu-id="951aa-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="951aa-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span></span>

### <span data-ttu-id="951aa-134">Microsoft. Azure. Commands. DataLakeAnalytics. model. AdlDataSource</span><span class="sxs-lookup"><span data-stu-id="951aa-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span></span>

## <span data-ttu-id="951aa-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="951aa-135">NOTES</span></span>

## <span data-ttu-id="951aa-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="951aa-136">RELATED LINKS</span></span>

[<span data-ttu-id="951aa-137">Add-Azurermdatalakeanalyzer Ticsdatasource</span><span class="sxs-lookup"><span data-stu-id="951aa-137">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="951aa-138">Remove-Azurermdatalakeanalyzer Ticsdatasource</span><span class="sxs-lookup"><span data-stu-id="951aa-138">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="951aa-139">Set-Azurermdatalakeanalyzer Ticsdatasource</span><span class="sxs-lookup"><span data-stu-id="951aa-139">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)

