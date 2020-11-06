---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 6203c5554dcdbfbd40c861a3f73e1a5947228030
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594913"
---
# <span data-ttu-id="b1bfb-101">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="b1bfb-101">Set-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="b1bfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1bfb-102">SYNOPSIS</span></span>
<span data-ttu-id="b1bfb-103">Bildirim Hub 'ına yönelik yetkilendirme kurallarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-103">Sets authorization rules for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1bfb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b1bfb-104">SYNTAX</span></span>

### <span data-ttu-id="b1bfb-105">Inputfileparameterset</span><span class="sxs-lookup"><span data-stu-id="b1bfb-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1bfb-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1bfb-106">SASRuleParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1bfb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b1bfb-107">DESCRIPTION</span></span>
<span data-ttu-id="b1bfb-108">**Set-AzureRmNotificationHubAuthorizationRules** cmdlet 'i bir Bildirim Hub 'ına atanan paylaşılan erişim IMZASıNı (SAS) yetkilendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-108">The **Set-AzureRmNotificationHubAuthorizationRules** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>

<span data-ttu-id="b1bfb-109">Yetkilendirme kuralları, farklı izin düzeylerine dayalı olarak, bağlantı oluşturarak Bildirim Hub 'larına erişimi yönetir.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="b1bfb-110">İzin düzeyleri aşağıdakilerden biri olabilir:</span><span class="sxs-lookup"><span data-stu-id="b1bfb-110">Permission levels can be one of the following:</span></span> 

- <span data-ttu-id="b1bfb-111">Sten</span><span class="sxs-lookup"><span data-stu-id="b1bfb-111">Listen</span></span>
- <span data-ttu-id="b1bfb-112">Gönder</span><span class="sxs-lookup"><span data-stu-id="b1bfb-112">Send</span></span>
- <span data-ttu-id="b1bfb-113">Yönetebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b1bfb-113">Manage</span></span>

<span data-ttu-id="b1bfb-114">İstemciler, uygun izin düzeyine dayalı olarak bu URI 'Lardan birine yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-114">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="b1bfb-115">Örneğin, dinleme izni verilen bir istemci bu izin için URI 'ye yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-115">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="b1bfb-116">Bu cmdlet, Bildirim Hub 'ına atanmış yetkilendirme kuralını değiştirmek için iki yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-116">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="b1bfb-117">Bir tane için, **Sharedaccessauthorizationruleattributes** nesnesinin bir örneğini oluşturabilir ve bu nesneyi kuralın sahip olmasını istediğiniz özellik değerleriyle yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-117">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="b1bfb-118">Nesneyi .NET Framework aracılığıyla yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-118">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="b1bfb-119">Bu özellik değerlerini, *sasrule* parametresini kullanarak kuralınıza kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-119">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>

<span data-ttu-id="b1bfb-120">Alternatif olarak, ilgili yapılandırma değerlerini içeren bir JSON (JavaScript nesnesi Gösterim) dosyası oluşturabilir ve bu değerleri, *GirdiDosyası* parametresi aracılığıyla uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-120">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="b1bfb-121">JSON dosyası, aşağıdakine benzer sözdizimi kullanan bir metin dosyasıdır:</span><span class="sxs-lookup"><span data-stu-id="b1bfb-121">A JSON file is a text file that uses syntax similar to this:</span></span>

