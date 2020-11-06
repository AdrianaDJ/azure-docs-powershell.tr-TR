---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: ed94e34f754298e89bf1f18d5264f11c2c9c308c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594911"
---
# <span data-ttu-id="8590e-101">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="8590e-101">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="8590e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8590e-102">SYNOPSIS</span></span>
<span data-ttu-id="8590e-103">Bildirim Merkezi ad alanı için yetkilendirme kurallarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8590e-103">Sets authorization rules for a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8590e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8590e-104">SYNTAX</span></span>

### <span data-ttu-id="8590e-105">Inputfileparameterset</span><span class="sxs-lookup"><span data-stu-id="8590e-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8590e-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="8590e-106">SASRuleParameterSet</span></span>
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8590e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8590e-107">DESCRIPTION</span></span>
<span data-ttu-id="8590e-108">**Set-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet 'i, bir Bildirim Hub ad alanına atanan paylaşılan erişim IMZASıNı (SAS) yetkilendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8590e-108">The **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="8590e-109">Yetkilendirme kuralları ad alanındaki Kullanıcı haklarını ve bu ad alanında bulunan bildirim hubları yönetir.</span><span class="sxs-lookup"><span data-stu-id="8590e-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>

<span data-ttu-id="8590e-110">Bu cmdlet, bir ad boşluğuna atanmış yetkilendirme kuralını değiştirmek için iki yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="8590e-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="8590e-111">Bir tane için, **Sharedaccessauthorizationruleattributes** nesnesinin bir örneğini oluşturabilir ve bu nesneyi kuralın sahip olmasını istediğiniz özellik değerleriyle yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8590e-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="8590e-112">Bunu yapmak için .NET Framework kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8590e-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="8590e-113">Bu özellik değerlerini, *sasrule* parametresi aracılığıyla kurala kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8590e-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>

<span data-ttu-id="8590e-114">Alternatif olarak, ilgili yapılandırma değerlerini içeren bir JSON (JavaScript nesnesi Gösterim) dosyası oluşturabilir ve bu değerleri, *GirdiDosyası* parametresi aracılığıyla uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8590e-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="8590e-115">JSON dosyası, aşağıdakine benzer sözdizimi kullanan bir metin dosyasıdır:</span><span class="sxs-lookup"><span data-stu-id="8590e-115">A JSON file is a text file that uses syntax similar to this:</span></span>

<span data-ttu-id="8590e-116">{</span><span class="sxs-lookup"><span data-stu-id="8590e-116">{</span></span>  
    <span data-ttu-id="8590e-117">"Ad": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="8590e-117">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="8590e-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",</span><span class="sxs-lookup"><span data-stu-id="8590e-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="8590e-119">"Haklar": \[</span><span class="sxs-lookup"><span data-stu-id="8590e-119">"Rights": \[</span></span>  
        <span data-ttu-id="8590e-120">"Dinle",</span><span class="sxs-lookup"><span data-stu-id="8590e-120">"Listen",</span></span>  
        <span data-ttu-id="8590e-121">Göndermek</span><span class="sxs-lookup"><span data-stu-id="8590e-121">"Send"</span></span>  
    \]  
<span data-ttu-id="8590e-122">}</span><span class="sxs-lookup"><span data-stu-id="8590e-122">}</span></span>

<span data-ttu-id="8590e-123">**Set-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet 'i ile birlikte kullanıldığında, önceki JSON örneği, kullanıcılara ad boşluğuna erişme yetkisi vermek Için ContosoAuthorizationRule adlı bir yetkilendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8590e-123">When used in conjunction with the **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="8590e-124">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8590e-124">EXAMPLES</span></span>

### <span data-ttu-id="8590e-125">Örnek 1: ad alanına atanan yetkilendirme kuralını değiştirme</span><span class="sxs-lookup"><span data-stu-id="8590e-125">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="8590e-126">Bu komut, ContosoNamespace adlı ad boşluğuna atanmış yetkilendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8590e-126">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="8590e-127">Ad alanının atandığı kaynak grubunu belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8590e-127">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="8590e-128">Yetkilendirme kuralıyla ilgili bilgiler komuta dahil değildir.</span><span class="sxs-lookup"><span data-stu-id="8590e-128">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="8590e-129">Bunun yerine bu bilgiler C:\Configuration\AuthorizationRules.jsgiriş dosyasından alınır.</span><span class="sxs-lookup"><span data-stu-id="8590e-129">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="8590e-130">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8590e-130">PARAMETERS</span></span>

### <span data-ttu-id="8590e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8590e-131">-DefaultProfile</span></span>
<span data-ttu-id="8590e-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8590e-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8590e-133">-Force</span><span class="sxs-lookup"><span data-stu-id="8590e-133">-Force</span></span>
<span data-ttu-id="8590e-134">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="8590e-134">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8590e-135">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="8590e-135">-InputFile</span></span>
<span data-ttu-id="8590e-136">Yeni kuralın yapılandırma bilgilerini içeren bir JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8590e-136">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="8590e-137">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8590e-137">-Namespace</span></span>
<span data-ttu-id="8590e-138">Bu cmdlet 'in değiştirdiği yetkilendirme kurallarını içeren ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8590e-138">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="8590e-139">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="8590e-139">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="8590e-140">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8590e-140">-ResourceGroup</span></span>
<span data-ttu-id="8590e-141">Ad alanının atandığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8590e-141">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="8590e-142">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="8590e-142">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="8590e-143">-SASRule</span><span class="sxs-lookup"><span data-stu-id="8590e-143">-SASRule</span></span>
<span data-ttu-id="8590e-144">Bu cmdlet 'in değiştirdiği yetkilendirme kuralları için yapılandırma bilgilerini içeren **Sharedaccessauthorizationruleattributes** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8590e-144">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8590e-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="8590e-145">-Confirm</span></span>
<span data-ttu-id="8590e-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8590e-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8590e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8590e-147">-WhatIf</span></span>
<span data-ttu-id="8590e-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8590e-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8590e-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8590e-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8590e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8590e-150">CommonParameters</span></span>
<span data-ttu-id="8590e-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8590e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8590e-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8590e-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8590e-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8590e-153">INPUTS</span></span>

### <span data-ttu-id="8590e-154">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8590e-154">None</span></span>
<span data-ttu-id="8590e-155">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="8590e-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8590e-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8590e-156">OUTPUTS</span></span>

### <span data-ttu-id="8590e-157">Microsoft. Azure. Commands. Notificationhub. modeller. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="8590e-157">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="8590e-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8590e-158">NOTES</span></span>

## <span data-ttu-id="8590e-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8590e-159">RELATED LINKS</span></span>

[<span data-ttu-id="8590e-160">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="8590e-160">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="8590e-161">Yeni-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="8590e-161">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="8590e-162">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="8590e-162">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


