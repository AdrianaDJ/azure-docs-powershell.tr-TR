---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
ms.openlocfilehash: 24cbdaebc21456268d050b5c3a56ec9fc443fedf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760363"
---
# <span data-ttu-id="c1bbe-101">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1bbe-101">New-AzContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="c1bbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1bbe-102">SYNOPSIS</span></span>
<span data-ttu-id="c1bbe-103">Kapsayıcı NIC yapılandırması IP yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c1bbe-103">Creates a container nic configuration ip configuration object.</span></span>

## <span data-ttu-id="c1bbe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c1bbe-104">SYNTAX</span></span>

```
New-AzContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1bbe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1bbe-105">DESCRIPTION</span></span>
<span data-ttu-id="c1bbe-106">**Yeni-Azcontainernicconfigıconfig** cmdlet 'i yeni bir kapsayıcı ağ arabirimi yapılandırması IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c1bbe-106">The **New-AzContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="c1bbe-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c1bbe-107">EXAMPLES</span></span>

### <span data-ttu-id="c1bbe-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c1bbe-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="c1bbe-109">İlk iki komut bir VNET ve bir alt ağ oluşturur ve başlatır.</span><span class="sxs-lookup"><span data-stu-id="c1bbe-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="c1bbe-110">Üçüncü komut, oluşturulan alt ağa başvuruda bulunan bir kapsayıcı NIC IP yapılandırması profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c1bbe-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span> <span data-ttu-id="c1bbe-111">Dördüncü komut, önceki komutta oluşturulan IP yapılandırması profilini sağlayan bir kapsayıcı ağı arabirim yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c1bbe-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="c1bbe-112">Son olarak, beşinci komut, $containerNicConfig depolanan kapsayıcı ağ arabirimi yapılandırması ile başlatılmış bir ağ profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c1bbe-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="c1bbe-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c1bbe-113">PARAMETERS</span></span>

### <span data-ttu-id="c1bbe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1bbe-114">-DefaultProfile</span></span>
<span data-ttu-id="c1bbe-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c1bbe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1bbe-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="c1bbe-116">-Name</span></span>
<span data-ttu-id="c1bbe-117">Kapsayıcı ağ arabirimi yapılandırması IP yapılandırma profilinin adı.</span><span class="sxs-lookup"><span data-stu-id="c1bbe-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="c1bbe-118">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="c1bbe-118">-Subnet</span></span>
<span data-ttu-id="c1bbe-119">AI</span><span class="sxs-lookup"><span data-stu-id="c1bbe-119">Subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1bbe-120">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c1bbe-120">-SubnetId</span></span>
<span data-ttu-id="c1bbe-121">Alt Netid</span><span class="sxs-lookup"><span data-stu-id="c1bbe-121">SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1bbe-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="c1bbe-122">-Confirm</span></span>
<span data-ttu-id="c1bbe-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c1bbe-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1bbe-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1bbe-124">-WhatIf</span></span>
<span data-ttu-id="c1bbe-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c1bbe-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1bbe-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c1bbe-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1bbe-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1bbe-127">CommonParameters</span></span>
<span data-ttu-id="c1bbe-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c1bbe-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1bbe-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1bbe-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1bbe-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c1bbe-130">INPUTS</span></span>

### <span data-ttu-id="c1bbe-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c1bbe-131">None</span></span>

## <span data-ttu-id="c1bbe-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c1bbe-132">OUTPUTS</span></span>

### <span data-ttu-id="c1bbe-133">Microsoft. Azure. Commands. Network. model. Pscontainernetworkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="c1bbe-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="c1bbe-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c1bbe-134">NOTES</span></span>

## <span data-ttu-id="c1bbe-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c1bbe-135">RELATED LINKS</span></span>

[<span data-ttu-id="c1bbe-136">Yeni-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="c1bbe-136">New-AzContainerNicConfig</span></span>](./New-AzContainerNicConfig.md)