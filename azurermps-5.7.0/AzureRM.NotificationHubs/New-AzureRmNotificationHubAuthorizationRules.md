---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 8e1da1576b080f9930d123cb7ddab48761392e15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764414"
---
# <span data-ttu-id="3105b-101">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="3105b-101">New-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="3105b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3105b-102">SYNOPSIS</span></span>
<span data-ttu-id="3105b-103">Yetkilendirme kuralı oluşturur ve kuralı Bildirim Hub 'ına atar.</span><span class="sxs-lookup"><span data-stu-id="3105b-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3105b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3105b-104">SYNTAX</span></span>

### <span data-ttu-id="3105b-105">Inputfileparameterset</span><span class="sxs-lookup"><span data-stu-id="3105b-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3105b-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="3105b-106">SASRuleParameterSet</span></span>
```
New-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3105b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3105b-107">DESCRIPTION</span></span>
<span data-ttu-id="3105b-108">**Yeni-AzureRmNotificationHubAuthorizationRules** cmdlet 'i bir bildirim merkezi paylaşılan erişim IMZASı (SAS) yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3105b-108">The **New-AzureRmNotificationHubAuthorizationRules** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>

<span data-ttu-id="3105b-109">Bildirim Hub 'larına erişimi yönetmek için yetkilendirme kuralları kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3105b-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="3105b-110">Bu, farklı izin düzeylerine bağlı olarak, bağlantıların oluşturulması tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="3105b-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="3105b-111">İstemciler, uygun izin düzeyine dayalı olarak bu URI 'Lardan birine yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="3105b-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="3105b-112">Örneğin, dinleme izni verilen bir istemci bu izin için URI 'ye yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="3105b-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="3105b-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3105b-113">EXAMPLES</span></span>

### <span data-ttu-id="3105b-114">Örnek 1: Bildirim Merkezi yetkilendirme kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="3105b-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="3105b-115">Bu komut yeni bir yetkilendirme kuralı oluşturur ve bu kuralı Contosoınterınternalhub adlı Bildirim Hub 'ına atar.</span><span class="sxs-lookup"><span data-stu-id="3105b-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="3105b-116">Bu hub ContosoNamespace ad alanında bulunur ve ContosoNotificationsGroup kaynak grubuna atanır.</span><span class="sxs-lookup"><span data-stu-id="3105b-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="3105b-117">Kural adı da dahil, kuralın tüm yapılandırma bilgilerinin, C:\Configuration\ExternalAccessRule.jsgiriş dosyasından alınacağını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="3105b-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="3105b-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3105b-118">PARAMETERS</span></span>

### <span data-ttu-id="3105b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3105b-119">-DefaultProfile</span></span>
<span data-ttu-id="3105b-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3105b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3105b-121">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="3105b-121">-InputFile</span></span>
<span data-ttu-id="3105b-122">Bu cmdlet 'in oluşturduğu yetkilendirme kuralının giriş dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3105b-122">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="3105b-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3105b-123">-Namespace</span></span>
<span data-ttu-id="3105b-124">Yetkilendirme kurallarının atandığı ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3105b-124">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="3105b-125">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="3105b-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="3105b-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="3105b-126">-NotificationHub</span></span>
<span data-ttu-id="3105b-127">Yetkilendirme kurallarının atanacağı Bildirim Hub 'ını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3105b-127">Specifies the notification hub that the authorization rules will be assigned to.</span></span>

<span data-ttu-id="3105b-128">Bildirim Hub 'ları, bu istemcilerin kullandığı platforma bakılmaksızın birden çok istemciye anında bildirim göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3105b-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="3105b-129">Var olan bir Bildirim Hub 'ının adını belirtmeniz gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="3105b-129">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="3105b-130">**Yeni-AzureRmNotificationHubAuthorizationRules** cmdlet 'i yeni Bildirim Hub 'ları oluşturamaz.</span><span class="sxs-lookup"><span data-stu-id="3105b-130">The **New-AzureRmNotificationHubAuthorizationRules** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="3105b-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3105b-131">-ResourceGroup</span></span>
<span data-ttu-id="3105b-132">Bildirim Hub 'ının atandığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3105b-132">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="3105b-133">-SASRule</span><span class="sxs-lookup"><span data-stu-id="3105b-133">-SASRule</span></span>
<span data-ttu-id="3105b-134">Yeni kuralların yapılandırma bilgilerini içeren **Sharedaccessauthorizationruleattributes** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3105b-134">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="3105b-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="3105b-135">-Confirm</span></span>
<span data-ttu-id="3105b-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3105b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3105b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3105b-137">-WhatIf</span></span>
<span data-ttu-id="3105b-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3105b-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3105b-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3105b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3105b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3105b-140">CommonParameters</span></span>
<span data-ttu-id="3105b-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3105b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3105b-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3105b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3105b-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3105b-143">INPUTS</span></span>

### <span data-ttu-id="3105b-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3105b-144">None</span></span>
<span data-ttu-id="3105b-145">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="3105b-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3105b-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3105b-146">OUTPUTS</span></span>

### <span data-ttu-id="3105b-147">Microsoft. Azure. Commands. Notificationhub. modeller. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="3105b-147">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="3105b-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3105b-148">NOTES</span></span>

## <span data-ttu-id="3105b-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3105b-149">RELATED LINKS</span></span>

[<span data-ttu-id="3105b-150">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="3105b-150">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="3105b-151">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="3105b-151">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="3105b-152">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="3105b-152">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


