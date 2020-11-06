---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-AzureRmNetworkProfileContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfigIpConfig.md
ms.openlocfilehash: 0a2157d006277aa491281c51f1c3b7a910b8a5c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591360"
---
# <span data-ttu-id="b62ae-101">New-AzureRmNetworkProfileContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="b62ae-101">New-AzureRmNetworkProfileContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="b62ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b62ae-102">SYNOPSIS</span></span>
<span data-ttu-id="b62ae-103">Kapsayıcı NIC yapılandırması IP yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b62ae-103">Creates a container nic configuration ip configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b62ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b62ae-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfileContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b62ae-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b62ae-105">DESCRIPTION</span></span>
<span data-ttu-id="b62ae-106">**Yeni-Azurermnetworkprofilecontainernicconfigıconfig** cmdlet 'i yeni bir kapsayıcı ağ arabirimi yapılandırması IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b62ae-106">The **New-AzureRmNetworkProfileContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="b62ae-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b62ae-107">EXAMPLES</span></span>

### <span data-ttu-id="b62ae-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b62ae-108">Example 1</span></span>
```powershell
$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzureRmVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzureRmNetworkProfileContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzureRmNetworkProfileContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzureRmNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="b62ae-109">İlk iki komut bir VNET ve bir alt ağ oluşturur ve başlatır.</span><span class="sxs-lookup"><span data-stu-id="b62ae-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="b62ae-110">Üçüncü komut, oluşturulan alt ağa başvuruda bulunan bir kapsayıcı NIC IP yapılandırması profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b62ae-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span>  <span data-ttu-id="b62ae-111">Dördüncü komut, önceki komutta oluşturulan IP yapılandırması profilini sağlayan bir kapsayıcı ağı arabirim yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b62ae-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="b62ae-112">Son olarak, beşinci komut, $containerNicConfig depolanan kapsayıcı ağ arabirimi yapılandırması ile başlatılmış bir ağ profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b62ae-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="b62ae-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b62ae-113">PARAMETERS</span></span>

### <span data-ttu-id="b62ae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b62ae-114">-DefaultProfile</span></span>
<span data-ttu-id="b62ae-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b62ae-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b62ae-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="b62ae-116">-Name</span></span>
<span data-ttu-id="b62ae-117">Kapsayıcı ağ arabirimi yapılandırması IP yapılandırma profilinin adı.</span><span class="sxs-lookup"><span data-stu-id="b62ae-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="b62ae-118">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="b62ae-118">-Subnet</span></span>
<span data-ttu-id="b62ae-119">AI</span><span class="sxs-lookup"><span data-stu-id="b62ae-119">Subnet</span></span>

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

### <span data-ttu-id="b62ae-120">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b62ae-120">-SubnetId</span></span>
<span data-ttu-id="b62ae-121">Alt Netid</span><span class="sxs-lookup"><span data-stu-id="b62ae-121">SubnetId</span></span>

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

### <span data-ttu-id="b62ae-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="b62ae-122">-Confirm</span></span>
<span data-ttu-id="b62ae-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b62ae-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b62ae-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b62ae-124">-WhatIf</span></span>
<span data-ttu-id="b62ae-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b62ae-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b62ae-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b62ae-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b62ae-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b62ae-127">CommonParameters</span></span>
<span data-ttu-id="b62ae-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b62ae-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b62ae-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b62ae-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b62ae-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b62ae-130">INPUTS</span></span>

### <span data-ttu-id="b62ae-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b62ae-131">None</span></span>

## <span data-ttu-id="b62ae-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b62ae-132">OUTPUTS</span></span>

### <span data-ttu-id="b62ae-133">Microsoft. Azure. Commands. Network. model. Pscontainernetworkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="b62ae-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="b62ae-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b62ae-134">NOTES</span></span>

## <span data-ttu-id="b62ae-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b62ae-135">RELATED LINKS</span></span>
