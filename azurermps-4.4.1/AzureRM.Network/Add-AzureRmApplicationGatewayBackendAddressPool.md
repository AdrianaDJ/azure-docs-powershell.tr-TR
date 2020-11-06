---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: ada3ab6c2539561f440816215049030960ff21a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587883"
---
# <span data-ttu-id="6a632-101">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6a632-101">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="6a632-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a632-102">SYNOPSIS</span></span>
<span data-ttu-id="6a632-103">Uygulama ağ geçidine arka uç adres havuzu ekler.</span><span class="sxs-lookup"><span data-stu-id="6a632-103">Adds a back-end address pool to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a632-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a632-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a632-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a632-105">DESCRIPTION</span></span>
<span data-ttu-id="6a632-106">**Add-AzureRmApplicationGatewayBackendAddressPool** cmdlet 'i bir uygulama ağ geçidine arka uç adres havuzu ekler.</span><span class="sxs-lookup"><span data-stu-id="6a632-106">The **Add-AzureRmApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="6a632-107">Bir arka uç adresi IP adresi, tam nitelenmiş etki alanı adı (FQDN) veya IP yapılandırma kimliği kullanılarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="6a632-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="6a632-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a632-108">EXAMPLES</span></span>

### <span data-ttu-id="6a632-109">Örnek 1: arka uç sunucu FQDN 'SI kullanarak arka uç adres havuzu ekleme</span><span class="sxs-lookup"><span data-stu-id="6a632-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="6a632-110">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut, FQDN kullanarak $AppGw depolanan uygulama ağ geçidinin arka uç adres havuzunu ekler.</span><span class="sxs-lookup"><span data-stu-id="6a632-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="6a632-111">Örnek 2: arka uç sunucusu IP adreslerini kullanarak arka uç adres havuzu ekleme</span><span class="sxs-lookup"><span data-stu-id="6a632-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add -AzureApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="6a632-112">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut, IP adreslerini kullanarak $AppGw depolanan uygulama ağ geçidinin arka uç adres havuzunu ekler.</span><span class="sxs-lookup"><span data-stu-id="6a632-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="6a632-113">Örnek 3: arka uç sunucusunun IP adresinin KIMLIĞINI kullanarak Seta arka uç adres havuzu</span><span class="sxs-lookup"><span data-stu-id="6a632-113">Example 3: Seta back-end address pool by using the ID of the backend server's IP address</span></span>
```
PS C:\>$Nic01 = Get-AzureRmNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzureRmNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="6a632-114">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan Nic01 adlı bir ağ arabirimi nesnesini alır ve $Nic 01 değişkeninde depolar. İkinci komut, ResourceGroup02 adındaki kaynak grubuna ait olan Nic02 adlı bir ağ arabirimi nesnesini alır ve $Nic 02 değişkeninde depolar. Üçüncü komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İleri komutu, $AppGw depolanan uygulama ağ geçidinin arka uç adres havuzunu eklemek için $Nic 01 ve $Nic 02 ' dan arka uç IP yapılandırma kimliklerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="6a632-114">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to add the back-end address pool of the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="6a632-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a632-115">PARAMETERS</span></span>

### <span data-ttu-id="6a632-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a632-116">-ApplicationGateway</span></span>
<span data-ttu-id="6a632-117">Bu cmdlet 'in arka uç adres havuzu eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a632-117">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

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

### <span data-ttu-id="6a632-118">-Backendfqdn 'leri</span><span class="sxs-lookup"><span data-stu-id="6a632-118">-BackendFqdns</span></span>
<span data-ttu-id="6a632-119">Bu cmdlet 'in arka uç sunucu havuzu olarak eklediği arka uç FQDN 'lerin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a632-119">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="6a632-120">Backentüm adresler</span><span class="sxs-lookup"><span data-stu-id="6a632-120">-BackendIPAddresses</span></span>
<span data-ttu-id="6a632-121">Bu cmdlet 'in arka uç sunucu havuzu olarak eklediği arka uç IP adresleri listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a632-121">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="6a632-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="6a632-122">-Name</span></span>
<span data-ttu-id="6a632-123">Bu cmdlet 'in eklediği arka uç sunucu havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a632-123">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="6a632-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="6a632-124">-Confirm</span></span>
<span data-ttu-id="6a632-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6a632-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a632-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a632-126">-WhatIf</span></span>
<span data-ttu-id="6a632-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6a632-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a632-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6a632-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a632-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a632-129">-DefaultProfile</span></span>
<span data-ttu-id="6a632-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6a632-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a632-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a632-131">CommonParameters</span></span>
<span data-ttu-id="6a632-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a632-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a632-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a632-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a632-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a632-134">INPUTS</span></span>

###  
<span data-ttu-id="6a632-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6a632-135">System.String</span></span>

## <span data-ttu-id="6a632-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a632-136">OUTPUTS</span></span>

### <span data-ttu-id="6a632-137">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a632-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6a632-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a632-138">NOTES</span></span>

## <span data-ttu-id="6a632-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a632-139">RELATED LINKS</span></span>

[<span data-ttu-id="6a632-140">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6a632-140">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="6a632-141">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6a632-141">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="6a632-142">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6a632-142">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="6a632-143">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6a632-143">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="6a632-144">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6a632-144">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


