---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: 6908bc4d474d0dbe9df045332f3820b5f7536dac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592511"
---
# <span data-ttu-id="928f4-101">Set-AzureRmDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="928f4-101">Set-AzureRmDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="928f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="928f4-102">SYNOPSIS</span></span>
<span data-ttu-id="928f4-103">Azure Data Lake Store hesabındaki bir dosyanın süresi bitim süresini ayarlar veya kaldırır.</span><span class="sxs-lookup"><span data-stu-id="928f4-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="928f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="928f4-104">SYNTAX</span></span>

### <span data-ttu-id="928f4-105">SetAbsoluteNeverExpireExpiry (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="928f4-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="928f4-106">Setrelativesüre sonu</span><span class="sxs-lookup"><span data-stu-id="928f4-106">SetRelativeExpiry</span></span>
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-RelativeFileExpiryOption] <PathRelativeExpiryOptions>] [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="928f4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="928f4-107">DESCRIPTION</span></span>
<span data-ttu-id="928f4-108">**Set-AzureRmDataLakeStoreItemExpiry** cmdlet 'ı, Azure Data Lake Store hesabındaki bir dosyanın süresi bitim süresini ayarlar veya kaldırır.</span><span class="sxs-lookup"><span data-stu-id="928f4-108">The **Set-AzureRmDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="928f4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="928f4-109">EXAMPLES</span></span>

### <span data-ttu-id="928f4-110">Örnek 1: dosya için son kullanma zamanını ayarlama</span><span class="sxs-lookup"><span data-stu-id="928f4-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="928f4-111">Şu andan itibaren, ContosoADL hesabındaki myfile.txt zaman aşımı süresini iki saat olacak şekilde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="928f4-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="928f4-112">Bu, dosyanın süresi dolmasına neden olur (silme için işaretlenir) iki saat içinde.</span><span class="sxs-lookup"><span data-stu-id="928f4-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="928f4-113">Örnek 2: dosyanın süre sonunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="928f4-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="928f4-114">' ContosoADL ' hesabında ' myfile.txt ' dosyasında daha önce ayarlanmış olan sona erdirmeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="928f4-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="928f4-115">Bu, dosyanın otomatik olarak süresinin dolamayacağı anlamına gelir (silme için işaretlenir) ve el ile silinmesi veya yeniden kullanım süresi olarak ayarlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="928f4-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>


### <span data-ttu-id="928f4-116">Örnek 3: Şu an için bir dosya için son kullanma tarihi ayarlama</span><span class="sxs-lookup"><span data-stu-id="928f4-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="928f4-117">İlk komut, sunucudaki geçerli saate göre dosya/myfile.txt 240 saniyesi kullanım süresi sonunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="928f4-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>

<span data-ttu-id="928f4-118">İkinci komut, sunucudaki oluşturulma zamanı saatine göre dosya/myfile.txt 240 saniyesi kullanım süresi sonunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="928f4-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="928f4-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="928f4-119">PARAMETERS</span></span>

### <span data-ttu-id="928f4-120">-Hesap</span><span class="sxs-lookup"><span data-stu-id="928f4-120">-Account</span></span>
<span data-ttu-id="928f4-121">Data Lake Store hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="928f4-121">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="928f4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="928f4-122">-DefaultProfile</span></span>
<span data-ttu-id="928f4-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="928f4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="928f4-124">-Süre sonu</span><span class="sxs-lookup"><span data-stu-id="928f4-124">-Expiration</span></span>
<span data-ttu-id="928f4-125">Belirtilen dosyanın mutlak son kullanma tarihi.</span><span class="sxs-lookup"><span data-stu-id="928f4-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="928f4-126">Değer yoksa veya MaxValue olarak ayarlanmamışsa, dosyanın süresi dolmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="928f4-126">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: Set expiry as Absolute or NeverExpire
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="928f4-127">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="928f4-127">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="928f4-128">Göreli süre sonu seçenekleri.</span><span class="sxs-lookup"><span data-stu-id="928f4-128">Relative expiry options.</span></span> <span data-ttu-id="928f4-129">RelativeToNow veya RelativeToCreationDate geçerli seçeneklerdir</span><span class="sxs-lookup"><span data-stu-id="928f4-129">RelativeToNow or RelativeToCreationDate are current options</span></span>
```yaml
Type: PathRelativeExpiryOptions
Parameter Sets: Set expiry as relative to creation or now
Aliases: 
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="928f4-130">-Yol</span><span class="sxs-lookup"><span data-stu-id="928f4-130">-Path</span></span>
<span data-ttu-id="928f4-131">Bitiş tarihi ayarlanacak veya kaldırılacak dosya öğesinin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="928f4-131">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="928f4-132">-RelativeTime</span><span class="sxs-lookup"><span data-stu-id="928f4-132">-RelativeTime</span></span>
<span data-ttu-id="928f4-133">Şimdi veya oluşturulma saatine göre milisaniye cinsinden göreli zaman</span><span class="sxs-lookup"><span data-stu-id="928f4-133">The relative time in milliseconds with respect to now or creation time</span></span>
```yaml
Type: Int64
Parameter Sets: Set expiry as relative to creation or now
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="928f4-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="928f4-134">-Confirm</span></span>
<span data-ttu-id="928f4-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="928f4-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="928f4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="928f4-136">-WhatIf</span></span>
<span data-ttu-id="928f4-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="928f4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="928f4-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="928f4-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="928f4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="928f4-139">CommonParameters</span></span>
<span data-ttu-id="928f4-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="928f4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="928f4-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="928f4-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="928f4-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="928f4-142">INPUTS</span></span>

### <span data-ttu-id="928f4-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="928f4-143">None</span></span>
<span data-ttu-id="928f4-144">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="928f4-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="928f4-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="928f4-145">OUTPUTS</span></span>

### <span data-ttu-id="928f4-146">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="928f4-146">DataLakeStoreItem</span></span>
<span data-ttu-id="928f4-147">Yeni son kullanma tarihi olan güncelleştirilmiş dosya.</span><span class="sxs-lookup"><span data-stu-id="928f4-147">The updated file with a new expiration time.</span></span>

## <span data-ttu-id="928f4-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="928f4-148">NOTES</span></span>
<span data-ttu-id="928f4-149">Diğer ad: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="928f4-149">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="928f4-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="928f4-150">RELATED LINKS</span></span>

[<span data-ttu-id="928f4-151">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="928f4-151">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

