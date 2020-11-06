---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 7c35821cbaf75a616ab1b9b8bbc2db9fc2a96794
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594291"
---
# <span data-ttu-id="51cb4-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="51cb4-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="51cb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51cb4-102">SYNOPSIS</span></span>
<span data-ttu-id="51cb4-103">Veri Lake Analytics hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="51cb4-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51cb4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="51cb4-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tags] <Hashtable>] [-MaxDegreeOfParallelism <Int32>]
 [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51cb4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="51cb4-105">DESCRIPTION</span></span>
<span data-ttu-id="51cb4-106">**Yeni-Azurermdatalakeanalizizsaccount** cmdlet 'ı bir Azure Data Lake Analytics hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="51cb4-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="51cb4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="51cb4-107">EXAMPLES</span></span>

### <span data-ttu-id="51cb4-108">Örnek 1: veri Lake Analytics hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="51cb4-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="51cb4-109">Bu komut, ContosoOrg adlı kaynak grubunda ContosoAdlStore veri deposunu kullanan ContosoAdlAccount adlı bir Data Lake Analytics hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="51cb4-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="51cb4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="51cb4-110">PARAMETERS</span></span>

### <span data-ttu-id="51cb4-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="51cb4-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="51cb4-112">Varsayılan veri kaynağı olarak ayarlanacak Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51cb4-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51cb4-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="51cb4-113">-Location</span></span>
<span data-ttu-id="51cb4-114">Veri Lake Analytics hesabının oluşturulacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="51cb4-114">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="51cb4-115">Şu anda yalnızca Doğu ABD 2 destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="51cb4-115">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="51cb4-116">-Maxdegreeofparalellizm</span><span class="sxs-lookup"><span data-stu-id="51cb4-116">-MaxDegreeOfParallelism</span></span>
<span data-ttu-id="51cb4-117">Bu hesap için isteğe bağlı en yüksek paralellik değeri</span><span class="sxs-lookup"><span data-stu-id="51cb4-117">The optional maximum supported degree of parallelism for this account.</span></span> <span data-ttu-id="51cb4-118">Hiçbiri belirtilmezse, varsayılan değeri 30 olur</span><span class="sxs-lookup"><span data-stu-id="51cb4-118">If none is specified, defaults to 30</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51cb4-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="51cb4-119">-MaxJobCount</span></span>
<span data-ttu-id="51cb4-120">Aynı anda hesabın altında çalışan isteğe bağlı en yüksek işler.</span><span class="sxs-lookup"><span data-stu-id="51cb4-120">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="51cb4-121">Hiçbiri belirtilmezse, varsayılan 3 olur</span><span class="sxs-lookup"><span data-stu-id="51cb4-121">If none is specified, defaults to 3</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51cb4-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="51cb4-122">-Name</span></span>
<span data-ttu-id="51cb4-123">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51cb4-123">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51cb4-124">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="51cb4-124">-QueryStoreRetention</span></span>
<span data-ttu-id="51cb4-125">İş meta verilerinin tutulacağı isteğe bağlı gün sayısı.</span><span class="sxs-lookup"><span data-stu-id="51cb4-125">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="51cb4-126">Belirtilmezse, varsayılan 30 gündür.</span><span class="sxs-lookup"><span data-stu-id="51cb4-126">If none specified, the default is 30 days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51cb4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51cb4-127">-ResourceGroupName</span></span>
<span data-ttu-id="51cb4-128">Data Lake Analytics hesabının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51cb4-128">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="51cb4-129">Kaynak grubu oluşturmak için New-AzureRmResourceGroup cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="51cb4-129">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51cb4-130">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="51cb4-130">-Tags</span></span>
<span data-ttu-id="51cb4-131">Diğer Azure kaynakları arasında Data Lake Analytics hesabını tanıtmak için kullanılabilecek anahtar değeri çiftlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="51cb4-131">Specifies key-value pairs that can be used to identify the Data Lake Analytics account among other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51cb4-132">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="51cb4-132">-Tier</span></span>
<span data-ttu-id="51cb4-133">Bu hesabın kullanması için istenen taahhüt katmanı.</span><span class="sxs-lookup"><span data-stu-id="51cb4-133">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType]
Parameter Sets: (All)
Aliases: 
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51cb4-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51cb4-134">-DefaultProfile</span></span>
<span data-ttu-id="51cb4-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="51cb4-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51cb4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51cb4-136">CommonParameters</span></span>
<span data-ttu-id="51cb4-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="51cb4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51cb4-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51cb4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51cb4-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="51cb4-139">INPUTS</span></span>

## <span data-ttu-id="51cb4-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="51cb4-140">OUTPUTS</span></span>

### <span data-ttu-id="51cb4-141">Psdatalakeanalyzer Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="51cb4-141">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="51cb4-142">Yeni oluşturulan hesabın ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="51cb4-142">The details of the newly created account.</span></span>

## <span data-ttu-id="51cb4-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="51cb4-143">NOTES</span></span>

## <span data-ttu-id="51cb4-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="51cb4-144">RELATED LINKS</span></span>

[<span data-ttu-id="51cb4-145">Get-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="51cb4-145">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="51cb4-146">Remove-Azurermdatalakeanalyzer Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="51cb4-146">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="51cb4-147">Set-Azurermdatalakeanalyzer Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="51cb4-147">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="51cb4-148">Test-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="51cb4-148">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


