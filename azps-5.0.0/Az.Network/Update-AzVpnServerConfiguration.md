---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: 8897b2e1175c82f3dcc25642dec920a4b6d7343c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275939"
---
# <span data-ttu-id="8584a-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="8584a-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="8584a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8584a-102">SYNOPSIS</span></span>
<span data-ttu-id="8584a-103">Var olan bir Vpnserveryapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8584a-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="8584a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8584a-104">SYNTAX</span></span>

### <span data-ttu-id="8584a-105">ByVpnServerConfigurationNameByCertificateAuthentication (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8584a-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8584a-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="8584a-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8584a-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="8584a-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8584a-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="8584a-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8584a-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="8584a-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8584a-110">ByVpnServerConfigurationObjectByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="8584a-110">ByVpnServerConfigurationObjectByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8584a-111">Byvpnserverconfigurationresourceıdbycertificateauthentication</span><span class="sxs-lookup"><span data-stu-id="8584a-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8584a-112">Byvpnserverconfigurationresourceıdbyradiusauthentication</span><span class="sxs-lookup"><span data-stu-id="8584a-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8584a-113">Byvpnserverconfigurationresourceıdbyaadauthentication</span><span class="sxs-lookup"><span data-stu-id="8584a-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8584a-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="8584a-114">DESCRIPTION</span></span>
<span data-ttu-id="8584a-115">**Update-AzVpnServerConfiguration** cmdlet 'i, var olan vpnserverconfiguration 'ı farklı Vpnprotocols, VpnAuthenticationTypes, ıpsecpolicies ile güncelleştirmenize ve Seçilen VPN kimlik doğrulama türüyle ilgili parametrelerin, müşterinin site bağlantısı için gerekme gereksinimlerine göre ayarlanmasını olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="8584a-115">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="8584a-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8584a-116">EXAMPLES</span></span>

### <span data-ttu-id="8584a-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8584a-117">Example 1</span></span>
```powershell
PS C:\> Update-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2

PS C:\> New-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2 -VpnAuthenticationType Certificate -VpnClientRootCertificateFilesList $listOfCerts -VpnClientRevokedCertificateFilesList $listOfCerts -Location "westus"
ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2}
VpnAuthenticationTypes       : {Certificate}
VpnClientRootCertificates    :
VpnClientRevokedCertificates : [
                                 {
                                   "Name": "cert2",
                                   "Thumbprint": "83FFBFC8848B5A5836C94D0112367E16148A286F"
                                 }
                               ]
RadiusServerAddress          :
RadiusServerRootCertificates : []
RadiusClientRootCertificates : []
VpnClientIpsecPolicies       : []
AadAuthenticationParameters  : null
P2sVpnGateways               : []
Type                         : Microsoft.Network/vpnServerConfigurations
ProvisioningState            : Succeeded
```

<span data-ttu-id="8584a-118">Yukarıdaki komut, VpnProtocol ile mevcut bir Vpnserveryapılandırmasını Ikev2 olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8584a-118">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="8584a-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8584a-119">PARAMETERS</span></span>

