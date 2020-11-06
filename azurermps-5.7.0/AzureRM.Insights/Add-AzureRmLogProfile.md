---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
ms.openlocfilehash: 0ef53015b3e07eeb69cdcfd0ab70c67317ab92cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594478"
---
# <span data-ttu-id="70f9a-101">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="70f9a-101">Add-AzureRmLogProfile</span></span>

## <span data-ttu-id="70f9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70f9a-102">SYNOPSIS</span></span>
<span data-ttu-id="70f9a-103">Yeni etkinlik günlüğü profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70f9a-103">Creates a new activity log profile.</span></span> <span data-ttu-id="70f9a-104">Bu profil, etkinlik günlüğünü bir Azure depolama hesabına arşivlemek veya aynı abonelikteki bir Azure Olay Hub 'ına aktarmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="70f9a-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70f9a-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="70f9a-105">SYNTAX</span></span>

```
Add-AzureRmLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70f9a-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="70f9a-106">DESCRIPTION</span></span>
<span data-ttu-id="70f9a-107">**Add-AzureRmLogProfile** cmdlet 'i bir günlük profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70f9a-107">The **Add-AzureRmLogProfile** cmdlet creates a log profile.</span></span>

- <span data-ttu-id="70f9a-108">**Depolama hesabı** -yalnızca standart depolama hesabı (Premium depolama hesabı desteklenmiyor) desteklenir.</span><span class="sxs-lookup"><span data-stu-id="70f9a-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="70f9a-109">ARM veya klasik türünde olabilir.</span><span class="sxs-lookup"><span data-stu-id="70f9a-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="70f9a-110">Depolama hesabına oturum açtıysa, etkinlik günlüğünü depolama maliyeti normal standart depolama tarifeleriyle faturalanır.</span><span class="sxs-lookup"><span data-stu-id="70f9a-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="70f9a-111">Abonelik başına yalnızca bir günlük profili olabilir etkinlik günlüğü dışarı aktarmak için abonelik başına yalnızca bir depolama hesabı kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="70f9a-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="70f9a-112">**Olay Hub 'ı** -etkinlik günlüğünü dışarı aktarmak için abonelik başına yalnızca bir olay hub 'ı olabilir.</span><span class="sxs-lookup"><span data-stu-id="70f9a-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="70f9a-113">Etkinlik günlüğü bir olay hub 'ına akıtısa, standart Olay Hub fiyatlandırması uygulanır.</span><span class="sxs-lookup"><span data-stu-id="70f9a-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="70f9a-114">Etkinlik günlüğünde, olaylar bir bölgeye ait olabilir veya "Global" olabilir.</span><span class="sxs-lookup"><span data-stu-id="70f9a-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="70f9a-115">Genel aslýnda bu olaylarda, olayların gerçekten bu kategoriye giren çoğunluğunda bölge çoğunluğu ve bölgeden bağımsızdır.</span><span class="sxs-lookup"><span data-stu-id="70f9a-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="70f9a-116">Etkinlik günlüğü profili portaldan ayarlanmışsa, Kullanıcı arabiriminde seçili diğer bölgelerin yanına örtülü olarak "genel" ekler.</span><span class="sxs-lookup"><span data-stu-id="70f9a-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="70f9a-117">Cmdlet kullanıldığında, "Global" olarak konum, başka herhangi bir bölgeden ayrı olarak bahsedilmelidir.</span><span class="sxs-lookup"><span data-stu-id="70f9a-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="70f9a-118">**Not** :- **konumlarda "Global" ayarlanamayan Etkinlik günlüğünün büyük bir bölümünü dışarı aktarmaz.**</span><span class="sxs-lookup"><span data-stu-id="70f9a-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

<span data-ttu-id="70f9a-119">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="70f9a-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="70f9a-120">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="70f9a-120">EXAMPLES</span></span>

### <span data-ttu-id="70f9a-121">Örnek 1: konum koşulunu eşleştiren etkinlik günlüğünü bir depolama hesabıyla dışarı aktarmak için yeni bir günlük profili ekleme</span><span class="sxs-lookup"><span data-stu-id="70f9a-121">Example 1 : Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```
Add-AzureRmLogProfile -Locations "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="70f9a-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="70f9a-122">PARAMETERS</span></span>

