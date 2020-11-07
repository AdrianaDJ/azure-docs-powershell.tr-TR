---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: b1fe6ae9085dcfc1d74eaf86af831a1e984a9143
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764974"
---
# <span data-ttu-id="a1f52-101">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="a1f52-101">Set-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="a1f52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1f52-102">SYNOPSIS</span></span>
<span data-ttu-id="a1f52-103">Bildirim Merkezi ad alanı için özellik değerlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a1f52-103">Sets property values for a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1f52-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1f52-104">SYNTAX</span></span>

```
Set-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1f52-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1f52-105">DESCRIPTION</span></span>
<span data-ttu-id="a1f52-106">**Set-AzureRmNotificationHubsNamespace** cmdlet 'i var olan bir Bildirim Hub ad alanının özellik değerlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a1f52-106">The **Set-AzureRmNotificationHubsNamespace** cmdlet sets the property values of an existing notification hub namespace.</span></span>

<span data-ttu-id="a1f52-107">Ad alanları, Bildirim Hub 'larınızı düzenlemenize ve yönetmenize yardımcı olan mantıksal kapsayıcılardır.</span><span class="sxs-lookup"><span data-stu-id="a1f52-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="a1f52-108">En az bir Bildirim Hub ad alanınız olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a1f52-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="a1f52-109">Ayrıca, tüm Bildirim Hub 'larının atanmış bir ad alanı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a1f52-109">Additionally, all notification hubs must have an assigned namespace.</span></span>

<span data-ttu-id="a1f52-110">Bu cmdlet öncelikle ad alanını etkinleştirmek ve devre dışı bırakmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a1f52-110">This cmdlet is primarily used to enable and disable a namespace.</span></span>
<span data-ttu-id="a1f52-111">Bir ad alanı devre dışı bırakıldığında, kullanıcılar ad alanındaki Bildirim Hub 'larına herhangi birine bağlanamaz ve bu hub 'ları kullanarak anında iletme bildirimleri gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="a1f52-111">When a namespace is disabled, users cannot connect to any of the notification hubs in the namespace, nor can administrators use those hubs to send push notifications.</span></span>
<span data-ttu-id="a1f52-112">Devre dışı bırakılmış bir ad alanını yeniden etkinleştirmek için, bu cmdlet 'i kullanarak ad uzayının **State** özelliğini etkin olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a1f52-112">To re-enable a disabled namespace, use this cmdlet to set the **State** property of the namespace to Active.</span></span>

<span data-ttu-id="a1f52-113">Bu cmdlet 'i, bir ad alanını kritik olarak etiketlemek için de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a1f52-113">You can also use this cmdlet to tag a namespace as critical.</span></span>
<span data-ttu-id="a1f52-114">Bu, ad alanının silinmesini engeller.</span><span class="sxs-lookup"><span data-stu-id="a1f52-114">This prevents the namespace from being deleted.</span></span>
<span data-ttu-id="a1f52-115">Kritik bir ad alanını kaldırmak için önce kritik etiketini kaldırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="a1f52-115">To remove a critical namespace you must first remove the Critical tag.</span></span>

## <span data-ttu-id="a1f52-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1f52-116">EXAMPLES</span></span>

### <span data-ttu-id="a1f52-117">Örnek 1: ad alanını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="a1f52-117">Example 1: Disable a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

<span data-ttu-id="a1f52-118">Bu komut, Batı ABD veri merkezinde bulunan ContosoPartners adındaki ve ContosoNotificationsGroup kaynak grubuna atanmış olan ad alanını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="a1f52-118">This command disables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="a1f52-119">Örnek 2: ad alanını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="a1f52-119">Example 2: Enable a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

<span data-ttu-id="a1f52-120">Bu komut, Batı ABD veri merkezinde bulunan ContosoPartners adlı ve ContosoNotificationsGroup kaynak grubuna atanmış olan ad alanını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="a1f52-120">This command enables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

## <span data-ttu-id="a1f52-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1f52-121">PARAMETERS</span></span>

### <span data-ttu-id="a1f52-122">-Kritik</span><span class="sxs-lookup"><span data-stu-id="a1f52-122">-Critical</span></span>
<span data-ttu-id="a1f52-123">Ad alanının kritik bir ad alanı olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a1f52-123">Indicates whether the namespace is a critical namespace.</span></span>
<span data-ttu-id="a1f52-124">Kritik ad alanları silinemez.</span><span class="sxs-lookup"><span data-stu-id="a1f52-124">Critical namespaces cannot be deleted.</span></span>
<span data-ttu-id="a1f52-125">Kritik bir ad alanını silmek için, bu özelliğin değerini false olarak ayarlamanız gerekir ve ad alanını kritik olmayan olarak işaretlemektir.</span><span class="sxs-lookup"><span data-stu-id="a1f52-125">To delete a critical namespace, you must set the value of this property to False in order to mark the namespace as non-critical.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1f52-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1f52-126">-DefaultProfile</span></span>
<span data-ttu-id="a1f52-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a1f52-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1f52-128">-Force</span><span class="sxs-lookup"><span data-stu-id="a1f52-128">-Force</span></span>
<span data-ttu-id="a1f52-129">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="a1f52-129">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f52-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="a1f52-130">-Location</span></span>
<span data-ttu-id="a1f52-131">Ad alanını barındıran veri merkezinin görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1f52-131">Specifies the display name of the datacenter that hosts the namespace.</span></span>
<span data-ttu-id="a1f52-132">Bu parametreyi geçerli bir Azure konumuna ayarlayabilirsiniz, ancak en iyi performans için kullanıcılarınızın çoğunluğunda bulunan bir veri merkezi kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="a1f52-132">Although you can set this parameter to any valid Azure location, for optimal performance you should use a datacenter located near the majority of your users.</span></span>

<span data-ttu-id="a1f52-133">Azure konumlarının güncel listesini almak için aşağıdaki komutu çalıştırırsınız:</span><span class="sxs-lookup"><span data-stu-id="a1f52-133">To get an up-to-date list of Azure locations run the following command:</span></span>

`Get-AzureLocation | Select-Object DisplayName`

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1f52-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a1f52-134">-Namespace</span></span>
<span data-ttu-id="a1f52-135">Bu cmdlet 'in değiştirdiği ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1f52-135">Specifies the namespace that this cmdlet modifies.</span></span>

<span data-ttu-id="a1f52-136">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="a1f52-136">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1f52-137">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a1f52-137">-ResourceGroup</span></span>
<span data-ttu-id="a1f52-138">Ad alanının atandığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1f52-138">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="a1f52-139">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="a1f52-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="a1f52-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="a1f52-140">-SkuTier</span></span>
<span data-ttu-id="a1f52-141">Ad alanının SKU katmanı</span><span class="sxs-lookup"><span data-stu-id="a1f52-141">Sku tier of the namespace</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1f52-142">Durumlu</span><span class="sxs-lookup"><span data-stu-id="a1f52-142">-State</span></span>
<span data-ttu-id="a1f52-143">Ad alanının geçerli durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1f52-143">Specifies the current state of the namespace.</span></span>
<span data-ttu-id="a1f52-144">Bu parametre için kabul edilebilir değerler şunlardır: etkin ve devre dışı.</span><span class="sxs-lookup"><span data-stu-id="a1f52-144">The acceptable values for this parameter are: Active and Disabled.</span></span>

```yaml
Type: NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1f52-145">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a1f52-145">-Tag</span></span>
<span data-ttu-id="a1f52-146">Azure öğelerini kategorilere ayırmak ve düzenlemek için kullanılabilecek ad değeri çiftlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1f52-146">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="a1f52-147">Etiketler, anahtar sözcüklere benzer ve bir dağıtımda çalışır.</span><span class="sxs-lookup"><span data-stu-id="a1f52-147">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="a1f52-148">Örneğin, etiket departmanı olan tüm öğeleri arıyorsanız, öğe türü, konum veya kaynak grubu gibi öğelere bakılmaksızın, arama bu etikete sahip tüm Azure öğelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a1f52-148">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>

