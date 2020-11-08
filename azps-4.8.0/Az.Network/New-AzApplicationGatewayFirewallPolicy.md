---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 03e03de70f61672d1246ffeb8469efe0c04b3ea4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109477"
---
# <span data-ttu-id="3b3ae-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="3b3ae-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="3b3ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b3ae-102">SYNOPSIS</span></span>
<span data-ttu-id="3b3ae-103">Uygulama ağ geçidi güvenlik duvarı ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="3b3ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b3ae-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b3ae-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b3ae-105">DESCRIPTION</span></span>
<span data-ttu-id="3b3ae-106">**Yeni-AzApplicationGatewayFirewallPolicy** cmdlet 'i uygulama ağ geçidi güvenlik ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="3b3ae-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b3ae-107">EXAMPLES</span></span>

### <span data-ttu-id="3b3ae-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3b3ae-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRule $customRule
```

<span data-ttu-id="3b3ae-109">Bu komut, $customRule değişkeninde tanımlanan özel kurallarla "westus" kaynak grubunda "RG1" kaynak grubunda "" adlı yeni bir Azure uygulama ağ geçidi güvenlik ilkesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="3b3ae-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="3b3ae-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b3ae-110">PARAMETERS</span></span>

### <span data-ttu-id="3b3ae-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="3b3ae-111">-AsJob</span></span>
<span data-ttu-id="3b3ae-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3b3ae-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3b3ae-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="3b3ae-113">-CustomRule</span></span>
<span data-ttu-id="3b3ae-114">CustomRules listesi</span><span class="sxs-lookup"><span data-stu-id="3b3ae-114">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b3ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b3ae-115">-DefaultProfile</span></span>
<span data-ttu-id="3b3ae-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b3ae-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3b3ae-117">-Force</span></span>
<span data-ttu-id="3b3ae-118">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="3b3ae-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="3b3ae-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="3b3ae-119">-Location</span></span>
<span data-ttu-id="3b3ae-120">konumuyla.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-120">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b3ae-121">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="3b3ae-121">-ManagedRule</span></span>
<span data-ttu-id="3b3ae-122">Yönetilen kural ayarı</span><span class="sxs-lookup"><span data-stu-id="3b3ae-122">Managed Rule Setting</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b3ae-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="3b3ae-123">-Name</span></span>
<span data-ttu-id="3b3ae-124">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b3ae-125">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="3b3ae-125">-PolicySetting</span></span>
<span data-ttu-id="3b3ae-126">Web uygulaması güvenlik duvarı için ilke ayarları</span><span class="sxs-lookup"><span data-stu-id="3b3ae-126">Policy Settings for Web Application Firewall</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b3ae-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b3ae-127">-ResourceGroupName</span></span>
<span data-ttu-id="3b3ae-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b3ae-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3b3ae-129">-Tag</span></span>
<span data-ttu-id="3b3ae-130">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b3ae-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="3b3ae-131">-Confirm</span></span>
<span data-ttu-id="3b3ae-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b3ae-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b3ae-133">-WhatIf</span></span>
<span data-ttu-id="3b3ae-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b3ae-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b3ae-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b3ae-136">CommonParameters</span></span>
<span data-ttu-id="3b3ae-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b3ae-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b3ae-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b3ae-139">INPUTS</span></span>

### <span data-ttu-id="3b3ae-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3b3ae-140">System.String</span></span>

### <span data-ttu-id="3b3ae-141">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallCustomRule []</span><span class="sxs-lookup"><span data-stu-id="3b3ae-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="3b3ae-142">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="3b3ae-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

### <span data-ttu-id="3b3ae-143">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="3b3ae-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

### <span data-ttu-id="3b3ae-144">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3b3ae-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3b3ae-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b3ae-145">OUTPUTS</span></span>

### <span data-ttu-id="3b3ae-146">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="3b3ae-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="3b3ae-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b3ae-147">NOTES</span></span>

## <span data-ttu-id="3b3ae-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b3ae-148">RELATED LINKS</span></span>
