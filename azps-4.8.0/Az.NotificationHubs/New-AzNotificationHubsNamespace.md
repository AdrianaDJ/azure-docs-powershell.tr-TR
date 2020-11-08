---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 24a42fba23427f437cb064e1915c19e36e7a71bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274751"
---
# <span data-ttu-id="732ca-101">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="732ca-101">New-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="732ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="732ca-102">SYNOPSIS</span></span>
<span data-ttu-id="732ca-103">Bildirim Merkezi ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="732ca-103">Creates a notification hub namespace.</span></span>

## <span data-ttu-id="732ca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="732ca-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="732ca-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="732ca-105">DESCRIPTION</span></span>
<span data-ttu-id="732ca-106">**New-AzNotificationHubsNamespace** cmdlet 'i bir bildirim merkezi ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="732ca-106">The **New-AzNotificationHubsNamespace** cmdlet creates a notification hub namespace.</span></span>
<span data-ttu-id="732ca-107">Ad alanları, Bildirim Hub 'larınızı düzenlemenize ve yönetmenize yardımcı olan mantıksal kapsayıcılardır.</span><span class="sxs-lookup"><span data-stu-id="732ca-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="732ca-108">En az bir Bildirim Hub ad alanınız olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="732ca-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="732ca-109">Tek bir ad alanı birden çok hub 'ı oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="732ca-109">A single namespace can house multiple hubs.</span></span>
<span data-ttu-id="732ca-110">Hub 'larınızı düzenlemek veya belirli kişilere, hub 'larınızın seçili alt kümesini yönetme izni vermek için birden fazla ad alanınız olabilir.</span><span class="sxs-lookup"><span data-stu-id="732ca-110">You can have multiple namespaces to organize your hubs, or to give specific individuals permission to manage a selected subset of your hubs.</span></span>
<span data-ttu-id="732ca-111">Ad alanı oluşturmak için, ad alanı için benzersiz bir ad belirttiğinizden emin olun; ad alanının yerleştirileceği veri merkezi 'ni belirtin; ve ad alanının atanacağı kaynak grubunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="732ca-111">To create a namespace, make sure that you specify a unique name for the namespace; specify the datacenter where the namespace will be located; and, specify the resource group that the namespace will be assigned to.</span></span>
<span data-ttu-id="732ca-112">Ad alanı oluşturulduktan sonra, bu ad alanına yetkilendirme kuralları atamak için New-AzNotificationHubsNamespaceAuthorizationRules cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="732ca-112">After the namespace has been created you can use the New-AzNotificationHubsNamespaceAuthorizationRules cmdlet to assign authorization rules to that namespace.</span></span>
<span data-ttu-id="732ca-113">Kimlik alanı izinlerini yönetmek için yetkilendirme kuralları kullanılır.</span><span class="sxs-lookup"><span data-stu-id="732ca-113">Authorization rules are used to manage permissions to the namespace.</span></span>

## <span data-ttu-id="732ca-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="732ca-114">EXAMPLES</span></span>

### <span data-ttu-id="732ca-115">Örnek 1: bildirim merkezi oluşturma</span><span class="sxs-lookup"><span data-stu-id="732ca-115">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

<span data-ttu-id="732ca-116">Bu komut, ContosoPartners adlı bir bildirim merkezi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="732ca-116">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="732ca-117">Ad alanı Batı ABD veri merkezinde yer alır ve ContosoNotificationsGroup kaynak grubuna atanır.</span><span class="sxs-lookup"><span data-stu-id="732ca-117">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="732ca-118">Örnek 2: etiketlerle bildirim merkezi oluşturma</span><span class="sxs-lookup"><span data-stu-id="732ca-118">Example 2: Create a notification hub with tags</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

<span data-ttu-id="732ca-119">Bu komut, ContosoPartners adlı bir bildirim merkezi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="732ca-119">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="732ca-120">Ad alanı Batı ABD veri merkezinde yer alır ve ContosoNotificationsGroup kaynak grubuna atanır.</span><span class="sxs-lookup"><span data-stu-id="732ca-120">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="732ca-121">Buna ek olarak, bu komut ad Izleyicisine sahip bir etiket oluşturur ve bu da isim uzayına atanır.</span><span class="sxs-lookup"><span data-stu-id="732ca-121">In addition, this command creates a tag with the name Audience and the value PartnerOrganizations and is assigned to the namespace.</span></span>
<span data-ttu-id="732ca-122">Bu, hedef kitle etiketinin Partnerkuruluşları olarak ayarlandığı öğeleri filtrelediğinizde, ad alanının gösterilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="732ca-122">This ensures that the namespace will be displayed any time you filter for items where the Audience tag is set to PartnerOrganizations.</span></span>

