---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 75315de4e6ca2cf799f6cefb1d3b9c143631f5a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098700"
---
# <span data-ttu-id="ee040-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="ee040-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="ee040-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee040-102">SYNOPSIS</span></span>
<span data-ttu-id="ee040-103">Bir Azure VirtualRouter oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ee040-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="ee040-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee040-104">SYNTAX</span></span>

### <span data-ttu-id="ee040-105">HostedGatewayParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ee040-105">HostedGatewayParameterSet (Default)</span></span>
```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedGateway <PSVirtualNetworkGateway>
 -Location <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee040-106">HostedGatewayIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee040-106">HostedGatewayIdParameterSet</span></span>
```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedGatewayId <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ee040-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee040-107">DESCRIPTION</span></span>
<span data-ttu-id="ee040-108">**New-AzVirtualRouter** cmdlet 'ı bir Azure virtualrouter oluşturur</span><span class="sxs-lookup"><span data-stu-id="ee040-108">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>


## <span data-ttu-id="ee040-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee040-109">EXAMPLES</span></span>

### <span data-ttu-id="ee040-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ee040-110">Example 1</span></span>
```powershell
$gatewayId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualNetworkGateways/erGateway'
New-AzVirtualRouter -RouterName virtualRouter -ResourceGroupName virtualRouterRG -Location 'West US'  -HostedGatewayId $gatewayId
```

### <span data-ttu-id="ee040-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ee040-111">Example 2</span></span>
```powershell
$gateway = Get-AzVirtualNetworkGateway -Name erGateway -ResourceGroupName virtualRouterRG
New-AzVirtualRouter -RouterName virtualRouter -ResourceGroupName virtualRouterRG -Location 'West US'  -HostedGateway $gateway
```

## <span data-ttu-id="ee040-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee040-112">PARAMETERS</span></span>

### <span data-ttu-id="ee040-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="ee040-113">-AsJob</span></span>
<span data-ttu-id="ee040-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ee040-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee040-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee040-115">-DefaultProfile</span></span>
<span data-ttu-id="ee040-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ee040-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee040-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ee040-117">-Force</span></span>
<span data-ttu-id="ee040-118">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="ee040-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee040-119">-HostedGateway</span><span class="sxs-lookup"><span data-stu-id="ee040-119">-HostedGateway</span></span>
<span data-ttu-id="ee040-120">Sanal yönlendiricinin barındırılması gerektiği ağ geçidi.</span><span class="sxs-lookup"><span data-stu-id="ee040-120">The gateway where Virtual Router needs to be hosted.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: HostedGatewayParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee040-121">-Hostedgatewayıd</span><span class="sxs-lookup"><span data-stu-id="ee040-121">-HostedGatewayId</span></span>
<span data-ttu-id="ee040-122">Sanal yönlendiricinin barındırılması gerektiği ağ geçidi kimliği.</span><span class="sxs-lookup"><span data-stu-id="ee040-122">The id of gateway where Virtual Router needs to be hosted.</span></span>

```yaml
Type: String
Parameter Sets: HostedGatewayIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee040-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="ee040-123">-Location</span></span>
<span data-ttu-id="ee040-124">Konum.</span><span class="sxs-lookup"><span data-stu-id="ee040-124">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee040-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="ee040-125">-Name</span></span>
<span data-ttu-id="ee040-126">Sanal yönlendiricinin adı.</span><span class="sxs-lookup"><span data-stu-id="ee040-126">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee040-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee040-127">-ResourceGroupName</span></span>
<span data-ttu-id="ee040-128">Sanal yönlendiricinin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ee040-128">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee040-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ee040-129">-Tag</span></span>
<span data-ttu-id="ee040-130">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="ee040-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee040-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="ee040-131">-Confirm</span></span>
<span data-ttu-id="ee040-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ee040-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee040-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee040-133">-WhatIf</span></span>
<span data-ttu-id="ee040-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ee040-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee040-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ee040-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee040-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee040-136">CommonParameters</span></span>
<span data-ttu-id="ee040-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee040-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ee040-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee040-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee040-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee040-139">INPUTS</span></span>

### <span data-ttu-id="ee040-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ee040-140">System.String</span></span>

### <span data-ttu-id="ee040-141">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ee040-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="ee040-142">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ee040-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ee040-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee040-143">OUTPUTS</span></span>

### <span data-ttu-id="ee040-144">Microsoft. Azure. Commands. Network. modeller. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="ee040-144">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="ee040-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee040-145">NOTES</span></span>

## <span data-ttu-id="ee040-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee040-146">RELATED LINKS</span></span>
