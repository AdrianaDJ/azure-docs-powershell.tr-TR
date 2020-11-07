---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
ms.openlocfilehash: 87591f5ecf928fb2dc9444fd826ce03f484e665c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760087"
---
# <span data-ttu-id="a43aa-101">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a43aa-101">Remove-AzVpnConnection</span></span>

## <span data-ttu-id="a43aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a43aa-102">SYNOPSIS</span></span>
<span data-ttu-id="a43aa-103">VpnConnection öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a43aa-103">Removes a VpnConnection.</span></span>

## <span data-ttu-id="a43aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a43aa-104">SYNTAX</span></span>

### <span data-ttu-id="a43aa-105">ByVpnConnectionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a43aa-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a43aa-106">Byvpnconnectionresourceıd</span><span class="sxs-lookup"><span data-stu-id="a43aa-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzVpnConnection -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a43aa-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="a43aa-107">ByVpnConnectionObject</span></span>
```
Remove-AzVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a43aa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a43aa-108">DESCRIPTION</span></span>
<span data-ttu-id="a43aa-109">VpnConnection öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a43aa-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="a43aa-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a43aa-110">EXAMPLES</span></span>

### <span data-ttu-id="a43aa-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a43aa-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Remove-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"
```

<span data-ttu-id="a43aa-112">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'de bir kaynak grubu, sanal WAN, sanal ağ, sanal hub ve bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a43aa-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="a43aa-113">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a43aa-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="a43aa-114">Ağ Geçidi oluşturulduktan sonra, New-AzVpnConnection komutunu kullanarak VpnSite 'ye bağlanır.</span><span class="sxs-lookup"><span data-stu-id="a43aa-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="a43aa-115">Ardından bağlantı adını kullanarak bağlantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a43aa-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="a43aa-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a43aa-116">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" | Remove-AzVpnConnection
```

<span data-ttu-id="a43aa-117">Örnek 1 ile aynıdır, ancak şimdi Get-Azvpnbağlantısından Piped nesneyi kullanarak bağlantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a43aa-117">Same as example 1, but it now removes the connection using the piped object from Get-AzVpnConnection.</span></span>

## <span data-ttu-id="a43aa-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a43aa-118">PARAMETERS</span></span>

### <span data-ttu-id="a43aa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a43aa-119">-DefaultProfile</span></span>
<span data-ttu-id="a43aa-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a43aa-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a43aa-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a43aa-121">-Force</span></span>
<span data-ttu-id="a43aa-122">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="a43aa-122">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="a43aa-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a43aa-123">-InputObject</span></span>
<span data-ttu-id="a43aa-124">Güncelleştirilecek VpnConenction nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a43aa-124">The VpnConenction object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a43aa-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="a43aa-125">-Name</span></span>
<span data-ttu-id="a43aa-126">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="a43aa-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a43aa-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="a43aa-127">-ParentResourceName</span></span>
<span data-ttu-id="a43aa-128">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="a43aa-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a43aa-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a43aa-129">-PassThru</span></span>
<span data-ttu-id="a43aa-130">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="a43aa-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a43aa-131">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a43aa-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a43aa-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a43aa-132">-ResourceGroupName</span></span>
<span data-ttu-id="a43aa-133">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a43aa-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a43aa-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a43aa-134">-ResourceId</span></span>
<span data-ttu-id="a43aa-135">Silinecek VpnConenction nesnesinin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="a43aa-135">The resource id of the VpnConenction object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a43aa-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="a43aa-136">-Confirm</span></span>
<span data-ttu-id="a43aa-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a43aa-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a43aa-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a43aa-138">-WhatIf</span></span>
<span data-ttu-id="a43aa-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a43aa-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a43aa-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a43aa-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a43aa-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a43aa-141">CommonParameters</span></span>
<span data-ttu-id="a43aa-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a43aa-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a43aa-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a43aa-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a43aa-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a43aa-144">INPUTS</span></span>

### <span data-ttu-id="a43aa-145">System. String</span><span class="sxs-lookup"><span data-stu-id="a43aa-145">System.String</span></span>

### <span data-ttu-id="a43aa-146">Microsoft. Azure. Commands. Network. model. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a43aa-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="a43aa-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a43aa-147">OUTPUTS</span></span>

### <span data-ttu-id="a43aa-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a43aa-148">System.Boolean</span></span>

## <span data-ttu-id="a43aa-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a43aa-149">NOTES</span></span>

## <span data-ttu-id="a43aa-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a43aa-150">RELATED LINKS</span></span>

[<span data-ttu-id="a43aa-151">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a43aa-151">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="a43aa-152">Yeni-Azvpnbağlantısı</span><span class="sxs-lookup"><span data-stu-id="a43aa-152">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="a43aa-153">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a43aa-153">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
