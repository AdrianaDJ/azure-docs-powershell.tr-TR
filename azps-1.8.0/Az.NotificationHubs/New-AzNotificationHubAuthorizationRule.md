---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 436ed6aaa720074be2014d9c736ab0636a09869f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759903"
---
# <span data-ttu-id="e2356-101">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e2356-101">New-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="e2356-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2356-102">SYNOPSIS</span></span>
<span data-ttu-id="e2356-103">Yetkilendirme kuralı oluşturur ve kuralı Bildirim Hub 'ına atar.</span><span class="sxs-lookup"><span data-stu-id="e2356-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

## <span data-ttu-id="e2356-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2356-104">SYNTAX</span></span>

### <span data-ttu-id="e2356-105">Inputfileparameterset</span><span class="sxs-lookup"><span data-stu-id="e2356-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2356-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2356-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2356-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2356-107">DESCRIPTION</span></span>
<span data-ttu-id="e2356-108">**New-AzNotificationHubAuthorizationRule** cmdlet 'i bir bildirim merkezi paylaşılan erişim IMZASı (SAS) yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2356-108">The **New-AzNotificationHubAuthorizationRule** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="e2356-109">Bildirim Hub 'larına erişimi yönetmek için yetkilendirme kuralları kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e2356-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="e2356-110">Bu, farklı izin düzeylerine bağlı olarak, bağlantıların oluşturulması tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="e2356-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="e2356-111">İstemciler, uygun izin düzeyine dayalı olarak bu URI 'Lardan birine yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="e2356-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="e2356-112">Örneğin, dinleme izni verilen bir istemci bu izin için URI 'ye yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="e2356-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="e2356-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2356-113">EXAMPLES</span></span>

### <span data-ttu-id="e2356-114">Örnek 1: Bildirim Merkezi yetkilendirme kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="e2356-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="e2356-115">Bu komut yeni bir yetkilendirme kuralı oluşturur ve bu kuralı Contosoınterınternalhub adlı Bildirim Hub 'ına atar.</span><span class="sxs-lookup"><span data-stu-id="e2356-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="e2356-116">Bu hub ContosoNamespace ad alanında bulunur ve ContosoNotificationsGroup kaynak grubuna atanır.</span><span class="sxs-lookup"><span data-stu-id="e2356-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="e2356-117">Kural adı da dahil, kuralın tüm yapılandırma bilgilerinin, C:\Configuration\ExternalAccessRule.jsgiriş dosyasından alınacağını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="e2356-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="e2356-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2356-118">PARAMETERS</span></span>

### <span data-ttu-id="e2356-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2356-119">-DefaultProfile</span></span>
<span data-ttu-id="e2356-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e2356-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2356-121">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="e2356-121">-InputFile</span></span>
<span data-ttu-id="e2356-122">Bu cmdlet 'in oluşturduğu yetkilendirme kuralının giriş dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2356-122">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e2356-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e2356-123">-Namespace</span></span>
<span data-ttu-id="e2356-124">Yetkilendirme kurallarının atandığı ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2356-124">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="e2356-125">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="e2356-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="e2356-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="e2356-126">-NotificationHub</span></span>
<span data-ttu-id="e2356-127">Yetkilendirme kurallarının atanacağı Bildirim Hub 'ını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2356-127">Specifies the notification hub that the authorization rules will be assigned to.</span></span>
<span data-ttu-id="e2356-128">Bildirim Hub 'ları, bu istemcilerin kullandığı platforma bakılmaksızın birden çok istemciye anında bildirim göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e2356-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="e2356-129">Var olan bir Bildirim Hub 'ının adını belirtmeniz gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="e2356-129">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="e2356-130">**Yeni-AzNotificationHubAuthorizationRule** cmdlet 'i yeni Bildirim Hub 'ları oluşturamaz.</span><span class="sxs-lookup"><span data-stu-id="e2356-130">The **New-AzNotificationHubAuthorizationRule** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="e2356-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e2356-131">-ResourceGroup</span></span>
<span data-ttu-id="e2356-132">Bildirim Hub 'ının atandığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2356-132">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="e2356-133">-SASRule</span><span class="sxs-lookup"><span data-stu-id="e2356-133">-SASRule</span></span>
<span data-ttu-id="e2356-134">Yeni kuralların yapılandırma bilgilerini içeren **Sharedaccessauthorizationruleattributes** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2356-134">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="e2356-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="e2356-135">-Confirm</span></span>
<span data-ttu-id="e2356-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e2356-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2356-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2356-137">-WhatIf</span></span>
<span data-ttu-id="e2356-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2356-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2356-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e2356-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2356-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2356-140">CommonParameters</span></span>
<span data-ttu-id="e2356-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2356-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2356-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2356-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2356-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2356-143">INPUTS</span></span>

### <span data-ttu-id="e2356-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e2356-144">System.String</span></span>

## <span data-ttu-id="e2356-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2356-145">OUTPUTS</span></span>

### <span data-ttu-id="e2356-146">Microsoft. Azure. Commands. Notificationhub. modeller. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e2356-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="e2356-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2356-147">NOTES</span></span>

## <span data-ttu-id="e2356-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2356-148">RELATED LINKS</span></span>

[<span data-ttu-id="e2356-149">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e2356-149">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="e2356-150">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e2356-150">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="e2356-151">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e2356-151">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


