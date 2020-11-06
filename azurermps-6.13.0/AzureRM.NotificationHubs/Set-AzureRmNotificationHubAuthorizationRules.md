---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 24c65b6f7bf39d4fe046b020a9427dba7bf53aa9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590109"
---
# <span data-ttu-id="46dc4-101">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="46dc4-101">Set-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="46dc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46dc4-102">SYNOPSIS</span></span>
<span data-ttu-id="46dc4-103">Bildirim Hub 'ına yönelik yetkilendirme kurallarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="46dc4-103">Sets authorization rules for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46dc4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46dc4-104">SYNTAX</span></span>

### <span data-ttu-id="46dc4-105">Inputfileparameterset</span><span class="sxs-lookup"><span data-stu-id="46dc4-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46dc4-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="46dc4-106">SASRuleParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46dc4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="46dc4-107">DESCRIPTION</span></span>
<span data-ttu-id="46dc4-108">**Set-AzureRmNotificationHubAuthorizationRules** cmdlet 'i bir Bildirim Hub 'ına atanan paylaşılan erişim IMZASıNı (SAS) yetkilendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="46dc4-108">The **Set-AzureRmNotificationHubAuthorizationRules** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="46dc4-109">Yetkilendirme kuralları, farklı izin düzeylerine dayalı olarak, bağlantı oluşturarak Bildirim Hub 'larına erişimi yönetir.</span><span class="sxs-lookup"><span data-stu-id="46dc4-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="46dc4-110">İzin düzeyleri aşağıdakilerden biri olabilir:</span><span class="sxs-lookup"><span data-stu-id="46dc4-110">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="46dc4-111">Sten</span><span class="sxs-lookup"><span data-stu-id="46dc4-111">Listen</span></span>
- <span data-ttu-id="46dc4-112">Gönder</span><span class="sxs-lookup"><span data-stu-id="46dc4-112">Send</span></span>
- <span data-ttu-id="46dc4-113">Istemcileri yönetme, bu URI 'Lardan birine uygun izin düzeyine göre yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="46dc4-113">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="46dc4-114">Örneğin, dinleme izni verilen bir istemci bu izin için URI 'ye yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="46dc4-114">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="46dc4-115">Bu cmdlet, Bildirim Hub 'ına atanmış yetkilendirme kuralını değiştirmek için iki yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="46dc4-115">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="46dc4-116">Bir tane için, **Sharedaccessauthorizationruleattributes** nesnesinin bir örneğini oluşturabilir ve bu nesneyi kuralın sahip olmasını istediğiniz özellik değerleriyle yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="46dc4-116">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="46dc4-117">Nesneyi .NET Framework aracılığıyla yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="46dc4-117">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="46dc4-118">Bu özellik değerlerini, *sasrule* parametresini kullanarak kuralınıza kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="46dc4-118">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="46dc4-119">Alternatif olarak, ilgili yapılandırma değerlerini içeren bir JSON (JavaScript nesnesi Gösterim) dosyası oluşturabilir ve bu değerleri, *GirdiDosyası* parametresi aracılığıyla uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="46dc4-119">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="46dc4-120">JSON dosyası şuna benzer sözdizimi kullanan bir metin dosyasıdır: {"ad": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="46dc4-120">A JSON file is a text file that uses syntax similar to this: {      "Name": "ContosoAuthorizationRule",</span></span>  
  <span data-ttu-id="46dc4-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",</span><span class="sxs-lookup"><span data-stu-id="46dc4-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
  <span data-ttu-id="46dc4-122">"Haklar": \[</span><span class="sxs-lookup"><span data-stu-id="46dc4-122">"Rights": \[</span></span>  
        <span data-ttu-id="46dc4-123">"Dinle",</span><span class="sxs-lookup"><span data-stu-id="46dc4-123">"Listen",</span></span>  
        <span data-ttu-id="46dc4-124">Göndermek</span><span class="sxs-lookup"><span data-stu-id="46dc4-124">"Send"</span></span>  
    \]  
  <span data-ttu-id="46dc4-125">} New-AzureRmNotificationHubAuthorizationRules cmdlet 'i ile birlikte kullanıldığında, önceki JSON örneği, kullanıcıların hub 'a dinlemesi ve göndermesine izin vermek için ContosoAuthorizationRule adlı bir yetkilendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="46dc4-125">} When used in conjunction with the New-AzureRmNotificationHubAuthorizationRules cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="46dc4-126">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46dc4-126">EXAMPLES</span></span>

