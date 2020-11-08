---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 31a02e6f27d766d9f74b34c331a69c66e82d8fc5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097964"
---
# <span data-ttu-id="34d3a-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="34d3a-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="34d3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34d3a-102">SYNOPSIS</span></span>
<span data-ttu-id="34d3a-103">Ağ arabirimi için bir dokunma yapılandırması güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="34d3a-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="34d3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34d3a-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34d3a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="34d3a-105">DESCRIPTION</span></span>
<span data-ttu-id="34d3a-106">**Set-Aznetworkınterfacetapconfig** , bir ağ arabiriminin bir dokunma yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="34d3a-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="34d3a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34d3a-107">EXAMPLES</span></span>

### <span data-ttu-id="34d3a-108">Örnek 1: güncelleştirilmiş TapConfig adıyla TapConfiguration 'ı ayarlama</span><span class="sxs-lookup"><span data-stu-id="34d3a-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="34d3a-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34d3a-109">PARAMETERS</span></span>

### <span data-ttu-id="34d3a-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="34d3a-110">-AsJob</span></span>
<span data-ttu-id="34d3a-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="34d3a-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34d3a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34d3a-112">-DefaultProfile</span></span>
<span data-ttu-id="34d3a-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34d3a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34d3a-114">-Force</span><span class="sxs-lookup"><span data-stu-id="34d3a-114">-Force</span></span>
<span data-ttu-id="34d3a-115">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="34d3a-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="34d3a-116">-Networkınterfacetapconfig</span><span class="sxs-lookup"><span data-stu-id="34d3a-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="34d3a-117">NetworkInterface yapılandırma</span><span class="sxs-lookup"><span data-stu-id="34d3a-117">The NetworkInterface Tap configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34d3a-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="34d3a-118">-Confirm</span></span>
<span data-ttu-id="34d3a-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="34d3a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34d3a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34d3a-120">-WhatIf</span></span>
<span data-ttu-id="34d3a-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34d3a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34d3a-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="34d3a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34d3a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34d3a-123">CommonParameters</span></span>
<span data-ttu-id="34d3a-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34d3a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34d3a-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34d3a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34d3a-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34d3a-126">INPUTS</span></span>

### <span data-ttu-id="34d3a-127">Microsoft. Azure. Commands. Network. model. Psnetworkınterfacetapconfiguration</span><span class="sxs-lookup"><span data-stu-id="34d3a-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="34d3a-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34d3a-128">OUTPUTS</span></span>

### <span data-ttu-id="34d3a-129">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="34d3a-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="34d3a-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34d3a-130">NOTES</span></span>

## <span data-ttu-id="34d3a-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34d3a-131">RELATED LINKS</span></span>

[<span data-ttu-id="34d3a-132">Add-Aznetworkınterfacetapconfig</span><span class="sxs-lookup"><span data-stu-id="34d3a-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="34d3a-133">Get-Aznetworkınterfacetapconfig</span><span class="sxs-lookup"><span data-stu-id="34d3a-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="34d3a-134">Remove-Aznetworkınterfacetapconfig</span><span class="sxs-lookup"><span data-stu-id="34d3a-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)
