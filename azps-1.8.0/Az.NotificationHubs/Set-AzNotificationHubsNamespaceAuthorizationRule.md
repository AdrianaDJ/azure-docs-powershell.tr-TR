---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 5fb832a7a72f0b201ea20660a5e94e67d470ba95
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759878"
---
# <span data-ttu-id="1e196-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1e196-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="1e196-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e196-102">SYNOPSIS</span></span>
<span data-ttu-id="1e196-103">Bildirim Merkezi ad alanı için yetkilendirme kurallarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1e196-103">Sets authorization rules for a notification hub namespace.</span></span>

## <span data-ttu-id="1e196-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e196-104">SYNTAX</span></span>

### <span data-ttu-id="1e196-105">Inputfileparameterset</span><span class="sxs-lookup"><span data-stu-id="1e196-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e196-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e196-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e196-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e196-107">DESCRIPTION</span></span>
<span data-ttu-id="1e196-108">**Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet 'i, bir Bildirim Hub ad alanına atanan paylaşılan erişim IMZASıNı (SAS) yetkilendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1e196-108">The **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="1e196-109">Yetkilendirme kuralları ad alanındaki Kullanıcı haklarını ve bu ad alanında bulunan bildirim hubları yönetir.</span><span class="sxs-lookup"><span data-stu-id="1e196-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>
<span data-ttu-id="1e196-110">Bu cmdlet, bir ad boşluğuna atanmış yetkilendirme kuralını değiştirmek için iki yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="1e196-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="1e196-111">Bir tane için, **Sharedaccessauthorizationruleattributes** nesnesinin bir örneğini oluşturabilir ve bu nesneyi kuralın sahip olmasını istediğiniz özellik değerleriyle yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1e196-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="1e196-112">Bunu yapmak için .NET Framework kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1e196-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="1e196-113">Bu özellik değerlerini, *sasrule* parametresi aracılığıyla kurala kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1e196-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>
<span data-ttu-id="1e196-114">Alternatif olarak, ilgili yapılandırma değerlerini içeren bir JSON (JavaScript nesnesi Gösterim) dosyası oluşturabilir ve bu değerleri, *GirdiDosyası* parametresi aracılığıyla uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1e196-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="1e196-115">JSON dosyası, aşağıdakine benzer bir sözdizimi kullanan bir metin dosyasıdır: {</span><span class="sxs-lookup"><span data-stu-id="1e196-115">A JSON file is a text file that uses syntax similar to this: {</span></span>  
    <span data-ttu-id="1e196-116">"Ad": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="1e196-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="1e196-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",</span><span class="sxs-lookup"><span data-stu-id="1e196-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="1e196-118">"Haklar": \[</span><span class="sxs-lookup"><span data-stu-id="1e196-118">"Rights": \[</span></span>  
        <span data-ttu-id="1e196-119">"Dinle",</span><span class="sxs-lookup"><span data-stu-id="1e196-119">"Listen",</span></span>  
        <span data-ttu-id="1e196-120">Göndermek</span><span class="sxs-lookup"><span data-stu-id="1e196-120">"Send"</span></span>  
    \]  
<span data-ttu-id="1e196-121">} **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet 'i ile birlikte kullanıldığında, önceki JSON örneği, kullanıcılara ad boşluğuna Kullanıcı dinlemesi ve Gönderimi Için contosoauthorizationrule adlı bir yetkilendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1e196-121">} When used in conjunction with the **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="1e196-122">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e196-122">EXAMPLES</span></span>

### <span data-ttu-id="1e196-123">Örnek 1: ad alanına atanan yetkilendirme kuralını değiştirme</span><span class="sxs-lookup"><span data-stu-id="1e196-123">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="1e196-124">Bu komut, ContosoNamespace adlı ad boşluğuna atanmış yetkilendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1e196-124">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="1e196-125">Ad alanının atandığı kaynak grubunu belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1e196-125">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="1e196-126">Yetkilendirme kuralıyla ilgili bilgiler komuta dahil değildir.</span><span class="sxs-lookup"><span data-stu-id="1e196-126">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="1e196-127">Bunun yerine bu bilgiler C:\Configuration\AuthorizationRules.jsgiriş dosyasından alınır.</span><span class="sxs-lookup"><span data-stu-id="1e196-127">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="1e196-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e196-128">PARAMETERS</span></span>

### <span data-ttu-id="1e196-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e196-129">-DefaultProfile</span></span>
<span data-ttu-id="1e196-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1e196-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e196-131">-Force</span><span class="sxs-lookup"><span data-stu-id="1e196-131">-Force</span></span>
<span data-ttu-id="1e196-132">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="1e196-132">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e196-133">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="1e196-133">-InputFile</span></span>
<span data-ttu-id="1e196-134">Yeni kuralın yapılandırma bilgilerini içeren bir JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e196-134">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="1e196-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1e196-135">-Namespace</span></span>
<span data-ttu-id="1e196-136">Bu cmdlet 'in değiştirdiği yetkilendirme kurallarını içeren ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e196-136">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="1e196-137">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="1e196-137">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="1e196-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1e196-138">-ResourceGroup</span></span>
<span data-ttu-id="1e196-139">Ad alanının atandığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e196-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="1e196-140">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="1e196-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="1e196-141">-SASRule</span><span class="sxs-lookup"><span data-stu-id="1e196-141">-SASRule</span></span>
<span data-ttu-id="1e196-142">Bu cmdlet 'in değiştirdiği yetkilendirme kuralları için yapılandırma bilgilerini içeren **Sharedaccessauthorizationruleattributes** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e196-142">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1e196-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="1e196-143">-Confirm</span></span>
<span data-ttu-id="1e196-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1e196-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e196-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e196-145">-WhatIf</span></span>
<span data-ttu-id="1e196-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1e196-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e196-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1e196-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e196-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e196-148">CommonParameters</span></span>
<span data-ttu-id="1e196-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e196-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e196-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e196-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e196-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e196-151">INPUTS</span></span>

### <span data-ttu-id="1e196-152">System. String</span><span class="sxs-lookup"><span data-stu-id="1e196-152">System.String</span></span>

## <span data-ttu-id="1e196-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e196-153">OUTPUTS</span></span>

### <span data-ttu-id="1e196-154">Microsoft. Azure. Commands. Notificationhub. modeller. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="1e196-154">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="1e196-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e196-155">NOTES</span></span>

## <span data-ttu-id="1e196-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e196-156">RELATED LINKS</span></span>

[<span data-ttu-id="1e196-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1e196-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="1e196-158">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1e196-158">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="1e196-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1e196-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Remove-AzNotificationHubsNamespaceAuthorizationRule.md)