### <span data-ttu-id="70f9a-123">-Kategori</span><span class="sxs-lookup"><span data-stu-id="70f9a-123">-Category</span></span>
<span data-ttu-id="70f9a-124">Kategorilerin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="70f9a-124">Specifies the list of categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: Categories

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f9a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70f9a-125">-DefaultProfile</span></span>
<span data-ttu-id="70f9a-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="70f9a-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70f9a-127">-Konum</span><span class="sxs-lookup"><span data-stu-id="70f9a-127">-Location</span></span>
<span data-ttu-id="70f9a-128">Günlük profilinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="70f9a-128">Specifies the location of the log profile.</span></span>
<span data-ttu-id="70f9a-129">Geçerli değerler: en son konum listesini almak için aşağıdaki cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="70f9a-129">Valid values: Run below cmdlet to get the latest list of locations.</span></span> 

<span data-ttu-id="70f9a-130">Get-AzureLocation | DisplayName 'i seçin</span><span class="sxs-lookup"><span data-stu-id="70f9a-130">Get-AzureLocation | Select DisplayName</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: Locations

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f9a-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="70f9a-131">-Name</span></span>
<span data-ttu-id="70f9a-132">Profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="70f9a-132">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f9a-133">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="70f9a-133">-RetentionInDays</span></span>
<span data-ttu-id="70f9a-134">Bekletme ilkesini gün olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="70f9a-134">Specifies the retention policy, in days.</span></span> <span data-ttu-id="70f9a-135">Bu, belirtilen depolama hesabında günlüklerin korunduğu gün sayısıdır.</span><span class="sxs-lookup"><span data-stu-id="70f9a-135">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="70f9a-136">Bu ayarı süresiz olarak **0** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="70f9a-136">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="70f9a-137">Belirtilmemişse, varsayılan olarak **0** değerini alır.</span><span class="sxs-lookup"><span data-stu-id="70f9a-137">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="70f9a-138">Veri bekletmesi için normal standart depolama veya Olay Hub faturalama ücretleri uygulanacaktır.</span><span class="sxs-lookup"><span data-stu-id="70f9a-138">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="70f9a-139">-Servicebusruleıd</span><span class="sxs-lookup"><span data-stu-id="70f9a-139">-ServiceBusRuleId</span></span>
<span data-ttu-id="70f9a-140">Hizmet veri yolu kuralının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="70f9a-140">Specifies the ID of the Service Bus rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f9a-141">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="70f9a-141">-StorageAccountId</span></span>
<span data-ttu-id="70f9a-142">Depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="70f9a-142">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="70f9a-143">KIMLIK, depolama hesabının tam kaynak KIMLIĞIDIR Örneğin,</span><span class="sxs-lookup"><span data-stu-id="70f9a-143">ID is the fully qualified Resource ID of the storage account for example</span></span>  

<span data-ttu-id="70f9a-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="70f9a-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f9a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f9a-145">CommonParameters</span></span>
<span data-ttu-id="70f9a-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="70f9a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f9a-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70f9a-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f9a-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="70f9a-148">INPUTS</span></span>

### <span data-ttu-id="70f9a-149">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="70f9a-149">None</span></span>
<span data-ttu-id="70f9a-150">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="70f9a-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="70f9a-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="70f9a-151">OUTPUTS</span></span>

### <span data-ttu-id="70f9a-152">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="70f9a-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="70f9a-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="70f9a-153">NOTES</span></span>

## <span data-ttu-id="70f9a-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="70f9a-154">RELATED LINKS</span></span>

[<span data-ttu-id="70f9a-155">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="70f9a-155">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)

[<span data-ttu-id="70f9a-156">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="70f9a-156">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


