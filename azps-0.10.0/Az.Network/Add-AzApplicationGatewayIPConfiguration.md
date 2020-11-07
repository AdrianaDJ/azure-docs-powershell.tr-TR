---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: c26fe80110066e1f6305e2d35b952ed8ab45f00d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935652"
---
# <span data-ttu-id="2e2ae-101">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e2ae-101">Add-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="2e2ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e2ae-102">SYNOPSIS</span></span>
<span data-ttu-id="2e2ae-103">Uygulama ağ geçidine IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="2e2ae-103">Adds an IP configuration to an application gateway.</span></span>

## <span data-ttu-id="2e2ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e2ae-104">SYNTAX</span></span>

### <span data-ttu-id="2e2ae-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="2e2ae-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e2ae-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2e2ae-106">SetByResource</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e2ae-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e2ae-107">DESCRIPTION</span></span>
<span data-ttu-id="2e2ae-108">**Add-Azapplicationgatewayıpconfiguration** cmdlet 'i, uygulama ağ GEÇIDINE bir IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="2e2ae-108">The **Add-AzApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="2e2ae-109">IP yapılandırmaları, uygulama ağ geçidinin dağıtıldığı alt ağı içerir.</span><span class="sxs-lookup"><span data-stu-id="2e2ae-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="2e2ae-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e2ae-110">EXAMPLES</span></span>

### <span data-ttu-id="2e2ae-111">Örnek 1: uygulama ağ geçidine sanal ağ yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="2e2ae-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="2e2ae-112">İlk komut sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2e2ae-112">The first command creates a virtual network.</span></span>
<span data-ttu-id="2e2ae-113">İkinci komut, önceden oluşturulmuş sanal ağı kullanarak bir alt ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2e2ae-113">The second command creates a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="2e2ae-114">Üçüncü komut, uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2e2ae-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2e2ae-115">Fouth komutu, IP yapılandırmasını $AppGw depolanan uygulama ağ geçidine ekler.</span><span class="sxs-lookup"><span data-stu-id="2e2ae-115">The fouth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="2e2ae-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e2ae-116">PARAMETERS</span></span>

### <span data-ttu-id="2e2ae-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e2ae-117">-ApplicationGateway</span></span>
<span data-ttu-id="2e2ae-118">Bu cmdlet 'in IP yapılandırması eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e2ae-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="2e2ae-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e2ae-119">-DefaultProfile</span></span>
<span data-ttu-id="2e2ae-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2e2ae-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e2ae-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="2e2ae-121">-Name</span></span>
<span data-ttu-id="2e2ae-122">Eklenecek IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e2ae-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="2e2ae-123">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="2e2ae-123">-Subnet</span></span>
<span data-ttu-id="2e2ae-124">Alt ağ belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e2ae-124">Specifies a subnet.</span></span>
<span data-ttu-id="2e2ae-125">Bu, uygulama ağ geçidinin dağıtıldığı alt ağdır.</span><span class="sxs-lookup"><span data-stu-id="2e2ae-125">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e2ae-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="2e2ae-126">-SubnetId</span></span>
<span data-ttu-id="2e2ae-127">Alt ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e2ae-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="2e2ae-128">Bu, uygulama ağ geçidinin dağıtıldığı alt ağdır.</span><span class="sxs-lookup"><span data-stu-id="2e2ae-128">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e2ae-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e2ae-129">CommonParameters</span></span>
<span data-ttu-id="2e2ae-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e2ae-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e2ae-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e2ae-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e2ae-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e2ae-132">INPUTS</span></span>

### <span data-ttu-id="2e2ae-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2e2ae-133">System.String</span></span>

## <span data-ttu-id="2e2ae-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e2ae-134">OUTPUTS</span></span>

### <span data-ttu-id="2e2ae-135">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e2ae-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2e2ae-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e2ae-136">NOTES</span></span>

## <span data-ttu-id="2e2ae-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e2ae-137">RELATED LINKS</span></span>

[<span data-ttu-id="2e2ae-138">Get-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="2e2ae-138">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2e2ae-139">Yeni-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="2e2ae-139">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2e2ae-140">Remove-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="2e2ae-140">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2e2ae-141">Set-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="2e2ae-141">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


