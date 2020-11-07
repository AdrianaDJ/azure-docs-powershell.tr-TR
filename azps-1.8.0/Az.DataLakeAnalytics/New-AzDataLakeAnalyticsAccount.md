---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 49da4b322a2782ad23079c07e7f6c5dce171adb4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761094"
---
# <span data-ttu-id="a9aa4-101">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a9aa4-101">New-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="a9aa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="a9aa4-103">Veri Lake Analytics hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9aa4-103">Creates a Data Lake Analytics account.</span></span>

## <span data-ttu-id="a9aa4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9aa4-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9aa4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9aa4-105">DESCRIPTION</span></span>
<span data-ttu-id="a9aa4-106">**New-Azdatalakeanalizleri Ticsaccount** cmdlet 'ı bir Azure Data Lake Analytics hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9aa4-106">The **New-AzDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="a9aa4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9aa4-107">EXAMPLES</span></span>

### <span data-ttu-id="a9aa4-108">Örnek 1: veri Lake Analytics hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="a9aa4-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="a9aa4-109">Bu komut, ContosoOrg adlı kaynak grubunda ContosoAdlStore veri deposunu kullanan ContosoAdlAccount adlı bir Data Lake Analytics hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9aa4-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="a9aa4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9aa4-110">PARAMETERS</span></span>

### <span data-ttu-id="a9aa4-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a9aa4-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="a9aa4-112">Varsayılan veri kaynağı olarak ayarlanacak Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9aa4-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

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

### <span data-ttu-id="a9aa4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9aa4-113">-DefaultProfile</span></span>
<span data-ttu-id="a9aa4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a9aa4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9aa4-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="a9aa4-115">-Location</span></span>
<span data-ttu-id="a9aa4-116">Veri Lake Analytics hesabının oluşturulacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9aa4-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="a9aa4-117">Şu anda yalnızca Doğu ABD 2 destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="a9aa4-117">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="a9aa4-118">-Maxçözümlerken</span><span class="sxs-lookup"><span data-stu-id="a9aa4-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="a9aa4-119">Bu hesap için isteğe bağlı en yüksek çözümleme birimleri.</span><span class="sxs-lookup"><span data-stu-id="a9aa4-119">The optional maximum supported analytics units for this account.</span></span>

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

### <span data-ttu-id="a9aa4-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="a9aa4-120">-MaxJobCount</span></span>
<span data-ttu-id="a9aa4-121">Aynı anda hesabın altında çalışan isteğe bağlı en yüksek işler.</span><span class="sxs-lookup"><span data-stu-id="a9aa4-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="a9aa4-122">Hiçbiri belirtilmezse, varsayılan 3 olur</span><span class="sxs-lookup"><span data-stu-id="a9aa4-122">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="a9aa4-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="a9aa4-123">-Name</span></span>
<span data-ttu-id="a9aa4-124">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9aa4-124">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="a9aa4-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="a9aa4-125">-QueryStoreRetention</span></span>
<span data-ttu-id="a9aa4-126">İş meta verilerinin tutulacağı isteğe bağlı gün sayısı.</span><span class="sxs-lookup"><span data-stu-id="a9aa4-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="a9aa4-127">Belirtilmezse, varsayılan 30 gündür.</span><span class="sxs-lookup"><span data-stu-id="a9aa4-127">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="a9aa4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9aa4-128">-ResourceGroupName</span></span>
<span data-ttu-id="a9aa4-129">Data Lake Analytics hesabının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9aa4-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="a9aa4-130">Kaynak grubu oluşturmak için New-AzResourceGroup cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a9aa4-130">To create a resource group, use the New-AzResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="a9aa4-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a9aa4-131">-Tag</span></span>
<span data-ttu-id="a9aa4-132">Bu hesapla ilişkilendirilmiş etiketlerin dize sözlüğü</span><span class="sxs-lookup"><span data-stu-id="a9aa4-132">A string,string dictionary of tags associated with this account</span></span>

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

### <span data-ttu-id="a9aa4-133">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="a9aa4-133">-Tier</span></span>
<span data-ttu-id="a9aa4-134">Bu hesabın kullanması için istenen taahhüt katmanı.</span><span class="sxs-lookup"><span data-stu-id="a9aa4-134">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="a9aa4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9aa4-135">CommonParameters</span></span>
<span data-ttu-id="a9aa4-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9aa4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9aa4-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9aa4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9aa4-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9aa4-138">INPUTS</span></span>

### <span data-ttu-id="a9aa4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a9aa4-139">System.String</span></span>

### <span data-ttu-id="a9aa4-140">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a9aa4-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a9aa4-141">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="a9aa4-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a9aa4-142">System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Analytics. modeller. TierType, Microsoft. Azure. Management. DataLake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a9aa4-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="a9aa4-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9aa4-143">OUTPUTS</span></span>

### <span data-ttu-id="a9aa4-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDAtalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="a9aa4-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="a9aa4-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9aa4-145">NOTES</span></span>

## <span data-ttu-id="a9aa4-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9aa4-146">RELATED LINKS</span></span>

[<span data-ttu-id="a9aa4-147">Get-Azdatalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="a9aa4-147">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a9aa4-148">Remove-Azdatalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="a9aa4-148">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a9aa4-149">Set-Azdatalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="a9aa4-149">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a9aa4-150">Test-Azdatalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="a9aa4-150">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


