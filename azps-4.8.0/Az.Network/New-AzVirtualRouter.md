---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 9bfaea690ab23df6e7ba5480aaeb28ca00dfa20c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274812"
---
# <span data-ttu-id="dbe78-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="dbe78-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="dbe78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbe78-102">SYNOPSIS</span></span>
<span data-ttu-id="dbe78-103">Bir Azure VirtualRouter oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dbe78-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="dbe78-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dbe78-104">SYNTAX</span></span>

```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedSubnet <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dbe78-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dbe78-105">DESCRIPTION</span></span>
<span data-ttu-id="dbe78-106">**New-AzVirtualRouter** cmdlet 'ı bir Azure virtualrouter oluşturur</span><span class="sxs-lookup"><span data-stu-id="dbe78-106">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>

## <span data-ttu-id="dbe78-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dbe78-107">EXAMPLES</span></span>

### <span data-ttu-id="dbe78-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dbe78-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzVirtualRouter -Name $virtualRouterName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="dbe78-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dbe78-109">PARAMETERS</span></span>

### <span data-ttu-id="dbe78-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="dbe78-110">-AsJob</span></span>
<span data-ttu-id="dbe78-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="dbe78-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dbe78-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbe78-112">-DefaultProfile</span></span>
<span data-ttu-id="dbe78-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dbe78-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbe78-114">-Force</span><span class="sxs-lookup"><span data-stu-id="dbe78-114">-Force</span></span>
<span data-ttu-id="dbe78-115">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="dbe78-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="dbe78-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="dbe78-116">-HostedSubnet</span></span>
<span data-ttu-id="dbe78-117">Sanal yönlendiricinin barındırıldığı alt ağ.</span><span class="sxs-lookup"><span data-stu-id="dbe78-117">The subnet where the virtual router is hosted.</span></span>

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

### <span data-ttu-id="dbe78-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="dbe78-118">-Location</span></span>
<span data-ttu-id="dbe78-119">Konum.</span><span class="sxs-lookup"><span data-stu-id="dbe78-119">The location.</span></span>

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

### <span data-ttu-id="dbe78-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="dbe78-120">-Name</span></span>
<span data-ttu-id="dbe78-121">Sanal yönlendiricinin adı.</span><span class="sxs-lookup"><span data-stu-id="dbe78-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="dbe78-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbe78-122">-ResourceGroupName</span></span>
<span data-ttu-id="dbe78-123">Sanal yönlendiricinin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="dbe78-123">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="dbe78-124">Etiketli</span><span class="sxs-lookup"><span data-stu-id="dbe78-124">-Tag</span></span>
<span data-ttu-id="dbe78-125">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="dbe78-125">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="dbe78-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="dbe78-126">-Confirm</span></span>
<span data-ttu-id="dbe78-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dbe78-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbe78-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbe78-128">-WhatIf</span></span>
<span data-ttu-id="dbe78-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dbe78-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbe78-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dbe78-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbe78-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbe78-131">CommonParameters</span></span>
<span data-ttu-id="dbe78-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dbe78-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbe78-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dbe78-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbe78-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dbe78-134">INPUTS</span></span>

### <span data-ttu-id="dbe78-135">System. String</span><span class="sxs-lookup"><span data-stu-id="dbe78-135">System.String</span></span>

### <span data-ttu-id="dbe78-136">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dbe78-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dbe78-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dbe78-137">OUTPUTS</span></span>

### <span data-ttu-id="dbe78-138">Microsoft. Azure. Commands. Network. modeller. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="dbe78-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="dbe78-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dbe78-139">NOTES</span></span>

## <span data-ttu-id="dbe78-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dbe78-140">RELATED LINKS</span></span>
