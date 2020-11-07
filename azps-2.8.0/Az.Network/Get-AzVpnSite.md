---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
ms.openlocfilehash: 0c6ede26826547e525610c76f4a2883f9b738b33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918379"
---
# <span data-ttu-id="1ed3b-101">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="1ed3b-101">Get-AzVpnSite</span></span>

## <span data-ttu-id="1ed3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ed3b-102">SYNOPSIS</span></span>
<span data-ttu-id="1ed3b-103">Bir ResourceGroup veya SubscriptionID 'deki tüm VpnSites adına göre bir Azure VpnSite kaynağını alır veya bu kaynağı listeler.</span><span class="sxs-lookup"><span data-stu-id="1ed3b-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="1ed3b-104">Bu, Cortex sanal hub ile S2S bağlantısı için Azure 'a yüklenen müşteri dallarının RM temsilidir.</span><span class="sxs-lookup"><span data-stu-id="1ed3b-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="1ed3b-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ed3b-105">SYNTAX</span></span>

### <span data-ttu-id="1ed3b-106">Listbysubscriptionıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1ed3b-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ed3b-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ed3b-107">ListByResourceGroupName</span></span>
```
Get-AzVpnSite [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ed3b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ed3b-108">DESCRIPTION</span></span>
<span data-ttu-id="1ed3b-109">Bir ResourceGroup veya SubscriptionID 'deki tüm VpnSites adına göre bir Azure VpnSite kaynağını alır veya bu kaynağı listeler.</span><span class="sxs-lookup"><span data-stu-id="1ed3b-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="1ed3b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ed3b-110">EXAMPLES</span></span>

### <span data-ttu-id="1ed3b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1ed3b-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="1ed3b-112">Yukarıdaki, Azure 'daki "testRG" kaynak grubundaki Batı</span><span class="sxs-lookup"><span data-stu-id="1ed3b-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="1ed3b-113">Ardından bir müşteri dalının temsil etmesi ve sanal WAN 'a bağlandığı bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ed3b-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="1ed3b-114">Site oluşturulduğunda, siteyi Get-AzVpnSite komutunu kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="1ed3b-114">Once the site is created, it gets the site using the Get-AzVpnSite command.</span></span>

### <span data-ttu-id="1ed3b-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1ed3b-115">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnSite -Name test*

ResourceGroupName : testRG
Name              : testVpnSite1
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite1
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded

ResourceGroupName : testRG
Name              : testVpnSite2
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite2
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="1ed3b-116">Bu cmdlet, "test" ile başlayan tüm siteleri alır.</span><span class="sxs-lookup"><span data-stu-id="1ed3b-116">This cmdlet gets all Sites that start with "test".</span></span>

## <span data-ttu-id="1ed3b-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ed3b-117">PARAMETERS</span></span>

### <span data-ttu-id="1ed3b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ed3b-118">-DefaultProfile</span></span>
<span data-ttu-id="1ed3b-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1ed3b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ed3b-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="1ed3b-120">-Name</span></span>
<span data-ttu-id="1ed3b-121">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="1ed3b-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnSiteName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ed3b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ed3b-122">-ResourceGroupName</span></span>
<span data-ttu-id="1ed3b-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1ed3b-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ed3b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ed3b-124">CommonParameters</span></span>
<span data-ttu-id="1ed3b-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ed3b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ed3b-126">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1ed3b-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ed3b-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ed3b-127">INPUTS</span></span>

### <span data-ttu-id="1ed3b-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1ed3b-128">None</span></span>

## <span data-ttu-id="1ed3b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ed3b-129">OUTPUTS</span></span>

### <span data-ttu-id="1ed3b-130">Microsoft. Azure. Commands. Network. modeller. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="1ed3b-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="1ed3b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ed3b-131">NOTES</span></span>

## <span data-ttu-id="1ed3b-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ed3b-132">RELATED LINKS</span></span>

[<span data-ttu-id="1ed3b-133">Yeni-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="1ed3b-133">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="1ed3b-134">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="1ed3b-134">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="1ed3b-135">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="1ed3b-135">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
