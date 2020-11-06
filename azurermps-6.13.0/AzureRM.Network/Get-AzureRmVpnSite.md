---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnSite.md
ms.openlocfilehash: 0277e61a6b1b180691908b2e86c0050eb8d62b1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589477"
---
# <span data-ttu-id="3b1d3-101">Get-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="3b1d3-101">Get-AzureRmVpnSite</span></span>

## <span data-ttu-id="3b1d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b1d3-102">SYNOPSIS</span></span>
<span data-ttu-id="3b1d3-103">Bir ResourceGroup veya SubscriptionID 'deki tüm VpnSites adına göre bir Azure VpnSite kaynağını alır veya bu kaynağı listeler.</span><span class="sxs-lookup"><span data-stu-id="3b1d3-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="3b1d3-104">Bu, Cortex sanal hub ile S2S bağlantısı için Azure 'a yüklenen müşteri dallarının RM temsilidir.</span><span class="sxs-lookup"><span data-stu-id="3b1d3-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b1d3-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b1d3-105">SYNTAX</span></span>

### <span data-ttu-id="3b1d3-106">Listbysubscriptionıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3b1d3-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b1d3-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b1d3-107">ListByResourceGroupName</span></span>
```
Get-AzureRmVpnSite -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3b1d3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b1d3-108">DESCRIPTION</span></span>
<span data-ttu-id="3b1d3-109">Bir ResourceGroup veya SubscriptionID 'deki tüm VpnSites adına göre bir Azure VpnSite kaynağını alır veya bu kaynağı listeler.</span><span class="sxs-lookup"><span data-stu-id="3b1d3-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="3b1d3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b1d3-110">EXAMPLES</span></span>

### <span data-ttu-id="3b1d3-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3b1d3-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"

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

<span data-ttu-id="3b1d3-112">Yukarıdaki, Azure 'daki "testRG" kaynak grubundaki Batı</span><span class="sxs-lookup"><span data-stu-id="3b1d3-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="3b1d3-113">Ardından bir müşteri dalının temsil etmesi ve sanal WAN 'a bağlandığı bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3b1d3-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="3b1d3-114">Site oluşturulduğunda, siteyi Get-AzureRmVpnSite komutunu kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="3b1d3-114">Once the site is created, it gets the site using the Get-AzureRmVpnSite command.</span></span>

## <span data-ttu-id="3b1d3-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b1d3-115">PARAMETERS</span></span>

### <span data-ttu-id="3b1d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b1d3-116">-DefaultProfile</span></span>
<span data-ttu-id="3b1d3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3b1d3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b1d3-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="3b1d3-118">-Name</span></span>
<span data-ttu-id="3b1d3-119">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="3b1d3-119">The resource name.</span></span>

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

### <span data-ttu-id="3b1d3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b1d3-120">-ResourceGroupName</span></span>
<span data-ttu-id="3b1d3-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3b1d3-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b1d3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b1d3-122">CommonParameters</span></span>
<span data-ttu-id="3b1d3-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b1d3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b1d3-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b1d3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b1d3-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b1d3-125">INPUTS</span></span>

### <span data-ttu-id="3b1d3-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3b1d3-126">None</span></span>

## <span data-ttu-id="3b1d3-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b1d3-127">OUTPUTS</span></span>

### <span data-ttu-id="3b1d3-128">Microsoft. Azure. Commands. Network. modeller. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="3b1d3-128">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="3b1d3-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b1d3-129">NOTES</span></span>

## <span data-ttu-id="3b1d3-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b1d3-130">RELATED LINKS</span></span>
