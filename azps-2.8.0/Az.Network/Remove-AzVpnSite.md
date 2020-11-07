---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
ms.openlocfilehash: 950e2d3e36695646bba16c098fc3abbd63cae113
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932235"
---
# <span data-ttu-id="0667a-101">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="0667a-101">Remove-AzVpnSite</span></span>

## <span data-ttu-id="0667a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0667a-102">SYNOPSIS</span></span>
<span data-ttu-id="0667a-103">Bir Azure VpnSite kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0667a-103">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="0667a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0667a-104">SYNTAX</span></span>

### <span data-ttu-id="0667a-105">ByVpnSiteName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0667a-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0667a-106">Byvpnsitenesnesi</span><span class="sxs-lookup"><span data-stu-id="0667a-106">ByVpnSiteObject</span></span>
```
Remove-AzVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0667a-107">Byvpnsiteresourceıd</span><span class="sxs-lookup"><span data-stu-id="0667a-107">ByVpnSiteResourceId</span></span>
```
Remove-AzVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0667a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0667a-108">DESCRIPTION</span></span>
<span data-ttu-id="0667a-109">Bir Azure VpnSite kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0667a-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="0667a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0667a-110">EXAMPLES</span></span>

### <span data-ttu-id="0667a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0667a-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="0667a-112">Yukarıdaki, Azure 'daki "testRG" kaynak grubundaki Batı</span><span class="sxs-lookup"><span data-stu-id="0667a-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="0667a-113">Ardından bir müşteri dalının temsil etmesi ve sanal WAN 'a bağlandığı bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0667a-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="0667a-114">Site oluşturulduktan sonra Remove-AzVpnSite komutu kullanılarak hemen kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="0667a-114">Once the site is created, it is immediately removed using the Remove-AzVpnSite command.</span></span>

### <span data-ttu-id="0667a-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0667a-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzVpnSite
```

<span data-ttu-id="0667a-116">Örnek 1 ile aynıdır, ancak buradan kaldırma işlemi Get-Azvpnsitesinden Piped çıkışı kullanılarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="0667a-116">Same as example 1 but here the removal happens using the piped output from Get-AzVpnSite.</span></span>

## <span data-ttu-id="0667a-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0667a-117">PARAMETERS</span></span>

### <span data-ttu-id="0667a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0667a-118">-DefaultProfile</span></span>
<span data-ttu-id="0667a-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0667a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0667a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0667a-120">-Force</span></span>
<span data-ttu-id="0667a-121">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="0667a-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0667a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0667a-122">-InputObject</span></span>
<span data-ttu-id="0667a-123">Silinecek vpnSite nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0667a-123">The vpnSite object to be deleted.</span></span>

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

### <span data-ttu-id="0667a-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="0667a-124">-Name</span></span>
<span data-ttu-id="0667a-125">VpnSite adı.</span><span class="sxs-lookup"><span data-stu-id="0667a-125">The vpnSite name.</span></span>

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

### <span data-ttu-id="0667a-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0667a-126">-PassThru</span></span>
<span data-ttu-id="0667a-127">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="0667a-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="0667a-128">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="0667a-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0667a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0667a-129">-ResourceGroupName</span></span>
<span data-ttu-id="0667a-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0667a-130">The resource group name.</span></span>

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

### <span data-ttu-id="0667a-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0667a-131">-ResourceId</span></span>
<span data-ttu-id="0667a-132">Silinecek vpnSite için Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0667a-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

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

### <span data-ttu-id="0667a-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="0667a-133">-Confirm</span></span>
<span data-ttu-id="0667a-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0667a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0667a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0667a-135">-WhatIf</span></span>
<span data-ttu-id="0667a-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0667a-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0667a-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0667a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0667a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0667a-138">CommonParameters</span></span>
<span data-ttu-id="0667a-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0667a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0667a-140">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0667a-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0667a-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0667a-141">INPUTS</span></span>

### <span data-ttu-id="0667a-142">Microsoft. Azure. Commands. Network. modeller. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="0667a-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="0667a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="0667a-143">System.String</span></span>

## <span data-ttu-id="0667a-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0667a-144">OUTPUTS</span></span>

### <span data-ttu-id="0667a-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0667a-145">System.Boolean</span></span>

## <span data-ttu-id="0667a-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0667a-146">NOTES</span></span>

## <span data-ttu-id="0667a-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0667a-147">RELATED LINKS</span></span>

[<span data-ttu-id="0667a-148">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="0667a-148">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="0667a-149">Yeni-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="0667a-149">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="0667a-150">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="0667a-150">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
