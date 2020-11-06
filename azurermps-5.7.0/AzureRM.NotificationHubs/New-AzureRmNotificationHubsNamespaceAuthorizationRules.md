---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: 2530d4b0075856b6a172bdcf104474d320f657bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592927"
---
# <span data-ttu-id="ffb03-101">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="ffb03-101">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="ffb03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffb03-102">SYNOPSIS</span></span>
<span data-ttu-id="ffb03-103">Yetkilendirme kuralı oluşturur ve bu kuralı bir Bildirim Hub ad alanına atar.</span><span class="sxs-lookup"><span data-stu-id="ffb03-103">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffb03-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ffb03-104">SYNTAX</span></span>

### <span data-ttu-id="ffb03-105">Inputfileparameterset</span><span class="sxs-lookup"><span data-stu-id="ffb03-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffb03-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffb03-106">SASRuleParameterSet</span></span>
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffb03-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ffb03-107">DESCRIPTION</span></span>
<span data-ttu-id="ffb03-108">**Yeni-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet 'ı paylaşılan erişim IMZASı (SAS) yetkilendirme kuralı oluşturur ve bunu bir Bildirim Hub alanına atar.</span><span class="sxs-lookup"><span data-stu-id="ffb03-108">The **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet creates a Shared Access Signature (SAS) authorization rule and assigns it to a notification hub namespace.</span></span>
<span data-ttu-id="ffb03-109">Yetkilendirme kuralları ad alanındaki Kullanıcı haklarını ve bu ad alanıyla birlikte gelen bildirim hubları yönetir.</span><span class="sxs-lookup"><span data-stu-id="ffb03-109">Authorization rules manage user rights to the namespace and to the notification hubs contained with that namespace.</span></span>

<span data-ttu-id="ffb03-110">Bu cmdlet, yeni yetkilendirme kuralı oluşturmak ve bunu bir ad alanına atamak için iki yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="ffb03-110">This cmdlet provides two ways to create a new authorization rule and assign it to a namespace.</span></span>
<span data-ttu-id="ffb03-111">**Sharedaccessauthorizationruleattributes** nesnesinin bir örneğini oluşturabilir ve bu nesneyi yeni kuralın sahip olmasını istediğiniz özellik değerleriyle yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ffb03-111">You can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the new rule to possess.</span></span>
<span data-ttu-id="ffb03-112">Bu, .NET Framework kullanılarak yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="ffb03-112">This can be done using .NET Framework.</span></span>
<span data-ttu-id="ffb03-113">Bu özellik değerlerini, *sasrule* parametresini kullanarak yeni kuralınıza kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ffb03-113">You can then copy those property values to your new rule by using *SASRule* parameter.</span></span>

<span data-ttu-id="ffb03-114">Alternatif olarak, ilgili yapılandırma değerlerini içeren bir JSON (JavaScript nesnesi Gösterim) dosyası oluşturabilir ve bu değerleri, *GirdiDosyası* parametresini kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ffb03-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="ffb03-115">JSON dosyası, aşağıdakine benzer sözdizimi kullanan bir metin dosyasıdır:</span><span class="sxs-lookup"><span data-stu-id="ffb03-115">A JSON file is a text file that uses syntax similar to the following:</span></span>

<span data-ttu-id="ffb03-116">{</span><span class="sxs-lookup"><span data-stu-id="ffb03-116">{</span></span>  
    <span data-ttu-id="ffb03-117">"Ad": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="ffb03-117">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="ffb03-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",</span><span class="sxs-lookup"><span data-stu-id="ffb03-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="ffb03-119">"Haklar": \[</span><span class="sxs-lookup"><span data-stu-id="ffb03-119">"Rights": \[</span></span>  
        <span data-ttu-id="ffb03-120">"Dinle",</span><span class="sxs-lookup"><span data-stu-id="ffb03-120">"Listen",</span></span>  
        <span data-ttu-id="ffb03-121">Göndermek</span><span class="sxs-lookup"><span data-stu-id="ffb03-121">"Send"</span></span>  
    \]  
<span data-ttu-id="ffb03-122">}</span><span class="sxs-lookup"><span data-stu-id="ffb03-122">}</span></span>

<span data-ttu-id="ffb03-123">**New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet 'i ile birlikte kullanıldığında, önceki JSON örneği, kullanıcılara ad boşluğuna izin veren, contosoauthorizationrule adlı bir yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ffb03-123">When used in conjunction with the **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet, the preceding JSON sample creates an authorization rule named ContosoAuthorizationRule that gives users Listen and Send rights to the namespace.</span></span>
<span data-ttu-id="ffb03-124">Kimlik doğrulaması için kullanılan *PrimaryKey* , aşağıdaki Windows PowerShell komutu kullanılarak rasgele oluşturulabilir:</span><span class="sxs-lookup"><span data-stu-id="ffb03-124">The *PrimaryKey* that is used for authentication, can be randomly generated by using the following Windows PowerShell command:</span></span>

