---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: bc0f1a6aacc6188a982fe75fa021bdafdc4e02de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277295"
---
# <span data-ttu-id="9a4b9-101">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="9a4b9-101">Add-AzLogProfile</span></span>

## <span data-ttu-id="9a4b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a4b9-102">SYNOPSIS</span></span>
<span data-ttu-id="9a4b9-103">Yeni etkinlik günlüğü profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-103">Creates a new activity log profile.</span></span> <span data-ttu-id="9a4b9-104">Bu profil, etkinlik günlüğünü bir Azure depolama hesabına arşivlemek veya aynı abonelikteki bir Azure Olay Hub 'ına aktarmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

## <span data-ttu-id="9a4b9-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9a4b9-105">SYNTAX</span></span>

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a4b9-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="9a4b9-106">DESCRIPTION</span></span>
<span data-ttu-id="9a4b9-107">**Add-AzLogProfile** cmdlet 'i bir günlük profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-107">The **Add-AzLogProfile** cmdlet creates a log profile.</span></span>
- <span data-ttu-id="9a4b9-108">**Depolama hesabı** -yalnızca standart depolama hesabı (Premium depolama hesabı desteklenmiyor) desteklenir.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="9a4b9-109">ARM veya klasik türünde olabilir.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="9a4b9-110">Depolama hesabına oturum açtıysa, etkinlik günlüğünü depolama maliyeti normal standart depolama tarifeleriyle faturalanır.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="9a4b9-111">Abonelik başına yalnızca bir günlük profili olabilir etkinlik günlüğü dışarı aktarmak için abonelik başına yalnızca bir depolama hesabı kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 
- <span data-ttu-id="9a4b9-112">**Olay Hub 'ı** -etkinlik günlüğünü dışarı aktarmak için abonelik başına yalnızca bir olay hub 'ı olabilir.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="9a4b9-113">Etkinlik günlüğü bir olay hub 'ına akıtısa, standart Olay Hub fiyatlandırması uygulanır.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> <span data-ttu-id="9a4b9-114">Etkinlik günlüğünde, olaylar bir bölgeye ait olabilir veya "Global" olabilir.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="9a4b9-115">Genel aslýnda bu olaylarda, olayların gerçekten bu kategoriye giren çoğunluğunda bölge çoğunluğu ve bölgeden bağımsızdır.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="9a4b9-116">Etkinlik günlüğü profili portaldan ayarlanmışsa, Kullanıcı arabiriminde seçili diğer bölgelerin yanına örtülü olarak "genel" ekler.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="9a4b9-117">Cmdlet kullanıldığında, "Global" olarak konum, başka herhangi bir bölgeden ayrı olarak bahsedilmelidir.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 
<span data-ttu-id="9a4b9-118">**Not** :- **konumlarda "Global" ayarlanamayan Etkinlik günlüğünün büyük bir bölümünü dışarı aktarmaz.**</span><span class="sxs-lookup"><span data-stu-id="9a4b9-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> <span data-ttu-id="9a4b9-119">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="9a4b9-120">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9a4b9-120">EXAMPLES</span></span>

### <span data-ttu-id="9a4b9-121">Örnek 1: konum koşulunu eşleştiren etkinlik günlüğünü bir depolama hesabıyla dışarı aktarmak için yeni bir günlük profili ekleme</span><span class="sxs-lookup"><span data-stu-id="9a4b9-121">Example 1: Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```powershell
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

### <span data-ttu-id="9a4b9-122">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9a4b9-122">Example 2</span></span>

<span data-ttu-id="9a4b9-123">Yeni etkinlik günlüğü profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-123">Creates a new activity log profile.</span></span> <span data-ttu-id="9a4b9-124">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="9a4b9-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Add-AzLogProfile -Location 'Global' -Name ExportLogProfile -RetentionInDays <Int32> -ServiceBusRuleId <String> -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="9a4b9-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9a4b9-125">PARAMETERS</span></span>

