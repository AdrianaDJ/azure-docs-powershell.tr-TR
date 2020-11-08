---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
ms.openlocfilehash: 7cc9dbe5c4727c283ead66e88b6c52c9c2fcd00e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096810"
---
# <span data-ttu-id="cc46f-101">Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="cc46f-101">Set-AzExpressRouteGateway</span></span>

## <span data-ttu-id="cc46f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc46f-102">SYNOPSIS</span></span>
<span data-ttu-id="cc46f-103">Ölçeklenebilir ExpressRoute ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="cc46f-103">Updates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="cc46f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cc46f-104">SYNTAX</span></span>

### <span data-ttu-id="cc46f-105">ByExpressRouteGatewayName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cc46f-105">ByExpressRouteGatewayName (Default)</span></span>
```
Set-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 -MaxScaleUnits <UInt32> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc46f-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="cc46f-106">ByExpressRouteGatewayObject</span></span>
```
Set-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> -MinScaleUnits <UInt32> -MaxScaleUnits <UInt32>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc46f-107">Byexpressroutegatewayresourceıd</span><span class="sxs-lookup"><span data-stu-id="cc46f-107">ByExpressRouteGatewayResourceId</span></span>
```
Set-AzExpressRouteGateway -ResourceId <String> -MinScaleUnits <UInt32> -MaxScaleUnits <UInt32>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cc46f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cc46f-108">DESCRIPTION</span></span>

<span data-ttu-id="cc46f-109">ExpressRouteGateway Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="cc46f-109">Set-AzExpressRouteGateway updates the scale units for the ExpressRouteGateway</span></span>

## <span data-ttu-id="cc46f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cc46f-110">EXAMPLES</span></span>

### <span data-ttu-id="cc46f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cc46f-111">Example 1</span></span>

```powershell
PS C:\>Set-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan =Set-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub =Set-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\>New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\>Set-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -MinScaleUnits 3

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 3
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="cc46f-112">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda bir kaynak grubu, sanal WAN, sanal ağ, Batı ABD 'deki sanal hub 'ı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cc46f-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="cc46f-113">Daha sonra 3 ölçek birimi ile değiştirilecek şekilde sanal hub 'da bir ExpressRoute ağ geçidi oluşturulur</span><span class="sxs-lookup"><span data-stu-id="cc46f-113">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units which will then be modified to 3 scale units</span></span>

## <span data-ttu-id="cc46f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cc46f-114">PARAMETERS</span></span>

### <span data-ttu-id="cc46f-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="cc46f-115">-AsJob</span></span>
<span data-ttu-id="cc46f-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="cc46f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc46f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc46f-117">-DefaultProfile</span></span>
<span data-ttu-id="cc46f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cc46f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc46f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc46f-119">-InputObject</span></span>
<span data-ttu-id="cc46f-120">Güncelleştirilmesi gereken ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="cc46f-120">The ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc46f-121">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="cc46f-121">-MaxScaleUnits</span></span>
<span data-ttu-id="cc46f-122">Bu ExpressRouteGateway için en yüksek ölçek birimi sayısı.</span><span class="sxs-lookup"><span data-stu-id="cc46f-122">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="cc46f-123">Geçerli Aralık > 2</span><span class="sxs-lookup"><span data-stu-id="cc46f-123">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc46f-124">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="cc46f-124">-MinScaleUnits</span></span>
<span data-ttu-id="cc46f-125">Bu ExpressRouteGateway için en az ölçek birimi sayısı.</span><span class="sxs-lookup"><span data-stu-id="cc46f-125">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="cc46f-126">Geçerli Aralık > 2</span><span class="sxs-lookup"><span data-stu-id="cc46f-126">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc46f-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="cc46f-127">-Name</span></span>
<span data-ttu-id="cc46f-128">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="cc46f-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc46f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc46f-129">-ResourceGroupName</span></span>
<span data-ttu-id="cc46f-130">Güncelleştirilecek ExpressRouteGateway 'in kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="cc46f-130">The resource group name of the ExpressRouteGateway to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc46f-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cc46f-131">-ResourceId</span></span>
<span data-ttu-id="cc46f-132">Güncelleştirilmesi gereken ExpressRouteGateway kimliği.</span><span class="sxs-lookup"><span data-stu-id="cc46f-132">The Id of the ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc46f-133">Etiketli</span><span class="sxs-lookup"><span data-stu-id="cc46f-133">-Tag</span></span>
<span data-ttu-id="cc46f-134">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="cc46f-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc46f-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="cc46f-135">-Confirm</span></span>
<span data-ttu-id="cc46f-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cc46f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc46f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc46f-137">-WhatIf</span></span>
<span data-ttu-id="cc46f-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cc46f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc46f-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cc46f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc46f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc46f-140">CommonParameters</span></span>
<span data-ttu-id="cc46f-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cc46f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc46f-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc46f-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc46f-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cc46f-143">INPUTS</span></span>

### <span data-ttu-id="cc46f-144">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="cc46f-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="cc46f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="cc46f-145">System.String</span></span>

## <span data-ttu-id="cc46f-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cc46f-146">OUTPUTS</span></span>

### <span data-ttu-id="cc46f-147">Microsoft. Azure. Commands. Network. model. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="cc46f-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="cc46f-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cc46f-148">NOTES</span></span>

## <span data-ttu-id="cc46f-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cc46f-149">RELATED LINKS</span></span>