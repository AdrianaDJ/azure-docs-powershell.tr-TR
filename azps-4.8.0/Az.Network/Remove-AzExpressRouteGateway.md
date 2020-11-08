---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
ms.openlocfilehash: 73bf40456b1fa99093f2c84c11f71e945004a8fa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274090"
---
# <span data-ttu-id="bb68c-101">Remove-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="bb68c-101">Remove-AzExpressRouteGateway</span></span>

## <span data-ttu-id="bb68c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb68c-102">SYNOPSIS</span></span>
<span data-ttu-id="bb68c-103">Remove-AzExpressRouteGateway cmdlet 'i bir Azure ExpressRoute ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bb68c-103">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="bb68c-104">Bu, Azure sanal WAN 'nın yazılım tanımlı bağlantısına özgü bir ağ geçididir.</span><span class="sxs-lookup"><span data-stu-id="bb68c-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="bb68c-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb68c-105">SYNTAX</span></span>

### <span data-ttu-id="bb68c-106">ByExpressRouteGatewayName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bb68c-106">ByExpressRouteGatewayName (Default)</span></span>
```
Remove-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb68c-107">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="bb68c-107">ByExpressRouteGatewayObject</span></span>
```
Remove-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb68c-108">Byexpressroutegatewayresourceıd</span><span class="sxs-lookup"><span data-stu-id="bb68c-108">ByExpressRouteGatewayResourceId</span></span>
```
Remove-AzExpressRouteGateway -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb68c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb68c-109">DESCRIPTION</span></span>
<span data-ttu-id="bb68c-110">Remove-AzExpressRouteGateway cmdlet 'i bir Azure ExpressRoute ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bb68c-110">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="bb68c-111">Bu, Azure sanal WAN 'nın yazılım tanımlı bağlantısına özgü bir ağ geçididir.</span><span class="sxs-lookup"><span data-stu-id="bb68c-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="bb68c-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb68c-112">EXAMPLES</span></span>

### <span data-ttu-id="bb68c-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bb68c-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Remove-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -Passthru
```

<span data-ttu-id="bb68c-114">Bu örnekte, Merkezi ABD 'de bir kaynak grubu, sanal WAN, sanal hub, ölçeklenebilir ExpressRoute ağ geçidi oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="bb68c-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="bb68c-115">Sanal ağ geçidini silerken bilgi istemini bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="bb68c-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="bb68c-116">Bu, ExpressRouteGateway ve ona bağlı tüm ExpressRouteConnections 'ı silecek.</span><span class="sxs-lookup"><span data-stu-id="bb68c-116">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

### <span data-ttu-id="bb68c-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="bb68c-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" | Remove-AzExpressRouteGateway-Passthru
```

<span data-ttu-id="bb68c-118">Bu örnekte, Batı merkezi ABD 'de bir kaynak grubu, sanal WAN, sanal hub, ölçeklenebilir ExpressRoute ağ geçidi oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="bb68c-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in West Central US and then immediately deletes it.</span></span> <span data-ttu-id="bb68c-119">Bu silme işlemi, Get-AzExpressRouteGateway komutu tarafından döndürülen ExpressRouteGateway nesnesini kullanan PowerShell şeridi kullanılarak gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="bb68c-119">This deletion happens using powershell piping, which uses the ExpressRouteGateway object returned by the Get-AzExpressRouteGateway command.</span></span>
<span data-ttu-id="bb68c-120">Sanal ağ geçidini silerken bilgi istemini bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="bb68c-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="bb68c-121">Bu, ExpressRouteGateway ve ona bağlı tüm ExpressRouteConnections 'ı silecek.</span><span class="sxs-lookup"><span data-stu-id="bb68c-121">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

## <span data-ttu-id="bb68c-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb68c-122">PARAMETERS</span></span>

### <span data-ttu-id="bb68c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb68c-123">-DefaultProfile</span></span>
<span data-ttu-id="bb68c-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bb68c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb68c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="bb68c-125">-Force</span></span>
<span data-ttu-id="bb68c-126">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="bb68c-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bb68c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb68c-127">-InputObject</span></span>
<span data-ttu-id="bb68c-128">Silinecek ExpressRouteGateway nesnesi.</span><span class="sxs-lookup"><span data-stu-id="bb68c-128">The ExpressRouteGateway object to be deleted.</span></span>

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

### <span data-ttu-id="bb68c-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="bb68c-129">-Name</span></span>
<span data-ttu-id="bb68c-130">ExpressRouteGateway adı.</span><span class="sxs-lookup"><span data-stu-id="bb68c-130">The ExpressRouteGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb68c-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bb68c-131">-PassThru</span></span>
<span data-ttu-id="bb68c-132">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="bb68c-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bb68c-133">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="bb68c-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bb68c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb68c-134">-ResourceGroupName</span></span>
<span data-ttu-id="bb68c-135">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="bb68c-135">The resource group name.</span></span>

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

### <span data-ttu-id="bb68c-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bb68c-136">-ResourceId</span></span>
<span data-ttu-id="bb68c-137">ExpressRouteGateway 'in silineceği Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bb68c-137">The Azure resource ID for the ExpressRouteGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: expressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb68c-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="bb68c-138">-Confirm</span></span>
<span data-ttu-id="bb68c-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bb68c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb68c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb68c-140">-WhatIf</span></span>
<span data-ttu-id="bb68c-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bb68c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb68c-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bb68c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb68c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb68c-143">CommonParameters</span></span>
<span data-ttu-id="bb68c-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb68c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb68c-145">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb68c-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb68c-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb68c-146">INPUTS</span></span>

### <span data-ttu-id="bb68c-147">Microsoft. Azure. Commands. Network. model. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="bb68c-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="bb68c-148">System. String</span><span class="sxs-lookup"><span data-stu-id="bb68c-148">System.String</span></span>

## <span data-ttu-id="bb68c-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb68c-149">OUTPUTS</span></span>

### <span data-ttu-id="bb68c-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bb68c-150">System.Boolean</span></span>

## <span data-ttu-id="bb68c-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb68c-151">NOTES</span></span>

## <span data-ttu-id="bb68c-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb68c-152">RELATED LINKS</span></span>
