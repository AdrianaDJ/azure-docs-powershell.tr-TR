---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
ms.openlocfilehash: 0215a05db7e18dad9aeb26476d7076bdc556b021
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760083"
---
# <span data-ttu-id="a7609-101">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="a7609-101">Remove-AzVpnSite</span></span>

## <span data-ttu-id="a7609-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7609-102">SYNOPSIS</span></span>
<span data-ttu-id="a7609-103">Bir Azure VpnSite kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a7609-103">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="a7609-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7609-104">SYNTAX</span></span>

### <span data-ttu-id="a7609-105">ByVpnSiteName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a7609-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7609-106">Byvpnsitenesnesi</span><span class="sxs-lookup"><span data-stu-id="a7609-106">ByVpnSiteObject</span></span>
```
Remove-AzVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7609-107">Byvpnsiteresourceıd</span><span class="sxs-lookup"><span data-stu-id="a7609-107">ByVpnSiteResourceId</span></span>
```
Remove-AzVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7609-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7609-108">DESCRIPTION</span></span>
<span data-ttu-id="a7609-109">Bir Azure VpnSite kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a7609-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="a7609-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7609-110">EXAMPLES</span></span>

### <span data-ttu-id="a7609-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a7609-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="a7609-112">Yukarıdaki, Azure 'daki "testRG" kaynak grubundaki Batı</span><span class="sxs-lookup"><span data-stu-id="a7609-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="a7609-113">Ardından bir müşteri dalının temsil etmesi ve sanal WAN 'a bağlandığı bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a7609-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="a7609-114">Site oluşturulduktan sonra Remove-AzVpnSite komutu kullanılarak hemen kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="a7609-114">Once the site is created, it is immediately removed using the Remove-AzVpnSite command.</span></span>

### <span data-ttu-id="a7609-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a7609-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzVpnSite
```

<span data-ttu-id="a7609-116">Örnek 1 ile aynıdır, ancak buradan kaldırma işlemi Get-Azvpnsitesinden Piped çıkışı kullanılarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="a7609-116">Same as example 1 but here the removal happens using the piped output from Get-AzVpnSite.</span></span>

## <span data-ttu-id="a7609-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7609-117">PARAMETERS</span></span>

### <span data-ttu-id="a7609-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7609-118">-DefaultProfile</span></span>
<span data-ttu-id="a7609-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a7609-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7609-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a7609-120">-Force</span></span>
<span data-ttu-id="a7609-121">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="a7609-121">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7609-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7609-122">-InputObject</span></span>
<span data-ttu-id="a7609-123">Silinecek vpnSite nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a7609-123">The vpnSite object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnSiteObject
Aliases: VpnSite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7609-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="a7609-124">-Name</span></span>
<span data-ttu-id="a7609-125">VpnSite adı.</span><span class="sxs-lookup"><span data-stu-id="a7609-125">The vpnSite name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteName
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7609-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a7609-126">-PassThru</span></span>
<span data-ttu-id="a7609-127">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="a7609-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="a7609-128">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a7609-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7609-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7609-129">-ResourceGroupName</span></span>
<span data-ttu-id="a7609-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a7609-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7609-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a7609-131">-ResourceId</span></span>
<span data-ttu-id="a7609-132">Silinecek vpnSite için Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a7609-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteResourceId
Aliases: VpnSiteId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7609-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="a7609-133">-Confirm</span></span>
<span data-ttu-id="a7609-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a7609-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7609-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7609-135">-WhatIf</span></span>
<span data-ttu-id="a7609-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a7609-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7609-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a7609-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7609-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7609-138">CommonParameters</span></span>
<span data-ttu-id="a7609-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7609-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7609-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7609-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7609-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7609-141">INPUTS</span></span>

### <span data-ttu-id="a7609-142">Microsoft. Azure. Commands. Network. modeller. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="a7609-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="a7609-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a7609-143">System.String</span></span>

## <span data-ttu-id="a7609-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7609-144">OUTPUTS</span></span>

### <span data-ttu-id="a7609-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a7609-145">System.Boolean</span></span>

## <span data-ttu-id="a7609-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7609-146">NOTES</span></span>

## <span data-ttu-id="a7609-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7609-147">RELATED LINKS</span></span>

[<span data-ttu-id="a7609-148">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="a7609-148">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="a7609-149">Yeni-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="a7609-149">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="a7609-150">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="a7609-150">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)