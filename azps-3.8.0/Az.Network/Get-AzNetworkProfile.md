---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
ms.openlocfilehash: 4b96ec4fb263d262419d1c545cd9b1f0c35da413
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098796"
---
# <span data-ttu-id="426a1-101">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="426a1-101">Get-AzNetworkProfile</span></span>

## <span data-ttu-id="426a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="426a1-102">SYNOPSIS</span></span>
<span data-ttu-id="426a1-103">Var olan bir ağ profili üst düzey kaynağını alır</span><span class="sxs-lookup"><span data-stu-id="426a1-103">Gets an existing network profile top level resource</span></span>

## <span data-ttu-id="426a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="426a1-104">SYNTAX</span></span>

### <span data-ttu-id="426a1-105">Getbyresourcenparameteroexpandparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="426a1-105">GetByResourceNameNoExpandParameterSet (Default)</span></span>
```
Get-AzNetworkProfile [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="426a1-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="426a1-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="426a1-107">Getbyresourceidexpanvseçparameterset</span><span class="sxs-lookup"><span data-stu-id="426a1-107">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="426a1-108">Getbyresourceıdnoexpandparameterset</span><span class="sxs-lookup"><span data-stu-id="426a1-108">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="426a1-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="426a1-109">DESCRIPTION</span></span>
<span data-ttu-id="426a1-110">**Get-AzNetworkProfile** cmdlet 'i var olan bir ağ profili üst düzey kaynağını alır</span><span class="sxs-lookup"><span data-stu-id="426a1-110">The **Get-AzNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="426a1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="426a1-111">EXAMPLES</span></span>

### <span data-ttu-id="426a1-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="426a1-112">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np1
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np1
```

<span data-ttu-id="426a1-113">Bu, kaynak grubundaki NP1 ağ profilini alır RG1</span><span class="sxs-lookup"><span data-stu-id="426a1-113">This retrieves the network profile np1 in resource group rg1</span></span>

### <span data-ttu-id="426a1-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="426a1-114">Example 2</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np*

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np1
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np1

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np2
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np2
```

<span data-ttu-id="426a1-115">Bu, "NP" ile başlayan ağ profillerini alır</span><span class="sxs-lookup"><span data-stu-id="426a1-115">This retrieves the network profiles that start with "np"</span></span>

## <span data-ttu-id="426a1-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="426a1-116">PARAMETERS</span></span>

### <span data-ttu-id="426a1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="426a1-117">-DefaultProfile</span></span>
<span data-ttu-id="426a1-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="426a1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="426a1-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="426a1-119">-ExpandResource</span></span>
<span data-ttu-id="426a1-120">Genişletilecek kaynak başvurusu.</span><span class="sxs-lookup"><span data-stu-id="426a1-120">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet, GetByResourceIdExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="426a1-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="426a1-121">-Name</span></span>
<span data-ttu-id="426a1-122">Ağ profilinin adı.</span><span class="sxs-lookup"><span data-stu-id="426a1-122">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="426a1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="426a1-123">-ResourceGroupName</span></span>
<span data-ttu-id="426a1-124">Ağ profilinin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="426a1-124">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="426a1-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="426a1-125">-ResourceId</span></span>
<span data-ttu-id="426a1-126">Ağ profilinin Azure Kaynak Yöneticisi kimliği.</span><span class="sxs-lookup"><span data-stu-id="426a1-126">The Azure resource manager id of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="426a1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="426a1-127">CommonParameters</span></span>
<span data-ttu-id="426a1-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="426a1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="426a1-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="426a1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="426a1-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="426a1-130">INPUTS</span></span>

### <span data-ttu-id="426a1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="426a1-131">System.String</span></span>

## <span data-ttu-id="426a1-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="426a1-132">OUTPUTS</span></span>

### <span data-ttu-id="426a1-133">Microsoft. Azure. Commands. Network. modeller. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="426a1-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="426a1-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="426a1-134">NOTES</span></span>

## <span data-ttu-id="426a1-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="426a1-135">RELATED LINKS</span></span>

[<span data-ttu-id="426a1-136">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="426a1-136">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="426a1-137">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="426a1-137">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="426a1-138">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="426a1-138">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