### <span data-ttu-id="8584a-120">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="8584a-120">-AadAudience</span></span>
<span data-ttu-id="8584a-121">P2S AAD kimlik doğrulaması için AAD izleyiciyi.</span><span class="sxs-lookup"><span data-stu-id="8584a-121">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8584a-122">-Aadıssuer</span><span class="sxs-lookup"><span data-stu-id="8584a-122">-AadIssuer</span></span>
<span data-ttu-id="8584a-123">P2S AAD kimlik doğrulaması için AAD vericisi.</span><span class="sxs-lookup"><span data-stu-id="8584a-123">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8584a-124">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="8584a-124">-AadTenant</span></span>
<span data-ttu-id="8584a-125">P2S AAD kimlik doğrulaması için AAD kiracısı.</span><span class="sxs-lookup"><span data-stu-id="8584a-125">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8584a-126">-Iş</span><span class="sxs-lookup"><span data-stu-id="8584a-126">-AsJob</span></span>
<span data-ttu-id="8584a-127">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8584a-127">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8584a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8584a-128">-DefaultProfile</span></span>
<span data-ttu-id="8584a-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8584a-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8584a-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8584a-130">-InputObject</span></span>
<span data-ttu-id="8584a-131">Değiştirilecek VPN sunucusu yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="8584a-131">The vpn server configuration object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationObjectByAadAuthentication
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8584a-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="8584a-132">-Name</span></span>
<span data-ttu-id="8584a-133">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="8584a-133">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8584a-134">-Radiusclientrootcertificatefileslistesi</span><span class="sxs-lookup"><span data-stu-id="8584a-134">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="8584a-135">RadiusClientRootCertificate dosyalarının yollarının listesi</span><span class="sxs-lookup"><span data-stu-id="8584a-135">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8584a-136">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="8584a-136">-RadiusServerAddress</span></span>
<span data-ttu-id="8584a-137">P2S dış RADIUS sunucusu adresi.</span><span class="sxs-lookup"><span data-stu-id="8584a-137">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8584a-138">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="8584a-138">-RadiusServerList</span></span>
<span data-ttu-id="8584a-139">Dış çoklu RADIUS sunucularını P2S.</span><span class="sxs-lookup"><span data-stu-id="8584a-139">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8584a-140">-Radiusserverrootcertificatefileslistesi</span><span class="sxs-lookup"><span data-stu-id="8584a-140">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="8584a-141">RadiusClientRootCertificate dosyalarının yollarının listesi</span><span class="sxs-lookup"><span data-stu-id="8584a-141">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8584a-142">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="8584a-142">-RadiusServerSecret</span></span>
<span data-ttu-id="8584a-143">Dış RADIUS sunucusu gizliliğini P2S.</span><span class="sxs-lookup"><span data-stu-id="8584a-143">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8584a-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8584a-144">-ResourceGroupName</span></span>
<span data-ttu-id="8584a-145">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8584a-145">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8584a-146">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8584a-146">-ResourceId</span></span>
<span data-ttu-id="8584a-147">VPN sunucusu yapılandırması için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="8584a-147">The Azure resource ID for the vpn server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationResourceIdByCertificateAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8584a-148">Etiketli</span><span class="sxs-lookup"><span data-stu-id="8584a-148">-Tag</span></span>
<span data-ttu-id="8584a-149">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="8584a-149">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8584a-150">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="8584a-150">-VpnAuthenticationType</span></span>
<span data-ttu-id="8584a-151">P2S VPN istemci tünel protokollerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="8584a-151">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Certificate, Radius, AAD

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8584a-152">-Vpnclientıpsecpolicy</span><span class="sxs-lookup"><span data-stu-id="8584a-152">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="8584a-153">VpnServerConfiguration için IPSec ilkelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="8584a-153">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8584a-154">-Vpnclientgeri</span><span class="sxs-lookup"><span data-stu-id="8584a-154">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="8584a-155">Dosyaların yollarını iptal edilecek VpnClientCertificates listesi</span><span class="sxs-lookup"><span data-stu-id="8584a-155">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8584a-156">-Vpnclientrootcertificatefileslistesi</span><span class="sxs-lookup"><span data-stu-id="8584a-156">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="8584a-157">Dosya yollarının ekleneceği VpnClientRootCertificates listesi</span><span class="sxs-lookup"><span data-stu-id="8584a-157">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8584a-158">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="8584a-158">-VpnProtocol</span></span>
<span data-ttu-id="8584a-159">P2S VPN istemci tünel protokollerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="8584a-159">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8584a-160">-Onay</span><span class="sxs-lookup"><span data-stu-id="8584a-160">-Confirm</span></span>
<span data-ttu-id="8584a-161">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8584a-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8584a-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8584a-162">-WhatIf</span></span>
<span data-ttu-id="8584a-163">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8584a-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8584a-164">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8584a-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8584a-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8584a-165">CommonParameters</span></span>
<span data-ttu-id="8584a-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8584a-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8584a-167">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8584a-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8584a-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8584a-168">INPUTS</span></span>

### <span data-ttu-id="8584a-169">Microsoft. Azure. Commands. Network. model. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="8584a-169">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="8584a-170">System. String Microsoft. Azure. Commands. Network. modeller. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="8584a-170">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="8584a-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8584a-171">OUTPUTS</span></span>

### <span data-ttu-id="8584a-172">Microsoft. Azure. Commands. Network. model. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="8584a-172">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="8584a-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8584a-173">NOTES</span></span>

## <span data-ttu-id="8584a-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8584a-174">RELATED LINKS</span></span>
