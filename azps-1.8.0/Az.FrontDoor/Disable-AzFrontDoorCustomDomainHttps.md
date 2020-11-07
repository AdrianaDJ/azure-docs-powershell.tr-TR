---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/disable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 2f6b5635b029548f8d92917e0abfca18d5c0c415
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916787"
---
# <span data-ttu-id="63c44-101">Disable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="63c44-101">Disable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="63c44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63c44-102">SYNOPSIS</span></span>
<span data-ttu-id="63c44-103">Özel etki alanı için HTTPS 'yi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="63c44-103">Disable HTTPS for a custom domain</span></span>

## <span data-ttu-id="63c44-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="63c44-104">SYNTAX</span></span>

### <span data-ttu-id="63c44-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="63c44-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63c44-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="63c44-106">ByResourceIdParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63c44-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63c44-107">ByObjectParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63c44-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="63c44-108">DESCRIPTION</span></span>
<span data-ttu-id="63c44-109">**Disable-AzFrontDoorCustomDomainHttps** , özel bir etki alanı için https 'yi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="63c44-109">The **Disable-AzFrontDoorCustomDomainHttps** disables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="63c44-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="63c44-110">EXAMPLES</span></span>

### <span data-ttu-id="63c44-111">Örnek 1: FrontDoorName ve ResourceGroupName ile özel bir etki alanı için HTTPS 'yi devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="63c44-111">Example 1: Disable HTTPS for a custom domain with FrontDoorName and ResourceGroupName.</span></span>
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

<span data-ttu-id="63c44-112">HTTPS 'yi "frontendpointname1-Custom-XYZ" özel etki alanı için "FrontDoorName" olarak devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="63c44-112">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with FrontDoorName as "frontdoor1" and ResourceGroupName as "resourcegroup1".</span></span>

### <span data-ttu-id="63c44-113">Örnek 2: Psfrontendenvseçpoint nesnesiyle özel bir etki alanı için HTTPS 'yi devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="63c44-113">Example 2: Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>
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

<span data-ttu-id="63c44-114">Psfrontendenvseçpoint nesnesiyle özel bir etki alanı için HTTPS 'yi devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="63c44-114">Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>

### <span data-ttu-id="63c44-115">Örnek 3: RESOURCEID ile özel bir etki alanı için HTTPS 'yi devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="63c44-115">Example 3: Disable HTTPS for a custom domain with ResourceId.</span></span>
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

<span data-ttu-id="63c44-116">"Frontendpointname1-Custom-XYZ" özel etki alanı için HTTPS 'yi $resourceId olarak devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="63c44-116">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with ResourceId as $resourceId.</span></span>

## <span data-ttu-id="63c44-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="63c44-117">PARAMETERS</span></span>

### <span data-ttu-id="63c44-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63c44-118">-DefaultProfile</span></span>
<span data-ttu-id="63c44-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="63c44-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63c44-120">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="63c44-120">-FrontDoorName</span></span>
<span data-ttu-id="63c44-121">Ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="63c44-121">The name of the Front Door.</span></span>

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

### <span data-ttu-id="63c44-122">-Frontendenvseçpointname</span><span class="sxs-lookup"><span data-stu-id="63c44-122">-FrontendEndpointName</span></span>
<span data-ttu-id="63c44-123">Ön uç uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="63c44-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="63c44-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63c44-124">-InputObject</span></span>
<span data-ttu-id="63c44-125">Güncelleştirilecek ön uç uç noktası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="63c44-125">The Frontend endpoint object to update.</span></span>

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

### <span data-ttu-id="63c44-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63c44-126">-ResourceGroupName</span></span>
<span data-ttu-id="63c44-127">Ön kapıya ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="63c44-127">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="63c44-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="63c44-128">-ResourceId</span></span>
<span data-ttu-id="63c44-129">Https 'yi devre dışı bırakmak için ön kapı uç noktasının kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="63c44-129">Resource Id of the Front Door endpoint to disable https</span></span>

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

### <span data-ttu-id="63c44-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="63c44-130">-Confirm</span></span>
<span data-ttu-id="63c44-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="63c44-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63c44-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63c44-132">-WhatIf</span></span>
<span data-ttu-id="63c44-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="63c44-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63c44-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="63c44-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63c44-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63c44-135">CommonParameters</span></span>
<span data-ttu-id="63c44-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="63c44-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63c44-137">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="63c44-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63c44-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="63c44-138">INPUTS</span></span>

### <span data-ttu-id="63c44-139">System. String</span><span class="sxs-lookup"><span data-stu-id="63c44-139">System.String</span></span>

## <span data-ttu-id="63c44-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="63c44-140">OUTPUTS</span></span>

### <span data-ttu-id="63c44-141">Microsoft. Azure. Commands. Frontkapısı. modeller. Psfrontendenvseçpoint</span><span class="sxs-lookup"><span data-stu-id="63c44-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="63c44-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="63c44-142">NOTES</span></span>

## <span data-ttu-id="63c44-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63c44-143">RELATED LINKS</span></span>
