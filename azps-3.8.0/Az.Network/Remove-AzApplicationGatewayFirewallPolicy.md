---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 18795b91b6dfe25b64946587dc9199078c4cd727
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097520"
---
# <span data-ttu-id="e35f3-101">Remove-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e35f3-101">Remove-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="e35f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e35f3-102">SYNOPSIS</span></span>
<span data-ttu-id="e35f3-103">Uygulama ağ geçidi güvenlik ilkesi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e35f3-103">Removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="e35f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e35f3-104">SYNTAX</span></span>

### <span data-ttu-id="e35f3-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e35f3-105">ByFactoryName (Default)</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e35f3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e35f3-106">ByFactoryObject</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e35f3-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="e35f3-107">ByResourceId</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e35f3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e35f3-108">DESCRIPTION</span></span>
<span data-ttu-id="e35f3-109">**Remove-AzApplicationGatewayFirewallPolicy** cmdlet 'i uygulama ağ geçidi güvenlik ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e35f3-109">The **Remove-AzApplicationGatewayFirewallPolicy** cmdlet removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="e35f3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e35f3-110">EXAMPLES</span></span>

### <span data-ttu-id="e35f3-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e35f3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzApplicationGatewayFirewallPolicy -Name "ApplicationGatewayFirewallPolicy01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e35f3-112">Bu komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGatewayFirewallPolicy01 adındaki uygulama ağ geçidi güvenlik ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e35f3-112">This command removes the application gateway firewall policy named ApplicationGatewayFirewallPolicy01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="e35f3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e35f3-113">PARAMETERS</span></span>

### <span data-ttu-id="e35f3-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="e35f3-114">-AsJob</span></span>
<span data-ttu-id="e35f3-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e35f3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e35f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e35f3-116">-DefaultProfile</span></span>
<span data-ttu-id="e35f3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e35f3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e35f3-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e35f3-118">-Force</span></span>
<span data-ttu-id="e35f3-119">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="e35f3-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e35f3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e35f3-120">-InputObject</span></span>
<span data-ttu-id="e35f3-121">Güvenlik Duvarı ilke nesnesi</span><span class="sxs-lookup"><span data-stu-id="e35f3-121">The firewall policy object</span></span>

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

### <span data-ttu-id="e35f3-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="e35f3-122">-Name</span></span>
<span data-ttu-id="e35f3-123">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="e35f3-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35f3-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e35f3-124">-PassThru</span></span>
<span data-ttu-id="e35f3-125">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="e35f3-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e35f3-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="e35f3-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e35f3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e35f3-127">-ResourceGroupName</span></span>
<span data-ttu-id="e35f3-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e35f3-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35f3-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e35f3-129">-ResourceId</span></span>
<span data-ttu-id="e35f3-130">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="e35f3-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e35f3-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="e35f3-131">-Confirm</span></span>
<span data-ttu-id="e35f3-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e35f3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e35f3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e35f3-133">-WhatIf</span></span>
<span data-ttu-id="e35f3-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e35f3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e35f3-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e35f3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e35f3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e35f3-136">CommonParameters</span></span>
<span data-ttu-id="e35f3-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e35f3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e35f3-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e35f3-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e35f3-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e35f3-139">INPUTS</span></span>

### <span data-ttu-id="e35f3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e35f3-140">System.String</span></span>

## <span data-ttu-id="e35f3-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e35f3-141">OUTPUTS</span></span>

### <span data-ttu-id="e35f3-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e35f3-142">System.Boolean</span></span>

## <span data-ttu-id="e35f3-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e35f3-143">NOTES</span></span>

## <span data-ttu-id="e35f3-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e35f3-144">RELATED LINKS</span></span>
