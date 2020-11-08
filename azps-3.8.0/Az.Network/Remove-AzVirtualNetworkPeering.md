---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 38530b5e4034286d623c82b841064760fe2e49e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103972"
---
# <span data-ttu-id="43943-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="43943-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="43943-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43943-102">SYNOPSIS</span></span>
<span data-ttu-id="43943-103">Sanal ağ eşliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="43943-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="43943-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="43943-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43943-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="43943-105">DESCRIPTION</span></span>
<span data-ttu-id="43943-106">Sanal ağ eşliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="43943-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="43943-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="43943-107">EXAMPLES</span></span>

### <span data-ttu-id="43943-108">Örnek 1: sanal ağ eşliğini kaldırma</span><span class="sxs-lookup"><span data-stu-id="43943-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="43943-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="43943-109">PARAMETERS</span></span>

### <span data-ttu-id="43943-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="43943-110">-AsJob</span></span>
<span data-ttu-id="43943-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="43943-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43943-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43943-112">-DefaultProfile</span></span>
<span data-ttu-id="43943-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="43943-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43943-114">-Force</span><span class="sxs-lookup"><span data-stu-id="43943-114">-Force</span></span>
<span data-ttu-id="43943-115">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="43943-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="43943-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="43943-116">-Name</span></span>
<span data-ttu-id="43943-117">Sanal ağ eşleme adı.</span><span class="sxs-lookup"><span data-stu-id="43943-117">The virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43943-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="43943-118">-PassThru</span></span>
<span data-ttu-id="43943-119">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="43943-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="43943-120">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="43943-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="43943-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43943-121">-ResourceGroupName</span></span>
<span data-ttu-id="43943-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="43943-122">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43943-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="43943-123">-VirtualNetworkName</span></span>
<span data-ttu-id="43943-124">Sanal ağ adı.</span><span class="sxs-lookup"><span data-stu-id="43943-124">The virtual network name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43943-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="43943-125">-Confirm</span></span>
<span data-ttu-id="43943-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="43943-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43943-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43943-127">-WhatIf</span></span>
<span data-ttu-id="43943-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="43943-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43943-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="43943-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43943-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43943-130">CommonParameters</span></span>
<span data-ttu-id="43943-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="43943-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43943-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43943-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43943-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="43943-133">INPUTS</span></span>

### <span data-ttu-id="43943-134">System. String</span><span class="sxs-lookup"><span data-stu-id="43943-134">System.String</span></span>

## <span data-ttu-id="43943-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="43943-135">OUTPUTS</span></span>

### <span data-ttu-id="43943-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43943-136">System.Boolean</span></span>

## <span data-ttu-id="43943-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="43943-137">NOTES</span></span>

## <span data-ttu-id="43943-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="43943-138">RELATED LINKS</span></span>

[<span data-ttu-id="43943-139">Add-azvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="43943-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="43943-140">Get-azvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="43943-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="43943-141">Set-azvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="43943-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
