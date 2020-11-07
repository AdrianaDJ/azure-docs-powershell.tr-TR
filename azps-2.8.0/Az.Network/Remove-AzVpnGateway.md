---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
ms.openlocfilehash: 17731d3f864f429fdad58bf767fb5cb25950387d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917991"
---
# <span data-ttu-id="9c07f-101">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9c07f-101">Remove-AzVpnGateway</span></span>

## <span data-ttu-id="9c07f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c07f-102">SYNOPSIS</span></span>
<span data-ttu-id="9c07f-103">Remove-AzVpnGateway cmdlet 'i bir Azure VPN ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9c07f-103">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="9c07f-104">Bu, Azure sanal WAN 'nın yazılım tanımlı bağlantısına özgü bir ağ geçididir.</span><span class="sxs-lookup"><span data-stu-id="9c07f-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="9c07f-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9c07f-105">SYNTAX</span></span>

### <span data-ttu-id="9c07f-106">ByVpnGatewayName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9c07f-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c07f-107">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="9c07f-107">ByVpnGatewayObject</span></span>
```
Remove-AzVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c07f-108">Byvpngatewayresourceıd</span><span class="sxs-lookup"><span data-stu-id="9c07f-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c07f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="9c07f-109">DESCRIPTION</span></span>
<span data-ttu-id="9c07f-110">Remove-AzVpnGateway cmdlet 'i bir Azure VPN ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9c07f-110">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="9c07f-111">Bu, Azure sanal WAN 'nın yazılım tanımlı bağlantısına özgü bir ağ geçididir.</span><span class="sxs-lookup"><span data-stu-id="9c07f-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="9c07f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9c07f-112">EXAMPLES</span></span>

### <span data-ttu-id="9c07f-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9c07f-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="9c07f-114">Bu örnekte, merkezinizdeki bir kaynak grubu, sanal WAN, sanal hub, ölçeklenebilir VPN ağ geçidi oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="9c07f-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="9c07f-115">Sanal ağ geçidini silerken bilgi istemini bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="9c07f-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="9c07f-116">Bu, VpnGateway 'i ve ona iliştirilmiş tüm VpnConnections 'ı silecek.</span><span class="sxs-lookup"><span data-stu-id="9c07f-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="9c07f-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9c07f-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzVpnGateway-Passthru
```

<span data-ttu-id="9c07f-118">Bu örnekte, merkezinizdeki bir kaynak grubu, sanal WAN, sanal hub, ölçeklenebilir VPN ağ geçidi oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="9c07f-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="9c07f-119">Bu silme işlemi, Get-AzVpnGateway komutu tarafından döndürülen VpnGateway nesnesini kullanan PowerShell yöneltme kullanılarak gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="9c07f-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzVpnGateway command.</span></span>
<span data-ttu-id="9c07f-120">Sanal ağ geçidini silerken bilgi istemini bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="9c07f-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="9c07f-121">Bu, VpnGateway 'i ve ona iliştirilmiş tüm VpnConnections 'ı silecek.</span><span class="sxs-lookup"><span data-stu-id="9c07f-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="9c07f-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9c07f-122">PARAMETERS</span></span>

### <span data-ttu-id="9c07f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c07f-123">-DefaultProfile</span></span>
<span data-ttu-id="9c07f-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9c07f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c07f-125">-Force</span><span class="sxs-lookup"><span data-stu-id="9c07f-125">-Force</span></span>
<span data-ttu-id="9c07f-126">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="9c07f-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9c07f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c07f-127">-InputObject</span></span>
<span data-ttu-id="9c07f-128">Silinecek vpnGateway nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9c07f-128">The vpnGateway object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c07f-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="9c07f-129">-Name</span></span>
<span data-ttu-id="9c07f-130">VpnGateway adı.</span><span class="sxs-lookup"><span data-stu-id="9c07f-130">The vpnGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c07f-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9c07f-131">-PassThru</span></span>
<span data-ttu-id="9c07f-132">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="9c07f-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9c07f-133">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="9c07f-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9c07f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c07f-134">-ResourceGroupName</span></span>
<span data-ttu-id="9c07f-135">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9c07f-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c07f-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9c07f-136">-ResourceId</span></span>
<span data-ttu-id="9c07f-137">Silinecek vpnGateway için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="9c07f-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: vpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c07f-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="9c07f-138">-Confirm</span></span>
<span data-ttu-id="9c07f-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9c07f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c07f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c07f-140">-WhatIf</span></span>
<span data-ttu-id="9c07f-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9c07f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c07f-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9c07f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c07f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c07f-143">CommonParameters</span></span>
<span data-ttu-id="9c07f-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9c07f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c07f-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c07f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c07f-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9c07f-146">INPUTS</span></span>

### <span data-ttu-id="9c07f-147">Microsoft. Azure. Commands. Network. model. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9c07f-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="9c07f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="9c07f-148">System.String</span></span>

## <span data-ttu-id="9c07f-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9c07f-149">OUTPUTS</span></span>

### <span data-ttu-id="9c07f-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c07f-150">System.Boolean</span></span>

## <span data-ttu-id="9c07f-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9c07f-151">NOTES</span></span>

## <span data-ttu-id="9c07f-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9c07f-152">RELATED LINKS</span></span>

[<span data-ttu-id="9c07f-153">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9c07f-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="9c07f-154">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9c07f-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="9c07f-155">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9c07f-155">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
