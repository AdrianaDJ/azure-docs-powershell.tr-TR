---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: ee1b1b70abf8256a6974c34bd21c16877e84ef84
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935666"
---
# <span data-ttu-id="6dc59-101">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6dc59-101">Add-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="6dc59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dc59-102">SYNOPSIS</span></span>
<span data-ttu-id="6dc59-103">Uygulama ağ geçidine arka uç adres havuzu ekler.</span><span class="sxs-lookup"><span data-stu-id="6dc59-103">Adds a back-end address pool to an application gateway.</span></span>

## <span data-ttu-id="6dc59-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6dc59-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dc59-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6dc59-105">DESCRIPTION</span></span>
<span data-ttu-id="6dc59-106">**Add-AzApplicationGatewayBackendAddressPool** cmdlet 'i bir uygulama ağ geçidine arka uç adres havuzu ekler.</span><span class="sxs-lookup"><span data-stu-id="6dc59-106">The **Add-AzApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="6dc59-107">Bir arka uç adresi IP adresi, tam nitelenmiş etki alanı adı (FQDN) veya IP yapılandırma kimliği kullanılarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="6dc59-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="6dc59-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6dc59-108">EXAMPLES</span></span>

### <span data-ttu-id="6dc59-109">Örnek 1: arka uç sunucu FQDN 'SI kullanarak arka uç adres havuzu ekleme</span><span class="sxs-lookup"><span data-stu-id="6dc59-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="6dc59-110">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut, FQDN kullanarak $AppGw depolanan uygulama ağ geçidinin arka uç adres havuzunu ekler.</span><span class="sxs-lookup"><span data-stu-id="6dc59-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="6dc59-111">Örnek 2: arka uç sunucusu IP adreslerini kullanarak arka uç adres havuzu ekleme</span><span class="sxs-lookup"><span data-stu-id="6dc59-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add -AzureApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="6dc59-112">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut, IP adreslerini kullanarak $AppGw depolanan uygulama ağ geçidinin arka uç adres havuzunu ekler.</span><span class="sxs-lookup"><span data-stu-id="6dc59-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="6dc59-113">Örnek 3: arka uç sunucusunun IP adresinin KIMLIĞINI kullanarak Seta arka uç adres havuzu</span><span class="sxs-lookup"><span data-stu-id="6dc59-113">Example 3: Seta back-end address pool by using the ID of the backend server's IP address</span></span>
```
PS C:\>$Nic01 = Get-AzNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="6dc59-114">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan Nic01 adlı bir ağ arabirimi nesnesini alır ve $Nic 01 değişkeninde depolar. İkinci komut, ResourceGroup02 adındaki kaynak grubuna ait olan Nic02 adlı bir ağ arabirimi nesnesini alır ve $Nic 02 değişkeninde depolar. Üçüncü komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İleri komutu, $AppGw depolanan uygulama ağ geçidinin arka uç adres havuzunu eklemek için $Nic 01 ve $Nic 02 ' dan arka uç IP yapılandırma kimliklerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="6dc59-114">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to add the back-end address pool of the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="6dc59-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6dc59-115">PARAMETERS</span></span>

### <span data-ttu-id="6dc59-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6dc59-116">-ApplicationGateway</span></span>
<span data-ttu-id="6dc59-117">Bu cmdlet 'in arka uç adres havuzu eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dc59-117">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

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

### <span data-ttu-id="6dc59-118">-Backendfqdn 'leri</span><span class="sxs-lookup"><span data-stu-id="6dc59-118">-BackendFqdns</span></span>
<span data-ttu-id="6dc59-119">Bu cmdlet 'in arka uç sunucu havuzu olarak eklediği arka uç FQDN 'lerin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dc59-119">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="6dc59-120">Backentüm adresler</span><span class="sxs-lookup"><span data-stu-id="6dc59-120">-BackendIPAddresses</span></span>
<span data-ttu-id="6dc59-121">Bu cmdlet 'in arka uç sunucu havuzu olarak eklediği arka uç IP adresleri listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dc59-121">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="6dc59-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dc59-122">-DefaultProfile</span></span>
<span data-ttu-id="6dc59-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6dc59-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6dc59-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="6dc59-124">-Name</span></span>
<span data-ttu-id="6dc59-125">Bu cmdlet 'in eklediği arka uç sunucu havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dc59-125">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="6dc59-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="6dc59-126">-Confirm</span></span>
<span data-ttu-id="6dc59-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6dc59-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dc59-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dc59-128">-WhatIf</span></span>
<span data-ttu-id="6dc59-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6dc59-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dc59-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6dc59-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dc59-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dc59-131">CommonParameters</span></span>
<span data-ttu-id="6dc59-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6dc59-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dc59-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dc59-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dc59-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6dc59-134">INPUTS</span></span>

###  
<span data-ttu-id="6dc59-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6dc59-135">System.String</span></span>

## <span data-ttu-id="6dc59-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6dc59-136">OUTPUTS</span></span>

### <span data-ttu-id="6dc59-137">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6dc59-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6dc59-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6dc59-138">NOTES</span></span>

## <span data-ttu-id="6dc59-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6dc59-139">RELATED LINKS</span></span>

[<span data-ttu-id="6dc59-140">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6dc59-140">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="6dc59-141">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6dc59-141">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="6dc59-142">Yeni-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6dc59-142">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="6dc59-143">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6dc59-143">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="6dc59-144">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6dc59-144">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


