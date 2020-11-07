---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: dc6005c77a72b3965f2fca670c1d729fc7c7bd07
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931935"
---
# <span data-ttu-id="f34aa-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f34aa-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="f34aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f34aa-102">SYNOPSIS</span></span>
<span data-ttu-id="f34aa-103">Uygulama ağ geçidi güvenlik duvarı ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f34aa-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="f34aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f34aa-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f34aa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f34aa-105">DESCRIPTION</span></span>
<span data-ttu-id="f34aa-106">**Yeni-AzApplicationGatewayFirewallPolicy** cmdlet 'i uygulama ağ geçidi güvenlik ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f34aa-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="f34aa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f34aa-107">EXAMPLES</span></span>

### <span data-ttu-id="f34aa-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f34aa-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRules $customRule
```

<span data-ttu-id="f34aa-109">Bu komut, $customRule değişkeninde tanımlanan özel kurallarla "westus" kaynak grubunda "RG1" kaynak grubunda "" adlı yeni bir Azure uygulama ağ geçidi güvenlik ilkesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="f34aa-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="f34aa-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f34aa-110">PARAMETERS</span></span>

### <span data-ttu-id="f34aa-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="f34aa-111">-AsJob</span></span>
<span data-ttu-id="f34aa-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f34aa-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f34aa-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="f34aa-113">-CustomRule</span></span>
<span data-ttu-id="f34aa-114">CustomRules listesi</span><span class="sxs-lookup"><span data-stu-id="f34aa-114">The list of CustomRules</span></span>

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

### <span data-ttu-id="f34aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f34aa-115">-DefaultProfile</span></span>
<span data-ttu-id="f34aa-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f34aa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f34aa-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f34aa-117">-Force</span></span>
<span data-ttu-id="f34aa-118">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="f34aa-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f34aa-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="f34aa-119">-Location</span></span>
<span data-ttu-id="f34aa-120">konumuyla.</span><span class="sxs-lookup"><span data-stu-id="f34aa-120">location.</span></span>

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

### <span data-ttu-id="f34aa-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="f34aa-121">-Name</span></span>
<span data-ttu-id="f34aa-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="f34aa-122">The resource name.</span></span>

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

### <span data-ttu-id="f34aa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f34aa-123">-ResourceGroupName</span></span>
<span data-ttu-id="f34aa-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f34aa-124">The resource group name.</span></span>

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

### <span data-ttu-id="f34aa-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f34aa-125">-Tag</span></span>
<span data-ttu-id="f34aa-126">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="f34aa-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f34aa-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="f34aa-127">-Confirm</span></span>
<span data-ttu-id="f34aa-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f34aa-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f34aa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f34aa-129">-WhatIf</span></span>
<span data-ttu-id="f34aa-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f34aa-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f34aa-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f34aa-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f34aa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f34aa-132">CommonParameters</span></span>
<span data-ttu-id="f34aa-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f34aa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f34aa-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f34aa-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f34aa-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f34aa-135">INPUTS</span></span>

### <span data-ttu-id="f34aa-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f34aa-136">System.String</span></span>

### <span data-ttu-id="f34aa-137">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallCustomRule []</span><span class="sxs-lookup"><span data-stu-id="f34aa-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="f34aa-138">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f34aa-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f34aa-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f34aa-139">OUTPUTS</span></span>

### <span data-ttu-id="f34aa-140">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f34aa-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="f34aa-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f34aa-141">NOTES</span></span>

## <span data-ttu-id="f34aa-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f34aa-142">RELATED LINKS</span></span>