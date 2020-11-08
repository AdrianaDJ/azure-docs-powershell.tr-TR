---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 0b4cc79358723e6249a0c9d4e22929e224165402
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098741"
---
# <span data-ttu-id="218d2-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="218d2-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="218d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="218d2-102">SYNOPSIS</span></span>
<span data-ttu-id="218d2-103">Özel bağlantı hizmeti oluşturur</span><span class="sxs-lookup"><span data-stu-id="218d2-103">Creates a private link service</span></span>

## <span data-ttu-id="218d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="218d2-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="218d2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="218d2-105">DESCRIPTION</span></span>
<span data-ttu-id="218d2-106">**Yeni-AzPrivateLinkService** cmdlet 'i özel bir bağlantı hizmeti oluşturur</span><span class="sxs-lookup"><span data-stu-id="218d2-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="218d2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="218d2-107">EXAMPLES</span></span>

### <span data-ttu-id="218d2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="218d2-108">Example 1</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
New-AzPrivateLinkService -Name "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

<span data-ttu-id="218d2-109">Bu örnek özel bir bağlantı hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="218d2-109">This example creates a private link service.</span></span>

## <span data-ttu-id="218d2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="218d2-110">PARAMETERS</span></span>

### <span data-ttu-id="218d2-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="218d2-111">-AsJob</span></span>
<span data-ttu-id="218d2-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="218d2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="218d2-113">-Otomatik onay</span><span class="sxs-lookup"><span data-stu-id="218d2-113">-AutoApproval</span></span>
<span data-ttu-id="218d2-114">Özel bağlantı hizmeti 'nin otomatik onay abonelikleri</span><span class="sxs-lookup"><span data-stu-id="218d2-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="218d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="218d2-115">-DefaultProfile</span></span>
<span data-ttu-id="218d2-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="218d2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="218d2-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="218d2-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="218d2-118">Özel bağlantı hizmeti için proxy protokolünü etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="218d2-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="218d2-119">-Force</span><span class="sxs-lookup"><span data-stu-id="218d2-119">-Force</span></span>
<span data-ttu-id="218d2-120">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="218d2-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="218d2-121">-IP yapılandırması</span><span class="sxs-lookup"><span data-stu-id="218d2-121">-IpConfiguration</span></span>
<span data-ttu-id="218d2-122">IP yapılandırmaları</span><span class="sxs-lookup"><span data-stu-id="218d2-122">The ip configurations</span></span>

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

### <span data-ttu-id="218d2-123">-Loadbalancerfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="218d2-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="218d2-124">Ön uç IP yapılandırmaları</span><span class="sxs-lookup"><span data-stu-id="218d2-124">The front end ip configurations</span></span>

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

### <span data-ttu-id="218d2-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="218d2-125">-Location</span></span>
<span data-ttu-id="218d2-126">konumuyla.</span><span class="sxs-lookup"><span data-stu-id="218d2-126">location.</span></span>

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

### <span data-ttu-id="218d2-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="218d2-127">-Name</span></span>
<span data-ttu-id="218d2-128">Hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="218d2-128">The name of the service.</span></span>

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

### <span data-ttu-id="218d2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="218d2-129">-ResourceGroupName</span></span>
<span data-ttu-id="218d2-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="218d2-130">The resource group name.</span></span>

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

### <span data-ttu-id="218d2-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="218d2-131">-Tag</span></span>
<span data-ttu-id="218d2-132">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="218d2-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="218d2-133">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="218d2-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="218d2-134">-Görünürlük</span><span class="sxs-lookup"><span data-stu-id="218d2-134">-Visibility</span></span>
<span data-ttu-id="218d2-135">Özel bağlantı hizmetinin görünürlük abonelikleri</span><span class="sxs-lookup"><span data-stu-id="218d2-135">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="218d2-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="218d2-136">-Confirm</span></span>
<span data-ttu-id="218d2-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="218d2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="218d2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="218d2-138">-WhatIf</span></span>
<span data-ttu-id="218d2-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="218d2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="218d2-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="218d2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="218d2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="218d2-141">CommonParameters</span></span>
<span data-ttu-id="218d2-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="218d2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="218d2-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="218d2-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="218d2-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="218d2-144">INPUTS</span></span>

### <span data-ttu-id="218d2-145">System. String</span><span class="sxs-lookup"><span data-stu-id="218d2-145">System.String</span></span>

### <span data-ttu-id="218d2-146">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration []</span><span class="sxs-lookup"><span data-stu-id="218d2-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="218d2-147">Microsoft. Azure. Commands. Network. model. Psprivatelinkserviceıp []</span><span class="sxs-lookup"><span data-stu-id="218d2-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="218d2-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="218d2-148">OUTPUTS</span></span>

### <span data-ttu-id="218d2-149">Microsoft. Azure. Commands. Network. model. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="218d2-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="218d2-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="218d2-150">NOTES</span></span>

## <span data-ttu-id="218d2-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="218d2-151">RELATED LINKS</span></span>

[<span data-ttu-id="218d2-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="218d2-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="218d2-153">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="218d2-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="218d2-154">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="218d2-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
