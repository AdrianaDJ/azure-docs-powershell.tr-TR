---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: bc869f6bccd2b87927b0cbe3b73cedc1999a261c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096880"
---
# <span data-ttu-id="78e82-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="78e82-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="78e82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78e82-102">SYNOPSIS</span></span>
<span data-ttu-id="78e82-103">Uygulama ağ geçidi güvenlik ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="78e82-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="78e82-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="78e82-104">SYNTAX</span></span>

### <span data-ttu-id="78e82-105">ByFactoryObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="78e82-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78e82-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="78e82-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78e82-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="78e82-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78e82-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="78e82-108">DESCRIPTION</span></span>
<span data-ttu-id="78e82-109">**Set-AzApplicationGatewayFirewallPolicy** cmdlet 'i, bir Azure uygulama ağ geçidi güvenlik duvarı ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="78e82-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="78e82-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="78e82-110">EXAMPLES</span></span>

### <span data-ttu-id="78e82-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="78e82-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="78e82-112">Bu komut, uygulama ağ geçidi güvenlik ilkesini $AppGwFirewallPolicy değişkeninde ayarlarla güncelleştirir ve güncelleştirilmiş ağ geçidini $UpdatedAppGwFirewallPolicy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="78e82-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="78e82-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="78e82-113">PARAMETERS</span></span>

### <span data-ttu-id="78e82-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="78e82-114">-AsJob</span></span>
<span data-ttu-id="78e82-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="78e82-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78e82-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="78e82-116">-CustomRule</span></span>
<span data-ttu-id="78e82-117">CustomRules listesi</span><span class="sxs-lookup"><span data-stu-id="78e82-117">The list of CustomRules</span></span>

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

### <span data-ttu-id="78e82-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78e82-118">-DefaultProfile</span></span>
<span data-ttu-id="78e82-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="78e82-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78e82-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78e82-120">-InputObject</span></span>
<span data-ttu-id="78e82-121">ApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="78e82-121">The applicationGatewayFirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78e82-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="78e82-122">-ManagedRule</span></span>
<span data-ttu-id="78e82-123">Güvenlik Duvarı ilkesinin ManagedRules</span><span class="sxs-lookup"><span data-stu-id="78e82-123">ManagedRules of the firewall policy</span></span>

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

### <span data-ttu-id="78e82-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="78e82-124">-Name</span></span>
<span data-ttu-id="78e82-125">Güvenlik Duvarı Ilke adı.</span><span class="sxs-lookup"><span data-stu-id="78e82-125">The Firewall Policy Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78e82-126">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="78e82-126">-PolicySetting</span></span>
<span data-ttu-id="78e82-127">Güvenlik Duvarı ilkesinin policysettings</span><span class="sxs-lookup"><span data-stu-id="78e82-127">Policysettings of the firewall policy</span></span>

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

### <span data-ttu-id="78e82-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78e82-128">-ResourceGroupName</span></span>
<span data-ttu-id="78e82-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="78e82-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78e82-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="78e82-130">-ResourceId</span></span>
<span data-ttu-id="78e82-131">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="78e82-131">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78e82-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="78e82-132">-Confirm</span></span>
<span data-ttu-id="78e82-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="78e82-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78e82-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78e82-134">-WhatIf</span></span>
<span data-ttu-id="78e82-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="78e82-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78e82-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="78e82-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78e82-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78e82-137">CommonParameters</span></span>
<span data-ttu-id="78e82-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="78e82-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78e82-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="78e82-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78e82-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="78e82-140">INPUTS</span></span>

### <span data-ttu-id="78e82-141">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="78e82-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="78e82-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="78e82-142">OUTPUTS</span></span>

### <span data-ttu-id="78e82-143">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="78e82-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="78e82-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="78e82-144">NOTES</span></span>

## <span data-ttu-id="78e82-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="78e82-145">RELATED LINKS</span></span>