---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
ms.openlocfilehash: 825090358ea94223d483fe418d06896f1f741045
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103949"
---
# <span data-ttu-id="56bee-101">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="56bee-101">Remove-AzVpnConnection</span></span>

## <span data-ttu-id="56bee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56bee-102">SYNOPSIS</span></span>
<span data-ttu-id="56bee-103">VpnConnection öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="56bee-103">Removes a VpnConnection.</span></span>

## <span data-ttu-id="56bee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="56bee-104">SYNTAX</span></span>

### <span data-ttu-id="56bee-105">ByVpnConnectionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="56bee-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56bee-106">Byvpnconnectionresourceıd</span><span class="sxs-lookup"><span data-stu-id="56bee-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzVpnConnection -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56bee-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="56bee-107">ByVpnConnectionObject</span></span>
```
Remove-AzVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56bee-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="56bee-108">DESCRIPTION</span></span>
<span data-ttu-id="56bee-109">VpnConnection öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="56bee-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="56bee-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="56bee-110">EXAMPLES</span></span>

### <span data-ttu-id="56bee-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="56bee-111">Example 1</span></span>
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

<span data-ttu-id="56bee-112">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'de bir kaynak grubu, sanal WAN, sanal ağ, sanal hub ve bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="56bee-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="56bee-113">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="56bee-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="56bee-114">Ağ Geçidi oluşturulduktan sonra, New-AzVpnConnection komutunu kullanarak VpnSite 'ye bağlanır.</span><span class="sxs-lookup"><span data-stu-id="56bee-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="56bee-115">Ardından bağlantı adını kullanarak bağlantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="56bee-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="56bee-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="56bee-116">Example 2</span></span>

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

<span data-ttu-id="56bee-117">Örnek 1 ile aynıdır, ancak şimdi Get-Azvpnbağlantısından Piped nesneyi kullanarak bağlantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="56bee-117">Same as example 1, but it now removes the connection using the piped object from Get-AzVpnConnection.</span></span>

## <span data-ttu-id="56bee-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="56bee-118">PARAMETERS</span></span>

### <span data-ttu-id="56bee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56bee-119">-DefaultProfile</span></span>
<span data-ttu-id="56bee-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="56bee-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56bee-121">-Force</span><span class="sxs-lookup"><span data-stu-id="56bee-121">-Force</span></span>
<span data-ttu-id="56bee-122">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="56bee-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="56bee-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56bee-123">-InputObject</span></span>
<span data-ttu-id="56bee-124">Güncelleştirilecek VpnConnection nesnesi.</span><span class="sxs-lookup"><span data-stu-id="56bee-124">The VpnConnection object to update.</span></span>

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

### <span data-ttu-id="56bee-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="56bee-125">-Name</span></span>
<span data-ttu-id="56bee-126">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="56bee-126">The resource name.</span></span>

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

### <span data-ttu-id="56bee-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="56bee-127">-ParentResourceName</span></span>
<span data-ttu-id="56bee-128">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="56bee-128">The parent resource name.</span></span>

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

### <span data-ttu-id="56bee-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="56bee-129">-PassThru</span></span>
<span data-ttu-id="56bee-130">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="56bee-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="56bee-131">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="56bee-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="56bee-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56bee-132">-ResourceGroupName</span></span>
<span data-ttu-id="56bee-133">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="56bee-133">The resource group name.</span></span>

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

### <span data-ttu-id="56bee-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="56bee-134">-ResourceId</span></span>
<span data-ttu-id="56bee-135">Silinecek VpnConnection nesnesinin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="56bee-135">The resource id of the VpnConnection object to delete.</span></span>

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

### <span data-ttu-id="56bee-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="56bee-136">-Confirm</span></span>
<span data-ttu-id="56bee-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="56bee-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56bee-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56bee-138">-WhatIf</span></span>
<span data-ttu-id="56bee-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="56bee-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56bee-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="56bee-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56bee-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56bee-141">CommonParameters</span></span>
<span data-ttu-id="56bee-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="56bee-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56bee-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="56bee-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56bee-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="56bee-144">INPUTS</span></span>

### <span data-ttu-id="56bee-145">System. String</span><span class="sxs-lookup"><span data-stu-id="56bee-145">System.String</span></span>

### <span data-ttu-id="56bee-146">Microsoft. Azure. Commands. Network. model. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="56bee-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="56bee-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="56bee-147">OUTPUTS</span></span>

### <span data-ttu-id="56bee-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="56bee-148">System.Boolean</span></span>

## <span data-ttu-id="56bee-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="56bee-149">NOTES</span></span>

## <span data-ttu-id="56bee-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="56bee-150">RELATED LINKS</span></span>

[<span data-ttu-id="56bee-151">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="56bee-151">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="56bee-152">Yeni-Azvpnbağlantısı</span><span class="sxs-lookup"><span data-stu-id="56bee-152">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="56bee-153">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="56bee-153">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
