---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: 3cd241b84f7ac03dc268a8f04df0490f6a9f9665
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939916"
---
# <span data-ttu-id="50a8c-101">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="50a8c-101">New-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="50a8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50a8c-102">SYNOPSIS</span></span>
<span data-ttu-id="50a8c-103">Bir yük dengeleyici için ön uç IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="50a8c-103">Creates a front-end IP configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50a8c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50a8c-104">SYNTAX</span></span>

### <span data-ttu-id="50a8c-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="50a8c-105">SetByResourceSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -Subnet <PSSubnet>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50a8c-106">Setbyresourceıdsubnet</span><span class="sxs-lookup"><span data-stu-id="50a8c-106">SetByResourceIdSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -SubnetId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50a8c-107">Setbyresourceidpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="50a8c-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddressId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50a8c-108">Setbyresourcepublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="50a8c-108">SetByResourcePublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddress <PSPublicIpAddress>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="50a8c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="50a8c-109">DESCRIPTION</span></span>
<span data-ttu-id="50a8c-110">**Yeni-Azurermloadbalancerfrontendıl** cmdlet 'i, bir Azure yük dengeleyicisi için ön uç IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="50a8c-110">The **New-AzureRmLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="50a8c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50a8c-111">EXAMPLES</span></span>

### <span data-ttu-id="50a8c-112">Örnek 1: yük dengeleyici için ön uç IP yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="50a8c-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="50a8c-113">İlk komut MyResourceGroup adlı kaynak grubunda MyPublicIP adlı bir dinamik ortak IP adresi oluşturur ve $publicip değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="50a8c-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="50a8c-114">İkinci komut, $publicip genel IP adresini kullanarak FrontendIpConfig01 adlı bir ön uç IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="50a8c-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="50a8c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50a8c-115">PARAMETERS</span></span>

### <span data-ttu-id="50a8c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50a8c-116">-DefaultProfile</span></span>
<span data-ttu-id="50a8c-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="50a8c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50a8c-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="50a8c-118">-Name</span></span>
<span data-ttu-id="50a8c-119">Bu cmdlet 'in oluşturduğu ön uç IP yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50a8c-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="50a8c-120">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="50a8c-120">-PrivateIpAddress</span></span>
<span data-ttu-id="50a8c-121">Yük dengeleyicinin özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="50a8c-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="50a8c-122">Bu parametreyi yalnızca, *alt ağ* parametresini de belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="50a8c-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50a8c-123">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="50a8c-123">-PublicIpAddress</span></span>
<span data-ttu-id="50a8c-124">Ön uç IP yapılandırmasıyla ilişkilendirilecek **Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="50a8c-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50a8c-125">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="50a8c-125">-PublicIpAddressId</span></span>
<span data-ttu-id="50a8c-126">Ön uç IP yapılandırmasıyla ilişkilendirilecek **Publicıpaddress** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="50a8c-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50a8c-127">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="50a8c-127">-Subnet</span></span>
<span data-ttu-id="50a8c-128">Ön uç IP yapılandırması oluşturacağınız **alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="50a8c-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50a8c-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="50a8c-129">-SubnetId</span></span>
<span data-ttu-id="50a8c-130">Ön uç IP yapılandırması oluşturacağınız alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="50a8c-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50a8c-131">-Bölge</span><span class="sxs-lookup"><span data-stu-id="50a8c-131">-Zone</span></span>
<span data-ttu-id="50a8c-132">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="50a8c-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="50a8c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50a8c-133">CommonParameters</span></span>
<span data-ttu-id="50a8c-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="50a8c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50a8c-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50a8c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50a8c-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50a8c-136">INPUTS</span></span>

## <span data-ttu-id="50a8c-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50a8c-137">OUTPUTS</span></span>

### <span data-ttu-id="50a8c-138">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration yapılandırması</span><span class="sxs-lookup"><span data-stu-id="50a8c-138">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="50a8c-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50a8c-139">NOTES</span></span>

## <span data-ttu-id="50a8c-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50a8c-140">RELATED LINKS</span></span>

[<span data-ttu-id="50a8c-141">Add-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="50a8c-141">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="50a8c-142">Get-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="50a8c-142">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="50a8c-143">Yeni-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="50a8c-143">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="50a8c-144">Remove-Azurermloadbalancerfrontendıconfig</span><span class="sxs-lookup"><span data-stu-id="50a8c-144">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="50a8c-145">Set-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="50a8c-145">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