### <span data-ttu-id="46dc4-127">Örnek 1: Bildirim Hub 'ına atanan yetkilendirme kuralını değiştirme</span><span class="sxs-lookup"><span data-stu-id="46dc4-127">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="46dc4-128">Bu komut, ContosoExternalHub adlı Bildirim Hub 'ına atanmış yetkilendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="46dc4-128">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="46dc4-129">Hub 'ın bulunduğu ad boşluğunu ve hub 'ın atandığı kaynak grubunu belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="46dc4-129">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="46dc4-130">Değiştirilen kuralla ilgili bilgiler komuta dahil değildir.</span><span class="sxs-lookup"><span data-stu-id="46dc4-130">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="46dc4-131">Bunun yerine bu bilgiler C:\Configuration\AuthorizationRules.jsgiriş dosyasında bulunur.</span><span class="sxs-lookup"><span data-stu-id="46dc4-131">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="46dc4-132">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46dc4-132">PARAMETERS</span></span>

### <span data-ttu-id="46dc4-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46dc4-133">-DefaultProfile</span></span>
<span data-ttu-id="46dc4-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="46dc4-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46dc4-135">-Force</span><span class="sxs-lookup"><span data-stu-id="46dc4-135">-Force</span></span>
<span data-ttu-id="46dc4-136">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="46dc4-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="46dc4-137">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="46dc4-137">-InputFile</span></span>
<span data-ttu-id="46dc4-138">Yeni kuralın yapılandırma bilgilerini içeren bir JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="46dc4-138">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dc4-139">-Namespace</span><span class="sxs-lookup"><span data-stu-id="46dc4-139">-Namespace</span></span>
<span data-ttu-id="46dc4-140">Bildirim Hub 'ına atanmış olan ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="46dc4-140">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="46dc4-141">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="46dc4-141">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="46dc4-142">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="46dc4-142">-NotificationHub</span></span>
<span data-ttu-id="46dc4-143">Bu cmdlet 'in yetkilendirme kuralları atadığı Bildirim Merkezi 'ni belirtir.</span><span class="sxs-lookup"><span data-stu-id="46dc4-143">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="46dc4-144">Bildirim hubları, bu istemciler tarafından kullanılan bağımsız olarak birden fazla istemciye anında bildirim göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="46dc4-144">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="46dc4-145">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="46dc4-145">-ResourceGroup</span></span>
<span data-ttu-id="46dc4-146">Bildirim Hub 'ına atanmış kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="46dc4-146">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="46dc4-147">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="46dc4-147">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="46dc4-148">-SASRule</span><span class="sxs-lookup"><span data-stu-id="46dc4-148">-SASRule</span></span>
<span data-ttu-id="46dc4-149">Değiştirilen yetkilendirme kuralları için yapılandırma bilgilerini içeren **Sharedaccessauthorizationruleattributes** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46dc4-149">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dc4-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="46dc4-150">-Confirm</span></span>
<span data-ttu-id="46dc4-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="46dc4-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46dc4-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46dc4-152">-WhatIf</span></span>
<span data-ttu-id="46dc4-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46dc4-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46dc4-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="46dc4-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46dc4-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46dc4-155">CommonParameters</span></span>
<span data-ttu-id="46dc4-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46dc4-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46dc4-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46dc4-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46dc4-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46dc4-158">INPUTS</span></span>

### <span data-ttu-id="46dc4-159">System. String</span><span class="sxs-lookup"><span data-stu-id="46dc4-159">System.String</span></span>

## <span data-ttu-id="46dc4-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46dc4-160">OUTPUTS</span></span>

### <span data-ttu-id="46dc4-161">Microsoft. Azure. Commands. Notificationhub. modeller. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="46dc4-161">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="46dc4-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46dc4-162">NOTES</span></span>

## <span data-ttu-id="46dc4-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46dc4-163">RELATED LINKS</span></span>

[<span data-ttu-id="46dc4-164">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="46dc4-164">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="46dc4-165">Yeni-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="46dc4-165">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="46dc4-166">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="46dc4-166">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)