### <span data-ttu-id="9a4b9-126">-Kategori</span><span class="sxs-lookup"><span data-stu-id="9a4b9-126">-Category</span></span>
<span data-ttu-id="9a4b9-127">Kategorilerin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-127">Specifies the list of categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a4b9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a4b9-128">-DefaultProfile</span></span>
<span data-ttu-id="9a4b9-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9a4b9-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a4b9-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="9a4b9-130">-Location</span></span>
<span data-ttu-id="9a4b9-131">Günlük profilinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-131">Specifies the location of the log profile.</span></span>
<span data-ttu-id="9a4b9-132">Geçerli değerler: en son konum listesini almak için aşağıdaki cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-132">Valid values: Run below cmdlet to get the latest list of locations.</span></span> <span data-ttu-id="9a4b9-133">Get-AzLocation | DisplayName 'i seçin</span><span class="sxs-lookup"><span data-stu-id="9a4b9-133">Get-AzLocation | Select DisplayName</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a4b9-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="9a4b9-134">-Name</span></span>
<span data-ttu-id="9a4b9-135">Profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-135">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a4b9-136">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="9a4b9-136">-RetentionInDays</span></span>
<span data-ttu-id="9a4b9-137">Bekletme ilkesini gün olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-137">Specifies the retention policy, in days.</span></span> <span data-ttu-id="9a4b9-138">Bu, belirtilen depolama hesabında günlüklerin korunduğu gün sayısıdır.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-138">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="9a4b9-139">Bu ayarı süresiz olarak **0** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-139">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="9a4b9-140">Belirtilmemişse, varsayılan olarak **0** değerini alır.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-140">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="9a4b9-141">Veri bekletmesi için normal standart depolama veya Olay Hub faturalama ücretleri uygulanacaktır.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-141">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="9a4b9-142">-Servicebusruleıd</span><span class="sxs-lookup"><span data-stu-id="9a4b9-142">-ServiceBusRuleId</span></span>
<span data-ttu-id="9a4b9-143">Hizmet veri yolu kuralının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-143">Specifies the ID of the Service Bus rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a4b9-144">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="9a4b9-144">-StorageAccountId</span></span>
<span data-ttu-id="9a4b9-145">Depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-145">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="9a4b9-146">KIMLIK, depolama hesabının tam kaynak KIMLIĞIDIR Örneğin,</span><span class="sxs-lookup"><span data-stu-id="9a4b9-146">ID is the fully qualified Resource ID of the storage account for example</span></span>  
<span data-ttu-id="9a4b9-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="9a4b9-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a4b9-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="9a4b9-148">-Confirm</span></span>
<span data-ttu-id="9a4b9-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a4b9-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a4b9-150">-WhatIf</span></span>
<span data-ttu-id="9a4b9-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a4b9-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a4b9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a4b9-153">CommonParameters</span></span>
<span data-ttu-id="9a4b9-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a4b9-155">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9a4b9-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a4b9-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9a4b9-156">INPUTS</span></span>

### <span data-ttu-id="9a4b9-157">System. String</span><span class="sxs-lookup"><span data-stu-id="9a4b9-157">System.String</span></span>

### <span data-ttu-id="9a4b9-158">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="9a4b9-158">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9a4b9-159">System. Koleksiyonlar. Generic. LIST ' 1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0</span><span class="sxs-lookup"><span data-stu-id="9a4b9-159">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9a4b9-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9a4b9-160">OUTPUTS</span></span>

### <span data-ttu-id="9a4b9-161">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="9a4b9-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="9a4b9-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9a4b9-162">NOTES</span></span>

## <span data-ttu-id="9a4b9-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9a4b9-163">RELATED LINKS</span></span>

[<span data-ttu-id="9a4b9-164">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="9a4b9-164">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)

[<span data-ttu-id="9a4b9-165">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="9a4b9-165">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


