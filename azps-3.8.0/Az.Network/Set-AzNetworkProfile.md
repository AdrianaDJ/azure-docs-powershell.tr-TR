---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
ms.openlocfilehash: edbfdcdfc7e02c8bfdb266e1ec7a6b1308c07fa2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097963"
---
# <span data-ttu-id="ff14e-101">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ff14e-101">Set-AzNetworkProfile</span></span>

## <span data-ttu-id="ff14e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff14e-102">SYNOPSIS</span></span>
<span data-ttu-id="ff14e-103">Ağ profilini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ff14e-103">Updates a network profile.</span></span>

## <span data-ttu-id="ff14e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ff14e-104">SYNTAX</span></span>

```
Set-AzNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff14e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ff14e-105">DESCRIPTION</span></span>
<span data-ttu-id="ff14e-106">**Set-AzPublicIpPrefix** cmdlet 'i bir ağ profilini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ff14e-106">The **Set-AzPublicIpPrefix** cmdlet updates a network profile.</span></span>

## <span data-ttu-id="ff14e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ff14e-107">EXAMPLES</span></span>

### <span data-ttu-id="ff14e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ff14e-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzNetworkProfile
```

<span data-ttu-id="ff14e-109">İlk komut varolan bir ağ profilini alır.</span><span class="sxs-lookup"><span data-stu-id="ff14e-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="ff14e-110">İkinci komut bir etiketi güncelleştirir ve üçüncüsü ağ profilinde ağ arabirim yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="ff14e-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="ff14e-111">Dördüncü komut ağ profilini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ff14e-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="ff14e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ff14e-112">PARAMETERS</span></span>

### <span data-ttu-id="ff14e-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="ff14e-113">-AsJob</span></span>
<span data-ttu-id="ff14e-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ff14e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ff14e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff14e-115">-DefaultProfile</span></span>
<span data-ttu-id="ff14e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ff14e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff14e-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ff14e-117">-NetworkProfile</span></span>
<span data-ttu-id="ff14e-118">Ağ profili</span><span class="sxs-lookup"><span data-stu-id="ff14e-118">The network profile</span></span>

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

### <span data-ttu-id="ff14e-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="ff14e-119">-Confirm</span></span>
<span data-ttu-id="ff14e-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ff14e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff14e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff14e-121">-WhatIf</span></span>
<span data-ttu-id="ff14e-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ff14e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff14e-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ff14e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff14e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff14e-124">CommonParameters</span></span>
<span data-ttu-id="ff14e-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ff14e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff14e-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff14e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff14e-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ff14e-127">INPUTS</span></span>

### <span data-ttu-id="ff14e-128">Microsoft. Azure. Commands. Network. modeller. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ff14e-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="ff14e-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ff14e-129">OUTPUTS</span></span>

### <span data-ttu-id="ff14e-130">Microsoft. Azure. Commands. Network. modeller. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ff14e-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="ff14e-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ff14e-131">NOTES</span></span>

## <span data-ttu-id="ff14e-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ff14e-132">RELATED LINKS</span></span>

[<span data-ttu-id="ff14e-133">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ff14e-133">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="ff14e-134">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ff14e-134">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="ff14e-135">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ff14e-135">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)
