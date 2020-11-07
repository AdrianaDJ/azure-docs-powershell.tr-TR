---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 6edf891d693e0c1cb2143236d12e623fdd2b4a3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751917"
---
# <span data-ttu-id="66fbb-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="66fbb-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="66fbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66fbb-102">SYNOPSIS</span></span>
<span data-ttu-id="66fbb-103">Ön kapıyı yönetilen sertifikası kullanarak veya Azure Anahtar Kasası 'ndan kendi sertifikasını kullanarak özel bir etki alanı için HTTPS 'yi etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="66fbb-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="66fbb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66fbb-104">SYNTAX</span></span>

### <span data-ttu-id="66fbb-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="66fbb-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66fbb-106">Byalanwithvaultparameterset</span><span class="sxs-lookup"><span data-stu-id="66fbb-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66fbb-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="66fbb-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66fbb-108">Byresourceıdwithvaultparameterset</span><span class="sxs-lookup"><span data-stu-id="66fbb-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66fbb-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66fbb-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66fbb-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="66fbb-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66fbb-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="66fbb-111">DESCRIPTION</span></span>
<span data-ttu-id="66fbb-112">**Enable-AzFrontDoorCustomDomainHttps** , özel bir etki alanı için https 'yi etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="66fbb-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="66fbb-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66fbb-113">EXAMPLES</span></span>

### <span data-ttu-id="66fbb-114">Örnek 1: ön kapı yönetimli sertifikayı kullanarak FrontDoorName ve ResourceGroupName ile özel bir etki alanı için HTTPS 'yi etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="66fbb-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
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

<span data-ttu-id="66fbb-115">"Frontendpointname1-Custom-XYZ" özel etki alanında, ön kapı yönetimli sertifikayı kullanarak "resourcegroup1" ön kapısının parçası olan HTTPS 'yi etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="66fbb-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="66fbb-116">Örnek 2: anahtar kasasındaki kendi sertifikasını kullanarak FrontDoorName ve ResourceGroupName ile özel bir etki alanı için HTTPS 'yi etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="66fbb-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
```powershell
PS C:\> $vaultId = (Get-AzKeyVault -VaultName $vaultName).ResourceId
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -Vault $vaultId -secretName $secretName -SecretVersion $secretVersion


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : AzureKeyVault
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

<span data-ttu-id="66fbb-117">"Frontendpointname1-Custom-XYZ" özel etki alanında, ön kapı yönetimli sertifikayı kullanarak "resourcegroup1" ön kapısının parçası olan HTTPS 'yi etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="66fbb-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="66fbb-118">Örnek 3: ön kapı yönetimli sertifika kullanarak Psfrontendenvseçpoint nesnesiyle özel bir etki alanı için HTTPS 'yi etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="66fbb-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" | Enable-AzFrontDoorCustomDomainHttps 


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
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

<span data-ttu-id="66fbb-119">Ön kapı yönetimli sertifika kullanarak Psfrontendenvseçpoint nesnesiyle özel bir etki alanı için HTTPS 'yi etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="66fbb-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="66fbb-120">Örnek 4: ön kapı yönetilen sertifikası kullanarak kaynak kimliği olan özel bir etki alanı için HTTPS 'yi etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="66fbb-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceId $resourceId


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
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

<span data-ttu-id="66fbb-121">Ön kapı yönetimli sertifikayı kullanarak "frontendpointname1-Custom-XYZ" özel etki alanı için HTTPS 'yi etkinleştirme $resourceId.</span><span class="sxs-lookup"><span data-stu-id="66fbb-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="66fbb-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66fbb-122">PARAMETERS</span></span>

### <span data-ttu-id="66fbb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66fbb-123">-DefaultProfile</span></span>
<span data-ttu-id="66fbb-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="66fbb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66fbb-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="66fbb-125">-FrontDoorName</span></span>
<span data-ttu-id="66fbb-126">Ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="66fbb-126">The name of the Front Door.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66fbb-127">-Frontendenvseçpointname</span><span class="sxs-lookup"><span data-stu-id="66fbb-127">-FrontendEndpointName</span></span>
<span data-ttu-id="66fbb-128">Ön uç uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="66fbb-128">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66fbb-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66fbb-129">-InputObject</span></span>
<span data-ttu-id="66fbb-130">Güncelleştirilecek ön uç uç noktası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="66fbb-130">The Frontend endpoint object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint
Parameter Sets: ByObjectParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66fbb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66fbb-131">-ResourceGroupName</span></span>
<span data-ttu-id="66fbb-132">Ön kapıya ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="66fbb-132">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66fbb-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="66fbb-133">-ResourceId</span></span>
<span data-ttu-id="66fbb-134">Https 'yi etkinleştirmek için ön kapı uç noktasının kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="66fbb-134">Resource Id of the Front Door endpoint to enable https</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet, ByResourceIdWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66fbb-135">-SecretName</span><span class="sxs-lookup"><span data-stu-id="66fbb-135">-SecretName</span></span>
<span data-ttu-id="66fbb-136">Tam sertifika PFX 'yi temsil eden Anahtar Kasası parolasının adı</span><span class="sxs-lookup"><span data-stu-id="66fbb-136">The name of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66fbb-137">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="66fbb-137">-SecretVersion</span></span>
<span data-ttu-id="66fbb-138">Tam sertifika PFX 'yi temsil eden Anahtar Kasası parolasının sürümü</span><span class="sxs-lookup"><span data-stu-id="66fbb-138">The version of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66fbb-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="66fbb-139">-VaultId</span></span>
<span data-ttu-id="66fbb-140">SSL sertifikasını içeren tuş Kasası kimliği</span><span class="sxs-lookup"><span data-stu-id="66fbb-140">The Key Vault id containing the SSL certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66fbb-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="66fbb-141">-Confirm</span></span>
<span data-ttu-id="66fbb-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="66fbb-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66fbb-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66fbb-143">-WhatIf</span></span>
<span data-ttu-id="66fbb-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="66fbb-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66fbb-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="66fbb-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66fbb-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66fbb-146">CommonParameters</span></span>
<span data-ttu-id="66fbb-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66fbb-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66fbb-148">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="66fbb-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66fbb-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66fbb-149">INPUTS</span></span>

### <span data-ttu-id="66fbb-150">System. String</span><span class="sxs-lookup"><span data-stu-id="66fbb-150">System.String</span></span>

## <span data-ttu-id="66fbb-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66fbb-151">OUTPUTS</span></span>

### <span data-ttu-id="66fbb-152">Microsoft. Azure. Commands. Frontkapısı. modeller. Psfrontendenvseçpoint</span><span class="sxs-lookup"><span data-stu-id="66fbb-152">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="66fbb-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66fbb-153">NOTES</span></span>

## <span data-ttu-id="66fbb-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66fbb-154">RELATED LINKS</span></span>
