---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: eaf34373cb17fea94c498e16f623cef4bf65e937
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274749"
---
# <span data-ttu-id="5e68c-101">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5e68c-101">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="5e68c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e68c-102">SYNOPSIS</span></span>
<span data-ttu-id="5e68c-103">Yetkilendirme kuralı oluşturur ve bu kuralı bir Bildirim Hub ad alanına atar.</span><span class="sxs-lookup"><span data-stu-id="5e68c-103">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

## <span data-ttu-id="5e68c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e68c-104">SYNTAX</span></span>

### <span data-ttu-id="5e68c-105">Inputfileparameterset</span><span class="sxs-lookup"><span data-stu-id="5e68c-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e68c-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e68c-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e68c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e68c-107">DESCRIPTION</span></span>
<span data-ttu-id="5e68c-108">**New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet 'ı paylaşılan erişim IMZASı (SAS) yetkilendirme kuralı oluşturur ve bunu bir Bildirim Hub alanına atar.</span><span class="sxs-lookup"><span data-stu-id="5e68c-108">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet creates a Shared Access Signature (SAS) authorization rule and assigns it to a notification hub namespace.</span></span>
<span data-ttu-id="5e68c-109">Yetkilendirme kuralları ad alanındaki Kullanıcı haklarını ve bu ad alanıyla birlikte gelen bildirim hubları yönetir.</span><span class="sxs-lookup"><span data-stu-id="5e68c-109">Authorization rules manage user rights to the namespace and to the notification hubs contained with that namespace.</span></span>
<span data-ttu-id="5e68c-110">Bu cmdlet, yeni yetkilendirme kuralı oluşturmak ve bunu bir ad alanına atamak için iki yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="5e68c-110">This cmdlet provides two ways to create a new authorization rule and assign it to a namespace.</span></span>
<span data-ttu-id="5e68c-111">**Sharedaccessauthorizationruleattributes** nesnesinin bir örneğini oluşturabilir ve bu nesneyi yeni kuralın sahip olmasını istediğiniz özellik değerleriyle yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5e68c-111">You can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the new rule to possess.</span></span>
<span data-ttu-id="5e68c-112">Bu, .NET Framework kullanılarak yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="5e68c-112">This can be done using .NET Framework.</span></span>
<span data-ttu-id="5e68c-113">Bu özellik değerlerini, *sasrule* parametresini kullanarak yeni kuralınıza kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5e68c-113">You can then copy those property values to your new rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="5e68c-114">Alternatif olarak, ilgili yapılandırma değerlerini içeren bir JSON (JavaScript nesnesi Gösterim) dosyası oluşturabilir ve bu değerleri, *GirdiDosyası* parametresini kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5e68c-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="5e68c-115">JSON dosyası, aşağıdakine benzer sözdizimi kullanan bir metin dosyasıdır: {</span><span class="sxs-lookup"><span data-stu-id="5e68c-115">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="5e68c-116">"Ad": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="5e68c-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="5e68c-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",</span><span class="sxs-lookup"><span data-stu-id="5e68c-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="5e68c-118">"Haklar": \[</span><span class="sxs-lookup"><span data-stu-id="5e68c-118">"Rights": \[</span></span>  
        <span data-ttu-id="5e68c-119">"Dinle",</span><span class="sxs-lookup"><span data-stu-id="5e68c-119">"Listen",</span></span>  
        <span data-ttu-id="5e68c-120">Göndermek</span><span class="sxs-lookup"><span data-stu-id="5e68c-120">"Send"</span></span>  
    \]  
<span data-ttu-id="5e68c-121">} **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet 'i ile birlikte kullanıldığında, önceki JSON örneği, kullanıcılara ad boşluğuna izin veren, contosoauthorizationrule adlı bir yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5e68c-121">} When used in conjunction with the **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample creates an authorization rule named ContosoAuthorizationRule that gives users Listen and Send rights to the namespace.</span></span>
<span data-ttu-id="5e68c-122">Kimlik doğrulaması için kullanılan *PrimaryKey* , aşağıdaki Windows PowerShell komutu kullanılarak rasgele oluşturulabilir: \[ Convert \] :: ToBase64String ((1.. 32 |% { \[ Byte/] (Get-Random-en çok 255)}))</span><span class="sxs-lookup"><span data-stu-id="5e68c-122">The *PrimaryKey* that is used for authentication, can be randomly generated by using the following Windows PowerShell command: \[Convert\]::ToBase64String((1..32 |% { \[byte/](Get-Random -Minimum 0 -Maximum 255) }))</span></span>

