---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: 14f43ab66800969eb46554de898525ce8d687f5b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098689"
---
# <span data-ttu-id="e564b-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="e564b-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="e564b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e564b-102">SYNOPSIS</span></span>
<span data-ttu-id="e564b-103">Var olan bir Vpnserveryapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e564b-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="e564b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e564b-104">SYNTAX</span></span>

### <span data-ttu-id="e564b-105">ByVpnServerConfigurationNameByCertificateAuthentication (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e564b-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e564b-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="e564b-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e564b-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="e564b-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e564b-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="e564b-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e564b-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="e564b-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e564b-110">ByVpnServerConfigurationObjectByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="e564b-110">ByVpnServerConfigurationObjectByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e564b-111">Byvpnserverconfigurationresourceıdbycertificateauthentication</span><span class="sxs-lookup"><span data-stu-id="e564b-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e564b-112">Byvpnserverconfigurationresourceıdbyradiusauthentication</span><span class="sxs-lookup"><span data-stu-id="e564b-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e564b-113">Byvpnserverconfigurationresourceıdbyaadauthentication</span><span class="sxs-lookup"><span data-stu-id="e564b-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e564b-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="e564b-114">DESCRIPTION</span></span>
<span data-ttu-id="e564b-115">**Update-AzVpnServerConfiguration** cmdlet 'i, var olan vpnserverconfiguration 'ı farklı Vpnprotocols, VpnAuthenticationTypes, ıpsecpolicies ile güncelleştirmenize ve Seçilen VPN kimlik doğrulama türüyle ilgili parametrelerin, müşterinin site bağlantısı için gerekme gereksinimlerine göre ayarlanmasını olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="e564b-115">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="e564b-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e564b-116">EXAMPLES</span></span>

### <span data-ttu-id="e564b-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e564b-117">Example 1</span></span>
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

<span data-ttu-id="e564b-118">Yukarıdaki komut, VpnProtocol ile mevcut bir Vpnserveryapılandırmasını Ikev2 olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e564b-118">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="e564b-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e564b-119">PARAMETERS</span></span>

### <span data-ttu-id="e564b-120">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="e564b-120">-AadAudience</span></span>
<span data-ttu-id="e564b-121">P2S AAD kimlik doğrulaması için AAD izleyiciyi.</span><span class="sxs-lookup"><span data-stu-id="e564b-121">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e564b-122">-Aadıssuer</span><span class="sxs-lookup"><span data-stu-id="e564b-122">-AadIssuer</span></span>
<span data-ttu-id="e564b-123">P2S AAD kimlik doğrulaması için AAD vericisi.</span><span class="sxs-lookup"><span data-stu-id="e564b-123">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e564b-124">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="e564b-124">-AadTenant</span></span>
<span data-ttu-id="e564b-125">P2S AAD kimlik doğrulaması için AAD kiracısı.</span><span class="sxs-lookup"><span data-stu-id="e564b-125">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e564b-126">-Iş</span><span class="sxs-lookup"><span data-stu-id="e564b-126">-AsJob</span></span>
<span data-ttu-id="e564b-127">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e564b-127">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e564b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e564b-128">-DefaultProfile</span></span>
<span data-ttu-id="e564b-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e564b-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e564b-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e564b-130">-InputObject</span></span>
<span data-ttu-id="e564b-131">Değiştirilecek VPN sunucusu yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="e564b-131">The vpn server configuration object to be modified</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationObjectByAadAuthentication
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e564b-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="e564b-132">-Name</span></span>
<span data-ttu-id="e564b-133">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="e564b-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e564b-134">-Radiusclientrootcertificatefileslistesi</span><span class="sxs-lookup"><span data-stu-id="e564b-134">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="e564b-135">RadiusClientRootCertificate dosyalarının yollarının listesi</span><span class="sxs-lookup"><span data-stu-id="e564b-135">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e564b-136">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="e564b-136">-RadiusServerAddress</span></span>
<span data-ttu-id="e564b-137">P2S dış RADIUS sunucusu adresi.</span><span class="sxs-lookup"><span data-stu-id="e564b-137">P2S External Radius server address.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e564b-138">-Radiusserverrootcertificatefileslistesi</span><span class="sxs-lookup"><span data-stu-id="e564b-138">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="e564b-139">RadiusClientRootCertificate dosyalarının yollarının listesi</span><span class="sxs-lookup"><span data-stu-id="e564b-139">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e564b-140">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="e564b-140">-RadiusServerSecret</span></span>
<span data-ttu-id="e564b-141">Dış RADIUS sunucusu gizliliğini P2S.</span><span class="sxs-lookup"><span data-stu-id="e564b-141">P2S External Radius server secret.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e564b-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e564b-142">-ResourceGroupName</span></span>
<span data-ttu-id="e564b-143">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e564b-143">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e564b-144">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e564b-144">-ResourceId</span></span>
<span data-ttu-id="e564b-145">VPN sunucusu yapılandırması için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="e564b-145">The Azure resource ID for the vpn server configuration.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationResourceIdByCertificateAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e564b-146">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e564b-146">-Tag</span></span>
<span data-ttu-id="e564b-147">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="e564b-147">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e564b-148">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="e564b-148">-VpnAuthenticationType</span></span>
<span data-ttu-id="e564b-149">P2S VPN istemci tünel protokollerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="e564b-149">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Certificate, Radius, AAD

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e564b-150">-Vpnclientıpsecpolicy</span><span class="sxs-lookup"><span data-stu-id="e564b-150">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="e564b-151">VpnServerConfiguration için IPSec ilkelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="e564b-151">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e564b-152">-Vpnclientgeri</span><span class="sxs-lookup"><span data-stu-id="e564b-152">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="e564b-153">Dosyaların yollarını iptal edilecek VpnClientCertificates listesi</span><span class="sxs-lookup"><span data-stu-id="e564b-153">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e564b-154">-Vpnclientrootcertificatefileslistesi</span><span class="sxs-lookup"><span data-stu-id="e564b-154">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="e564b-155">Dosya yollarının ekleneceği VpnClientRootCertificates listesi</span><span class="sxs-lookup"><span data-stu-id="e564b-155">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e564b-156">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="e564b-156">-VpnProtocol</span></span>
<span data-ttu-id="e564b-157">P2S VPN istemci tünel protokollerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="e564b-157">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e564b-158">-Onay</span><span class="sxs-lookup"><span data-stu-id="e564b-158">-Confirm</span></span>
<span data-ttu-id="e564b-159">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e564b-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e564b-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e564b-160">-WhatIf</span></span>
<span data-ttu-id="e564b-161">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e564b-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e564b-162">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e564b-162">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e564b-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e564b-163">CommonParameters</span></span>
<span data-ttu-id="e564b-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e564b-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e564b-165">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e564b-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e564b-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e564b-166">INPUTS</span></span>

### <span data-ttu-id="e564b-167">Microsoft. Azure. Commands. Network. model. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="e564b-167">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="e564b-168">System. String Microsoft. Azure. Commands. Network. modeller. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="e564b-168">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="e564b-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e564b-169">OUTPUTS</span></span>

### <span data-ttu-id="e564b-170">Microsoft. Azure. Commands. Network. model. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="e564b-170">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="e564b-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e564b-171">NOTES</span></span>

## <span data-ttu-id="e564b-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e564b-172">RELATED LINKS</span></span>
