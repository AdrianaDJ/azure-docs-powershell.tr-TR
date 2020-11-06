---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnGateway.md
ms.openlocfilehash: 34e143b3ca6114fd90d52a5ad6ee8c022fda5688
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593945"
---
# <span data-ttu-id="1d838-101">Remove-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="1d838-101">Remove-AzureRmVpnGateway</span></span>

## <span data-ttu-id="1d838-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d838-102">SYNOPSIS</span></span>
<span data-ttu-id="1d838-103">Remove-AzureRmVpnGateway cmdlet 'i bir Azure VPN ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1d838-103">The Remove-AzureRmVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="1d838-104">Bu, Azure sanal WAN 'nın yazılım tanımlı bağlantısına özgü bir ağ geçididir.</span><span class="sxs-lookup"><span data-stu-id="1d838-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d838-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1d838-105">SYNTAX</span></span>

### <span data-ttu-id="1d838-106">ByVpnGatewayName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1d838-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d838-107">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="1d838-107">ByVpnGatewayObject</span></span>
```
Remove-AzureRmVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d838-108">Byvpngatewayresourceıd</span><span class="sxs-lookup"><span data-stu-id="1d838-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzureRmVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d838-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d838-109">DESCRIPTION</span></span>
<span data-ttu-id="1d838-110">Remove-AzureRmVpnGateway cmdlet 'i bir Azure VPN ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1d838-110">The Remove-AzureRmVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="1d838-111">Bu, Azure sanal WAN 'nın yazılım tanımlı bağlantısına özgü bir ağ geçididir.</span><span class="sxs-lookup"><span data-stu-id="1d838-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="1d838-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1d838-112">EXAMPLES</span></span>

### <span data-ttu-id="1d838-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1d838-113">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="1d838-114">Bu örnekte, merkezinizdeki bir kaynak grubu, sanal WAN, sanal hub, ölçeklenebilir VPN ağ geçidi oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="1d838-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="1d838-115">Sanal ağ geçidini silerken bilgi istemini bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="1d838-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="1d838-116">Bu, VpnGateway 'i ve ona iliştirilmiş tüm VpnConnections 'ı silecek.</span><span class="sxs-lookup"><span data-stu-id="1d838-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="1d838-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1d838-117">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzureRmVpnGateway-Passthru
```

<span data-ttu-id="1d838-118">Bu örnekte, merkezinizdeki bir kaynak grubu, sanal WAN, sanal hub, ölçeklenebilir VPN ağ geçidi oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="1d838-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="1d838-119">Bu silme işlemi, Get-AzureRmVpnGateway komutu tarafından döndürülen VpnGateway nesnesini kullanan PowerShell yöneltme kullanılarak gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="1d838-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzureRmVpnGateway command.</span></span>
<span data-ttu-id="1d838-120">Sanal ağ geçidini silerken bilgi istemini bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="1d838-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="1d838-121">Bu, VpnGateway 'i ve ona iliştirilmiş tüm VpnConnections 'ı silecek.</span><span class="sxs-lookup"><span data-stu-id="1d838-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="1d838-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1d838-122">PARAMETERS</span></span>

### <span data-ttu-id="1d838-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d838-123">-DefaultProfile</span></span>
<span data-ttu-id="1d838-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1d838-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d838-125">-Force</span><span class="sxs-lookup"><span data-stu-id="1d838-125">-Force</span></span>
<span data-ttu-id="1d838-126">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="1d838-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1d838-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d838-127">-InputObject</span></span>
<span data-ttu-id="1d838-128">Silinecek vpnGateway nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1d838-128">The vpnGateway object to be deleted.</span></span>

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

### <span data-ttu-id="1d838-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="1d838-129">-Name</span></span>
<span data-ttu-id="1d838-130">VpnGateway adı.</span><span class="sxs-lookup"><span data-stu-id="1d838-130">The vpnGateway name.</span></span>

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

### <span data-ttu-id="1d838-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1d838-131">-PassThru</span></span>
<span data-ttu-id="1d838-132">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="1d838-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1d838-133">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="1d838-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1d838-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d838-134">-ResourceGroupName</span></span>
<span data-ttu-id="1d838-135">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1d838-135">The resource group name.</span></span>

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

### <span data-ttu-id="1d838-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1d838-136">-ResourceId</span></span>
<span data-ttu-id="1d838-137">Silinecek vpnGateway için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="1d838-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

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

### <span data-ttu-id="1d838-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="1d838-138">-Confirm</span></span>
<span data-ttu-id="1d838-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1d838-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d838-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d838-140">-WhatIf</span></span>
<span data-ttu-id="1d838-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d838-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d838-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1d838-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d838-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d838-143">CommonParameters</span></span>
<span data-ttu-id="1d838-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1d838-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d838-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d838-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d838-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1d838-146">INPUTS</span></span>

### <span data-ttu-id="1d838-147">Microsoft. Azure. Commands. Network. model. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="1d838-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="1d838-148">System. String</span><span class="sxs-lookup"><span data-stu-id="1d838-148">System.String</span></span>

## <span data-ttu-id="1d838-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1d838-149">OUTPUTS</span></span>

### <span data-ttu-id="1d838-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1d838-150">System.Boolean</span></span>

## <span data-ttu-id="1d838-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1d838-151">NOTES</span></span>

## <span data-ttu-id="1d838-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1d838-152">RELATED LINKS</span></span>
