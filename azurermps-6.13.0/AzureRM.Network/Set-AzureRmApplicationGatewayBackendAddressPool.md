---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: d62afff67d1b5e7722b107b70810ac82e5b151d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763143"
---
# <span data-ttu-id="dab43-101">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dab43-101">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="dab43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dab43-102">SYNOPSIS</span></span>
<span data-ttu-id="dab43-103">Bir uygulama ağ geçidi için arka uç adres havuzunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dab43-103">Updates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dab43-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dab43-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dab43-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dab43-105">DESCRIPTION</span></span>
<span data-ttu-id="dab43-106">**Set-AzureRmApplicationGatewayBackendAddressPool** cmdlet 'ı bir Azure uygulama ağ geçidi için arka uç adres havuzunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dab43-106">The **Set-AzureRmApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="dab43-107">Arka uç adresleri IP adresleri, tam etki alanı adları (FQDN) veya IP yapılandırması kimlikleri olarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="dab43-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="dab43-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dab43-108">EXAMPLES</span></span>

### <span data-ttu-id="dab43-109">Örnek 1: FQDN 'Ler kullanarak arka uç adres havuzu ayarlama</span><span class="sxs-lookup"><span data-stu-id="dab43-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="dab43-110">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="dab43-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="dab43-111">İkinci komut $AppGw 'teki uygulama ağ geçidinin arka uç adres havuzunu FQDN kullanarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dab43-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="dab43-112">Örnek 2: arka uç sunucusu IP adreslerini kullanarak arka uç adres havuzu ayarlama</span><span class="sxs-lookup"><span data-stu-id="dab43-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="dab43-113">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="dab43-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="dab43-114">İkinci komut $AppGw 'teki uygulama ağ geçidinin arka uç adres havuzunu, IP adreslerini kullanarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dab43-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="dab43-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dab43-115">PARAMETERS</span></span>

### <span data-ttu-id="dab43-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dab43-116">-ApplicationGateway</span></span>
<span data-ttu-id="dab43-117">Bu cmdlet 'in arka uç adres havuzunu ilişkilendiren uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dab43-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="dab43-118">-Backendfqdn 'leri</span><span class="sxs-lookup"><span data-stu-id="dab43-118">-BackendFqdns</span></span>
<span data-ttu-id="dab43-119">Arka uç sunucu havuzu olarak kullanılacak arka uç IP adresleri listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dab43-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dab43-120">Backentüm adresler</span><span class="sxs-lookup"><span data-stu-id="dab43-120">-BackendIPAddresses</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dab43-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dab43-121">-DefaultProfile</span></span>
<span data-ttu-id="dab43-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dab43-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dab43-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="dab43-123">-Name</span></span>
<span data-ttu-id="dab43-124">Arka uç adres havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dab43-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="dab43-125">Bu arka uç adres havuzunun uygulama ağ geçidinde var olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="dab43-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="dab43-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="dab43-126">-Confirm</span></span>
<span data-ttu-id="dab43-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dab43-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dab43-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dab43-128">-WhatIf</span></span>
<span data-ttu-id="dab43-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dab43-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dab43-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dab43-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dab43-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dab43-131">CommonParameters</span></span>
<span data-ttu-id="dab43-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dab43-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dab43-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dab43-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dab43-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dab43-134">INPUTS</span></span>

### <span data-ttu-id="dab43-135">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dab43-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="dab43-136">Parametreler: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dab43-136">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="dab43-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dab43-137">OUTPUTS</span></span>

### <span data-ttu-id="dab43-138">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dab43-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dab43-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dab43-139">NOTES</span></span>

## <span data-ttu-id="dab43-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dab43-140">RELATED LINKS</span></span>

[<span data-ttu-id="dab43-141">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dab43-141">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dab43-142">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dab43-142">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dab43-143">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dab43-143">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dab43-144">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dab43-144">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

