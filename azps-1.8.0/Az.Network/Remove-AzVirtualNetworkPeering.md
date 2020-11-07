---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 3071b07e73d5038b5efef8a76b689dc0fff87e01
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760100"
---
# <span data-ttu-id="ac95c-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ac95c-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="ac95c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac95c-102">SYNOPSIS</span></span>
<span data-ttu-id="ac95c-103">Sanal ağ eşliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ac95c-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="ac95c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ac95c-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac95c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ac95c-105">DESCRIPTION</span></span>
<span data-ttu-id="ac95c-106">Sanal ağ eşliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ac95c-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="ac95c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ac95c-107">EXAMPLES</span></span>

### <span data-ttu-id="ac95c-108">Örnek 1: sanal ağ eşliğini kaldırma</span><span class="sxs-lookup"><span data-stu-id="ac95c-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="ac95c-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ac95c-109">PARAMETERS</span></span>

### <span data-ttu-id="ac95c-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="ac95c-110">-AsJob</span></span>
<span data-ttu-id="ac95c-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ac95c-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac95c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac95c-112">-DefaultProfile</span></span>
<span data-ttu-id="ac95c-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ac95c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac95c-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ac95c-114">-Force</span></span>
<span data-ttu-id="ac95c-115">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="ac95c-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ac95c-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="ac95c-116">-Name</span></span>
<span data-ttu-id="ac95c-117">Sanal ağ eşleme adı.</span><span class="sxs-lookup"><span data-stu-id="ac95c-117">The virtual network peering name.</span></span>

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

### <span data-ttu-id="ac95c-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ac95c-118">-PassThru</span></span>
<span data-ttu-id="ac95c-119">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="ac95c-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ac95c-120">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="ac95c-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ac95c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac95c-121">-ResourceGroupName</span></span>
<span data-ttu-id="ac95c-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ac95c-122">The resource group name</span></span>

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

### <span data-ttu-id="ac95c-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ac95c-123">-VirtualNetworkName</span></span>
<span data-ttu-id="ac95c-124">Sanal ağ adı.</span><span class="sxs-lookup"><span data-stu-id="ac95c-124">The virtual network name.</span></span>

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

### <span data-ttu-id="ac95c-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="ac95c-125">-Confirm</span></span>
<span data-ttu-id="ac95c-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ac95c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac95c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac95c-127">-WhatIf</span></span>
<span data-ttu-id="ac95c-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac95c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac95c-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ac95c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac95c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac95c-130">CommonParameters</span></span>
<span data-ttu-id="ac95c-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ac95c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac95c-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac95c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac95c-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ac95c-133">INPUTS</span></span>

### <span data-ttu-id="ac95c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ac95c-134">System.String</span></span>

## <span data-ttu-id="ac95c-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ac95c-135">OUTPUTS</span></span>

### <span data-ttu-id="ac95c-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ac95c-136">System.Boolean</span></span>

## <span data-ttu-id="ac95c-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ac95c-137">NOTES</span></span>

## <span data-ttu-id="ac95c-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ac95c-138">RELATED LINKS</span></span>

[<span data-ttu-id="ac95c-139">Add-azvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="ac95c-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="ac95c-140">Get-azvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="ac95c-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="ac95c-141">Set-azvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="ac95c-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)