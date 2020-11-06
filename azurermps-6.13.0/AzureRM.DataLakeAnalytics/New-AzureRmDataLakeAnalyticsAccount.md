---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 2fec19864e9d13e4b0e4ede1d351a08427e95357
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593266"
---
# <span data-ttu-id="ea0ac-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ea0ac-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="ea0ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea0ac-102">SYNOPSIS</span></span>
<span data-ttu-id="ea0ac-103">Veri Lake Analytics hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea0ac-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea0ac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea0ac-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea0ac-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea0ac-105">DESCRIPTION</span></span>
<span data-ttu-id="ea0ac-106">**Yeni-Azurermdatalakeanalizizsaccount** cmdlet 'ı bir Azure Data Lake Analytics hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea0ac-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="ea0ac-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea0ac-107">EXAMPLES</span></span>

### <span data-ttu-id="ea0ac-108">Örnek 1: veri Lake Analytics hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ea0ac-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="ea0ac-109">Bu komut, ContosoOrg adlı kaynak grubunda ContosoAdlStore veri deposunu kullanan ContosoAdlAccount adlı bir Data Lake Analytics hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea0ac-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="ea0ac-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea0ac-110">PARAMETERS</span></span>

### <span data-ttu-id="ea0ac-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ea0ac-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="ea0ac-112">Varsayılan veri kaynağı olarak ayarlanacak Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea0ac-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

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

### <span data-ttu-id="ea0ac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea0ac-113">-DefaultProfile</span></span>
<span data-ttu-id="ea0ac-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ea0ac-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea0ac-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="ea0ac-115">-Location</span></span>
<span data-ttu-id="ea0ac-116">Veri Lake Analytics hesabının oluşturulacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea0ac-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="ea0ac-117">Şu anda yalnızca Doğu ABD 2 destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="ea0ac-117">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="ea0ac-118">-Maxçözümlerken</span><span class="sxs-lookup"><span data-stu-id="ea0ac-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="ea0ac-119">Bu hesap için isteğe bağlı en yüksek çözümleme birimleri.</span><span class="sxs-lookup"><span data-stu-id="ea0ac-119">The optional maximum supported analytics units for this account.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0ac-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="ea0ac-120">-MaxJobCount</span></span>
<span data-ttu-id="ea0ac-121">Aynı anda hesabın altında çalışan isteğe bağlı en yüksek işler.</span><span class="sxs-lookup"><span data-stu-id="ea0ac-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="ea0ac-122">Hiçbiri belirtilmezse, varsayılan 3 olur</span><span class="sxs-lookup"><span data-stu-id="ea0ac-122">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="ea0ac-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="ea0ac-123">-Name</span></span>
<span data-ttu-id="ea0ac-124">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea0ac-124">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="ea0ac-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="ea0ac-125">-QueryStoreRetention</span></span>
<span data-ttu-id="ea0ac-126">İş meta verilerinin tutulacağı isteğe bağlı gün sayısı.</span><span class="sxs-lookup"><span data-stu-id="ea0ac-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="ea0ac-127">Belirtilmezse, varsayılan 30 gündür.</span><span class="sxs-lookup"><span data-stu-id="ea0ac-127">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="ea0ac-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea0ac-128">-ResourceGroupName</span></span>
<span data-ttu-id="ea0ac-129">Data Lake Analytics hesabının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea0ac-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="ea0ac-130">Kaynak grubu oluşturmak için New-AzureRmResourceGroup cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ea0ac-130">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="ea0ac-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ea0ac-131">-Tag</span></span>
<span data-ttu-id="ea0ac-132">Bu hesapla ilişkilendirilmiş etiketlerin dize sözlüğü</span><span class="sxs-lookup"><span data-stu-id="ea0ac-132">A string,string dictionary of tags associated with this account</span></span>

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

### <span data-ttu-id="ea0ac-133">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="ea0ac-133">-Tier</span></span>
<span data-ttu-id="ea0ac-134">Bu hesabın kullanması için istenen taahhüt katmanı.</span><span class="sxs-lookup"><span data-stu-id="ea0ac-134">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="ea0ac-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea0ac-135">CommonParameters</span></span>
<span data-ttu-id="ea0ac-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea0ac-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea0ac-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea0ac-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea0ac-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea0ac-138">INPUTS</span></span>

### <span data-ttu-id="ea0ac-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ea0ac-139">System.String</span></span>

### <span data-ttu-id="ea0ac-140">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ea0ac-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ea0ac-141">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ea0ac-141">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="ea0ac-142">System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Analytics. modeller. TierType, Microsoft. Azure. Management. DataLake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ea0ac-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="ea0ac-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea0ac-143">OUTPUTS</span></span>

### <span data-ttu-id="ea0ac-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDAtalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="ea0ac-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="ea0ac-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea0ac-145">NOTES</span></span>

## <span data-ttu-id="ea0ac-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea0ac-146">RELATED LINKS</span></span>

[<span data-ttu-id="ea0ac-147">Get-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="ea0ac-147">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ea0ac-148">Remove-Azurermdatalakeanalyzer Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="ea0ac-148">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ea0ac-149">Set-Azurermdatalakeanalyzer Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="ea0ac-149">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ea0ac-150">Test-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="ea0ac-150">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


