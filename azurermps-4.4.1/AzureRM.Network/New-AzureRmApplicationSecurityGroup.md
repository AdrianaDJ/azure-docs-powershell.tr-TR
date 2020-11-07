---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 97a49535ab02b2ccd75a1f7520bcd8a1e3e6264f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764044"
---
# <span data-ttu-id="2af63-101">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2af63-101">New-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="2af63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2af63-102">SYNOPSIS</span></span>
<span data-ttu-id="2af63-103">Uygulama güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2af63-103">Creates an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2af63-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2af63-104">SYNTAX</span></span>

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2af63-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2af63-105">DESCRIPTION</span></span>
<span data-ttu-id="2af63-106">**New-AzureRmApplicationSecurityGroup** cmdlet 'i bir uygulama güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2af63-106">The **New-AzureRmApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="2af63-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2af63-107">EXAMPLES</span></span>

### <span data-ttu-id="2af63-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2af63-108">Example 1</span></span>
```
PS C:\> New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="2af63-109">Bu örnek, ilişkilendirmesi olmayan bir uygulama güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2af63-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="2af63-110">Oluşturulduğunda, ağ arabirimindeki IP yapılandırmaları gruba dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="2af63-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="2af63-111">Güvenlik kuralları gruba kaynak veya hedef olarak başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="2af63-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="2af63-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2af63-112">PARAMETERS</span></span>

### <span data-ttu-id="2af63-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2af63-113">-DefaultProfile</span></span>
<span data-ttu-id="2af63-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2af63-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2af63-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2af63-115">-Force</span></span>
<span data-ttu-id="2af63-116">Kaynağın üzerine yazmak istiyorsanız onay isteyin.</span><span class="sxs-lookup"><span data-stu-id="2af63-116">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="2af63-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="2af63-117">-Location</span></span>
<span data-ttu-id="2af63-118">Konum.</span><span class="sxs-lookup"><span data-stu-id="2af63-118">The location.</span></span>

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

### <span data-ttu-id="2af63-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="2af63-119">-Name</span></span>
<span data-ttu-id="2af63-120">Uygulama güvenlik grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2af63-120">The name of the application security group.</span></span>

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

### <span data-ttu-id="2af63-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2af63-121">-ResourceGroupName</span></span>
<span data-ttu-id="2af63-122">Uygulama güvenlik grubunun kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2af63-122">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="2af63-123">Etiketli</span><span class="sxs-lookup"><span data-stu-id="2af63-123">-Tag</span></span>
<span data-ttu-id="2af63-124">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="2af63-124">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="2af63-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="2af63-125">-Confirm</span></span>
<span data-ttu-id="2af63-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2af63-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2af63-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2af63-127">-WhatIf</span></span>
<span data-ttu-id="2af63-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2af63-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2af63-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2af63-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2af63-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2af63-130">CommonParameters</span></span>
<span data-ttu-id="2af63-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2af63-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2af63-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2af63-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2af63-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2af63-133">INPUTS</span></span>

### <span data-ttu-id="2af63-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2af63-134">System.String</span></span>
<span data-ttu-id="2af63-135">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2af63-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2af63-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2af63-136">OUTPUTS</span></span>

### <span data-ttu-id="2af63-137">Microsoft. Azure. Commands. Network. modeller. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2af63-137">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="2af63-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2af63-138">NOTES</span></span>

## <span data-ttu-id="2af63-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2af63-139">RELATED LINKS</span></span>

[<span data-ttu-id="2af63-140">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2af63-140">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="2af63-141">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2af63-141">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="2af63-142">Yeni-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2af63-142">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="2af63-143">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2af63-143">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="2af63-144">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2af63-144">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="2af63-145">Yeni-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="2af63-145">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="2af63-146">Add-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="2af63-146">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="2af63-147">Set-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="2af63-147">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)
