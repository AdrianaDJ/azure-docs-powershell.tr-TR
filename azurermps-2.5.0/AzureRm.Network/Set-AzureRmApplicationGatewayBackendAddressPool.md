---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: 66ca482f2b284118ccf5095ec833a5278a5ea73d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940012"
---
# <span data-ttu-id="8e308-101">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8e308-101">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="8e308-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e308-102">SYNOPSIS</span></span>
<span data-ttu-id="8e308-103">Bir uygulama ağ geçidi için arka uç adres havuzunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8e308-103">Updates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e308-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8e308-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e308-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e308-105">DESCRIPTION</span></span>
<span data-ttu-id="8e308-106">**Set-AzureRmApplicationGatewayBackendAddressPool** cmdlet 'ı bir Azure uygulama ağ geçidi için arka uç adres havuzunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8e308-106">The **Set-AzureRmApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="8e308-107">Arka uç adresleri IP adresleri, tam etki alanı adları (FQDN) veya IP yapılandırması kimlikleri olarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="8e308-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="8e308-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8e308-108">EXAMPLES</span></span>

### <span data-ttu-id="8e308-109">Örnek 1: FQDN 'Ler kullanarak arka uç adres havuzu ayarlama</span><span class="sxs-lookup"><span data-stu-id="8e308-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="8e308-110">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8e308-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="8e308-111">İkinci komut $AppGw 'teki uygulama ağ geçidinin arka uç adres havuzunu FQDN kullanarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8e308-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="8e308-112">Örnek 2: arka uç sunucusu IP adreslerini kullanarak arka uç adres havuzu ayarlama</span><span class="sxs-lookup"><span data-stu-id="8e308-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="8e308-113">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8e308-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="8e308-114">İkinci komut $AppGw 'teki uygulama ağ geçidinin arka uç adres havuzunu, IP adreslerini kullanarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8e308-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="8e308-115">Örnek 3: arka uç sunucusunun KIMLIĞINI kullanarak arka uç adres havuzu ayarlama</span><span class="sxs-lookup"><span data-stu-id="8e308-115">Example 3: Setting a back-end address pool by using the ID of the backend server?s IP address</span></span>
```
PS C:\> $Nic01 = Get-AzureRmNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzureRmNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="8e308-116">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan Nic01 adlı bir ağ arabirimi nesnesini alır ve $Nic 01 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8e308-116">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.</span></span>

<span data-ttu-id="8e308-117">İkinci komut, ResourceGroup02 adındaki kaynak grubuna ait olan Nic02 adlı bir ağ arabirimi nesnesini alır ve $Nic 02 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8e308-117">The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.</span></span>

<span data-ttu-id="8e308-118">Üçüncü komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8e308-118">The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="8e308-119">İleri komutu, $AppGw 'daki uygulama ağ geçidinin arka uç adres havuzunu güncelleştirmek için $Nic 01 ve $Nic 02 ' dan arka uç IP yapılandırma kimliklerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="8e308-119">The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to update the back-end address pool of the application gateway in $AppGw.</span></span>

## <span data-ttu-id="8e308-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8e308-120">PARAMETERS</span></span>

### <span data-ttu-id="8e308-121">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e308-121">-ApplicationGateway</span></span>
<span data-ttu-id="8e308-122">Bu cmdlet 'in arka uç adres havuzunu ilişkilendiren uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e308-122">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e308-123">-Backendfqdn 'leri</span><span class="sxs-lookup"><span data-stu-id="8e308-123">-BackendFqdns</span></span>
<span data-ttu-id="8e308-124">Arka uç sunucu havuzu olarak kullanılacak arka uç IP adresleri listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e308-124">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="8e308-125">Backentüm adresler</span><span class="sxs-lookup"><span data-stu-id="8e308-125">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="8e308-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e308-126">-DefaultProfile</span></span>
<span data-ttu-id="8e308-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8e308-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e308-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="8e308-128">-Name</span></span>
<span data-ttu-id="8e308-129">Arka uç adres havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e308-129">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="8e308-130">Bu arka uç adres havuzunun uygulama ağ geçidinde var olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="8e308-130">This back-end address pool must exist in the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e308-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="8e308-131">-Confirm</span></span>
<span data-ttu-id="8e308-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8e308-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e308-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e308-133">-WhatIf</span></span>
<span data-ttu-id="8e308-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e308-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e308-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8e308-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e308-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e308-136">CommonParameters</span></span>
<span data-ttu-id="8e308-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8e308-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e308-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e308-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e308-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8e308-139">INPUTS</span></span>

### <span data-ttu-id="8e308-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8e308-140">System.String</span></span>

## <span data-ttu-id="8e308-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8e308-141">OUTPUTS</span></span>

### <span data-ttu-id="8e308-142">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e308-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8e308-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8e308-143">NOTES</span></span>

## <span data-ttu-id="8e308-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8e308-144">RELATED LINKS</span></span>

[<span data-ttu-id="8e308-145">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8e308-145">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="8e308-146">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8e308-146">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="8e308-147">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8e308-147">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="8e308-148">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8e308-148">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)