<span data-ttu-id="ffb03-125">\[Convert \] :: ToBase64String ((1.. 32 |% { \[ Byte/] (Get-Random-minimum 0-Maximum 255)))</span><span class="sxs-lookup"><span data-stu-id="ffb03-125">\[Convert\]::ToBase64String((1..32 |% { \[byte/](Get-Random -Minimum 0 -Maximum 255) }))</span></span>

## <span data-ttu-id="ffb03-126">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ffb03-126">EXAMPLES</span></span>

### <span data-ttu-id="ffb03-127">Örnek 1: yetkilendirme kuralı oluşturma ve bunu bir ad alanına atama</span><span class="sxs-lookup"><span data-stu-id="ffb03-127">Example 1: Create an authorization rule and assign it to a namespace</span></span>
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

<span data-ttu-id="ffb03-128">Bu komut, bir yetkilendirme kuralı oluşturur ve bu kuralı ContosoNamespace ad alanına atar.</span><span class="sxs-lookup"><span data-stu-id="ffb03-128">This command creates an authorization rule and assigns that rule to the namespace ContosoNamespace.</span></span>
<span data-ttu-id="ffb03-129">Bu kuralı oluştururken, uygun ad alanını ve ad alanının atandığı kaynak grubunu belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ffb03-129">When creating this rule you must specify the appropriate namespace and the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="ffb03-130">Bununla birlikte, kuralın kendisiyle ilgili herhangi bir bilgi belirtmeniz gerekmez: kural bilgileri C:\Configuration\NamespaceAuthorizationRules.jsgiriş dosyasından alınır.</span><span class="sxs-lookup"><span data-stu-id="ffb03-130">However, you do not need to specify any information about the rule itself: rule information will be taken from the input file C:\Configuration\NamespaceAuthorizationRules.json.</span></span>

## <span data-ttu-id="ffb03-131">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ffb03-131">PARAMETERS</span></span>

### <span data-ttu-id="ffb03-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffb03-132">-DefaultProfile</span></span>
<span data-ttu-id="ffb03-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ffb03-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ffb03-134">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="ffb03-134">-InputFile</span></span>
<span data-ttu-id="ffb03-135">Yeni yetkilendirme kuralı için yapılandırma bilgilerini içeren bir JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ffb03-135">Specifies the path to a JSON file containing configuration information for the new authorization rule.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffb03-136">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ffb03-136">-Namespace</span></span>
<span data-ttu-id="ffb03-137">Yetkilendirme kurallarının atanacağı ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ffb03-137">Specifies the namespace to which the authorization rules will be assigned.</span></span>

<span data-ttu-id="ffb03-138">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="ffb03-138">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="ffb03-139">Yeni kuralların varolan bir ad alanına atanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ffb03-139">The new rules must be assigned to an existing namespace.</span></span>
<span data-ttu-id="ffb03-140">**Yeni-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet 'i yeni bir ad alanı oluşturamaz.</span><span class="sxs-lookup"><span data-stu-id="ffb03-140">The **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="ffb03-141">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ffb03-141">-ResourceGroup</span></span>
<span data-ttu-id="ffb03-142">Ad alanının atandığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ffb03-142">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="ffb03-143">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="ffb03-143">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

<span data-ttu-id="ffb03-144">Var olan bir kaynak grubunu kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="ffb03-144">You must use an existing resource group.</span></span>
<span data-ttu-id="ffb03-145">Bu cmdlet yeni bir kaynak grubu oluşturamıyor.</span><span class="sxs-lookup"><span data-stu-id="ffb03-145">This cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="ffb03-146">-SASRule</span><span class="sxs-lookup"><span data-stu-id="ffb03-146">-SASRule</span></span>
<span data-ttu-id="ffb03-147">Yeni kuralların yapılandırma bilgilerini içeren **Sharedaccessauthorizationruleattributes** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ffb03-147">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffb03-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="ffb03-148">-Confirm</span></span>
<span data-ttu-id="ffb03-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ffb03-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffb03-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffb03-150">-WhatIf</span></span>
<span data-ttu-id="ffb03-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ffb03-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ffb03-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ffb03-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffb03-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffb03-153">CommonParameters</span></span>
<span data-ttu-id="ffb03-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ffb03-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffb03-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffb03-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffb03-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ffb03-156">INPUTS</span></span>

### <span data-ttu-id="ffb03-157">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ffb03-157">None</span></span>
<span data-ttu-id="ffb03-158">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="ffb03-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ffb03-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ffb03-159">OUTPUTS</span></span>

### <span data-ttu-id="ffb03-160">Microsoft. Azure. Commands. Notificationhub. modeller. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ffb03-160">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="ffb03-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ffb03-161">NOTES</span></span>

## <span data-ttu-id="ffb03-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ffb03-162">RELATED LINKS</span></span>

[<span data-ttu-id="ffb03-163">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="ffb03-163">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="ffb03-164">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="ffb03-164">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="ffb03-165">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="ffb03-165">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


