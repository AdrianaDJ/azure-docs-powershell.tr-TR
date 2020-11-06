---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnConnection.md
ms.openlocfilehash: da023b7c0b060e9e263b6b0677065746568524b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589422"
---
# <span data-ttu-id="06dc7-101">Remove-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="06dc7-101">Remove-AzureRmVpnConnection</span></span>

## <span data-ttu-id="06dc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="06dc7-103">VpnConnection öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="06dc7-103">Removes a VpnConnection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06dc7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06dc7-104">SYNTAX</span></span>

### <span data-ttu-id="06dc7-105">ByVpnConnectionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="06dc7-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06dc7-106">Byvpnconnectionresourceıd</span><span class="sxs-lookup"><span data-stu-id="06dc7-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzureRmVpnConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06dc7-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="06dc7-107">ByVpnConnectionObject</span></span>
```
Remove-AzureRmVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06dc7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="06dc7-108">DESCRIPTION</span></span>
<span data-ttu-id="06dc7-109">VpnConnection öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="06dc7-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="06dc7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06dc7-110">EXAMPLES</span></span>

### <span data-ttu-id="06dc7-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="06dc7-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Remove-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"
```

<span data-ttu-id="06dc7-112">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'de bir kaynak grubu, sanal WAN, sanal ağ, sanal hub ve bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="06dc7-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="06dc7-113">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="06dc7-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="06dc7-114">Ağ Geçidi oluşturulduktan sonra, New-AzureRmVpnConnection komutunu kullanarak VpnSite 'ye bağlanır.</span><span class="sxs-lookup"><span data-stu-id="06dc7-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="06dc7-115">Ardından bağlantı adını kullanarak bağlantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="06dc7-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="06dc7-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="06dc7-116">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" | Remove-AzureRmVpnConnection
```

<span data-ttu-id="06dc7-117">Örnek 1 ile aynıdır, ancak artık Get-AzureRmVpnConnection 'dan Piped nesnesini kullanarak bağlantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="06dc7-117">Same as example 1, but it now removes the connection using the piped object from Get-AzureRmVpnConnection.</span></span>

## <span data-ttu-id="06dc7-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06dc7-118">PARAMETERS</span></span>

### <span data-ttu-id="06dc7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06dc7-119">-DefaultProfile</span></span>
<span data-ttu-id="06dc7-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="06dc7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06dc7-121">-Force</span><span class="sxs-lookup"><span data-stu-id="06dc7-121">-Force</span></span>
<span data-ttu-id="06dc7-122">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="06dc7-122">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="06dc7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06dc7-123">-InputObject</span></span>
<span data-ttu-id="06dc7-124">Güncelleştirilecek VpnConenction nesnesi.</span><span class="sxs-lookup"><span data-stu-id="06dc7-124">The VpnConenction object to update.</span></span>

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

### <span data-ttu-id="06dc7-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="06dc7-125">-Name</span></span>
<span data-ttu-id="06dc7-126">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="06dc7-126">The resource name.</span></span>

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

### <span data-ttu-id="06dc7-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="06dc7-127">-ParentResourceName</span></span>
<span data-ttu-id="06dc7-128">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="06dc7-128">The parent resource name.</span></span>

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

### <span data-ttu-id="06dc7-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="06dc7-129">-PassThru</span></span>
<span data-ttu-id="06dc7-130">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="06dc7-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="06dc7-131">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="06dc7-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="06dc7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06dc7-132">-ResourceGroupName</span></span>
<span data-ttu-id="06dc7-133">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="06dc7-133">The resource group name.</span></span>

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

### <span data-ttu-id="06dc7-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="06dc7-134">-ResourceId</span></span>
<span data-ttu-id="06dc7-135">Silinecek VpnConenction nesnesinin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="06dc7-135">The resource id of the VpnConenction object to delete.</span></span>

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

### <span data-ttu-id="06dc7-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="06dc7-136">-Confirm</span></span>
<span data-ttu-id="06dc7-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="06dc7-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06dc7-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06dc7-138">-WhatIf</span></span>
<span data-ttu-id="06dc7-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="06dc7-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06dc7-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="06dc7-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06dc7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06dc7-141">CommonParameters</span></span>
<span data-ttu-id="06dc7-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06dc7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06dc7-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06dc7-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06dc7-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06dc7-144">INPUTS</span></span>

### <span data-ttu-id="06dc7-145">System. String</span><span class="sxs-lookup"><span data-stu-id="06dc7-145">System.String</span></span>

### <span data-ttu-id="06dc7-146">Microsoft. Azure. Commands. Network. model. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="06dc7-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="06dc7-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06dc7-147">OUTPUTS</span></span>

### <span data-ttu-id="06dc7-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="06dc7-148">System.Boolean</span></span>

## <span data-ttu-id="06dc7-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06dc7-149">NOTES</span></span>

## <span data-ttu-id="06dc7-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06dc7-150">RELATED LINKS</span></span>
