---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 0f5db9dd785f5fdfc45bf75b4da082900a563632
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594220"
---
# <span data-ttu-id="ac390-101">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ac390-101">New-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="ac390-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac390-102">SYNOPSIS</span></span>
<span data-ttu-id="ac390-103">Bir yük dengeleyici için ön uç IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ac390-103">Creates a front-end IP configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac390-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ac390-104">SYNTAX</span></span>

### <span data-ttu-id="ac390-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="ac390-105">SetByResourceSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -Subnet <PSSubnet>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac390-106">Setbyresourceıdsubnet</span><span class="sxs-lookup"><span data-stu-id="ac390-106">SetByResourceIdSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -SubnetId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac390-107">Setbyresourceidpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="ac390-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddressId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac390-108">Setbyresourcepublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="ac390-108">SetByResourcePublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddress <PSPublicIpAddress>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac390-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="ac390-109">DESCRIPTION</span></span>
<span data-ttu-id="ac390-110">**Yeni-Azurermloadbalancerfrontendıl** cmdlet 'i, bir Azure yük dengeleyicisi için ön uç IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ac390-110">The **New-AzureRmLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="ac390-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ac390-111">EXAMPLES</span></span>

### <span data-ttu-id="ac390-112">Örnek 1: yük dengeleyici için ön uç IP yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="ac390-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="ac390-113">İlk komut MyResourceGroup adlı kaynak grubunda MyPublicIP adlı bir dinamik ortak IP adresi oluşturur ve $publicip değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ac390-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="ac390-114">İkinci komut, $publicip genel IP adresini kullanarak FrontendIpConfig01 adlı bir ön uç IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ac390-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="ac390-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ac390-115">PARAMETERS</span></span>

### <span data-ttu-id="ac390-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac390-116">-DefaultProfile</span></span>
<span data-ttu-id="ac390-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ac390-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac390-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="ac390-118">-Name</span></span>
<span data-ttu-id="ac390-119">Bu cmdlet 'in oluşturduğu ön uç IP yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac390-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ac390-120">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="ac390-120">-PrivateIpAddress</span></span>
<span data-ttu-id="ac390-121">Yük dengeleyicinin özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac390-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="ac390-122">Bu parametreyi yalnızca, *alt ağ* parametresini de belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="ac390-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac390-123">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="ac390-123">-PublicIpAddress</span></span>
<span data-ttu-id="ac390-124">Ön uç IP yapılandırmasıyla ilişkilendirilecek **Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac390-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac390-125">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="ac390-125">-PublicIpAddressId</span></span>
<span data-ttu-id="ac390-126">Ön uç IP yapılandırmasıyla ilişkilendirilecek **Publicıpaddress** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac390-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac390-127">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="ac390-127">-Subnet</span></span>
<span data-ttu-id="ac390-128">Ön uç IP yapılandırması oluşturacağınız **alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac390-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac390-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ac390-129">-SubnetId</span></span>
<span data-ttu-id="ac390-130">Ön uç IP yapılandırması oluşturacağınız alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac390-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac390-131">-Bölge</span><span class="sxs-lookup"><span data-stu-id="ac390-131">-Zone</span></span>
<span data-ttu-id="ac390-132">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="ac390-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac390-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac390-133">CommonParameters</span></span>
<span data-ttu-id="ac390-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ac390-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac390-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac390-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac390-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ac390-136">INPUTS</span></span>

## <span data-ttu-id="ac390-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ac390-137">OUTPUTS</span></span>

### <span data-ttu-id="ac390-138">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration yapılandırması</span><span class="sxs-lookup"><span data-stu-id="ac390-138">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="ac390-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ac390-139">NOTES</span></span>

## <span data-ttu-id="ac390-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ac390-140">RELATED LINKS</span></span>

[<span data-ttu-id="ac390-141">Add-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="ac390-141">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ac390-142">Get-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="ac390-142">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ac390-143">Yeni-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="ac390-143">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="ac390-144">Remove-Azurermloadbalancerfrontendıconfig</span><span class="sxs-lookup"><span data-stu-id="ac390-144">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ac390-145">Set-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="ac390-145">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)

