---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
ms.openlocfilehash: bffd818df21be78d0418bf3d2ac1ebea401dbf19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593458"
---
# <span data-ttu-id="ef9b7-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="ef9b7-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="ef9b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef9b7-102">SYNOPSIS</span></span>
<span data-ttu-id="ef9b7-103">Cmdlet 'lerin geçerli oturumda kullanması için kiracı, abonelik ve ortamı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ef9b7-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef9b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ef9b7-104">SYNTAX</span></span>

### <span data-ttu-id="ef9b7-105">Bağlam (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ef9b7-105">Context (Default)</span></span>
```
Set-AzureRmContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef9b7-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="ef9b7-106">TenantObject</span></span>
```
Set-AzureRmContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef9b7-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="ef9b7-107">SubscriptionObject</span></span>
```
Set-AzureRmContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef9b7-108">Aşırı</span><span class="sxs-lookup"><span data-stu-id="ef9b7-108">Subscription</span></span>
```
Set-AzureRmContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef9b7-109">Yalnızca TenantName</span><span class="sxs-lookup"><span data-stu-id="ef9b7-109">TenantNameOnly</span></span>
```
Set-AzureRmContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef9b7-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="ef9b7-110">DESCRIPTION</span></span>
<span data-ttu-id="ef9b7-111">Set-AzureRmContext cmdlet, geçerli oturumda çalıştırdığınız cmdlet 'lerin kimlik doğrulama bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ef9b7-111">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="ef9b7-112">Bağlam kiracı, abonelik ve ortam bilgilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="ef9b7-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="ef9b7-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ef9b7-113">EXAMPLES</span></span>

### <span data-ttu-id="ef9b7-114">Örnek 1: abonelik bağlamını ayarlama</span><span class="sxs-lookup"><span data-stu-id="ef9b7-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="ef9b7-115">Bu komut, bağlamı belirtilen aboneliği kullanacak şekilde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ef9b7-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="ef9b7-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ef9b7-116">PARAMETERS</span></span>

### <span data-ttu-id="ef9b7-117">-Context</span><span class="sxs-lookup"><span data-stu-id="ef9b7-117">-Context</span></span>
<span data-ttu-id="ef9b7-118">Geçerli oturumun bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ef9b7-118">Specifies the context for the current session.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef9b7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef9b7-119">-DefaultProfile</span></span>
<span data-ttu-id="ef9b7-120">Azure ile iletişim için kullanılan kimlik bilgileri, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ef9b7-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef9b7-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="ef9b7-121">-ExtendedProperty</span></span>
<span data-ttu-id="ef9b7-122">Ek bağlam özellikleri</span><span class="sxs-lookup"><span data-stu-id="ef9b7-122">Additional context properties</span></span>

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

### <span data-ttu-id="ef9b7-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ef9b7-123">-Force</span></span>
<span data-ttu-id="ef9b7-124">Varsa, var olan içeriğin üzerine yazın.</span><span class="sxs-lookup"><span data-stu-id="ef9b7-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="ef9b7-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="ef9b7-125">-Name</span></span>
<span data-ttu-id="ef9b7-126">Bağlam adı</span><span class="sxs-lookup"><span data-stu-id="ef9b7-126">Name of the context</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef9b7-127">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="ef9b7-127">-Scope</span></span>
<span data-ttu-id="ef9b7-128">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="ef9b7-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef9b7-129">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="ef9b7-129">-Subscription</span></span>
<span data-ttu-id="ef9b7-130">Abonelik adı veya kimliği</span><span class="sxs-lookup"><span data-stu-id="ef9b7-130">Subscription Name or Id</span></span>

```yaml
Type: String
Parameter Sets: Subscription
Aliases: SubscriptionId, SubscriptionName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef9b7-131">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="ef9b7-131">-SubscriptionObject</span></span>
<span data-ttu-id="ef9b7-132">Bir abonelik nesnesi</span><span class="sxs-lookup"><span data-stu-id="ef9b7-132">A subscription object</span></span>

```yaml
Type: PSAzureSubscription
Parameter Sets: SubscriptionObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef9b7-133">-Tenant</span><span class="sxs-lookup"><span data-stu-id="ef9b7-133">-Tenant</span></span>
<span data-ttu-id="ef9b7-134">Kiracı adı veya KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="ef9b7-134">Tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: Subscription
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: TenantNameOnly
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef9b7-135">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="ef9b7-135">-TenantObject</span></span>
<span data-ttu-id="ef9b7-136">Kiracı nesnesi</span><span class="sxs-lookup"><span data-stu-id="ef9b7-136">A Tenant Object</span></span>

```yaml
Type: PSAzureTenant
Parameter Sets: TenantObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef9b7-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="ef9b7-137">-Confirm</span></span>
<span data-ttu-id="ef9b7-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ef9b7-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef9b7-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef9b7-139">-WhatIf</span></span>
<span data-ttu-id="ef9b7-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ef9b7-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef9b7-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ef9b7-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef9b7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef9b7-142">CommonParameters</span></span>
<span data-ttu-id="ef9b7-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ef9b7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef9b7-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef9b7-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef9b7-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ef9b7-145">INPUTS</span></span>

### <span data-ttu-id="ef9b7-146">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="ef9b7-146">PSAzureContext</span></span>
<span data-ttu-id="ef9b7-147">' Context ' parametresi ardışık düzenin ' PSAzureContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ef9b7-147">Parameter 'Context' accepts value of type 'PSAzureContext' from the pipeline</span></span>

## <span data-ttu-id="ef9b7-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ef9b7-148">OUTPUTS</span></span>

### <span data-ttu-id="ef9b7-149">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="ef9b7-149">PSAzureContext</span></span>

## <span data-ttu-id="ef9b7-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ef9b7-150">NOTES</span></span>

## <span data-ttu-id="ef9b7-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ef9b7-151">RELATED LINKS</span></span>

[<span data-ttu-id="ef9b7-152">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="ef9b7-152">Get-AzureRMContext</span></span>](./Get-AzureRMContext.md)

