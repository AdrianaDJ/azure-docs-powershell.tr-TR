---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 9bb6475f0e9ea688c9339980c1a8955ea011fbb7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761084"
---
# <span data-ttu-id="0b879-101">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0b879-101">Set-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="0b879-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b879-102">SYNOPSIS</span></span>
<span data-ttu-id="0b879-103">Data Lake Analytics hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0b879-103">Modifies a Data Lake Analytics account.</span></span>

## <span data-ttu-id="0b879-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b879-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsAccount [-Name] <String> [[-Tag] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b879-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b879-105">DESCRIPTION</span></span>
<span data-ttu-id="0b879-106">**Set-Azdatalakeanalizticsaccount** cmdlet 'ı bir Azure Data Lake Analytics hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0b879-106">The **Set-AzDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="0b879-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b879-107">EXAMPLES</span></span>

### <span data-ttu-id="0b879-108">Örnek 1: hesabın veri kaynağını değiştirme</span><span class="sxs-lookup"><span data-stu-id="0b879-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="0b879-109">Bu komut, hesabın varsayılan veri kaynağını ve Etiketler özelliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0b879-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="0b879-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b879-110">PARAMETERS</span></span>

### <span data-ttu-id="0b879-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="0b879-111">-AllowAzureIpState</span></span>
<span data-ttu-id="0b879-112">İsteğe bağlı olarak, Azure 'un güvenlik duvarından erişmesine izin ver/engelle.</span><span class="sxs-lookup"><span data-stu-id="0b879-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b879-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b879-113">-DefaultProfile</span></span>
<span data-ttu-id="0b879-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0b879-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b879-115">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="0b879-115">-FirewallState</span></span>
<span data-ttu-id="0b879-116">İsteğe bağlı olarak varolan güvenlik duvarı kurallarını etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="0b879-116">Optionally enable/disable existing firewall rules.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b879-117">-Maxçözümlerken</span><span class="sxs-lookup"><span data-stu-id="0b879-117">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="0b879-118">Hesabı güncelleştirmek için isteğe bağlı en yüksek analitik birim.</span><span class="sxs-lookup"><span data-stu-id="0b879-118">The optional maximum supported analytics units to update the account with.</span></span>

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

### <span data-ttu-id="0b879-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="0b879-119">-MaxJobCount</span></span>
<span data-ttu-id="0b879-120">Hesabın altında, aynı anda ayarlanması için, desteklenen isteğe bağlı en yüksek işler.</span><span class="sxs-lookup"><span data-stu-id="0b879-120">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="0b879-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="0b879-121">-Name</span></span>
<span data-ttu-id="0b879-122">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b879-122">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="0b879-123">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="0b879-123">-QueryStoreRetention</span></span>
<span data-ttu-id="0b879-124">Hesapta ayarlanması gereken isteğe bağlı gün sayısı.</span><span class="sxs-lookup"><span data-stu-id="0b879-124">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="0b879-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b879-125">-ResourceGroupName</span></span>
<span data-ttu-id="0b879-126">Data Lake Analytics hesabının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b879-126">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="0b879-127">Etiketli</span><span class="sxs-lookup"><span data-stu-id="0b879-127">-Tag</span></span>
<span data-ttu-id="0b879-128">Geçerli etiket kümesini değiştirmesi gereken bu hesapla ilişkilendirilmiş etiketlerin dize sözlüğü</span><span class="sxs-lookup"><span data-stu-id="0b879-128">A string,string dictionary of tags associated with this account that should replace the current set of tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b879-129">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="0b879-129">-Tier</span></span>
<span data-ttu-id="0b879-130">Bu hesabın kullanması için istenen taahhüt katmanı.</span><span class="sxs-lookup"><span data-stu-id="0b879-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="0b879-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b879-131">CommonParameters</span></span>
<span data-ttu-id="0b879-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b879-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b879-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b879-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b879-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b879-134">INPUTS</span></span>

### <span data-ttu-id="0b879-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0b879-135">System.String</span></span>

### <span data-ttu-id="0b879-136">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0b879-136">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0b879-137">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="0b879-137">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0b879-138">System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Analytics. modeller. TierType, Microsoft. Azure. Management. DataLake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0b879-138">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="0b879-139">System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Analytics. modeller. FirewallState, Microsoft. Azure. Management. DataLake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0b879-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="0b879-140">System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Analytics. modeller. FirewallAllowAzureIpsState, Microsoft. Azure. Management. DataLake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0b879-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="0b879-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b879-141">OUTPUTS</span></span>

### <span data-ttu-id="0b879-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDAtalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="0b879-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="0b879-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b879-143">NOTES</span></span>

## <span data-ttu-id="0b879-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b879-144">RELATED LINKS</span></span>

[<span data-ttu-id="0b879-145">Get-Azdatalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="0b879-145">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="0b879-146">Yeni-Azdatalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="0b879-146">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="0b879-147">Remove-Azdatalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="0b879-147">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="0b879-148">Test-Azdatalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="0b879-148">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


