---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: b7f2c6f2077d0b7e9c7510f6984ada15a65d6ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764866"
---
# <span data-ttu-id="792ef-101">Get-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="792ef-101">Get-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="792ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="792ef-102">SYNOPSIS</span></span>
<span data-ttu-id="792ef-103">Data Lake Analytics veri kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="792ef-103">Gets a Data Lake Analytics data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="792ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="792ef-104">SYNTAX</span></span>

### <span data-ttu-id="792ef-105">Tüm veri kaynaklarını Listele (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="792ef-105">List all data sources (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="792ef-106">Data Lake Store hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="792ef-106">Get a Data Lake Store account</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="792ef-107">BLOB depolama hesabı alma</span><span class="sxs-lookup"><span data-stu-id="792ef-107">Get a Blob storage account</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="792ef-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="792ef-108">DESCRIPTION</span></span>
<span data-ttu-id="792ef-109">**Get-Azurermdatalakeanalizleri** , bir Azure Data Lake Analytics veri kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="792ef-109">The **Get-AzureRmDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="792ef-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="792ef-110">EXAMPLES</span></span>

### <span data-ttu-id="792ef-111">Örnek 1: hesaptan veri kaynağı alma</span><span class="sxs-lookup"><span data-stu-id="792ef-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="792ef-112">Bu komut, Data Lake Analytics hesabından ContosoAdls adlı bir Data Lake Store veri kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="792ef-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="792ef-113">Örnek 2: veri Lake Analytics hesabındaki veri Lake Store hesaplarının listesini alma</span><span class="sxs-lookup"><span data-stu-id="792ef-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="792ef-114">Bu komut, veri Lake Analytics hesabındaki tüm Data Lake Store hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="792ef-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="792ef-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="792ef-115">PARAMETERS</span></span>

### <span data-ttu-id="792ef-116">-Hesap</span><span class="sxs-lookup"><span data-stu-id="792ef-116">-Account</span></span>
<span data-ttu-id="792ef-117">Bu cmdlet 'in veri kaynaklarını aldığı Data Lake Analytics hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="792ef-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="792ef-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="792ef-118">-Blob</span></span>
<span data-ttu-id="792ef-119">Azure Blob depolama veri kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="792ef-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a Blob storage account
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="792ef-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="792ef-120">-DataLakeStore</span></span>
<span data-ttu-id="792ef-121">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="792ef-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a Data Lake Store account
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="792ef-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="792ef-122">-ResourceGroupName</span></span>
<span data-ttu-id="792ef-123">Veri kaynağını içeren kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="792ef-123">Specifies the resource group name that contains the data source.</span></span>

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

### <span data-ttu-id="792ef-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="792ef-124">-DefaultProfile</span></span>
<span data-ttu-id="792ef-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="792ef-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="792ef-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="792ef-126">CommonParameters</span></span>
<span data-ttu-id="792ef-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="792ef-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="792ef-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="792ef-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="792ef-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="792ef-129">INPUTS</span></span>

## <span data-ttu-id="792ef-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="792ef-130">OUTPUTS</span></span>

### <span data-ttu-id="792ef-131">Psstorageaccountınfo</span><span class="sxs-lookup"><span data-stu-id="792ef-131">PSStorageAccountInfo</span></span>
<span data-ttu-id="792ef-132">Belirtilen Azure depolama hesabı ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="792ef-132">The specified Azure Storage account details.</span></span>

### <span data-ttu-id="792ef-133">PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="792ef-133">PSDataLakeStoreAccountInfo</span></span>
<span data-ttu-id="792ef-134">Belirtilen Data Lake Store hesap ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="792ef-134">The specified Data Lake Store account details</span></span>

### <span data-ttu-id="792ef-135">Listeniz<AdlDataSource></span><span class="sxs-lookup"><span data-stu-id="792ef-135">List<AdlDataSource></span></span>
<span data-ttu-id="792ef-136">Belirtilen veri Lake Analytics hesabındaki Azure depolama hesaplarının ve veri Lake Store hesaplarının listesi.</span><span class="sxs-lookup"><span data-stu-id="792ef-136">The list of both Azure Storage accounts and Data Lake Store accounts in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="792ef-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="792ef-137">NOTES</span></span>

## <span data-ttu-id="792ef-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="792ef-138">RELATED LINKS</span></span>

[<span data-ttu-id="792ef-139">Add-Azurermdatalakeanalyzer Ticsdatasource</span><span class="sxs-lookup"><span data-stu-id="792ef-139">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="792ef-140">Remove-Azurermdatalakeanalyzer Ticsdatasource</span><span class="sxs-lookup"><span data-stu-id="792ef-140">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="792ef-141">Set-Azurermdatalakeanalyzer Ticsdatasource</span><span class="sxs-lookup"><span data-stu-id="792ef-141">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


