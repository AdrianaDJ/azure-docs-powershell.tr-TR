---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 75c8f7b52fec0e429820d43f86a8a41798b1d5f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918219"
---
# <span data-ttu-id="7faf8-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7faf8-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="7faf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7faf8-102">SYNOPSIS</span></span>
<span data-ttu-id="7faf8-103">Özel bağlantı hizmeti oluşturur</span><span class="sxs-lookup"><span data-stu-id="7faf8-103">Creates a private link service</span></span>

## <span data-ttu-id="7faf8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7faf8-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7faf8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7faf8-105">DESCRIPTION</span></span>
<span data-ttu-id="7faf8-106">**Yeni-AzPrivateLinkService** cmdlet 'i özel bir bağlantı hizmeti oluşturur</span><span class="sxs-lookup"><span data-stu-id="7faf8-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="7faf8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7faf8-107">EXAMPLES</span></span>

### <span data-ttu-id="7faf8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7faf8-108">Example 1</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
New-AzPrivateLinkService -Name "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

<span data-ttu-id="7faf8-109">Bu örnek özel bir bağlantı hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7faf8-109">This example creates a private link service.</span></span>

## <span data-ttu-id="7faf8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7faf8-110">PARAMETERS</span></span>

### <span data-ttu-id="7faf8-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="7faf8-111">-AsJob</span></span>
<span data-ttu-id="7faf8-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7faf8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7faf8-113">-Otomatik onay</span><span class="sxs-lookup"><span data-stu-id="7faf8-113">-AutoApproval</span></span>
<span data-ttu-id="7faf8-114">Özel bağlantı hizmeti 'nin otomatik onay abonelikleri</span><span class="sxs-lookup"><span data-stu-id="7faf8-114">The auto approval subscriptions of private link service</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7faf8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7faf8-115">-DefaultProfile</span></span>
<span data-ttu-id="7faf8-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7faf8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7faf8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7faf8-117">-Force</span></span>
<span data-ttu-id="7faf8-118">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="7faf8-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7faf8-119">-IP yapılandırması</span><span class="sxs-lookup"><span data-stu-id="7faf8-119">-IpConfiguration</span></span>
<span data-ttu-id="7faf8-120">IP yapılandırmaları</span><span class="sxs-lookup"><span data-stu-id="7faf8-120">The ip configurations</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7faf8-121">-Loadbalancerfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="7faf8-121">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="7faf8-122">Ön uç IP yapılandırmaları</span><span class="sxs-lookup"><span data-stu-id="7faf8-122">The front end ip configurations</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7faf8-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="7faf8-123">-Location</span></span>
<span data-ttu-id="7faf8-124">konumuyla.</span><span class="sxs-lookup"><span data-stu-id="7faf8-124">location.</span></span>

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

### <span data-ttu-id="7faf8-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="7faf8-125">-Name</span></span>
<span data-ttu-id="7faf8-126">Hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="7faf8-126">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7faf8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7faf8-127">-ResourceGroupName</span></span>
<span data-ttu-id="7faf8-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7faf8-128">The resource group name.</span></span>

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

### <span data-ttu-id="7faf8-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7faf8-129">-Tag</span></span>
<span data-ttu-id="7faf8-130">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="7faf8-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7faf8-131">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="7faf8-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7faf8-132">-Görünürlük</span><span class="sxs-lookup"><span data-stu-id="7faf8-132">-Visibility</span></span>
<span data-ttu-id="7faf8-133">Özel bağlantı hizmetinin görünürlük abonelikleri</span><span class="sxs-lookup"><span data-stu-id="7faf8-133">The visibility subscriptions of private link service</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7faf8-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="7faf8-134">-Confirm</span></span>
<span data-ttu-id="7faf8-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7faf8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7faf8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7faf8-136">-WhatIf</span></span>
<span data-ttu-id="7faf8-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7faf8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7faf8-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7faf8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7faf8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7faf8-139">CommonParameters</span></span>
<span data-ttu-id="7faf8-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7faf8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7faf8-141">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7faf8-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7faf8-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7faf8-142">INPUTS</span></span>

### <span data-ttu-id="7faf8-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7faf8-143">System.String</span></span>

### <span data-ttu-id="7faf8-144">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration []</span><span class="sxs-lookup"><span data-stu-id="7faf8-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="7faf8-145">Microsoft. Azure. Commands. Network. model. Psprivatelinkserviceıp []</span><span class="sxs-lookup"><span data-stu-id="7faf8-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="7faf8-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7faf8-146">OUTPUTS</span></span>

### <span data-ttu-id="7faf8-147">Microsoft. Azure. Commands. Network. model. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7faf8-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="7faf8-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7faf8-148">NOTES</span></span>

## <span data-ttu-id="7faf8-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7faf8-149">RELATED LINKS</span></span>

[<span data-ttu-id="7faf8-150">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7faf8-150">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="7faf8-151">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7faf8-151">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="7faf8-152">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7faf8-152">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
