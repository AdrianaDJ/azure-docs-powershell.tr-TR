---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 657ffd65bd6dd477700002862060b931979de456
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275984"
---
# <span data-ttu-id="cd62d-101">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="cd62d-101">Get-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="cd62d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd62d-102">SYNOPSIS</span></span>
<span data-ttu-id="cd62d-103">Ağ sanal cihazları alın veya listeleyin.</span><span class="sxs-lookup"><span data-stu-id="cd62d-103">Get or List Network Virtual Appliances.</span></span>

## <span data-ttu-id="cd62d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd62d-104">SYNTAX</span></span>

### <span data-ttu-id="cd62d-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cd62d-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzNetworkVirtualAppliance [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd62d-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="cd62d-106">ResourceIdParameterSet</span></span>
```
Get-AzNetworkVirtualAppliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd62d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd62d-107">DESCRIPTION</span></span>
<span data-ttu-id="cd62d-108">Get-AzNetworkVirtualAppliance komutları ağ sanal gereç kaynaklarını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="cd62d-108">The Get-AzNetworkVirtualAppliance commands gets or lists Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="cd62d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd62d-109">EXAMPLES</span></span>

### <span data-ttu-id="cd62d-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cd62d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva                                                                                                                      

BootStrapConfigurationBlobs : {}
VirtualHub                  : Microsoft.Azure.Commands.Network.Models.PSResourceId
CloudInitConfigurationBlobs : {}
CloudInitConfiguration      : echo hi
VirtualApplianceAsn         : 1270
VirtualApplianceNics        : {privatenicipconfig, publicnicipconfig, privatenicipconfig, publicnicipconfig}
VirtualApplianceSites       : {}
ProvisioningState           : Succeeded
Identity                    :
NvaSku                      : Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
ResourceGroupName           : testrg
Location                    : eastus2
ResourceGuid                :
Type                        : Microsoft.Network/NetworkVirtualAppliances
Tag                         :
TagsTable                   :
Name                        : nva
Etag                        : 00000000-0000-0000-0000-000000000000
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva
```

<span data-ttu-id="cd62d-111">Ağ sanal bir gereç kaynağı alın.</span><span class="sxs-lookup"><span data-stu-id="cd62d-111">Get a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="cd62d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd62d-112">PARAMETERS</span></span>

### <span data-ttu-id="cd62d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd62d-113">-DefaultProfile</span></span>
<span data-ttu-id="cd62d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cd62d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd62d-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="cd62d-115">-Name</span></span>
<span data-ttu-id="cd62d-116">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="cd62d-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd62d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd62d-117">-ResourceGroupName</span></span>
<span data-ttu-id="cd62d-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="cd62d-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd62d-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cd62d-119">-ResourceId</span></span>
<span data-ttu-id="cd62d-120">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="cd62d-120">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd62d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd62d-121">CommonParameters</span></span>
<span data-ttu-id="cd62d-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd62d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd62d-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cd62d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd62d-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd62d-124">INPUTS</span></span>

### <span data-ttu-id="cd62d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="cd62d-125">System.String</span></span>

## <span data-ttu-id="cd62d-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd62d-126">OUTPUTS</span></span>

### <span data-ttu-id="cd62d-127">Microsoft. Azure. Commands. Network. model. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="cd62d-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="cd62d-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd62d-128">NOTES</span></span>

## <span data-ttu-id="cd62d-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd62d-129">RELATED LINKS</span></span>
