---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
ms.openlocfilehash: a0c4e6835525dfbecd4bb7eca239f8327df6ff8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763680"
---
# <span data-ttu-id="d79aa-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="d79aa-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>

## <span data-ttu-id="d79aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d79aa-102">SYNOPSIS</span></span>
<span data-ttu-id="d79aa-103">Sanal ağ geçidi için VPN istemcisi adres havuzunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d79aa-103">Sets the VPN client address pool for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d79aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d79aa-104">SYNTAX</span></span>

### <span data-ttu-id="d79aa-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d79aa-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d79aa-106">Radiusserveryapılandırması</span><span class="sxs-lookup"><span data-stu-id="d79aa-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d79aa-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d79aa-107">DESCRIPTION</span></span>
<span data-ttu-id="d79aa-108">**Set-AzureRmVirtualNetworkVpnClientConfig** cmdlet 'i sanal ağ geçidi için istemci adresi havuzunu yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="d79aa-108">The **Set-AzureRmVirtualNetworkVpnClientConfig** cmdlet configures the client address pool for a virtual network gateway.</span></span>
<span data-ttu-id="d79aa-109">Bu ağ geçidine bağlanan sanal özel ağ (VPN) istemcilerine, bu adres havuzundan bir IP adresi atanacaktır.</span><span class="sxs-lookup"><span data-stu-id="d79aa-109">Virtual private network (VPN) clients that connect to this gateway will be assigned an IP address from this address pool.</span></span>

## <span data-ttu-id="d79aa-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d79aa-110">EXAMPLES</span></span>

### <span data-ttu-id="d79aa-111">Örnek 1: sanal ağ ağ geçidine VPN istemcisi adres havuzu atama</span><span class="sxs-lookup"><span data-stu-id="d79aa-111">Example 1: Assign a VPN client address pool to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

<span data-ttu-id="d79aa-112">Bu örnekte, ContosoVirtualGateway adlı sanal ağ geçidine VPN istemcisi adres havuzu atanır.</span><span class="sxs-lookup"><span data-stu-id="d79aa-112">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="d79aa-113">İlk komut ağ geçidine bir nesne başvurusu oluşturur ve nesne $Gateway adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="d79aa-113">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="d79aa-114">Örnekteki ikinci komut, contoso/16 adres havuzunu ContosoVirtualGateway 'e atamak için **set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="d79aa-114">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span>

### <span data-ttu-id="d79aa-115">Örnek 2: mevcut ağ geçidinde dış RADIUS tabanlı kimlik doğrulamasını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="d79aa-115">Example 2: Configure external radius based authentication on existing gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="d79aa-116">Bu örnekte, ContosoVirtualGateway adlı sanal ağ geçidine VPN istemcisi adres havuzu atanır.</span><span class="sxs-lookup"><span data-stu-id="d79aa-116">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="d79aa-117">İlk komut ağ geçidine bir nesne başvurusu oluşturur ve nesne $Gateway adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="d79aa-117">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="d79aa-118">Örnekteki ikinci komut, contoso/16 adres havuzunu ContosoVirtualGateway 'e atamak için **set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="d79aa-118">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span> <span data-ttu-id="d79aa-119">Ayrıca "TestRadiusServer" dış RADIUS sunucusunu VPN istemcileri için kimlik doğrulama için kullanılacak şekilde yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="d79aa-119">It also configures the external radius server "TestRadiusServer" to be used for authentication for vpn clients.</span></span>

## <span data-ttu-id="d79aa-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d79aa-120">PARAMETERS</span></span>

### <span data-ttu-id="d79aa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d79aa-121">-DefaultProfile</span></span>
<span data-ttu-id="d79aa-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d79aa-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d79aa-123">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="d79aa-123">-RadiusServerAddress</span></span>
<span data-ttu-id="d79aa-124">P2S dış RADIUS sunucusu adresi.</span><span class="sxs-lookup"><span data-stu-id="d79aa-124">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d79aa-125">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="d79aa-125">-RadiusServerSecret</span></span>
<span data-ttu-id="d79aa-126">Dış RADIUS sunucusu gizliliğini P2S.</span><span class="sxs-lookup"><span data-stu-id="d79aa-126">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d79aa-127">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d79aa-127">-VirtualNetworkGateway</span></span>
<span data-ttu-id="d79aa-128">Bu cmdlet 'in değiştirdiği VPN istemcisi yapılandırma ayarlarını içeren sanal ağ geçidi için bir nesne başvurusu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d79aa-128">Specifies an object reference to the virtual network gateway that contains the VPN client configuration settings that this cmdlet modifies.</span></span>
<span data-ttu-id="d79aa-129">Sanal ağ geçidi için Get-AzureRmVirtualNetworkGateway kullanarak ve ağ geçidinin adını belirterek bir nesne başvurusu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d79aa-129">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d79aa-130">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="d79aa-130">-VpnClientAddressPool</span></span>
<span data-ttu-id="d79aa-131">Bu ağ geçidine bağlanan istemcilere atanacak IP adreslerini belirtir</span><span class="sxs-lookup"><span data-stu-id="d79aa-131">Specifies the IP addresses to be assigned to clients connecting to this gateway</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d79aa-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="d79aa-132">-Confirm</span></span>
<span data-ttu-id="d79aa-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d79aa-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d79aa-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d79aa-134">-WhatIf</span></span>
<span data-ttu-id="d79aa-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d79aa-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d79aa-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d79aa-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d79aa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d79aa-137">CommonParameters</span></span>
<span data-ttu-id="d79aa-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d79aa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d79aa-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d79aa-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d79aa-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d79aa-140">INPUTS</span></span>

###  
<span data-ttu-id="d79aa-141">Bu cmdlet, **Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway** nesnesinin ardışık olarak birleştirilmiş örneklerini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="d79aa-141">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="d79aa-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d79aa-142">OUTPUTS</span></span>

###  
<span data-ttu-id="d79aa-143">Bu cmdlet, **Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway** nesnesinin varolan örneklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d79aa-143">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="d79aa-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d79aa-144">NOTES</span></span>

## <span data-ttu-id="d79aa-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d79aa-145">RELATED LINKS</span></span>

[<span data-ttu-id="d79aa-146">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="d79aa-146">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="d79aa-147">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d79aa-147">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="d79aa-148">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d79aa-148">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