## <span data-ttu-id="732ca-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="732ca-123">PARAMETERS</span></span>

### <span data-ttu-id="732ca-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="732ca-124">-DefaultProfile</span></span>
<span data-ttu-id="732ca-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="732ca-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="732ca-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="732ca-126">-Location</span></span>
<span data-ttu-id="732ca-127">Ad alanını barındıracak veri merkezinin görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="732ca-127">Specifies the display name of the datacenter that will host the Namespace.</span></span>
<span data-ttu-id="732ca-128">Bu parametreyi geçerli bir konuma ayarlayabilirsiniz, ancak en iyi performans için kullanıcılarınızın çoğunluğunda bulunan bir veri merkezi 'ni kullanmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="732ca-128">Although you can set this parameter to any valid location, for optimal performance you might want to use a datacenter located near the majority of your users.</span></span>

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

### <span data-ttu-id="732ca-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="732ca-129">-Namespace</span></span>
<span data-ttu-id="732ca-130">Yeni ad alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="732ca-130">Specifies the name of the new namespace.</span></span>
<span data-ttu-id="732ca-131">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="732ca-131">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="732ca-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="732ca-132">-ResourceGroup</span></span>
<span data-ttu-id="732ca-133">Ad alanının atanacağı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="732ca-133">Specifies the resource group to which the namespace will be assigned.</span></span>
<span data-ttu-id="732ca-134">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri, yalnızca envanter yönetimi ve yönetimle ilgili yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="732ca-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and administration.</span></span>

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

### <span data-ttu-id="732ca-135">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="732ca-135">-SkuTier</span></span>
<span data-ttu-id="732ca-136">Ad alanının SKU katmanı</span><span class="sxs-lookup"><span data-stu-id="732ca-136">Sku tier of the namespace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="732ca-137">Etiketli</span><span class="sxs-lookup"><span data-stu-id="732ca-137">-Tag</span></span>
<span data-ttu-id="732ca-138">Azure öğelerini kategorilere ayırmak ve düzenlemek için kullanılabilecek ad değeri çiftlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="732ca-138">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="732ca-139">Etiketler, anahtar sözcüklere benzer ve bir dağıtımda çalışır.</span><span class="sxs-lookup"><span data-stu-id="732ca-139">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="732ca-140">Örneğin, etiket departmanı olan tüm öğeleri arıyorsanız, öğe türü, konum veya kaynak grubu gibi öğelere bakılmaksızın, arama bu etikete sahip tüm Azure öğelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="732ca-140">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="732ca-141">Tek bir etiket iki bölümden oluşur: *ad* ve isteğe bağlı olarak *değer*.</span><span class="sxs-lookup"><span data-stu-id="732ca-141">An individual tag consists of two parts: the *Name* and, optionally, the *Value*.</span></span>
<span data-ttu-id="732ca-142">Örneğin, departmandaki bölüm, etiket adı bölümdedir ve etiket değeri olur.</span><span class="sxs-lookup"><span data-stu-id="732ca-142">For instance, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="732ca-143">Etiket eklemek için, CalendarYear: 2016 etiketini oluşturan buna benzer karma tablo söz dizimini kullanın:</span><span class="sxs-lookup"><span data-stu-id="732ca-143">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016:</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="732ca-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="732ca-144">-Confirm</span></span>
<span data-ttu-id="732ca-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="732ca-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="732ca-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="732ca-146">-WhatIf</span></span>
<span data-ttu-id="732ca-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="732ca-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="732ca-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="732ca-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="732ca-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="732ca-149">CommonParameters</span></span>
<span data-ttu-id="732ca-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="732ca-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="732ca-151">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="732ca-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="732ca-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="732ca-152">INPUTS</span></span>

### <span data-ttu-id="732ca-153">System. String</span><span class="sxs-lookup"><span data-stu-id="732ca-153">System.String</span></span>

### <span data-ttu-id="732ca-154">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="732ca-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="732ca-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="732ca-155">OUTPUTS</span></span>

### <span data-ttu-id="732ca-156">Microsoft. Azure. Commands. Notificationhub. modeller. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="732ca-156">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="732ca-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="732ca-157">NOTES</span></span>

## <span data-ttu-id="732ca-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="732ca-158">RELATED LINKS</span></span>

[<span data-ttu-id="732ca-159">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="732ca-159">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="732ca-160">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="732ca-160">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="732ca-161">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="732ca-161">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


