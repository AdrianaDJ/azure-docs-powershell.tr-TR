---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/disable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 65c9bca6eb678ff3f3cb0a61d815f8415c715e43
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937496"
---
# <span data-ttu-id="98e9d-101">Disable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="98e9d-101">Disable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="98e9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98e9d-102">SYNOPSIS</span></span>
<span data-ttu-id="98e9d-103">Özel etki alanı için HTTPS 'yi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="98e9d-103">Disable HTTPS for a custom domain</span></span>

## <span data-ttu-id="98e9d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="98e9d-104">SYNTAX</span></span>

### <span data-ttu-id="98e9d-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="98e9d-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98e9d-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="98e9d-106">ByResourceIdParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98e9d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98e9d-107">ByObjectParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98e9d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="98e9d-108">DESCRIPTION</span></span>
<span data-ttu-id="98e9d-109">**Disable-AzFrontDoorCustomDomainHttps** , özel bir etki alanı için https 'yi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="98e9d-109">The **Disable-AzFrontDoorCustomDomainHttps** disables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="98e9d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="98e9d-110">EXAMPLES</span></span>

### <span data-ttu-id="98e9d-111">Örnek 1: FrontDoorName ve ResourceGroupName ile özel bir etki alanı için HTTPS 'yi devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="98e9d-111">Example 1: Disable HTTPS for a custom domain with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz"

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="98e9d-112">HTTPS 'yi "frontendpointname1-Custom-XYZ" özel etki alanı için "FrontDoorName" olarak devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="98e9d-112">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with FrontDoorName as "frontdoor1" and ResourceGroupName as "resourcegroup1".</span></span>

### <span data-ttu-id="98e9d-113">Örnek 2: Psfrontendenvseçpoint nesnesiyle özel bir etki alanı için HTTPS 'yi devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="98e9d-113">Example 2: Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" | Disable-AzFrontDoorCustomDomainHttps -InputObject $frontendEndpointObj 

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="98e9d-114">Psfrontendenvseçpoint nesnesiyle özel bir etki alanı için HTTPS 'yi devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="98e9d-114">Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>

### <span data-ttu-id="98e9d-115">Örnek 3: RESOURCEID ile özel bir etki alanı için HTTPS 'yi devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="98e9d-115">Example 3: Disable HTTPS for a custom domain with ResourceId.</span></span>
```powershell
PS C:\> Disable-AzFrontDoorCustomDomainHttps -ResourceId $resourceId 

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="98e9d-116">"Frontendpointname1-Custom-XYZ" özel etki alanı için HTTPS 'yi $resourceId olarak devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="98e9d-116">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with ResourceId as $resourceId.</span></span>

## <span data-ttu-id="98e9d-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="98e9d-117">PARAMETERS</span></span>

### <span data-ttu-id="98e9d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98e9d-118">-DefaultProfile</span></span>
<span data-ttu-id="98e9d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="98e9d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98e9d-120">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="98e9d-120">-FrontDoorName</span></span>
<span data-ttu-id="98e9d-121">Ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="98e9d-121">The name of the Front Door.</span></span>

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

### <span data-ttu-id="98e9d-122">-Frontendenvseçpointname</span><span class="sxs-lookup"><span data-stu-id="98e9d-122">-FrontendEndpointName</span></span>
<span data-ttu-id="98e9d-123">Ön uç uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="98e9d-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="98e9d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98e9d-124">-InputObject</span></span>
<span data-ttu-id="98e9d-125">Güncelleştirilecek ön uç uç noktası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="98e9d-125">The Frontend endpoint object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98e9d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98e9d-126">-ResourceGroupName</span></span>
<span data-ttu-id="98e9d-127">Ön kapıya ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="98e9d-127">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="98e9d-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="98e9d-128">-ResourceId</span></span>
<span data-ttu-id="98e9d-129">Https 'yi devre dışı bırakmak için ön kapı uç noktasının kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="98e9d-129">Resource Id of the Front Door endpoint to disable https</span></span>

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

### <span data-ttu-id="98e9d-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="98e9d-130">-Confirm</span></span>
<span data-ttu-id="98e9d-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="98e9d-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98e9d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98e9d-132">-WhatIf</span></span>
<span data-ttu-id="98e9d-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="98e9d-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98e9d-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="98e9d-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98e9d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98e9d-135">CommonParameters</span></span>
<span data-ttu-id="98e9d-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="98e9d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98e9d-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="98e9d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98e9d-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="98e9d-138">INPUTS</span></span>

### <span data-ttu-id="98e9d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="98e9d-139">System.String</span></span>

## <span data-ttu-id="98e9d-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="98e9d-140">OUTPUTS</span></span>

### <span data-ttu-id="98e9d-141">Microsoft. Azure. Commands. Frontkapısı. modeller. Psfrontendenvseçpoint</span><span class="sxs-lookup"><span data-stu-id="98e9d-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="98e9d-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="98e9d-142">NOTES</span></span>

## <span data-ttu-id="98e9d-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="98e9d-143">RELATED LINKS</span></span>
