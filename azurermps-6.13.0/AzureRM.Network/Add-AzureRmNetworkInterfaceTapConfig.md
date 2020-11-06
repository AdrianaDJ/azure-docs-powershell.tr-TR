---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: 10d51bd2e70db0d2b1d06b907769fb6842e413cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594883"
---
# <span data-ttu-id="93e75-101">Add-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="93e75-101">Add-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="93e75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93e75-102">SYNOPSIS</span></span>
<span data-ttu-id="93e75-103">Bir NetworkInterface ile ilişkilendirilmiş bir TapConfiguration kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="93e75-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="93e75-104">Bu, var olan bir VirtualNetworkTap kaynağına başvurur.</span><span class="sxs-lookup"><span data-stu-id="93e75-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93e75-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="93e75-105">SYNTAX</span></span>

### <span data-ttu-id="93e75-106">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="93e75-106">SetByResource (Default)</span></span>
```
Add-AzureRmNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93e75-107">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="93e75-107">SetByResourceId</span></span>
```
Add-AzureRmNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93e75-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="93e75-108">DESCRIPTION</span></span>
<span data-ttu-id="93e75-109">**Add-Azurermnetworkınterfacetapconfig** cmdlet 'i, bir NetworkInterface ile Ilişkilendirilmiş bir tapconfiguration kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="93e75-109">The **Add-AzureRmNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="93e75-110">Bu, var olan bir VirtualNetworkTap kaynağına başvurur.</span><span class="sxs-lookup"><span data-stu-id="93e75-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="93e75-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="93e75-111">EXAMPLES</span></span>

### <span data-ttu-id="93e75-112">Örnek 1: verilen bir ağ arabirimine TapConfiguration ekleme</span><span class="sxs-lookup"><span data-stu-id="93e75-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzureRmNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="93e75-113">Bir kaynak.</span><span class="sxs-lookup"><span data-stu-id="93e75-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="93e75-114">Sourcenıc VM 'nin trafiği vVirtualNetworkTap kaynağında başvurulan hedef VM 'ye yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="93e75-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="93e75-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="93e75-115">PARAMETERS</span></span>

### <span data-ttu-id="93e75-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93e75-116">-DefaultProfile</span></span>
<span data-ttu-id="93e75-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="93e75-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93e75-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="93e75-118">-Name</span></span>
<span data-ttu-id="93e75-119">Dokunun yapılandırması adı.</span><span class="sxs-lookup"><span data-stu-id="93e75-119">Name of the tap configuration.</span></span>

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

### <span data-ttu-id="93e75-120">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="93e75-120">-NetworkInterface</span></span>
<span data-ttu-id="93e75-121">Ağ arabirim kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="93e75-121">The reference of the network interface resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93e75-122">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="93e75-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="93e75-123">Sanal ağın başvurusu kaynak 'a dokunun.</span><span class="sxs-lookup"><span data-stu-id="93e75-123">The reference of the virtual network tap resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93e75-124">-VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="93e75-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="93e75-125">Sanal ağın başvurusu kaynak 'a dokunun.</span><span class="sxs-lookup"><span data-stu-id="93e75-125">The reference of the virtual network tap resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93e75-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="93e75-126">-Confirm</span></span>
<span data-ttu-id="93e75-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="93e75-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93e75-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93e75-128">-WhatIf</span></span>
<span data-ttu-id="93e75-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="93e75-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93e75-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="93e75-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93e75-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93e75-131">CommonParameters</span></span>
<span data-ttu-id="93e75-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="93e75-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93e75-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93e75-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93e75-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="93e75-134">INPUTS</span></span>

### <span data-ttu-id="93e75-135">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="93e75-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="93e75-136">System. String</span><span class="sxs-lookup"><span data-stu-id="93e75-136">System.String</span></span>

### <span data-ttu-id="93e75-137">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="93e75-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="93e75-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="93e75-138">OUTPUTS</span></span>

### <span data-ttu-id="93e75-139">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="93e75-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="93e75-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="93e75-140">NOTES</span></span>

## <span data-ttu-id="93e75-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="93e75-141">RELATED LINKS</span></span>
