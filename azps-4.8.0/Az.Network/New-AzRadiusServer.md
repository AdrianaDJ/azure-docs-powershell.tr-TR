---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azradiusserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
ms.openlocfilehash: 0f92f09d3caf481f845c96942fd038a82c1078ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109459"
---
# <span data-ttu-id="ea499-101">New-AzRadiusServer</span><span class="sxs-lookup"><span data-stu-id="ea499-101">New-AzRadiusServer</span></span>

## <span data-ttu-id="ea499-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea499-102">SYNOPSIS</span></span>
<span data-ttu-id="ea499-103">Dış RADIUS sunucu yapılandırması oluşturur</span><span class="sxs-lookup"><span data-stu-id="ea499-103">Creates an external radius server configuration</span></span>

## <span data-ttu-id="ea499-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea499-104">SYNTAX</span></span>

```
New-AzRadiusServer -RadiusServerAddress <String> -RadiusServerSecret <SecureString>
 [-RadiusServerScore <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea499-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea499-105">DESCRIPTION</span></span>
<span data-ttu-id="ea499-106">New-AzRadiusServer cmdlet 'i sanal ağ geçidi ve VPN sunucusu yapılandırmasında kullanılacak bir dış RADIUS sunucu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea499-106">The New-AzRadiusServer cmdlet creates an external radius server configuration to be used in virtual network gateway and VPN server configuration.</span></span>

## <span data-ttu-id="ea499-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea499-107">EXAMPLES</span></span>

### <span data-ttu-id="ea499-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ea499-108">Example 1</span></span>
```powershell
PS C:\> $radiusServer1 = New-AzRadiusServer -RadiusServerAddress 10.1.0.1 -RadiusServerSecret $radiuspd -RadiusServerScore 30
PS C:\> $radiusServer2 = New-AzRadiusServer -RadiusServerAddress 10.1.0.2 -RadiusServerSecret $radiuspd -RadiusServerScore 1
PS C:\> New-AzVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku VpnGw1 -VpnClientAddressPool 201.169.0.0/16 -VpnClientProtocol "IkeV2" -RadiusServerList $radiusServers
```

<span data-ttu-id="ea499-109">Yeni sanal ağ geçidinde P2S yapılandırmak için kullanılacak birden çok dış RADIUS sunucusu yapılandırması oluşturma.</span><span class="sxs-lookup"><span data-stu-id="ea499-109">Creating multiple external radius server configurations to be used for configuring P2S on a new virtual network gateway.</span></span>

## <span data-ttu-id="ea499-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea499-110">PARAMETERS</span></span>

### <span data-ttu-id="ea499-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea499-111">-DefaultProfile</span></span>
<span data-ttu-id="ea499-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ea499-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea499-113">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="ea499-113">-RadiusServerAddress</span></span>
<span data-ttu-id="ea499-114">Dış RADIUS sunucusu adresi</span><span class="sxs-lookup"><span data-stu-id="ea499-114">External radius server address</span></span>

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

### <span data-ttu-id="ea499-115">-RadiusServerScore</span><span class="sxs-lookup"><span data-stu-id="ea499-115">-RadiusServerScore</span></span>
<span data-ttu-id="ea499-116">Dış RADIUS sunucusu puanı</span><span class="sxs-lookup"><span data-stu-id="ea499-116">External radius server score</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea499-117">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="ea499-117">-RadiusServerSecret</span></span>
<span data-ttu-id="ea499-118">Dış RADIUS sunucusu parolası</span><span class="sxs-lookup"><span data-stu-id="ea499-118">External radius server secret</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea499-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea499-119">CommonParameters</span></span>
<span data-ttu-id="ea499-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea499-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea499-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ea499-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea499-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea499-122">INPUTS</span></span>

### <span data-ttu-id="ea499-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ea499-123">System.String</span></span>

### <span data-ttu-id="ea499-124">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="ea499-124">System.Security.SecureString</span></span>

### <span data-ttu-id="ea499-125">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ea499-125">System.Int32</span></span>

## <span data-ttu-id="ea499-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea499-126">OUTPUTS</span></span>

### <span data-ttu-id="ea499-127">Microsoft. Azure. Commands. Network. model. PSRadiusServer</span><span class="sxs-lookup"><span data-stu-id="ea499-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span></span>

## <span data-ttu-id="ea499-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea499-128">NOTES</span></span>

## <span data-ttu-id="ea499-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea499-129">RELATED LINKS</span></span>
