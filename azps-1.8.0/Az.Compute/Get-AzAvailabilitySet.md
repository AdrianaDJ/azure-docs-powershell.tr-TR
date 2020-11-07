---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
ms.openlocfilehash: 1ebb43f11d0286ca3fef4ab136c9e5a1e6ee031d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761363"
---
# <span data-ttu-id="339cf-101">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="339cf-101">Get-AzAvailabilitySet</span></span>

## <span data-ttu-id="339cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="339cf-102">SYNOPSIS</span></span>
<span data-ttu-id="339cf-103">Kaynak grubundaki Azure kullanılabilirlik kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="339cf-103">Gets Azure availability sets in a resource group.</span></span>

## <span data-ttu-id="339cf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="339cf-104">SYNTAX</span></span>

```
Get-AzAvailabilitySet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="339cf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="339cf-105">DESCRIPTION</span></span>
<span data-ttu-id="339cf-106">**Get-AzAvailabilitySet** cmdlet 'i kaynak grubundaki Azure kullanılabilirlik kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="339cf-106">The **Get-AzAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="339cf-107">Alınacak belirli bir kullanılabilirlik kümesinin adını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="339cf-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="339cf-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="339cf-108">EXAMPLES</span></span>

### <span data-ttu-id="339cf-109">Örnek 1: belirli bir kullanılabilirlik kümesi edinme</span><span class="sxs-lookup"><span data-stu-id="339cf-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="339cf-110">Bu komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet03 adındaki kullanılabilirlik kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="339cf-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="339cf-111">Örnek 2: tüm kullanılabilirlik kümelerini alma</span><span class="sxs-lookup"><span data-stu-id="339cf-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet10
Name                      : AvailabilitySet10
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="339cf-112">Bu komut, ResourceGroup11 adındaki kaynak grubundaki tüm kullanılabilirlik kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="339cf-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="339cf-113">Örnek 3: filtreleme ile tüm kullanılabilirlik kümelerini alma</span><span class="sxs-lookup"><span data-stu-id="339cf-113">Example 3: Get all availability sets with filtering</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup1*" -Name "AvailabilitySet0*"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="339cf-114">Bu komut, ResourceGroup11 adındaki kaynak grubundaki tüm kullanılabilirlik kümelerini "AvailabilitySet0" ile başlayan tüm kullanılabilirlik kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="339cf-114">This command gets all the availability sets in the resource group named ResourceGroup11 that start with "AvailabilitySet0".</span></span>

### <span data-ttu-id="339cf-115">Örnek 4: AvailabilitySet0 ile başlayan tüm kullanılabilirlik kümelerini alma</span><span class="sxs-lookup"><span data-stu-id="339cf-115">Example 4: Get all availability sets with name starting with AvailabilitySet0</span></span>
```
PS C:\> Get-AzAvailabilitySet -Name AvailabilitySet0*

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup12
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup12/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="339cf-116">Bu komut, "AvailabilitySet0" ile başlayan tüm kullanılabilirlik kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="339cf-116">This command gets all the availability sets that start with "AvailabilitySet0".</span></span>

## <span data-ttu-id="339cf-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="339cf-117">PARAMETERS</span></span>

### <span data-ttu-id="339cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="339cf-118">-DefaultProfile</span></span>
<span data-ttu-id="339cf-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="339cf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="339cf-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="339cf-120">-Name</span></span>
<span data-ttu-id="339cf-121">Bu cmdlet 'in aldığı kullanılabilirlik kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="339cf-121">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="339cf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="339cf-122">-ResourceGroupName</span></span>
<span data-ttu-id="339cf-123">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="339cf-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="339cf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="339cf-124">CommonParameters</span></span>
<span data-ttu-id="339cf-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="339cf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="339cf-126">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="339cf-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="339cf-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="339cf-127">INPUTS</span></span>

### <span data-ttu-id="339cf-128">System. String</span><span class="sxs-lookup"><span data-stu-id="339cf-128">System.String</span></span>

## <span data-ttu-id="339cf-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="339cf-129">OUTPUTS</span></span>

### <span data-ttu-id="339cf-130">Microsoft. Azure. Commands. COMPUTE. modeller. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="339cf-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="339cf-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="339cf-131">NOTES</span></span>

## <span data-ttu-id="339cf-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="339cf-132">RELATED LINKS</span></span>

[<span data-ttu-id="339cf-133">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="339cf-133">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)

[<span data-ttu-id="339cf-134">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="339cf-134">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)

