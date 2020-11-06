---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 8de6b2a0d86c9eb83a067f4982a5ef62d3a9adbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587963"
---
# <span data-ttu-id="5b05b-101">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="5b05b-101">Set-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="5b05b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b05b-102">SYNOPSIS</span></span>
<span data-ttu-id="5b05b-103">Data Lake Analytics hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5b05b-103">Modifies a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b05b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5b05b-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-Tags] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxDegreeOfParallelism <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b05b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b05b-105">DESCRIPTION</span></span>
<span data-ttu-id="5b05b-106">**Set-Azurermdatalakeanalizizsaccount** cmdlet 'ı bir Azure Data Lake Analytics hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5b05b-106">The **Set-AzureRmDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="5b05b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5b05b-107">EXAMPLES</span></span>

### <span data-ttu-id="5b05b-108">Örnek 1: hesabın veri kaynağını değiştirme</span><span class="sxs-lookup"><span data-stu-id="5b05b-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="5b05b-109">Bu komut, hesabın varsayılan veri kaynağını ve Etiketler özelliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5b05b-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="5b05b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5b05b-110">PARAMETERS</span></span>

### <span data-ttu-id="5b05b-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="5b05b-111">-AllowAzureIpState</span></span>
<span data-ttu-id="5b05b-112">İsteğe bağlı olarak, Azure 'un güvenlik duvarından erişmesine izin ver/engelle.</span><span class="sxs-lookup"><span data-stu-id="5b05b-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

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

### <span data-ttu-id="5b05b-113">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="5b05b-113">-FirewallState</span></span>
<span data-ttu-id="5b05b-114">İsteğe bağlı olarak varolan güvenlik duvarı kurallarını etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="5b05b-114">Optionally enable/disable existing firewall rules.</span></span>

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

### <span data-ttu-id="5b05b-115">-Maxdegreeofparalellizm</span><span class="sxs-lookup"><span data-stu-id="5b05b-115">-MaxDegreeOfParallelism</span></span>
<span data-ttu-id="5b05b-116">Hesabı güncelleştirmek için isteğe bağlı en yüksek paralellik derecesi</span><span class="sxs-lookup"><span data-stu-id="5b05b-116">The optional maximum supported degree of parallelism to update the account with.</span></span>

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

### <span data-ttu-id="5b05b-117">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="5b05b-117">-MaxJobCount</span></span>
<span data-ttu-id="5b05b-118">Hesabın altında, aynı anda ayarlanması için, desteklenen isteğe bağlı en yüksek işler.</span><span class="sxs-lookup"><span data-stu-id="5b05b-118">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="5b05b-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="5b05b-119">-Name</span></span>
<span data-ttu-id="5b05b-120">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b05b-120">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="5b05b-121">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="5b05b-121">-QueryStoreRetention</span></span>
<span data-ttu-id="5b05b-122">Hesapta ayarlanması gereken isteğe bağlı gün sayısı.</span><span class="sxs-lookup"><span data-stu-id="5b05b-122">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="5b05b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b05b-123">-ResourceGroupName</span></span>
<span data-ttu-id="5b05b-124">Data Lake Analytics hesabının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b05b-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="5b05b-125">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="5b05b-125">-Tags</span></span>
<span data-ttu-id="5b05b-126">Diğer Azure kaynakları arasında Data Lake Analytics hesabını tanıtmak için kullanılabilecek anahtar değeri çiftlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b05b-126">Specifies key-value pairs that can be used to identify the Data Lake Analytics account among other Azure resources.</span></span>

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

### <span data-ttu-id="5b05b-127">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="5b05b-127">-Tier</span></span>
<span data-ttu-id="5b05b-128">Bu hesabın kullanması için istenen taahhüt katmanı.</span><span class="sxs-lookup"><span data-stu-id="5b05b-128">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="5b05b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b05b-129">-DefaultProfile</span></span>
<span data-ttu-id="5b05b-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5b05b-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b05b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b05b-131">CommonParameters</span></span>
<span data-ttu-id="5b05b-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5b05b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b05b-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b05b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b05b-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5b05b-134">INPUTS</span></span>

## <span data-ttu-id="5b05b-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5b05b-135">OUTPUTS</span></span>

### <span data-ttu-id="5b05b-136">Psdatalakeanalyzer Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="5b05b-136">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="5b05b-137">Güncelleştirilmiş hesap ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="5b05b-137">The updated account details.</span></span>

## <span data-ttu-id="5b05b-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5b05b-138">NOTES</span></span>

## <span data-ttu-id="5b05b-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5b05b-139">RELATED LINKS</span></span>

[<span data-ttu-id="5b05b-140">Get-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="5b05b-140">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="5b05b-141">Yeni-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="5b05b-141">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="5b05b-142">Remove-Azurermdatalakeanalyzer Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="5b05b-142">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="5b05b-143">Test-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="5b05b-143">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


