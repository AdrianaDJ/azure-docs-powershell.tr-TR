---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
ms.openlocfilehash: 074e6224c7a5b1ea1e8039901b75d223581495d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752281"
---
# <span data-ttu-id="caed9-101">Set-AzDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="caed9-101">Set-AzDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="caed9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="caed9-102">SYNOPSIS</span></span>
<span data-ttu-id="caed9-103">Azure Data Lake Store hesabındaki bir dosyanın süresi bitim süresini ayarlar veya kaldırır.</span><span class="sxs-lookup"><span data-stu-id="caed9-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="caed9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="caed9-104">SYNTAX</span></span>

### <span data-ttu-id="caed9-105">SetAbsoluteNeverExpireExpiry (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="caed9-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="caed9-106">Setrelativesüre sonu</span><span class="sxs-lookup"><span data-stu-id="caed9-106">SetRelativeExpiry</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caed9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="caed9-107">DESCRIPTION</span></span>
<span data-ttu-id="caed9-108">**Set-AzDataLakeStoreItemExpiry** cmdlet 'ı, Azure Data Lake Store hesabındaki bir dosyanın süresi bitim süresini ayarlar veya kaldırır.</span><span class="sxs-lookup"><span data-stu-id="caed9-108">The **Set-AzDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="caed9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="caed9-109">EXAMPLES</span></span>

### <span data-ttu-id="caed9-110">Örnek 1: dosya için son kullanma zamanını ayarlama</span><span class="sxs-lookup"><span data-stu-id="caed9-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="caed9-111">Şu andan itibaren, ContosoADL hesabındaki myfile.txt zaman aşımı süresini iki saat olacak şekilde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="caed9-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="caed9-112">Bu, dosyanın süresi dolmasına neden olur (silme için işaretlenir) iki saat içinde.</span><span class="sxs-lookup"><span data-stu-id="caed9-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="caed9-113">Örnek 2: dosyanın süre sonunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="caed9-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="caed9-114">' ContosoADL ' hesabında ' myfile.txt ' dosyasında daha önce ayarlanmış olan sona erdirmeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="caed9-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="caed9-115">Bu, dosyanın otomatik olarak süresinin dolamayacağı anlamına gelir (silme için işaretlenir) ve el ile silinmesi veya yeniden kullanım süresi olarak ayarlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="caed9-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

### <span data-ttu-id="caed9-116">Örnek 3: Şu an için bir dosya için son kullanma tarihi ayarlama</span><span class="sxs-lookup"><span data-stu-id="caed9-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="caed9-117">İlk komut, sunucudaki geçerli saate göre dosya/myfile.txt 240 saniyesi kullanım süresi sonunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="caed9-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>
<span data-ttu-id="caed9-118">İkinci komut, sunucudaki oluşturulma zamanı saatine göre dosya/myfile.txt 240 saniyesi kullanım süresi sonunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="caed9-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="caed9-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="caed9-119">PARAMETERS</span></span>

### <span data-ttu-id="caed9-120">-Hesap</span><span class="sxs-lookup"><span data-stu-id="caed9-120">-Account</span></span>
<span data-ttu-id="caed9-121">Data Lake Store hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="caed9-121">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="caed9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caed9-122">-DefaultProfile</span></span>
<span data-ttu-id="caed9-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="caed9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="caed9-124">-Süre sonu</span><span class="sxs-lookup"><span data-stu-id="caed9-124">-Expiration</span></span>
<span data-ttu-id="caed9-125">Belirtilen dosyanın mutlak son kullanma tarihi.</span><span class="sxs-lookup"><span data-stu-id="caed9-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="caed9-126">Değer yoksa veya MaxValue olarak ayarlanmamışsa, dosyanın süresi dolmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="caed9-126">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: SetAbsoluteNeverExpireExpiry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caed9-127">-Yol</span><span class="sxs-lookup"><span data-stu-id="caed9-127">-Path</span></span>
<span data-ttu-id="caed9-128">Bitiş tarihi ayarlanacak veya kaldırılacak dosya öğesinin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="caed9-128">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caed9-129">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="caed9-129">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="caed9-130">Göreli süre sonu seçenekleri.</span><span class="sxs-lookup"><span data-stu-id="caed9-130">Relative expiry options.</span></span> <span data-ttu-id="caed9-131">RelativeToNow veya RelativeToCreationDate geçerli seçeneklerdir</span><span class="sxs-lookup"><span data-stu-id="caed9-131">RelativeToNow or RelativeToCreationDate are current options</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions
Parameter Sets: SetRelativeExpiry
Aliases:
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caed9-132">-RelativeTime</span><span class="sxs-lookup"><span data-stu-id="caed9-132">-RelativeTime</span></span>
<span data-ttu-id="caed9-133">Şimdi veya oluşturulma saatine göre milisaniye cinsinden göreli zaman</span><span class="sxs-lookup"><span data-stu-id="caed9-133">The relative time in milliseconds with respect to now or creation time</span></span>

```yaml
Type: System.Int64
Parameter Sets: SetRelativeExpiry
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caed9-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="caed9-134">-Confirm</span></span>
<span data-ttu-id="caed9-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="caed9-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caed9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caed9-136">-WhatIf</span></span>
<span data-ttu-id="caed9-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="caed9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caed9-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="caed9-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caed9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caed9-139">CommonParameters</span></span>
<span data-ttu-id="caed9-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="caed9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caed9-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caed9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caed9-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="caed9-142">INPUTS</span></span>

### <span data-ttu-id="caed9-143">System. String</span><span class="sxs-lookup"><span data-stu-id="caed9-143">System.String</span></span>

### <span data-ttu-id="caed9-144">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="caed9-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="caed9-145">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="caed9-145">System.DateTimeOffset</span></span>

### <span data-ttu-id="caed9-146">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreEnums + PathRelativeExpiryOptions</span><span class="sxs-lookup"><span data-stu-id="caed9-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span></span>

### <span data-ttu-id="caed9-147">System. Int64</span><span class="sxs-lookup"><span data-stu-id="caed9-147">System.Int64</span></span>

## <span data-ttu-id="caed9-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="caed9-148">OUTPUTS</span></span>

### <span data-ttu-id="caed9-149">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="caed9-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="caed9-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="caed9-150">NOTES</span></span>
<span data-ttu-id="caed9-151">Diğer ad: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="caed9-151">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="caed9-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="caed9-152">RELATED LINKS</span></span>

[<span data-ttu-id="caed9-153">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="caed9-153">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

