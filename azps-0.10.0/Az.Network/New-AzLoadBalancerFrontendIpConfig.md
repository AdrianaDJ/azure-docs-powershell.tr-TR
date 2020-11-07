---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: ba29cef7afe862f8aeb33f66488e0970b5ac6e9c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935390"
---
# <span data-ttu-id="0a4f1-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a4f1-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="0a4f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a4f1-102">SYNOPSIS</span></span>
<span data-ttu-id="0a4f1-103">Bir yük dengeleyici için ön uç IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="0a4f1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0a4f1-104">SYNTAX</span></span>

### <span data-ttu-id="0a4f1-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="0a4f1-105">SetByResourceSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -Subnet <PSSubnet>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0a4f1-106">Setbyresourceıdsubnet</span><span class="sxs-lookup"><span data-stu-id="0a4f1-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -SubnetId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0a4f1-107">Setbyresourceidpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="0a4f1-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddressId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0a4f1-108">Setbyresourcepublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="0a4f1-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddress <PSPublicIpAddress>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a4f1-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="0a4f1-109">DESCRIPTION</span></span>
<span data-ttu-id="0a4f1-110">**Yeni-Azloadbalancerfrontendıconfıg** cmdlet 'i, bir Azure yük dengeleyicisi için ön uç IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-110">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="0a4f1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0a4f1-111">EXAMPLES</span></span>

### <span data-ttu-id="0a4f1-112">Örnek 1: yük dengeleyici için ön uç IP yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="0a4f1-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="0a4f1-113">İlk komut MyResourceGroup adlı kaynak grubunda MyPublicIP adlı bir dinamik ortak IP adresi oluşturur ve $publicip değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="0a4f1-114">İkinci komut, $publicip genel IP adresini kullanarak FrontendIpConfig01 adlı bir ön uç IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="0a4f1-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0a4f1-115">PARAMETERS</span></span>

### <span data-ttu-id="0a4f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a4f1-116">-DefaultProfile</span></span>
<span data-ttu-id="0a4f1-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a4f1-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="0a4f1-118">-Name</span></span>
<span data-ttu-id="0a4f1-119">Bu cmdlet 'in oluşturduğu ön uç IP yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0a4f1-120">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="0a4f1-120">-PrivateIpAddress</span></span>
<span data-ttu-id="0a4f1-121">Yük dengeleyicinin özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="0a4f1-122">Bu parametreyi yalnızca, *alt ağ* parametresini de belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="0a4f1-123">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="0a4f1-123">-PublicIpAddress</span></span>
<span data-ttu-id="0a4f1-124">Ön uç IP yapılandırmasıyla ilişkilendirilecek **Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="0a4f1-125">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="0a4f1-125">-PublicIpAddressId</span></span>
<span data-ttu-id="0a4f1-126">Ön uç IP yapılandırmasıyla ilişkilendirilecek **Publicıpaddress** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="0a4f1-127">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="0a4f1-127">-Subnet</span></span>
<span data-ttu-id="0a4f1-128">Ön uç IP yapılandırması oluşturacağınız **alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="0a4f1-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="0a4f1-129">-SubnetId</span></span>
<span data-ttu-id="0a4f1-130">Ön uç IP yapılandırması oluşturacağınız alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="0a4f1-131">-Bölge</span><span class="sxs-lookup"><span data-stu-id="0a4f1-131">-Zone</span></span>
<span data-ttu-id="0a4f1-132">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="0a4f1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a4f1-133">CommonParameters</span></span>
<span data-ttu-id="0a4f1-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a4f1-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a4f1-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a4f1-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0a4f1-136">INPUTS</span></span>

## <span data-ttu-id="0a4f1-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0a4f1-137">OUTPUTS</span></span>

### <span data-ttu-id="0a4f1-138">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration yapılandırması</span><span class="sxs-lookup"><span data-stu-id="0a4f1-138">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="0a4f1-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0a4f1-139">NOTES</span></span>

## <span data-ttu-id="0a4f1-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0a4f1-140">RELATED LINKS</span></span>

[<span data-ttu-id="0a4f1-141">Add-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="0a4f1-141">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="0a4f1-142">Get-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="0a4f1-142">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="0a4f1-143">New-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="0a4f1-143">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="0a4f1-144">Remove-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="0a4f1-144">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="0a4f1-145">Set-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="0a4f1-145">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


