---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkProfile.md
ms.openlocfilehash: 370229f44b260367759ca2f51319258627d3d8c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572697"
---
# <span data-ttu-id="7abde-101">Set-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7abde-101">Set-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="7abde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7abde-102">SYNOPSIS</span></span>
<span data-ttu-id="7abde-103">Var olan bir ağ profilinin hedef durumunu ayarlar</span><span class="sxs-lookup"><span data-stu-id="7abde-103">Sets the goal state for an existing network profile</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7abde-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7abde-104">SYNTAX</span></span>

```
Set-AzureRmNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7abde-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7abde-105">DESCRIPTION</span></span>
<span data-ttu-id="7abde-106">**Set-AzureRmPublicIpPrefix** cmdlet 'i ağ profilinin hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7abde-106">The **Set-AzureRmPublicIpPrefix** cmdlet sets the goal state for a network profile.</span></span>

## <span data-ttu-id="7abde-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7abde-107">EXAMPLES</span></span>

### <span data-ttu-id="7abde-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7abde-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzureRmNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzureRmNetworkProfile
```

<span data-ttu-id="7abde-109">İlk komut varolan bir ağ profilini alır.</span><span class="sxs-lookup"><span data-stu-id="7abde-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="7abde-110">İkinci komut bir etiketi güncelleştirir ve üçüncüsü ağ profilinde ağ arabirim yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="7abde-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="7abde-111">Dördüncü komut ağ profilini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7abde-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="7abde-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7abde-112">PARAMETERS</span></span>

### <span data-ttu-id="7abde-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="7abde-113">-AsJob</span></span>
<span data-ttu-id="7abde-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7abde-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7abde-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7abde-115">-DefaultProfile</span></span>
<span data-ttu-id="7abde-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7abde-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7abde-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7abde-117">-NetworkProfile</span></span>
<span data-ttu-id="7abde-118">Ağ profili</span><span class="sxs-lookup"><span data-stu-id="7abde-118">The network profile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7abde-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="7abde-119">-Confirm</span></span>
<span data-ttu-id="7abde-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7abde-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7abde-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7abde-121">-WhatIf</span></span>
<span data-ttu-id="7abde-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7abde-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7abde-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7abde-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7abde-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7abde-124">CommonParameters</span></span>
<span data-ttu-id="7abde-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7abde-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7abde-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7abde-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7abde-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7abde-127">INPUTS</span></span>

### <span data-ttu-id="7abde-128">Microsoft. Azure. Commands. Network. modeller. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7abde-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="7abde-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7abde-129">OUTPUTS</span></span>

### <span data-ttu-id="7abde-130">Microsoft. Azure. Commands. Network. modeller. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7abde-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="7abde-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7abde-131">NOTES</span></span>

## <span data-ttu-id="7abde-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7abde-132">RELATED LINKS</span></span>
