---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 81eaa1f5c6e44586ae6ac9e5b6838f00063a9211
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935408"
---
# <span data-ttu-id="0b5fa-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0b5fa-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="0b5fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b5fa-102">SYNOPSIS</span></span>
<span data-ttu-id="0b5fa-103">Uygulama güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-103">Creates an application security group.</span></span>

## <span data-ttu-id="0b5fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b5fa-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b5fa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b5fa-105">DESCRIPTION</span></span>
<span data-ttu-id="0b5fa-106">**Yeni-AzApplicationSecurityGroup** cmdlet 'i uygulama güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="0b5fa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b5fa-107">EXAMPLES</span></span>

### <span data-ttu-id="0b5fa-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0b5fa-108">Example 1</span></span>
```
PS C:\> New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="0b5fa-109">Bu örnek, ilişkilendirmesi olmayan bir uygulama güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="0b5fa-110">Oluşturulduğunda, ağ arabirimindeki IP yapılandırmaları gruba dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="0b5fa-111">Güvenlik kuralları gruba kaynak veya hedef olarak başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="0b5fa-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b5fa-112">PARAMETERS</span></span>

### <span data-ttu-id="0b5fa-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="0b5fa-113">-AsJob</span></span>
<span data-ttu-id="0b5fa-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0b5fa-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b5fa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b5fa-115">-DefaultProfile</span></span>
<span data-ttu-id="0b5fa-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b5fa-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0b5fa-117">-Force</span></span>
<span data-ttu-id="0b5fa-118">Kaynağın üzerine yazmak istiyorsanız onay isteyin.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="0b5fa-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="0b5fa-119">-Location</span></span>
<span data-ttu-id="0b5fa-120">Konum.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-120">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b5fa-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="0b5fa-121">-Name</span></span>
<span data-ttu-id="0b5fa-122">Uygulama güvenlik grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-122">The name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b5fa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b5fa-123">-ResourceGroupName</span></span>
<span data-ttu-id="0b5fa-124">Uygulama güvenlik grubunun kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-124">The resource group name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b5fa-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="0b5fa-125">-Tag</span></span>
<span data-ttu-id="0b5fa-126">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b5fa-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="0b5fa-127">-Confirm</span></span>
<span data-ttu-id="0b5fa-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b5fa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b5fa-129">-WhatIf</span></span>
<span data-ttu-id="0b5fa-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b5fa-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b5fa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b5fa-132">CommonParameters</span></span>
<span data-ttu-id="0b5fa-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b5fa-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b5fa-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b5fa-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b5fa-135">INPUTS</span></span>

### <span data-ttu-id="0b5fa-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0b5fa-136">System.String</span></span>
<span data-ttu-id="0b5fa-137">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0b5fa-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0b5fa-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b5fa-138">OUTPUTS</span></span>

### <span data-ttu-id="0b5fa-139">Microsoft. Azure. Commands. Network. modeller. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0b5fa-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="0b5fa-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b5fa-140">NOTES</span></span>

## <span data-ttu-id="0b5fa-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b5fa-141">RELATED LINKS</span></span>

[<span data-ttu-id="0b5fa-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0b5fa-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="0b5fa-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0b5fa-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="0b5fa-144">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b5fa-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0b5fa-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b5fa-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0b5fa-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b5fa-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0b5fa-147">New-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="0b5fa-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="0b5fa-148">Add-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="0b5fa-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="0b5fa-149">Set-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="0b5fa-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
