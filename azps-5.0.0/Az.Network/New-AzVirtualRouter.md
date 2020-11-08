---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 9bfaea690ab23df6e7ba5480aaeb28ca00dfa20c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276400"
---
# <span data-ttu-id="338cc-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="338cc-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="338cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="338cc-102">SYNOPSIS</span></span>
<span data-ttu-id="338cc-103">Bir Azure VirtualRouter oluşturur.</span><span class="sxs-lookup"><span data-stu-id="338cc-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="338cc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="338cc-104">SYNTAX</span></span>

```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedSubnet <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="338cc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="338cc-105">DESCRIPTION</span></span>
<span data-ttu-id="338cc-106">**New-AzVirtualRouter** cmdlet 'ı bir Azure virtualrouter oluşturur</span><span class="sxs-lookup"><span data-stu-id="338cc-106">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>

## <span data-ttu-id="338cc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="338cc-107">EXAMPLES</span></span>

### <span data-ttu-id="338cc-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="338cc-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzVirtualRouter -Name $virtualRouterName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="338cc-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="338cc-109">PARAMETERS</span></span>

### <span data-ttu-id="338cc-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="338cc-110">-AsJob</span></span>
<span data-ttu-id="338cc-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="338cc-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="338cc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="338cc-112">-DefaultProfile</span></span>
<span data-ttu-id="338cc-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="338cc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="338cc-114">-Force</span><span class="sxs-lookup"><span data-stu-id="338cc-114">-Force</span></span>
<span data-ttu-id="338cc-115">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="338cc-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="338cc-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="338cc-116">-HostedSubnet</span></span>
<span data-ttu-id="338cc-117">Sanal yönlendiricinin barındırıldığı alt ağ.</span><span class="sxs-lookup"><span data-stu-id="338cc-117">The subnet where the virtual router is hosted.</span></span>

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

### <span data-ttu-id="338cc-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="338cc-118">-Location</span></span>
<span data-ttu-id="338cc-119">Konum.</span><span class="sxs-lookup"><span data-stu-id="338cc-119">The location.</span></span>

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

### <span data-ttu-id="338cc-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="338cc-120">-Name</span></span>
<span data-ttu-id="338cc-121">Sanal yönlendiricinin adı.</span><span class="sxs-lookup"><span data-stu-id="338cc-121">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="338cc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="338cc-122">-ResourceGroupName</span></span>
<span data-ttu-id="338cc-123">Sanal yönlendiricinin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="338cc-123">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="338cc-124">Etiketli</span><span class="sxs-lookup"><span data-stu-id="338cc-124">-Tag</span></span>
<span data-ttu-id="338cc-125">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="338cc-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="338cc-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="338cc-126">-Confirm</span></span>
<span data-ttu-id="338cc-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="338cc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="338cc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="338cc-128">-WhatIf</span></span>
<span data-ttu-id="338cc-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="338cc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="338cc-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="338cc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="338cc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="338cc-131">CommonParameters</span></span>
<span data-ttu-id="338cc-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="338cc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="338cc-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="338cc-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="338cc-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="338cc-134">INPUTS</span></span>

### <span data-ttu-id="338cc-135">System. String</span><span class="sxs-lookup"><span data-stu-id="338cc-135">System.String</span></span>

### <span data-ttu-id="338cc-136">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="338cc-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="338cc-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="338cc-137">OUTPUTS</span></span>

### <span data-ttu-id="338cc-138">Microsoft. Azure. Commands. Network. modeller. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="338cc-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="338cc-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="338cc-139">NOTES</span></span>

## <span data-ttu-id="338cc-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="338cc-140">RELATED LINKS</span></span>
