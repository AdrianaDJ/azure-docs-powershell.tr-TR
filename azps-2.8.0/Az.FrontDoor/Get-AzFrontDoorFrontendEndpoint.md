---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfrontendendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
ms.openlocfilehash: f685bb7bdad663e84a67397c89568d2263d0ed9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751911"
---
# <span data-ttu-id="8b4f7-101">Get-AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="8b4f7-101">Get-AzFrontDoorFrontendEndpoint</span></span>

## <span data-ttu-id="8b4f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b4f7-102">SYNOPSIS</span></span>
<span data-ttu-id="8b4f7-103">Ön kapı ön uç uç noktası alın.</span><span class="sxs-lookup"><span data-stu-id="8b4f7-103">Get a front door frontend endpoint.</span></span>

## <span data-ttu-id="8b4f7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b4f7-104">SYNTAX</span></span>

### <span data-ttu-id="8b4f7-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8b4f7-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b4f7-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b4f7-106">ByObjectParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint [-Name <String>] -FrontDoorObject <PSFrontDoor>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b4f7-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="8b4f7-107">ByResourceIdParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b4f7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b4f7-108">DESCRIPTION</span></span>
<span data-ttu-id="8b4f7-109">**Get-AzFrontDoorFrontendEndpoint** cmdlet 'ı geçerli ön kapı kaynağında sağlanan bilgilerle eşleşen tüm ön uç uç noktalarını alır.</span><span class="sxs-lookup"><span data-stu-id="8b4f7-109">The **Get-AzFrontDoorFrontendEndpoint** cmdlet gets all existing frontend endpoints in the current Front Door resource that matches provided information.</span></span>

## <span data-ttu-id="8b4f7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b4f7-110">EXAMPLES</span></span>

### <span data-ttu-id="8b4f7-111">Örnek 1: "RG1" kaynak grubunun bir parçası olan "frontdoor1" ön yüzünde tüm ön uç uç noktalarını alın.</span><span class="sxs-lookup"><span data-stu-id="8b4f7-111">Example 1: Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "rg1" -FrontDoorName "frontdoor1"


HostName                         : frontdoor1.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontdoor1-azurefd-net
Name                             : frontdoor1-azurefd-net
Type                             : Microsoft.Network/frontdoors/frontendendpoints

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="8b4f7-112">"RG1" kaynak grubunun bir parçası olan "frontdoor1" ön yüzünde tüm ön uç uç noktalarını alın.</span><span class="sxs-lookup"><span data-stu-id="8b4f7-112">Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>

### <span data-ttu-id="8b4f7-113">Örnek 2: "frontdoor1-azurefd-net" adında ön uç uç noktası</span><span class="sxs-lookup"><span data-stu-id="8b4f7-113">Example 2: Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "rg1" -FrontDoorName "frontdoor1" -Name "frontdoor1-azurefd-net"


HostName                         : frontdoor1.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontdoor1-azurefd-net
Name                             : frontdoor1-azurefd-net
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="8b4f7-114">"Frontdoor1-azurefd-net" adlı ön kapıda "frontdoor1" adlı ön uç uç noktasını</span><span class="sxs-lookup"><span data-stu-id="8b4f7-114">Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>

## <span data-ttu-id="8b4f7-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b4f7-115">PARAMETERS</span></span>

### <span data-ttu-id="8b4f7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b4f7-116">-DefaultProfile</span></span>
<span data-ttu-id="8b4f7-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8b4f7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b4f7-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="8b4f7-118">-FrontDoorName</span></span>
<span data-ttu-id="8b4f7-119">Ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="8b4f7-119">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4f7-120">-FrontDoorObject</span><span class="sxs-lookup"><span data-stu-id="8b4f7-120">-FrontDoorObject</span></span>
<span data-ttu-id="8b4f7-121">Frontkapı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8b4f7-121">The FrontDoor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b4f7-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="8b4f7-122">-Name</span></span>
<span data-ttu-id="8b4f7-123">Ön uç uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="8b4f7-123">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4f7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b4f7-124">-ResourceGroupName</span></span>
<span data-ttu-id="8b4f7-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8b4f7-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4f7-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8b4f7-126">-ResourceId</span></span>
<span data-ttu-id="8b4f7-127">Ön kapı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="8b4f7-127">Resource Id of the Front Door</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b4f7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b4f7-128">CommonParameters</span></span>
<span data-ttu-id="8b4f7-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b4f7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b4f7-130">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8b4f7-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b4f7-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b4f7-131">INPUTS</span></span>

### <span data-ttu-id="8b4f7-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8b4f7-132">None</span></span>

## <span data-ttu-id="8b4f7-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b4f7-133">OUTPUTS</span></span>

### <span data-ttu-id="8b4f7-134">Microsoft. Azure. Commands. Frontkapısı. modeller. Psfrontendenvseçpoint</span><span class="sxs-lookup"><span data-stu-id="8b4f7-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="8b4f7-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b4f7-135">NOTES</span></span>

## <span data-ttu-id="8b4f7-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b4f7-136">RELATED LINKS</span></span>