<span data-ttu-id="b1bfb-122">{"Ad": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="b1bfb-122">{      "Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="b1bfb-123">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",</span><span class="sxs-lookup"><span data-stu-id="b1bfb-123">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="b1bfb-124">"Haklar": \[</span><span class="sxs-lookup"><span data-stu-id="b1bfb-124">"Rights": \[</span></span>  
        <span data-ttu-id="b1bfb-125">"Dinle",</span><span class="sxs-lookup"><span data-stu-id="b1bfb-125">"Listen",</span></span>  
        <span data-ttu-id="b1bfb-126">Göndermek</span><span class="sxs-lookup"><span data-stu-id="b1bfb-126">"Send"</span></span>  
    \]  
<span data-ttu-id="b1bfb-127">}</span><span class="sxs-lookup"><span data-stu-id="b1bfb-127">}</span></span>

<span data-ttu-id="b1bfb-128">New-AzureRmNotificationHubAuthorizationRules cmdlet 'le birlikte kullanıldığında, önceki JSON örneği, kullanıcılara, hub 'a Kullanıcı dinlemesi ve gönderimi izni vermek için ContosoAuthorizationRule adlı bir yetkilendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-128">When used in conjunction with the New-AzureRmNotificationHubAuthorizationRules cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="b1bfb-129">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b1bfb-129">EXAMPLES</span></span>

### <span data-ttu-id="b1bfb-130">Örnek 1: Bildirim Hub 'ına atanan yetkilendirme kuralını değiştirme</span><span class="sxs-lookup"><span data-stu-id="b1bfb-130">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="b1bfb-131">Bu komut, ContosoExternalHub adlı Bildirim Hub 'ına atanmış yetkilendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-131">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="b1bfb-132">Hub 'ın bulunduğu ad boşluğunu ve hub 'ın atandığı kaynak grubunu belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-132">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="b1bfb-133">Değiştirilen kuralla ilgili bilgiler komuta dahil değildir.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-133">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="b1bfb-134">Bunun yerine bu bilgiler C:\Configuration\AuthorizationRules.jsgiriş dosyasında bulunur.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-134">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="b1bfb-135">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b1bfb-135">PARAMETERS</span></span>

### <span data-ttu-id="b1bfb-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1bfb-136">-DefaultProfile</span></span>
<span data-ttu-id="b1bfb-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b1bfb-137">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1bfb-138">-Force</span><span class="sxs-lookup"><span data-stu-id="b1bfb-138">-Force</span></span>
<span data-ttu-id="b1bfb-139">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-139">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b1bfb-140">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="b1bfb-140">-InputFile</span></span>
<span data-ttu-id="b1bfb-141">Yeni kuralın yapılandırma bilgilerini içeren bir JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-141">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1bfb-142">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b1bfb-142">-Namespace</span></span>
<span data-ttu-id="b1bfb-143">Bildirim Hub 'ına atanmış olan ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-143">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="b1bfb-144">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-144">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="b1bfb-145">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="b1bfb-145">-NotificationHub</span></span>
<span data-ttu-id="b1bfb-146">Bu cmdlet 'in yetkilendirme kuralları atadığı Bildirim Merkezi 'ni belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-146">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="b1bfb-147">Bildirim hubları, bu istemciler tarafından kullanılan bağımsız olarak birden fazla istemciye anında bildirim göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-147">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="b1bfb-148">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b1bfb-148">-ResourceGroup</span></span>
<span data-ttu-id="b1bfb-149">Bildirim Hub 'ına atanmış kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-149">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="b1bfb-150">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-150">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="b1bfb-151">-SASRule</span><span class="sxs-lookup"><span data-stu-id="b1bfb-151">-SASRule</span></span>
<span data-ttu-id="b1bfb-152">Değiştirilen yetkilendirme kuralları için yapılandırma bilgilerini içeren **Sharedaccessauthorizationruleattributes** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-152">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1bfb-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="b1bfb-153">-Confirm</span></span>
<span data-ttu-id="b1bfb-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1bfb-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1bfb-155">-WhatIf</span></span>
<span data-ttu-id="b1bfb-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1bfb-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1bfb-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1bfb-158">CommonParameters</span></span>
<span data-ttu-id="b1bfb-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1bfb-160">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1bfb-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1bfb-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b1bfb-161">INPUTS</span></span>

### <span data-ttu-id="b1bfb-162">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b1bfb-162">None</span></span>
<span data-ttu-id="b1bfb-163">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b1bfb-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b1bfb-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b1bfb-164">OUTPUTS</span></span>

### <span data-ttu-id="b1bfb-165">Microsoft. Azure. Commands. Notificationhub. modeller. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="b1bfb-165">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="b1bfb-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b1bfb-166">NOTES</span></span>

## <span data-ttu-id="b1bfb-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b1bfb-167">RELATED LINKS</span></span>

[<span data-ttu-id="b1bfb-168">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="b1bfb-168">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="b1bfb-169">Yeni-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="b1bfb-169">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="b1bfb-170">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="b1bfb-170">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)


