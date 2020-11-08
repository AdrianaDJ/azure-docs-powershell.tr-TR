---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 2723ca0f5bebfbf65fefbfbd94fa995d544d9f71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274364"
---
# <span data-ttu-id="bc848-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bc848-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="bc848-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc848-102">SYNOPSIS</span></span>
<span data-ttu-id="bc848-103">Özel bağlantı hizmeti oluşturur</span><span class="sxs-lookup"><span data-stu-id="bc848-103">Creates a private link service</span></span>

## <span data-ttu-id="bc848-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc848-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc848-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc848-105">DESCRIPTION</span></span>
<span data-ttu-id="bc848-106">**Yeni-AzPrivateLinkService** cmdlet 'i özel bir bağlantı hizmeti oluşturur</span><span class="sxs-lookup"><span data-stu-id="bc848-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="bc848-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc848-107">EXAMPLES</span></span>

### <span data-ttu-id="bc848-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bc848-108">Example 1</span></span>

<span data-ttu-id="bc848-109">Aşağıdaki örnek özel bir bağlantı hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bc848-109">The following example creates a private link service.</span></span>

```powershell
$vnet = Get-AzVirtualNetwork -ResourceName 'myvnet' -ResourceGroupName 'myresourcegroup'
# View the results of $vnet and change 'mysubnet' in the following line to the appropriate subnet name.
$subnet = $vnet | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mysubnet'
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name 'IP-Config' -Subnet $subnet -PrivateIpAddress '10.0.0.5'
$publicip = Get-AzPublicIpAddress -ResourceGroupName 'myresourcegroup'
$frontend = New-AzLoadBalancerFrontendIpConfig -Name 'FrontendIpConfig01' -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name 'MyLoadBalancer' -ResourceGroupName 'myresourcegroup' -Location 'West US' -FrontendIpConfiguration $frontend
New-AzPrivateLinkService -Name 'mypls' -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

## <span data-ttu-id="bc848-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc848-110">PARAMETERS</span></span>

### <span data-ttu-id="bc848-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="bc848-111">-AsJob</span></span>
<span data-ttu-id="bc848-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="bc848-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc848-113">-Otomatik onay</span><span class="sxs-lookup"><span data-stu-id="bc848-113">-AutoApproval</span></span>
<span data-ttu-id="bc848-114">Özel bağlantı hizmeti 'nin otomatik onay abonelikleri</span><span class="sxs-lookup"><span data-stu-id="bc848-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="bc848-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc848-115">-DefaultProfile</span></span>
<span data-ttu-id="bc848-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bc848-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc848-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="bc848-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="bc848-118">Özel bağlantı hizmeti için proxy protokolünü etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="bc848-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="bc848-119">-Force</span><span class="sxs-lookup"><span data-stu-id="bc848-119">-Force</span></span>
<span data-ttu-id="bc848-120">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="bc848-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="bc848-121">-IP yapılandırması</span><span class="sxs-lookup"><span data-stu-id="bc848-121">-IpConfiguration</span></span>
<span data-ttu-id="bc848-122">IP yapılandırmaları</span><span class="sxs-lookup"><span data-stu-id="bc848-122">The ip configurations</span></span>

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

### <span data-ttu-id="bc848-123">-Loadbalancerfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="bc848-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="bc848-124">Ön uç IP yapılandırmaları</span><span class="sxs-lookup"><span data-stu-id="bc848-124">The front end ip configurations</span></span>

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

### <span data-ttu-id="bc848-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="bc848-125">-Location</span></span>
<span data-ttu-id="bc848-126">konumuyla.</span><span class="sxs-lookup"><span data-stu-id="bc848-126">location.</span></span>

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

### <span data-ttu-id="bc848-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="bc848-127">-Name</span></span>
<span data-ttu-id="bc848-128">Hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="bc848-128">The name of the service.</span></span>

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

### <span data-ttu-id="bc848-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc848-129">-ResourceGroupName</span></span>
<span data-ttu-id="bc848-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="bc848-130">The resource group name.</span></span>

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

### <span data-ttu-id="bc848-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="bc848-131">-Tag</span></span>
<span data-ttu-id="bc848-132">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="bc848-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bc848-133">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="bc848-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="bc848-134">-Görünürlük</span><span class="sxs-lookup"><span data-stu-id="bc848-134">-Visibility</span></span>
<span data-ttu-id="bc848-135">Özel bağlantı hizmetinin görünürlük abonelikleri</span><span class="sxs-lookup"><span data-stu-id="bc848-135">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="bc848-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="bc848-136">-Confirm</span></span>
<span data-ttu-id="bc848-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bc848-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc848-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc848-138">-WhatIf</span></span>
<span data-ttu-id="bc848-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bc848-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc848-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bc848-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc848-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc848-141">CommonParameters</span></span>
<span data-ttu-id="bc848-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc848-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc848-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bc848-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc848-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc848-144">INPUTS</span></span>

### <span data-ttu-id="bc848-145">System. String</span><span class="sxs-lookup"><span data-stu-id="bc848-145">System.String</span></span>

### <span data-ttu-id="bc848-146">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration []</span><span class="sxs-lookup"><span data-stu-id="bc848-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="bc848-147">Microsoft. Azure. Commands. Network. model. Psprivatelinkserviceıp []</span><span class="sxs-lookup"><span data-stu-id="bc848-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="bc848-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc848-148">OUTPUTS</span></span>

### <span data-ttu-id="bc848-149">Microsoft. Azure. Commands. Network. model. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bc848-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="bc848-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc848-150">NOTES</span></span>

## <span data-ttu-id="bc848-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc848-151">RELATED LINKS</span></span>

[<span data-ttu-id="bc848-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bc848-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="bc848-153">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bc848-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="bc848-154">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bc848-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
