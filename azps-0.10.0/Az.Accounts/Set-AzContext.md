---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Set-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Set-AzContext.md
ms.openlocfilehash: 5dcb1636dc4ecc4556bea14f8b3cd52bec7c0927
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935227"
---
# <span data-ttu-id="54519-101">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="54519-101">Set-AzContext</span></span>

## <span data-ttu-id="54519-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54519-102">SYNOPSIS</span></span>
<span data-ttu-id="54519-103">Cmdlet 'lerin geçerli oturumda kullanması için kiracı, abonelik ve ortamı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="54519-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="54519-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54519-104">SYNTAX</span></span>

### <span data-ttu-id="54519-105">Bağlam (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="54519-105">Context (Default)</span></span>
```
Set-AzContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="54519-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="54519-106">TenantObject</span></span>
```
Set-AzContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="54519-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="54519-107">SubscriptionObject</span></span>
```
Set-AzContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="54519-108">Aşırı</span><span class="sxs-lookup"><span data-stu-id="54519-108">Subscription</span></span>
```
Set-AzContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="54519-109">Yalnızca TenantName</span><span class="sxs-lookup"><span data-stu-id="54519-109">TenantNameOnly</span></span>
```
Set-AzContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54519-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="54519-110">DESCRIPTION</span></span>
<span data-ttu-id="54519-111">Set-AzContext cmdlet, geçerli oturumda çalıştırdığınız cmdlet 'lerin kimlik doğrulama bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="54519-111">The Set-AzContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="54519-112">Bağlam kiracı, abonelik ve ortam bilgilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="54519-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="54519-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54519-113">EXAMPLES</span></span>

### <span data-ttu-id="54519-114">Örnek 1: abonelik bağlamını ayarlama</span><span class="sxs-lookup"><span data-stu-id="54519-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="54519-115">Bu komut, bağlamı belirtilen aboneliği kullanacak şekilde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="54519-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="54519-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54519-116">PARAMETERS</span></span>

### <span data-ttu-id="54519-117">-Context</span><span class="sxs-lookup"><span data-stu-id="54519-117">-Context</span></span>
<span data-ttu-id="54519-118">Geçerli oturumun bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54519-118">Specifies the context for the current session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: Context
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54519-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54519-119">-DefaultProfile</span></span>
<span data-ttu-id="54519-120">Azure ile iletişim için kullanılan kimlik bilgileri, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="54519-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54519-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="54519-121">-ExtendedProperty</span></span>
<span data-ttu-id="54519-122">Ek bağlam özellikleri</span><span class="sxs-lookup"><span data-stu-id="54519-122">Additional context properties</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54519-123">-Force</span><span class="sxs-lookup"><span data-stu-id="54519-123">-Force</span></span>
<span data-ttu-id="54519-124">Varsa, var olan içeriğin üzerine yazın.</span><span class="sxs-lookup"><span data-stu-id="54519-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="54519-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="54519-125">-Name</span></span>
<span data-ttu-id="54519-126">Bağlam adı</span><span class="sxs-lookup"><span data-stu-id="54519-126">Name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54519-127">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="54519-127">-Scope</span></span>
<span data-ttu-id="54519-128">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="54519-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54519-129">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="54519-129">-Subscription</span></span>
<span data-ttu-id="54519-130">İçeriğin ayarlanması gereken aboneliğin adı veya kimliği.</span><span class="sxs-lookup"><span data-stu-id="54519-130">The name or id of the subscription that the context should be set to.</span></span> <span data-ttu-id="54519-131">Bu parametrenin,-SubscriptionName ve-SubscriptionID adlarına sahip olduğu için, sırasıyla ad ve kimlik belirtildiğinde abonelik yerine bu ikisinden biri kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="54519-131">This parameter has aliases to -SubscriptionName and -SubscriptionId, so, for clarity, either of these can be used instead of -Subscription when specifying name and id, respectively.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: SubscriptionId, SubscriptionName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54519-132">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="54519-132">-SubscriptionObject</span></span>
<span data-ttu-id="54519-133">Bir abonelik nesnesi</span><span class="sxs-lookup"><span data-stu-id="54519-133">A subscription object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription
Parameter Sets: SubscriptionObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54519-134">-Tenant</span><span class="sxs-lookup"><span data-stu-id="54519-134">-Tenant</span></span>
<span data-ttu-id="54519-135">Kiracı adı veya KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="54519-135">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TenantNameOnly
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54519-136">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="54519-136">-TenantObject</span></span>
<span data-ttu-id="54519-137">Kiracı nesnesi</span><span class="sxs-lookup"><span data-stu-id="54519-137">A Tenant Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureTenant
Parameter Sets: TenantObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54519-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="54519-138">-Confirm</span></span>
<span data-ttu-id="54519-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="54519-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54519-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54519-140">-WhatIf</span></span>
<span data-ttu-id="54519-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="54519-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54519-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="54519-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54519-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54519-143">CommonParameters</span></span>
<span data-ttu-id="54519-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54519-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54519-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="54519-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54519-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54519-146">INPUTS</span></span>

### <span data-ttu-id="54519-147">Microsoft. Azure. Commands. Profile. modeller. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="54519-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

### <span data-ttu-id="54519-148">Microsoft. Azure. Commands. Profile. modeller. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="54519-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

### <span data-ttu-id="54519-149">Microsoft. Azure. Commands. Profile. modeller. psazuyeniden gönderme komutları</span><span class="sxs-lookup"><span data-stu-id="54519-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="54519-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54519-150">OUTPUTS</span></span>

### <span data-ttu-id="54519-151">Microsoft. Azure. Commands. Profile. modeller. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="54519-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="54519-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54519-152">NOTES</span></span>

## <span data-ttu-id="54519-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54519-153">RELATED LINKS</span></span>

[<span data-ttu-id="54519-154">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="54519-154">Get-AzContext</span></span>](./Get-AzContext.md)
