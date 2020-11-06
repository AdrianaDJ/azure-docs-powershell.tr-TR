---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
ms.openlocfilehash: 40efc9e6afbb4f1424fcbcfe70e3376eb9ab5a23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594676"
---
# <span data-ttu-id="7b4ee-101">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="7b4ee-101">Add-AzureRmLogProfile</span></span>

## <span data-ttu-id="7b4ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b4ee-102">SYNOPSIS</span></span>
<span data-ttu-id="7b4ee-103">Yeni etkinlik günlüğü profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-103">Creates a new activity log profile.</span></span> <span data-ttu-id="7b4ee-104">Bu profil, etkinlik günlüğünü bir Azure depolama hesabına arşivlemek veya aynı abonelikteki bir Azure Olay Hub 'ına aktarmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

- <span data-ttu-id="7b4ee-105">**Depolama hesabı** -yalnızca standart depolama hesabı (Premium depolama hesabı desteklenmiyor) desteklenir.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-105">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="7b4ee-106">ARM veya klasik türünde olabilir.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-106">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="7b4ee-107">Depolama hesabına oturum açtıysa, etkinlik günlüğünü depolama maliyeti normal standart depolama tarifeleriyle faturalanır.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-107">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="7b4ee-108">Abonelik başına yalnızca bir günlük profili olabilir etkinlik günlüğü dışarı aktarmak için abonelik başına yalnızca bir depolama hesabı kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-108">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="7b4ee-109">**Olay Hub 'ı** -etkinlik günlüğünü dışarı aktarmak için abonelik başına yalnızca bir olay hub 'ı olabilir.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-109">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="7b4ee-110">Etkinlik günlüğü bir olay hub 'ına akıtısa, standart Olay Hub fiyatlandırması uygulanır.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-110">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="7b4ee-111">Etkinlik günlüğünde, olaylar bir bölgeye ait olabilir veya "Global" olabilir.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-111">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="7b4ee-112">Genel aslýnda bu olaylarda, olayların gerçekten bu kategoriye giren çoğunluğunda bölge çoğunluğu ve bölgeden bağımsızdır.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-112">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="7b4ee-113">Etkinlik günlüğü profili portaldan ayarlanmışsa, Kullanıcı arabiriminde seçili diğer bölgelerin yanına örtülü olarak "genel" ekler.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-113">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="7b4ee-114">Cmdlet kullanıldığında, "Global" olarak konum, başka herhangi bir bölgeden ayrı olarak bahsedilmelidir.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-114">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="7b4ee-115">**Not** :- **konumlarda "Global" ayarlanamayan Etkinlik günlüğünün büyük bir bölümünü dışarı aktarmaz.**</span><span class="sxs-lookup"><span data-stu-id="7b4ee-115">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b4ee-116">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7b4ee-116">SYNTAX</span></span>

```
Add-AzureRmLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Locations <System.Collections.Generic.List`1[System.String]>
 [-Categories <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b4ee-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="7b4ee-117">DESCRIPTION</span></span>
<span data-ttu-id="7b4ee-118">**Add-AzureRmLogProfile** cmdlet 'i bir günlük profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-118">The **Add-AzureRmLogProfile** cmdlet creates a log profile.</span></span>

## <span data-ttu-id="7b4ee-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7b4ee-119">EXAMPLES</span></span>

### <span data-ttu-id="7b4ee-120">Örnek 1: konum koşulunu eşleştiren etkinlik günlüğünü bir depolama hesabıyla dışarı aktarmak için yeni bir günlük profili ekleme</span><span class="sxs-lookup"><span data-stu-id="7b4ee-120">Example 1 : Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```
Add-AzureRmLogProfile -Locations "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="7b4ee-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7b4ee-121">PARAMETERS</span></span>

### <span data-ttu-id="7b4ee-122">-Kategoriler</span><span class="sxs-lookup"><span data-stu-id="7b4ee-122">-Categories</span></span>
<span data-ttu-id="7b4ee-123">Kategorilerin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-123">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="7b4ee-124">-Konumlar</span><span class="sxs-lookup"><span data-stu-id="7b4ee-124">-Locations</span></span>
<span data-ttu-id="7b4ee-125">Günlük profilinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-125">Specifies the location of the log profile.</span></span>
<span data-ttu-id="7b4ee-126">Geçerli değerler: en son konum listesini almak için aşağıdaki cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-126">Valid values: Run below cmdlet to get the latest list of locations.</span></span> 

<span data-ttu-id="7b4ee-127">Get-AzureLocation | DisplayName 'i seçin</span><span class="sxs-lookup"><span data-stu-id="7b4ee-127">Get-AzureLocation | Select DisplayName</span></span>

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

### <span data-ttu-id="7b4ee-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="7b4ee-128">-Name</span></span>
<span data-ttu-id="7b4ee-129">Profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-129">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="7b4ee-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7b4ee-130">-RetentionInDays</span></span>
<span data-ttu-id="7b4ee-131">Bekletme ilkesini gün olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-131">Specifies the retention policy, in days.</span></span> <span data-ttu-id="7b4ee-132">Bu, belirtilen depolama hesabında günlüklerin korunduğu gün sayısıdır.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-132">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="7b4ee-133">Bu ayarı süresiz olarak **0** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-133">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="7b4ee-134">Belirtilmemişse, varsayılan olarak **0** değerini alır.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-134">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="7b4ee-135">Veri bekletmesi için normal standart depolama veya Olay Hub faturalama ücretleri uygulanacaktır.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-135">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="7b4ee-136">-Servicebusruleıd</span><span class="sxs-lookup"><span data-stu-id="7b4ee-136">-ServiceBusRuleId</span></span>
<span data-ttu-id="7b4ee-137">Hizmet veri yolu kuralının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-137">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="7b4ee-138">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="7b4ee-138">-StorageAccountId</span></span>
<span data-ttu-id="7b4ee-139">Depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-139">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="7b4ee-140">KIMLIK, depolama hesabının tam kaynak KIMLIĞIDIR Örneğin,</span><span class="sxs-lookup"><span data-stu-id="7b4ee-140">ID is the fully qualified Resource ID of the storage account for example</span></span>  

<span data-ttu-id="7b4ee-141">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="7b4ee-141">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="7b4ee-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b4ee-142">-DefaultProfile</span></span>
<span data-ttu-id="7b4ee-143">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b4ee-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b4ee-144">CommonParameters</span></span>
<span data-ttu-id="7b4ee-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7b4ee-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b4ee-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b4ee-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b4ee-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7b4ee-147">INPUTS</span></span>

## <span data-ttu-id="7b4ee-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7b4ee-148">OUTPUTS</span></span>

### <span data-ttu-id="7b4ee-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="7b4ee-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="7b4ee-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7b4ee-150">NOTES</span></span>

## <span data-ttu-id="7b4ee-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7b4ee-151">RELATED LINKS</span></span>

[<span data-ttu-id="7b4ee-152">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="7b4ee-152">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)

[<span data-ttu-id="7b4ee-153">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="7b4ee-153">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


