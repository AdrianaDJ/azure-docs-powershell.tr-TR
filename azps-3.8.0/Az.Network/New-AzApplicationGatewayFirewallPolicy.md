---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: da83c8cd863d8d3cfa62d47c7a4126d15c4dd670
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104818"
---
# <span data-ttu-id="4b57f-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="4b57f-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="4b57f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b57f-102">SYNOPSIS</span></span>
<span data-ttu-id="4b57f-103">Uygulama ağ geçidi güvenlik duvarı ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4b57f-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="4b57f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b57f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b57f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b57f-105">DESCRIPTION</span></span>
<span data-ttu-id="4b57f-106">**Yeni-AzApplicationGatewayFirewallPolicy** cmdlet 'i uygulama ağ geçidi güvenlik ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4b57f-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="4b57f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b57f-107">EXAMPLES</span></span>

### <span data-ttu-id="4b57f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4b57f-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRules $customRule
```

<span data-ttu-id="4b57f-109">Bu komut, $customRule değişkeninde tanımlanan özel kurallarla "westus" kaynak grubunda "RG1" kaynak grubunda "" adlı yeni bir Azure uygulama ağ geçidi güvenlik ilkesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="4b57f-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="4b57f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b57f-110">PARAMETERS</span></span>

### <span data-ttu-id="4b57f-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="4b57f-111">-AsJob</span></span>
<span data-ttu-id="4b57f-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4b57f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b57f-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="4b57f-113">-CustomRule</span></span>
<span data-ttu-id="4b57f-114">CustomRules listesi</span><span class="sxs-lookup"><span data-stu-id="4b57f-114">The list of CustomRules</span></span>

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

### <span data-ttu-id="4b57f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b57f-115">-DefaultProfile</span></span>
<span data-ttu-id="4b57f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b57f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b57f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4b57f-117">-Force</span></span>
<span data-ttu-id="4b57f-118">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="4b57f-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4b57f-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="4b57f-119">-Location</span></span>
<span data-ttu-id="4b57f-120">konumuyla.</span><span class="sxs-lookup"><span data-stu-id="4b57f-120">location.</span></span>

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

### <span data-ttu-id="4b57f-121">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="4b57f-121">-ManagedRule</span></span>
<span data-ttu-id="4b57f-122">Yönetilen kural ayarı</span><span class="sxs-lookup"><span data-stu-id="4b57f-122">Managed Rule Setting</span></span>

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

### <span data-ttu-id="4b57f-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="4b57f-123">-Name</span></span>
<span data-ttu-id="4b57f-124">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="4b57f-124">The resource name.</span></span>

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

### <span data-ttu-id="4b57f-125">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="4b57f-125">-PolicySetting</span></span>
<span data-ttu-id="4b57f-126">Web uygulaması güvenlik duvarı için ilke ayarları</span><span class="sxs-lookup"><span data-stu-id="4b57f-126">Policy Settings for Web Application Firewall</span></span>

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

### <span data-ttu-id="4b57f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b57f-127">-ResourceGroupName</span></span>
<span data-ttu-id="4b57f-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4b57f-128">The resource group name.</span></span>

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

### <span data-ttu-id="4b57f-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="4b57f-129">-Tag</span></span>
<span data-ttu-id="4b57f-130">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="4b57f-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4b57f-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="4b57f-131">-Confirm</span></span>
<span data-ttu-id="4b57f-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4b57f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b57f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b57f-133">-WhatIf</span></span>
<span data-ttu-id="4b57f-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b57f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b57f-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4b57f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b57f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b57f-136">CommonParameters</span></span>
<span data-ttu-id="4b57f-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b57f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b57f-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4b57f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b57f-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b57f-139">INPUTS</span></span>

### <span data-ttu-id="4b57f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4b57f-140">System.String</span></span>

### <span data-ttu-id="4b57f-141">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallCustomRule []</span><span class="sxs-lookup"><span data-stu-id="4b57f-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="4b57f-142">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="4b57f-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

### <span data-ttu-id="4b57f-143">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="4b57f-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

### <span data-ttu-id="4b57f-144">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4b57f-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4b57f-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b57f-145">OUTPUTS</span></span>

### <span data-ttu-id="4b57f-146">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="4b57f-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="4b57f-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b57f-147">NOTES</span></span>

## <span data-ttu-id="4b57f-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b57f-148">RELATED LINKS</span></span>
