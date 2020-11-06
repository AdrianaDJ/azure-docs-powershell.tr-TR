---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 8ca5efc7e5cee80fdf7ce34a13ce23ac733c0154
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589824"
---
# <span data-ttu-id="3b2c2-101">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="3b2c2-101">Set-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="3b2c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b2c2-102">SYNOPSIS</span></span>
<span data-ttu-id="3b2c2-103">Data Lake Analytics hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-103">Modifies a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b2c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b2c2-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-Tag] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b2c2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b2c2-105">DESCRIPTION</span></span>
<span data-ttu-id="3b2c2-106">**Set-Azurermdatalakeanalizizsaccount** cmdlet 'ı bir Azure Data Lake Analytics hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-106">The **Set-AzureRmDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="3b2c2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b2c2-107">EXAMPLES</span></span>

### <span data-ttu-id="3b2c2-108">Örnek 1: hesabın veri kaynağını değiştirme</span><span class="sxs-lookup"><span data-stu-id="3b2c2-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="3b2c2-109">Bu komut, hesabın varsayılan veri kaynağını ve Etiketler özelliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="3b2c2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b2c2-110">PARAMETERS</span></span>

### <span data-ttu-id="3b2c2-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="3b2c2-111">-AllowAzureIpState</span></span>
<span data-ttu-id="3b2c2-112">İsteğe bağlı olarak, Azure 'un güvenlik duvarından erişmesine izin ver/engelle.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: FirewallAllowAzureIpsState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b2c2-113">-DefaultProfile</span></span>
<span data-ttu-id="3b2c2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3b2c2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b2c2-115">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="3b2c2-115">-FirewallState</span></span>
<span data-ttu-id="3b2c2-116">İsteğe bağlı olarak varolan güvenlik duvarı kurallarını etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="3b2c2-116">Optionally enable/disable existing firewall rules.</span></span>

```yaml
Type: FirewallState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c2-117">-Maxçözümlerken</span><span class="sxs-lookup"><span data-stu-id="3b2c2-117">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="3b2c2-118">Hesabı güncelleştirmek için isteğe bağlı en yüksek analitik birim.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-118">The optional maximum supported analytics units to update the account with.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c2-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="3b2c2-119">-MaxJobCount</span></span>
<span data-ttu-id="3b2c2-120">Hesabın altında, aynı anda ayarlanması için, desteklenen isteğe bağlı en yüksek işler.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-120">The optional maximum supported jobs running under the account at the same time to set.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c2-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="3b2c2-121">-Name</span></span>
<span data-ttu-id="3b2c2-122">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-122">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c2-123">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="3b2c2-123">-QueryStoreRetention</span></span>
<span data-ttu-id="3b2c2-124">Hesapta ayarlanması gereken isteğe bağlı gün sayısı.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-124">The optional number of days that job metadata is retained to set in the account.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b2c2-125">-ResourceGroupName</span></span>
<span data-ttu-id="3b2c2-126">Data Lake Analytics hesabının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-126">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="3b2c2-127">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3b2c2-127">-Tag</span></span>
<span data-ttu-id="3b2c2-128">Geçerli etiket kümesini değiştirmesi gereken bu hesapla ilişkilendirilmiş etiketlerin dize sözlüğü</span><span class="sxs-lookup"><span data-stu-id="3b2c2-128">A string,string dictionary of tags associated with this account that should replace the current set of tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c2-129">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="3b2c2-129">-Tier</span></span>
<span data-ttu-id="3b2c2-130">Bu hesabın kullanması için istenen taahhüt katmanı.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-130">The desired commitment tier for this account to use.</span></span>

```yaml
Type: TierType
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b2c2-131">CommonParameters</span></span>
<span data-ttu-id="3b2c2-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b2c2-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b2c2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b2c2-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b2c2-134">INPUTS</span></span>

### <span data-ttu-id="3b2c2-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3b2c2-135">None</span></span>
<span data-ttu-id="3b2c2-136">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3b2c2-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b2c2-137">OUTPUTS</span></span>

### <span data-ttu-id="3b2c2-138">Psdatalakeanalyzer Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="3b2c2-138">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="3b2c2-139">Güncelleştirilmiş hesap ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="3b2c2-139">The updated account details.</span></span>

## <span data-ttu-id="3b2c2-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b2c2-140">NOTES</span></span>

## <span data-ttu-id="3b2c2-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b2c2-141">RELATED LINKS</span></span>

[<span data-ttu-id="3b2c2-142">Get-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="3b2c2-142">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="3b2c2-143">Yeni-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="3b2c2-143">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="3b2c2-144">Remove-Azurermdatalakeanalyzer Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="3b2c2-144">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="3b2c2-145">Test-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="3b2c2-145">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


