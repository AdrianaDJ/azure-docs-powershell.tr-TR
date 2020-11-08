---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliancesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
ms.openlocfilehash: e38e489207267faf53bb790aaab65ad60c74c8b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275980"
---
# <span data-ttu-id="ab9e8-101">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="ab9e8-101">Get-AzNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="ab9e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab9e8-102">SYNOPSIS</span></span>
<span data-ttu-id="ab9e8-103">Stoktaki kullanılabilir ağ sanal uygulaması SKU 'Larını alın veya listeleyin.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-103">Get or List available Network Virtual Appliance Skus in the inventory.</span></span>

## <span data-ttu-id="ab9e8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ab9e8-104">SYNTAX</span></span>

```
Get-AzNetworkVirtualApplianceSku [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab9e8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ab9e8-105">DESCRIPTION</span></span>
<span data-ttu-id="ab9e8-106">Get-AzNetworkVirtualApplianceSku, Microsoft Azure envanter'ndaki kullanılabilir ağ sanal gereç SKU 'Larını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-106">The Get-AzNetworkVirtualApplianceSku gets or lists available Network Virtual Appliance Skus in the Microsoft Azure inventory.</span></span>

## <span data-ttu-id="ab9e8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ab9e8-107">EXAMPLES</span></span>

### <span data-ttu-id="ab9e8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ab9e8-108">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku -SkuName barracudasdwanrelease                                                                                                                        

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="ab9e8-109">STB adına sahip olun.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-109">Get a sku by name.</span></span>

### <span data-ttu-id="ab9e8-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ab9e8-110">Example 2</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku                                                                                                                                                       

Vendor              : barracuda sdwan nightly
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan nightly
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracuda sdwan
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="ab9e8-111">Ağ sanal aygıtının tüm kullanılabilir SKU 'Larını listeler.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-111">List all available Skus of Network Virtual Appliance.</span></span>

## <span data-ttu-id="ab9e8-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ab9e8-112">PARAMETERS</span></span>

### <span data-ttu-id="ab9e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab9e8-113">-DefaultProfile</span></span>
<span data-ttu-id="ab9e8-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab9e8-115">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ab9e8-115">-SkuName</span></span>
<span data-ttu-id="ab9e8-116">SKU adı.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-116">The Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab9e8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab9e8-117">CommonParameters</span></span>
<span data-ttu-id="ab9e8-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab9e8-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab9e8-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ab9e8-120">INPUTS</span></span>

### <span data-ttu-id="ab9e8-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ab9e8-121">None</span></span>

## <span data-ttu-id="ab9e8-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ab9e8-122">OUTPUTS</span></span>

### <span data-ttu-id="ab9e8-123">Microsoft. Azure. Commands. Network. model. Psnetworkvirtualapplisku</span><span class="sxs-lookup"><span data-stu-id="ab9e8-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="ab9e8-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ab9e8-124">NOTES</span></span>

## <span data-ttu-id="ab9e8-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ab9e8-125">RELATED LINKS</span></span>
