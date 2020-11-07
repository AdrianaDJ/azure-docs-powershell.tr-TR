---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 29f9315063db7d6bb16f8656950da39e70ddced9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916984"
---
# <span data-ttu-id="33ad8-101">Get-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="33ad8-101">Get-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="33ad8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33ad8-102">SYNOPSIS</span></span>
<span data-ttu-id="33ad8-103">Data Lake Analytics veri kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="33ad8-103">Gets a Data Lake Analytics data source.</span></span>

## <span data-ttu-id="33ad8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="33ad8-104">SYNTAX</span></span>

### <span data-ttu-id="33ad8-105">GetAllDataSources (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="33ad8-105">GetAllDataSources (Default)</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33ad8-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="33ad8-106">GetDataLakeStoreAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33ad8-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="33ad8-107">GetBlobStorageAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33ad8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="33ad8-108">DESCRIPTION</span></span>
<span data-ttu-id="33ad8-109">**Get-Azdatalakeanaliz Ticsdatasource** cmdlet 'i, bir Azure Data Lake Analytics veri kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="33ad8-109">The **Get-AzDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="33ad8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="33ad8-110">EXAMPLES</span></span>

### <span data-ttu-id="33ad8-111">Örnek 1: hesaptan veri kaynağı alma</span><span class="sxs-lookup"><span data-stu-id="33ad8-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="33ad8-112">Bu komut, Data Lake Analytics hesabından ContosoAdls adlı bir Data Lake Store veri kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="33ad8-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="33ad8-113">Örnek 2: veri Lake Analytics hesabındaki veri Lake Store hesaplarının listesini alma</span><span class="sxs-lookup"><span data-stu-id="33ad8-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="33ad8-114">Bu komut, veri Lake Analytics hesabındaki tüm Data Lake Store hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="33ad8-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="33ad8-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="33ad8-115">PARAMETERS</span></span>

### <span data-ttu-id="33ad8-116">-Hesap</span><span class="sxs-lookup"><span data-stu-id="33ad8-116">-Account</span></span>
<span data-ttu-id="33ad8-117">Bu cmdlet 'in veri kaynaklarını aldığı Data Lake Analytics hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="33ad8-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="33ad8-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="33ad8-118">-Blob</span></span>
<span data-ttu-id="33ad8-119">Azure Blob depolama veri kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="33ad8-119">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="33ad8-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="33ad8-120">-DataLakeStore</span></span>
<span data-ttu-id="33ad8-121">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="33ad8-121">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="33ad8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33ad8-122">-DefaultProfile</span></span>
<span data-ttu-id="33ad8-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="33ad8-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33ad8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33ad8-124">-ResourceGroupName</span></span>
<span data-ttu-id="33ad8-125">Veri kaynağını içeren kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="33ad8-125">Specifies the resource group name that contains the data source.</span></span>

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

### <span data-ttu-id="33ad8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33ad8-126">CommonParameters</span></span>
<span data-ttu-id="33ad8-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="33ad8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33ad8-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33ad8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33ad8-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="33ad8-129">INPUTS</span></span>

### <span data-ttu-id="33ad8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="33ad8-130">System.String</span></span>

## <span data-ttu-id="33ad8-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="33ad8-131">OUTPUTS</span></span>

### <span data-ttu-id="33ad8-132">Microsoft. Azure. Commands. DataLakeAnalytics. model. Psstorageaccountınfo</span><span class="sxs-lookup"><span data-stu-id="33ad8-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span></span>

### <span data-ttu-id="33ad8-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="33ad8-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span></span>

### <span data-ttu-id="33ad8-134">Microsoft. Azure. Commands. DataLakeAnalytics. model. AdlDataSource</span><span class="sxs-lookup"><span data-stu-id="33ad8-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span></span>

## <span data-ttu-id="33ad8-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="33ad8-135">NOTES</span></span>

## <span data-ttu-id="33ad8-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="33ad8-136">RELATED LINKS</span></span>

[<span data-ttu-id="33ad8-137">Add-Azdatalakeçözümlerken</span><span class="sxs-lookup"><span data-stu-id="33ad8-137">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="33ad8-138">Remove-Azdatalakeanaliz Ticsdatasource</span><span class="sxs-lookup"><span data-stu-id="33ad8-138">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="33ad8-139">Set-Azdatalakeanaliz Ticsdatasource</span><span class="sxs-lookup"><span data-stu-id="33ad8-139">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


