---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
ms.openlocfilehash: aaace7e8bb7d1f2ed57ebad28f7b5a3399f0e190
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932369"
---
# <span data-ttu-id="ec312-101">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="ec312-101">New-AzContainerNicConfig</span></span>

## <span data-ttu-id="ec312-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec312-102">SYNOPSIS</span></span>
<span data-ttu-id="ec312-103">Yeni bir kapsayıcı ağ arabirimi yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ec312-103">Creates a new container network interface configuration object.</span></span>

## <span data-ttu-id="ec312-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec312-104">SYNTAX</span></span>

```
New-AzContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec312-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec312-105">DESCRIPTION</span></span>
<span data-ttu-id="ec312-106">**Yeni-AzContainerNicConfig** cmdlet 'i yeni bir kapsayıcı ağ arabirimi yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ec312-106">The **New-AzContainerNicConfig** cmdlet creates a new container network interface configuration object.</span></span> <span data-ttu-id="ec312-107">Bu nesne, üst ağ profiline başvuruda bulunan kapsayıcı ağ arabiriminin özelliklerini belirler.</span><span class="sxs-lookup"><span data-stu-id="ec312-107">This object determines the characteristics of container network interface created referencing the parent network profile.</span></span>

## <span data-ttu-id="ec312-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec312-108">EXAMPLES</span></span>

### <span data-ttu-id="ec312-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ec312-109">Example 1</span></span>
```powershell
$containerNicConfig = New-AzContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="ec312-110">İlk komut boş bir konteyner ağı arabirim yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ec312-110">The first command creates an empty container network interface configuration.</span></span> <span data-ttu-id="ec312-111">İkincisi, önceden oluşturulmuş kapsayıcı ağı arabirim yapılandırmasını bağımsız değişken olarak New-NetworkProfile cmdlet 'ine geçirerek yeni bir ağ profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ec312-111">The second creates a new network profile, passing the previously created container network interface configuration as an argument to the New-NetworkProfile cmdlet.</span></span>

## <span data-ttu-id="ec312-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec312-112">PARAMETERS</span></span>

### <span data-ttu-id="ec312-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec312-113">-DefaultProfile</span></span>
<span data-ttu-id="ec312-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ec312-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec312-115">-IP yapılandırması</span><span class="sxs-lookup"><span data-stu-id="ec312-115">-IpConfiguration</span></span>
<span data-ttu-id="ec312-116">Bu kapsayıcıdaki bir kapsayıcı NIC örneği oluşturulduğunda hangi IP yapılandırmalarının oluşturulduğunu belirleyen IP yapılandırma profilleri koleksiyonu</span><span class="sxs-lookup"><span data-stu-id="ec312-116">Collection of IP configuration profiles which determine what ip configurations are created when a container nic is instantiated from this container network interface configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]
Parameter Sets: (All)
Aliases: IpConfig

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec312-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="ec312-117">-Name</span></span>
<span data-ttu-id="ec312-118">Kapsayıcı ağ arabirimi yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="ec312-118">Name of the container network interface configuration.</span></span>

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

### <span data-ttu-id="ec312-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="ec312-119">-Confirm</span></span>
<span data-ttu-id="ec312-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ec312-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec312-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec312-121">-WhatIf</span></span>
<span data-ttu-id="ec312-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ec312-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec312-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ec312-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec312-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec312-124">CommonParameters</span></span>
<span data-ttu-id="ec312-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec312-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec312-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec312-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec312-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec312-127">INPUTS</span></span>

### <span data-ttu-id="ec312-128">Microsoft. Azure. Commands. Network. model. PSIPConfigurationProfile []</span><span class="sxs-lookup"><span data-stu-id="ec312-128">Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]</span></span>

## <span data-ttu-id="ec312-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec312-129">OUTPUTS</span></span>

### <span data-ttu-id="ec312-130">Microsoft. Azure. Commands. Network. model. Pscontainernetworkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="ec312-130">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="ec312-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec312-131">NOTES</span></span>

## <span data-ttu-id="ec312-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec312-132">RELATED LINKS</span></span>

[<span data-ttu-id="ec312-133">Yeni-Azcontainernicconfigıconfig</span><span class="sxs-lookup"><span data-stu-id="ec312-133">New-AzContainerNicConfigIpConfig</span></span>](./New-AzContainerNicConfigIpConfig.md)