<span data-ttu-id="a1f52-149">Tek bir etiket iki bölümden oluşur: *ad* ve (isteğe bağlı olarak) *değer*.</span><span class="sxs-lookup"><span data-stu-id="a1f52-149">An individual tag consists of two parts: the *Name* and (optionally) the *Value*.</span></span>
<span data-ttu-id="a1f52-150">Örneğin, departmandaki bölüm, etiket adı bölümdedir ve etiket değeri olur.</span><span class="sxs-lookup"><span data-stu-id="a1f52-150">For example, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="a1f52-151">Etiket eklemek için, CalendarYear: 2016 etiketini oluşturan buna benzer karma tablo söz dizimini kullanın:</span><span class="sxs-lookup"><span data-stu-id="a1f52-151">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016:</span></span>

<span data-ttu-id="a1f52-152">-Etiketler @ {Name = "Takvimyılı"; Value = "2016"}</span><span class="sxs-lookup"><span data-stu-id="a1f52-152">-Tags @{Name="CalendarYear";Value="2016"}</span></span>

<span data-ttu-id="a1f52-153">Aynı komutta birden çok etiket eklemek için, etiketleri virgülle ayırın:</span><span class="sxs-lookup"><span data-stu-id="a1f52-153">To add multiple tags in the same command, separate the individual tags by using commas:</span></span>

<span data-ttu-id="a1f52-154">-Tag @ {Name = "Takvimyılı"; Value = "2016"}, @ {Name = "Fcalyear"; Value = "2017"}</span><span class="sxs-lookup"><span data-stu-id="a1f52-154">-Tag @{Name="CalendarYear";Value="2016"}, @{Name="FiscalYear";Value="2017"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1f52-155">-Onay</span><span class="sxs-lookup"><span data-stu-id="a1f52-155">-Confirm</span></span>
<span data-ttu-id="a1f52-156">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a1f52-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1f52-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1f52-157">-WhatIf</span></span>
<span data-ttu-id="a1f52-158">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a1f52-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1f52-159">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a1f52-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1f52-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1f52-160">CommonParameters</span></span>
<span data-ttu-id="a1f52-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1f52-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1f52-162">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1f52-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1f52-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1f52-163">INPUTS</span></span>

### <span data-ttu-id="a1f52-164">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a1f52-164">None</span></span>
<span data-ttu-id="a1f52-165">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="a1f52-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a1f52-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1f52-166">OUTPUTS</span></span>

### <span data-ttu-id="a1f52-167">Microsoft. Azure. Commands. Notificationhub. modeller. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a1f52-167">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="a1f52-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1f52-168">NOTES</span></span>

## <span data-ttu-id="a1f52-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1f52-169">RELATED LINKS</span></span>

[<span data-ttu-id="a1f52-170">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="a1f52-170">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="a1f52-171">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="a1f52-171">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="a1f52-172">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="a1f52-172">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)


