---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: c415fb890240ea6f4fb03b71c3a249eece1ba02b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266596"
---
# <span data-ttu-id="35856-101">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="35856-101">Add-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="35856-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35856-102">SYNOPSIS</span></span>
<span data-ttu-id="35856-103">Uygulama ağ geçidine arka uç adres havuzu ekler.</span><span class="sxs-lookup"><span data-stu-id="35856-103">Adds a back-end address pool to an application gateway.</span></span>

## <span data-ttu-id="35856-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="35856-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35856-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="35856-105">DESCRIPTION</span></span>
<span data-ttu-id="35856-106">**Add-AzApplicationGatewayBackendAddressPool** cmdlet 'i bir uygulama ağ geçidine arka uç adres havuzu ekler.</span><span class="sxs-lookup"><span data-stu-id="35856-106">The **Add-AzApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="35856-107">Bir arka uç adresi IP adresi, tam nitelenmiş etki alanı adı (FQDN) veya IP yapılandırma kimliği kullanılarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="35856-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="35856-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="35856-108">EXAMPLES</span></span>

### <span data-ttu-id="35856-109">Örnek 1: arka uç sunucu FQDN 'SI kullanarak arka uç adres havuzu ekleme</span><span class="sxs-lookup"><span data-stu-id="35856-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="35856-110">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut, FQDN kullanarak $AppGw depolanan uygulama ağ geçidinin arka uç adres havuzunu ekler.</span><span class="sxs-lookup"><span data-stu-id="35856-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="35856-111">Örnek 2: arka uç sunucusu IP adreslerini kullanarak arka uç adres havuzu ekleme</span><span class="sxs-lookup"><span data-stu-id="35856-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="35856-112">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut, IP adreslerini kullanarak $AppGw depolanan uygulama ağ geçidinin arka uç adres havuzunu ekler.</span><span class="sxs-lookup"><span data-stu-id="35856-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="35856-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="35856-113">PARAMETERS</span></span>

### <span data-ttu-id="35856-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35856-114">-ApplicationGateway</span></span>
<span data-ttu-id="35856-115">Bu cmdlet 'in arka uç adres havuzu eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="35856-115">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35856-116">-Backendfqdn 'leri</span><span class="sxs-lookup"><span data-stu-id="35856-116">-BackendFqdns</span></span>
<span data-ttu-id="35856-117">Bu cmdlet 'in arka uç sunucu havuzu olarak eklediği arka uç FQDN 'lerin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="35856-117">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35856-118">Backentüm adresler</span><span class="sxs-lookup"><span data-stu-id="35856-118">-BackendIPAddresses</span></span>
<span data-ttu-id="35856-119">Bu cmdlet 'in arka uç sunucu havuzu olarak eklediği arka uç IP adresleri listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="35856-119">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35856-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35856-120">-DefaultProfile</span></span>
<span data-ttu-id="35856-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="35856-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35856-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="35856-122">-Name</span></span>
<span data-ttu-id="35856-123">Bu cmdlet 'in eklediği arka uç sunucu havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="35856-123">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35856-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="35856-124">-Confirm</span></span>
<span data-ttu-id="35856-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="35856-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35856-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35856-126">-WhatIf</span></span>
<span data-ttu-id="35856-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="35856-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35856-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="35856-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35856-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35856-129">CommonParameters</span></span>
<span data-ttu-id="35856-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="35856-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35856-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35856-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35856-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="35856-132">INPUTS</span></span>

### <span data-ttu-id="35856-133">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35856-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="35856-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="35856-134">OUTPUTS</span></span>

### <span data-ttu-id="35856-135">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35856-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="35856-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="35856-136">NOTES</span></span>

## <span data-ttu-id="35856-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="35856-137">RELATED LINKS</span></span>

[<span data-ttu-id="35856-138">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="35856-138">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="35856-139">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="35856-139">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="35856-140">Yeni-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="35856-140">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="35856-141">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="35856-141">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="35856-142">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="35856-142">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="35856-143">Set-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="35856-143">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
