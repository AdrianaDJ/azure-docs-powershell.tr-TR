---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 32d7767ac5bd43be8fb9a3129966a0a88d761953
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278559"
---
# <span data-ttu-id="4d677-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4d677-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="4d677-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d677-102">SYNOPSIS</span></span>
<span data-ttu-id="4d677-103">Uygulama güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4d677-103">Creates an application security group.</span></span>

## <span data-ttu-id="4d677-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d677-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d677-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d677-105">DESCRIPTION</span></span>
<span data-ttu-id="4d677-106">**Yeni-AzApplicationSecurityGroup** cmdlet 'i uygulama güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4d677-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="4d677-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d677-107">EXAMPLES</span></span>

### <span data-ttu-id="4d677-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4d677-108">Example 1</span></span>
```
PS C:\> New-AzApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="4d677-109">Bu örnek, ilişkilendirmesi olmayan bir uygulama güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4d677-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="4d677-110">Oluşturulduğunda, ağ arabirimindeki IP yapılandırmaları gruba dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="4d677-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="4d677-111">Güvenlik kuralları gruba kaynak veya hedef olarak başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="4d677-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="4d677-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d677-112">PARAMETERS</span></span>

### <span data-ttu-id="4d677-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="4d677-113">-AsJob</span></span>
<span data-ttu-id="4d677-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4d677-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d677-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d677-115">-DefaultProfile</span></span>
<span data-ttu-id="4d677-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4d677-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d677-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4d677-117">-Force</span></span>
<span data-ttu-id="4d677-118">Kaynağın üzerine yazmak istiyorsanız onay isteyin.</span><span class="sxs-lookup"><span data-stu-id="4d677-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="4d677-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="4d677-119">-Location</span></span>
<span data-ttu-id="4d677-120">Konum.</span><span class="sxs-lookup"><span data-stu-id="4d677-120">The location.</span></span>

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

### <span data-ttu-id="4d677-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="4d677-121">-Name</span></span>
<span data-ttu-id="4d677-122">Uygulama güvenlik grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4d677-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="4d677-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d677-123">-ResourceGroupName</span></span>
<span data-ttu-id="4d677-124">Uygulama güvenlik grubunun kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4d677-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="4d677-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="4d677-125">-Tag</span></span>
<span data-ttu-id="4d677-126">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="4d677-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4d677-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="4d677-127">-Confirm</span></span>
<span data-ttu-id="4d677-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4d677-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d677-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d677-129">-WhatIf</span></span>
<span data-ttu-id="4d677-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d677-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d677-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4d677-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d677-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d677-132">CommonParameters</span></span>
<span data-ttu-id="4d677-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d677-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d677-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d677-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d677-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d677-135">INPUTS</span></span>

### <span data-ttu-id="4d677-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4d677-136">System.String</span></span>

### <span data-ttu-id="4d677-137">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4d677-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4d677-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d677-138">OUTPUTS</span></span>

### <span data-ttu-id="4d677-139">Microsoft. Azure. Commands. Network. modeller. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4d677-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="4d677-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d677-140">NOTES</span></span>

## <span data-ttu-id="4d677-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d677-141">RELATED LINKS</span></span>

[<span data-ttu-id="4d677-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4d677-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="4d677-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4d677-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="4d677-144">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4d677-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4d677-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4d677-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4d677-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4d677-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4d677-147">New-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="4d677-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4d677-148">Add-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="4d677-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4d677-149">Set-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="4d677-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
