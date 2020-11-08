---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
ms.openlocfilehash: b21fe2cc51668548d4fedc8eb6fc9404d5626a41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266524"
---
# <span data-ttu-id="d36bd-101">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="d36bd-101">Get-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="d36bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d36bd-102">SYNOPSIS</span></span>
<span data-ttu-id="d36bd-103">Ağ sanal uygulaması kaynağına bağlı siteleri alın veya listeleyin.</span><span class="sxs-lookup"><span data-stu-id="d36bd-103">Get or List sites connected to Network Virtual Appliance resource(s).</span></span>

## <span data-ttu-id="d36bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d36bd-104">SYNTAX</span></span>

### <span data-ttu-id="d36bd-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d36bd-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzVirtualApplianceSite [-Name <String>] [-NetworkVirtualApplianceId <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d36bd-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d36bd-106">ResourceIdParameterSet</span></span>
```
Get-AzVirtualApplianceSite -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d36bd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d36bd-107">DESCRIPTION</span></span>
<span data-ttu-id="d36bd-108">Get-AzVirtualApplianceSite, bir veya daha fazla ağ sanal gereç kaynağına bağlı siteleri alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="d36bd-108">The Get-AzVirtualApplianceSite gets or lists sites connected to one or more Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="d36bd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d36bd-109">EXAMPLES</span></span>

### <span data-ttu-id="d36bd-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d36bd-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -Name testsite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite
```

<span data-ttu-id="d36bd-111">Sanal bir gereç sitesi kaynağı edinin.</span><span class="sxs-lookup"><span data-stu-id="d36bd-111">Get a Virtual Appliance site resource.</span></span>

### <span data-ttu-id="d36bd-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d36bd-112">Example 2</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite

AddressPrefix     : 10.0.2.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite2
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite2
```

<span data-ttu-id="d36bd-113">Ağ sanal uygulamasında Sanal Gereç sitesi kaynaklarını listeleyin.</span><span class="sxs-lookup"><span data-stu-id="d36bd-113">List Virtual Appliance site resources in a Network Virtual Appliance.</span></span>


## <span data-ttu-id="d36bd-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d36bd-114">PARAMETERS</span></span>

### <span data-ttu-id="d36bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d36bd-115">-DefaultProfile</span></span>
<span data-ttu-id="d36bd-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d36bd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d36bd-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="d36bd-117">-Name</span></span>
<span data-ttu-id="d36bd-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="d36bd-118">The resource name.</span></span>

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

### <span data-ttu-id="d36bd-119">-Networkvirtualapplianceıd</span><span class="sxs-lookup"><span data-stu-id="d36bd-119">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="d36bd-120">Sitenin bağlı olduğu ağ sanal uygulaması.</span><span class="sxs-lookup"><span data-stu-id="d36bd-120">The Network Virtual Appliance that the site is attached.</span></span>

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

### <span data-ttu-id="d36bd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d36bd-121">-ResourceGroupName</span></span>
<span data-ttu-id="d36bd-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d36bd-122">The resource group name.</span></span>

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

### <span data-ttu-id="d36bd-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d36bd-123">-ResourceId</span></span>
<span data-ttu-id="d36bd-124">Sanal Gereç sitesinin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="d36bd-124">The resource Id of the Virtual Appliance Site.</span></span>

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

### <span data-ttu-id="d36bd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d36bd-125">CommonParameters</span></span>
<span data-ttu-id="d36bd-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d36bd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d36bd-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d36bd-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d36bd-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d36bd-128">INPUTS</span></span>

### <span data-ttu-id="d36bd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d36bd-129">System.String</span></span>

## <span data-ttu-id="d36bd-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d36bd-130">OUTPUTS</span></span>

### <span data-ttu-id="d36bd-131">Microsoft. Azure. Commands. Network. model. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="d36bd-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="d36bd-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d36bd-132">NOTES</span></span>

## <span data-ttu-id="d36bd-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d36bd-133">RELATED LINKS</span></span>
