---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-AzureRmNetworkProfileContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfig.md
ms.openlocfilehash: b697fcd991304401e2af754cc223f19b956f2143
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764930"
---
# <span data-ttu-id="a5923-101">New-AzureRmNetworkProfileContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="a5923-101">New-AzureRmNetworkProfileContainerNicConfig</span></span>

## <span data-ttu-id="a5923-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5923-102">SYNOPSIS</span></span>
<span data-ttu-id="a5923-103">Yeni bir kapsayıcı ağ arabirimi yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a5923-103">Creates a new container network interface configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5923-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5923-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfileContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5923-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5923-105">DESCRIPTION</span></span>
<span data-ttu-id="a5923-106">**Yeni-AzureRmNetworkProfileContainerNicConfig** cmdlet 'i yeni bir kapsayıcı ağ arabirimi yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a5923-106">The **New-AzureRmNetworkProfileContainerNicConfig** cmdlet creates a new container network interface configuration object.</span></span> <span data-ttu-id="a5923-107">Bu nesne, üst ağ profiline başvuruda bulunan interfacs kapsayıcısının ağ özelliklerini belirler.</span><span class="sxs-lookup"><span data-stu-id="a5923-107">This object determines the characteristics of container network interfacs created referencing the parent network profile.</span></span>

## <span data-ttu-id="a5923-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5923-108">EXAMPLES</span></span>

### <span data-ttu-id="a5923-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a5923-109">Example 1</span></span>
```powershell
$containerNicConfig = New-AzureRmNetworkProfileContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="a5923-110">İlk komut boş bir konteyner ağı arabirim yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a5923-110">The first command creates an empty container network interface configuration.</span></span> <span data-ttu-id="a5923-111">İkincisi, önceden oluşturulmuş kapsayıcı ağı arabirim yapılandırmasını bağımsız değişken olarak New-NetworkProfile cmdlet 'ine geçirerek yeni bir ağ profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a5923-111">The second creates a new network profile, passing the previously created container network interface configuration as an argument to the New-NetworkProfile cmdlet.</span></span>

## <span data-ttu-id="a5923-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5923-112">PARAMETERS</span></span>

### <span data-ttu-id="a5923-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5923-113">-DefaultProfile</span></span>
<span data-ttu-id="a5923-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a5923-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5923-115">-IP yapılandırması</span><span class="sxs-lookup"><span data-stu-id="a5923-115">-IpConfiguration</span></span>
<span data-ttu-id="a5923-116">{{Fill IP açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="a5923-116">{{Fill IpConfiguration Description}}</span></span>

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

### <span data-ttu-id="a5923-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="a5923-117">-Name</span></span>
<span data-ttu-id="a5923-118">Kapsayıcı ağ arabirimi yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="a5923-118">Name of the container network interface configuration.</span></span>

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

### <span data-ttu-id="a5923-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="a5923-119">-Confirm</span></span>
<span data-ttu-id="a5923-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a5923-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5923-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5923-121">-WhatIf</span></span>
<span data-ttu-id="a5923-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5923-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5923-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a5923-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5923-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5923-124">CommonParameters</span></span>
<span data-ttu-id="a5923-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5923-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5923-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5923-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5923-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5923-127">INPUTS</span></span>

### <span data-ttu-id="a5923-128">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSIPConfigurationProfile, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a5923-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a5923-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5923-129">OUTPUTS</span></span>

### <span data-ttu-id="a5923-130">Microsoft. Azure. Commands. Network. model. Pscontainernetworkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="a5923-130">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="a5923-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5923-131">NOTES</span></span>

## <span data-ttu-id="a5923-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5923-132">RELATED LINKS</span></span>
