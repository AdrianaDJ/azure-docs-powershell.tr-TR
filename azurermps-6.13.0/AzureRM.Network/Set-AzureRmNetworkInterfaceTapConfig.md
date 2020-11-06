---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: b2034f27cb6c5332b190e3412963dde99f4c9ba0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572701"
---
# <span data-ttu-id="c2642-101">Set-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c2642-101">Set-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="c2642-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2642-102">SYNOPSIS</span></span>
<span data-ttu-id="c2642-103">Bir dokunun yapılandırmasının hedef durumunu ayarlar</span><span class="sxs-lookup"><span data-stu-id="c2642-103">Sets the goal state of a Tap Configuration</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2642-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c2642-104">SYNTAX</span></span>

```
Set-AzureRmNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2642-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c2642-105">DESCRIPTION</span></span>
<span data-ttu-id="c2642-106">**Set-Azurermnetworkınterfacetapconfig** , bir Azure ağ arabiriminin hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c2642-106">The **Set-AzureRmNetworkInterfaceTapConfig** sets the goal state for an Azure network interface.</span></span>

## <span data-ttu-id="c2642-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c2642-107">EXAMPLES</span></span>

### <span data-ttu-id="c2642-108">Örnek 1: güncelleştirilmiş TapConfig adıyla TapConfiguration 'ı ayarlama</span><span class="sxs-lookup"><span data-stu-id="c2642-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzureRmNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="c2642-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c2642-109">PARAMETERS</span></span>

### <span data-ttu-id="c2642-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="c2642-110">-AsJob</span></span>
<span data-ttu-id="c2642-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c2642-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2642-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2642-112">-DefaultProfile</span></span>
<span data-ttu-id="c2642-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c2642-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2642-114">-Force</span><span class="sxs-lookup"><span data-stu-id="c2642-114">-Force</span></span>
<span data-ttu-id="c2642-115">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="c2642-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c2642-116">-Networkınterfacetapconfig</span><span class="sxs-lookup"><span data-stu-id="c2642-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="c2642-117">Ağ arabirimi yapılandırması</span><span class="sxs-lookup"><span data-stu-id="c2642-117">The NetworkInterface Tap configurtion</span></span>

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

### <span data-ttu-id="c2642-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="c2642-118">-Confirm</span></span>
<span data-ttu-id="c2642-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c2642-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2642-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2642-120">-WhatIf</span></span>
<span data-ttu-id="c2642-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c2642-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2642-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c2642-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2642-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2642-123">CommonParameters</span></span>
<span data-ttu-id="c2642-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c2642-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2642-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2642-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2642-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c2642-126">INPUTS</span></span>

### <span data-ttu-id="c2642-127">Microsoft. Azure. Commands. Network. model. Psnetworkınterfacetapconfiguration</span><span class="sxs-lookup"><span data-stu-id="c2642-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="c2642-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c2642-128">OUTPUTS</span></span>

### <span data-ttu-id="c2642-129">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="c2642-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="c2642-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c2642-130">NOTES</span></span>

## <span data-ttu-id="c2642-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c2642-131">RELATED LINKS</span></span>
