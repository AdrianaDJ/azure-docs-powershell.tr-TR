---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnSite.md
ms.openlocfilehash: ac0513b7d411c2c95864aa6f619e80d2373a3554
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590133"
---
# <span data-ttu-id="c52e8-101">Remove-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="c52e8-101">Remove-AzureRmVpnSite</span></span>

## <span data-ttu-id="c52e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c52e8-102">SYNOPSIS</span></span>
<span data-ttu-id="c52e8-103">Bir Azure VpnSite kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c52e8-103">Removes an Azure VpnSite resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c52e8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c52e8-104">SYNTAX</span></span>

### <span data-ttu-id="c52e8-105">ByVpnSiteName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c52e8-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzureRmVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c52e8-106">Byvpnsitenesnesi</span><span class="sxs-lookup"><span data-stu-id="c52e8-106">ByVpnSiteObject</span></span>
```
Remove-AzureRmVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c52e8-107">Byvpnsiteresourceıd</span><span class="sxs-lookup"><span data-stu-id="c52e8-107">ByVpnSiteResourceId</span></span>
```
Remove-AzureRmVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c52e8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c52e8-108">DESCRIPTION</span></span>
<span data-ttu-id="c52e8-109">Bir Azure VpnSite kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c52e8-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="c52e8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c52e8-110">EXAMPLES</span></span>

### <span data-ttu-id="c52e8-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c52e8-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="c52e8-112">Yukarıdaki, Azure 'daki "testRG" kaynak grubundaki Batı</span><span class="sxs-lookup"><span data-stu-id="c52e8-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="c52e8-113">Ardından bir müşteri dalının temsil etmesi ve sanal WAN 'a bağlandığı bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c52e8-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="c52e8-114">Site oluşturulduktan sonra Remove-AzureRmVpnSite komutu kullanılarak hemen kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="c52e8-114">Once the site is created, it is immediately removed using the Remove-AzureRmVpnSite command.</span></span>

### <span data-ttu-id="c52e8-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c52e8-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzureRmVpnSite
```

<span data-ttu-id="c52e8-116">Örnek 1 ile aynıdır, ancak buradan kaldırma işlemi Get-AzureRmVpnSite tarafından yöneltilen çıkışı kullanarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="c52e8-116">Same as example 1 but here the removal happens using the piped output from Get-AzureRmVpnSite.</span></span>

## <span data-ttu-id="c52e8-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c52e8-117">PARAMETERS</span></span>

### <span data-ttu-id="c52e8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c52e8-118">-DefaultProfile</span></span>
<span data-ttu-id="c52e8-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c52e8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c52e8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c52e8-120">-Force</span></span>
<span data-ttu-id="c52e8-121">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="c52e8-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c52e8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c52e8-122">-InputObject</span></span>
<span data-ttu-id="c52e8-123">Silinecek vpnSite nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c52e8-123">The vpnSite object to be deleted.</span></span>

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

### <span data-ttu-id="c52e8-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="c52e8-124">-Name</span></span>
<span data-ttu-id="c52e8-125">VpnSite adı.</span><span class="sxs-lookup"><span data-stu-id="c52e8-125">The vpnSite name.</span></span>

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

### <span data-ttu-id="c52e8-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c52e8-126">-PassThru</span></span>
<span data-ttu-id="c52e8-127">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="c52e8-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="c52e8-128">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="c52e8-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c52e8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c52e8-129">-ResourceGroupName</span></span>
<span data-ttu-id="c52e8-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c52e8-130">The resource group name.</span></span>

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

### <span data-ttu-id="c52e8-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c52e8-131">-ResourceId</span></span>
<span data-ttu-id="c52e8-132">Silinecek vpnSite için Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c52e8-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

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

### <span data-ttu-id="c52e8-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="c52e8-133">-Confirm</span></span>
<span data-ttu-id="c52e8-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c52e8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c52e8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c52e8-135">-WhatIf</span></span>
<span data-ttu-id="c52e8-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c52e8-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c52e8-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c52e8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c52e8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c52e8-138">CommonParameters</span></span>
<span data-ttu-id="c52e8-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c52e8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c52e8-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c52e8-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c52e8-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c52e8-141">INPUTS</span></span>

### <span data-ttu-id="c52e8-142">Microsoft. Azure. Commands. Network. modeller. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="c52e8-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="c52e8-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c52e8-143">System.String</span></span>

## <span data-ttu-id="c52e8-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c52e8-144">OUTPUTS</span></span>

### <span data-ttu-id="c52e8-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c52e8-145">System.Boolean</span></span>

## <span data-ttu-id="c52e8-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c52e8-146">NOTES</span></span>

## <span data-ttu-id="c52e8-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c52e8-147">RELATED LINKS</span></span>
