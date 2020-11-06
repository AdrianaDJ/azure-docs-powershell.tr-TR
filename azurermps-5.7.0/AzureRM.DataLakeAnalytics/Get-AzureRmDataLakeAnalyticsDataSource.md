---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 93e64c4a64eecbe66fc3f9b2923ade65405a05a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586718"
---
# <span data-ttu-id="a99ae-101">Get-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="a99ae-101">Get-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="a99ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a99ae-102">SYNOPSIS</span></span>
<span data-ttu-id="a99ae-103">Data Lake Analytics veri kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="a99ae-103">Gets a Data Lake Analytics data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a99ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a99ae-104">SYNTAX</span></span>

### <span data-ttu-id="a99ae-105">GetAllDataSources (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a99ae-105">GetAllDataSources (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a99ae-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a99ae-106">GetDataLakeStoreAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a99ae-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a99ae-107">GetBlobStorageAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a99ae-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a99ae-108">DESCRIPTION</span></span>
<span data-ttu-id="a99ae-109">**Get-Azurermdatalakeanalizleri** , bir Azure Data Lake Analytics veri kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="a99ae-109">The **Get-AzureRmDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="a99ae-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a99ae-110">EXAMPLES</span></span>

### <span data-ttu-id="a99ae-111">Örnek 1: hesaptan veri kaynağı alma</span><span class="sxs-lookup"><span data-stu-id="a99ae-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="a99ae-112">Bu komut, Data Lake Analytics hesabından ContosoAdls adlı bir Data Lake Store veri kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="a99ae-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="a99ae-113">Örnek 2: veri Lake Analytics hesabındaki veri Lake Store hesaplarının listesini alma</span><span class="sxs-lookup"><span data-stu-id="a99ae-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="a99ae-114">Bu komut, veri Lake Analytics hesabındaki tüm Data Lake Store hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="a99ae-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="a99ae-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a99ae-115">PARAMETERS</span></span>

### <span data-ttu-id="a99ae-116">-Hesap</span><span class="sxs-lookup"><span data-stu-id="a99ae-116">-Account</span></span>
<span data-ttu-id="a99ae-117">Bu cmdlet 'in veri kaynaklarını aldığı Data Lake Analytics hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a99ae-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="a99ae-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="a99ae-118">-Blob</span></span>
<span data-ttu-id="a99ae-119">Azure Blob depolama veri kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a99ae-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: String
Parameter Sets: GetBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a99ae-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a99ae-120">-DataLakeStore</span></span>
<span data-ttu-id="a99ae-121">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a99ae-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: GetDataLakeStoreAccount
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a99ae-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a99ae-122">-DefaultProfile</span></span>
<span data-ttu-id="a99ae-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a99ae-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a99ae-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a99ae-124">-ResourceGroupName</span></span>
<span data-ttu-id="a99ae-125">Veri kaynağını içeren kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a99ae-125">Specifies the resource group name that contains the data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a99ae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a99ae-126">CommonParameters</span></span>
<span data-ttu-id="a99ae-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a99ae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a99ae-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a99ae-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a99ae-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a99ae-129">INPUTS</span></span>

### <span data-ttu-id="a99ae-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a99ae-130">None</span></span>
<span data-ttu-id="a99ae-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="a99ae-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a99ae-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a99ae-132">OUTPUTS</span></span>

### <span data-ttu-id="a99ae-133">Psstorageaccountınfo</span><span class="sxs-lookup"><span data-stu-id="a99ae-133">PSStorageAccountInfo</span></span>
<span data-ttu-id="a99ae-134">Belirtilen Azure depolama hesabı ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="a99ae-134">The specified Azure Storage account details.</span></span>

### <span data-ttu-id="a99ae-135">PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="a99ae-135">PSDataLakeStoreAccountInfo</span></span>
<span data-ttu-id="a99ae-136">Belirtilen Data Lake Store hesap ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="a99ae-136">The specified Data Lake Store account details</span></span>

### <span data-ttu-id="a99ae-137">Listeniz<AdlDataSource></span><span class="sxs-lookup"><span data-stu-id="a99ae-137">List<AdlDataSource></span></span>
<span data-ttu-id="a99ae-138">Belirtilen veri Lake Analytics hesabındaki Azure depolama hesaplarının ve veri Lake Store hesaplarının listesi.</span><span class="sxs-lookup"><span data-stu-id="a99ae-138">The list of both Azure Storage accounts and Data Lake Store accounts in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="a99ae-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a99ae-139">NOTES</span></span>

## <span data-ttu-id="a99ae-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a99ae-140">RELATED LINKS</span></span>

[<span data-ttu-id="a99ae-141">Add-Azurermdatalakeanalyzer Ticsdatasource</span><span class="sxs-lookup"><span data-stu-id="a99ae-141">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="a99ae-142">Remove-Azurermdatalakeanalyzer Ticsdatasource</span><span class="sxs-lookup"><span data-stu-id="a99ae-142">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="a99ae-143">Set-Azurermdatalakeanalyzer Ticsdatasource</span><span class="sxs-lookup"><span data-stu-id="a99ae-143">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