## <span data-ttu-id="5e68c-123">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e68c-123">EXAMPLES</span></span>

### <span data-ttu-id="5e68c-124">Örnek 1: yetkilendirme kuralı oluşturma ve bunu bir ad alanına atama</span><span class="sxs-lookup"><span data-stu-id="5e68c-124">Example 1: Create an authorization rule and assign it to a namespace</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

<span data-ttu-id="5e68c-125">Bu komut, bir yetkilendirme kuralı oluşturur ve bu kuralı ContosoNamespace ad alanına atar.</span><span class="sxs-lookup"><span data-stu-id="5e68c-125">This command creates an authorization rule and assigns that rule to the namespace ContosoNamespace.</span></span>
<span data-ttu-id="5e68c-126">Bu kuralı oluştururken, uygun ad alanını ve ad alanının atandığı kaynak grubunu belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="5e68c-126">When creating this rule you must specify the appropriate namespace and the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="5e68c-127">Bununla birlikte, kuralın kendisiyle ilgili herhangi bir bilgi belirtmeniz gerekmez: kural bilgileri C:\Configuration\NamespaceAuthorizationRules.jsgiriş dosyasından alınır.</span><span class="sxs-lookup"><span data-stu-id="5e68c-127">However, you do not need to specify any information about the rule itself: rule information will be taken from the input file C:\Configuration\NamespaceAuthorizationRules.json.</span></span>

## <span data-ttu-id="5e68c-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e68c-128">PARAMETERS</span></span>

### <span data-ttu-id="5e68c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e68c-129">-DefaultProfile</span></span>
<span data-ttu-id="5e68c-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5e68c-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e68c-131">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="5e68c-131">-InputFile</span></span>
<span data-ttu-id="5e68c-132">Yeni yetkilendirme kuralı için yapılandırma bilgilerini içeren bir JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e68c-132">Specifies the path to a JSON file containing configuration information for the new authorization rule.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e68c-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5e68c-133">-Namespace</span></span>
<span data-ttu-id="5e68c-134">Yetkilendirme kurallarının atanacağı ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e68c-134">Specifies the namespace to which the authorization rules will be assigned.</span></span>
<span data-ttu-id="5e68c-135">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="5e68c-135">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="5e68c-136">Yeni kuralların varolan bir ad alanına atanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="5e68c-136">The new rules must be assigned to an existing namespace.</span></span>
<span data-ttu-id="5e68c-137">**Yeni-AzNotificationHubsNamespaceAuthorizationRule** cmdlet 'i yeni bir ad alanı oluşturamaz.</span><span class="sxs-lookup"><span data-stu-id="5e68c-137">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="5e68c-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5e68c-138">-ResourceGroup</span></span>
<span data-ttu-id="5e68c-139">Ad alanının atandığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e68c-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="5e68c-140">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="5e68c-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="5e68c-141">Var olan bir kaynak grubunu kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="5e68c-141">You must use an existing resource group.</span></span>
<span data-ttu-id="5e68c-142">Bu cmdlet yeni bir kaynak grubu oluşturamıyor.</span><span class="sxs-lookup"><span data-stu-id="5e68c-142">This cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="5e68c-143">-SASRule</span><span class="sxs-lookup"><span data-stu-id="5e68c-143">-SASRule</span></span>
<span data-ttu-id="5e68c-144">Yeni kuralların yapılandırma bilgilerini içeren **Sharedaccessauthorizationruleattributes** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e68c-144">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e68c-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="5e68c-145">-Confirm</span></span>
<span data-ttu-id="5e68c-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5e68c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e68c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e68c-147">-WhatIf</span></span>
<span data-ttu-id="5e68c-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e68c-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e68c-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5e68c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e68c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e68c-150">CommonParameters</span></span>
<span data-ttu-id="5e68c-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e68c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e68c-152">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e68c-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e68c-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e68c-153">INPUTS</span></span>

### <span data-ttu-id="5e68c-154">System. String</span><span class="sxs-lookup"><span data-stu-id="5e68c-154">System.String</span></span>

## <span data-ttu-id="5e68c-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e68c-155">OUTPUTS</span></span>

### <span data-ttu-id="5e68c-156">Microsoft. Azure. Commands. Notificationhub. modeller. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="5e68c-156">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="5e68c-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e68c-157">NOTES</span></span>

## <span data-ttu-id="5e68c-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e68c-158">RELATED LINKS</span></span>

[<span data-ttu-id="5e68c-159">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5e68c-159">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="5e68c-160">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5e68c-160">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="5e68c-161">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5e68c-161">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


