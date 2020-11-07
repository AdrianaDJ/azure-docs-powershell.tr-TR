---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 359b98d19edfdbdd3c1ce8d6ab7286f13cf5dbfa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764932"
---
# <span data-ttu-id="476fc-101">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="476fc-101">New-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="476fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="476fc-102">SYNOPSIS</span></span>
<span data-ttu-id="476fc-103">Uygulama güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="476fc-103">Creates an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="476fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="476fc-104">SYNTAX</span></span>

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="476fc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="476fc-105">DESCRIPTION</span></span>
<span data-ttu-id="476fc-106">**New-AzureRmApplicationSecurityGroup** cmdlet 'i bir uygulama güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="476fc-106">The **New-AzureRmApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="476fc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="476fc-107">EXAMPLES</span></span>

### <span data-ttu-id="476fc-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="476fc-108">Example 1</span></span>
```
PS C:\> New-AzureRmApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="476fc-109">Bu örnek, ilişkilendirmesi olmayan bir uygulama güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="476fc-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="476fc-110">Oluşturulduğunda, ağ arabirimindeki IP yapılandırmaları gruba dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="476fc-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="476fc-111">Güvenlik kuralları gruba kaynak veya hedef olarak başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="476fc-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="476fc-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="476fc-112">PARAMETERS</span></span>

### <span data-ttu-id="476fc-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="476fc-113">-AsJob</span></span>
<span data-ttu-id="476fc-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="476fc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="476fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="476fc-115">-DefaultProfile</span></span>
<span data-ttu-id="476fc-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="476fc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476fc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="476fc-117">-Force</span></span>
<span data-ttu-id="476fc-118">Kaynağın üzerine yazmak istiyorsanız onay isteyin.</span><span class="sxs-lookup"><span data-stu-id="476fc-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="476fc-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="476fc-119">-Location</span></span>
<span data-ttu-id="476fc-120">Konum.</span><span class="sxs-lookup"><span data-stu-id="476fc-120">The location.</span></span>

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

### <span data-ttu-id="476fc-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="476fc-121">-Name</span></span>
<span data-ttu-id="476fc-122">Uygulama güvenlik grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="476fc-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="476fc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="476fc-123">-ResourceGroupName</span></span>
<span data-ttu-id="476fc-124">Uygulama güvenlik grubunun kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="476fc-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="476fc-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="476fc-125">-Tag</span></span>
<span data-ttu-id="476fc-126">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="476fc-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="476fc-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="476fc-127">-Confirm</span></span>
<span data-ttu-id="476fc-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="476fc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="476fc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="476fc-129">-WhatIf</span></span>
<span data-ttu-id="476fc-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="476fc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="476fc-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="476fc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="476fc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="476fc-132">CommonParameters</span></span>
<span data-ttu-id="476fc-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="476fc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="476fc-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="476fc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="476fc-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="476fc-135">INPUTS</span></span>

### <span data-ttu-id="476fc-136">System. String</span><span class="sxs-lookup"><span data-stu-id="476fc-136">System.String</span></span>

### <span data-ttu-id="476fc-137">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="476fc-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="476fc-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="476fc-138">OUTPUTS</span></span>

### <span data-ttu-id="476fc-139">Microsoft. Azure. Commands. Network. modeller. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="476fc-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="476fc-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="476fc-140">NOTES</span></span>

## <span data-ttu-id="476fc-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="476fc-141">RELATED LINKS</span></span>

[<span data-ttu-id="476fc-142">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="476fc-142">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="476fc-143">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="476fc-143">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="476fc-144">Yeni-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="476fc-144">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="476fc-145">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="476fc-145">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="476fc-146">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="476fc-146">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="476fc-147">Yeni-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="476fc-147">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="476fc-148">Add-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="476fc-148">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="476fc-149">Set-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="476fc-149">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)
