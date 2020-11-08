---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: 10feda31a97582ef56300b570ce2768c3ea0e277
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274800"
---
# <span data-ttu-id="02829-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="02829-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="02829-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02829-102">SYNOPSIS</span></span>
<span data-ttu-id="02829-103">Site bağlantısı noktası için yeni bir VpnServerConfiguration oluşturun.</span><span class="sxs-lookup"><span data-stu-id="02829-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="02829-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02829-104">SYNTAX</span></span>

### <span data-ttu-id="02829-105">ByVpnServerConfigurationNameByCertificateAuthentication (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="02829-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02829-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="02829-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02829-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="02829-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>]
 [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02829-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="02829-108">DESCRIPTION</span></span>
<span data-ttu-id="02829-109">**New-AzVpnServerConfiguration** cmdlet 'ı farklı Vpnprotocols, VpnAuthenticationTypes, ıpsecpolicies ile yeni bir Vpnserveryapılandırması oluşturmanıza ve Seçilen VPN kimlik doğrulaması türüyle ilgili parametrelerin, site bağlantısının üzerine gelmek için müşterinin gereksinimlerine göre ayarlanmasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="02829-109">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="02829-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02829-110">EXAMPLES</span></span>

### <span data-ttu-id="02829-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="02829-111">Example 1</span></span>
```powershell
PS C:\> $VpnServerConfigCertFilePath = Join-Path -Path $basedir -ChildPath "\ScenarioTests\Data\ApplicationGatewayAuthCert.cer"
PS C:\> $listOfCerts = New-Object "System.Collections.Generic.List[String]"
PS C:\> $listOfCerts.Add($VpnServerConfigCertFilePath)
PS C:\> New-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2 -VpnAuthenticationType Certificate -VpnClientRootCertificateFilesList $listOfCerts -VpnClientRevokedCertificateFilesList $listOfCerts -Location "westus"
ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2, OpenVPN}
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

<span data-ttu-id="02829-112">Yukarıdaki komut, VpnAuthenticationType ile Certificate olarak yeni bir VpnServerConfiguration oluşturur.</span><span class="sxs-lookup"><span data-stu-id="02829-112">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

### <span data-ttu-id="02829-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="02829-113">Example 2</span></span>

<span data-ttu-id="02829-114">Site bağlantısı noktası için yeni bir VpnServerConfiguration oluşturun.</span><span class="sxs-lookup"><span data-stu-id="02829-114">Create a new VpnServerConfiguration for point to site connectivity.</span></span> <span data-ttu-id="02829-115">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="02829-115">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnServerConfiguration -AadAudience <String> -AadIssuer <String> -AadTenant <String> -Location 'westus' -Name 'test1config' -ResourceGroupName 'P2SCortexGATesting' -VpnAuthenticationType Certificate -VpnProtocol IkeV2
```

## <span data-ttu-id="02829-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02829-116">PARAMETERS</span></span>

### <span data-ttu-id="02829-117">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="02829-117">-AadAudience</span></span>
<span data-ttu-id="02829-118">P2S AAD kimlik doğrulaması için AAD izleyiciyi.</span><span class="sxs-lookup"><span data-stu-id="02829-118">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02829-119">-Aadıssuer</span><span class="sxs-lookup"><span data-stu-id="02829-119">-AadIssuer</span></span>
<span data-ttu-id="02829-120">P2S AAD kimlik doğrulaması için AAD vericisi.</span><span class="sxs-lookup"><span data-stu-id="02829-120">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02829-121">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="02829-121">-AadTenant</span></span>
<span data-ttu-id="02829-122">P2S AAD kimlik doğrulaması için AAD kiracısı.</span><span class="sxs-lookup"><span data-stu-id="02829-122">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02829-123">-Iş</span><span class="sxs-lookup"><span data-stu-id="02829-123">-AsJob</span></span>
<span data-ttu-id="02829-124">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="02829-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02829-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02829-125">-DefaultProfile</span></span>
<span data-ttu-id="02829-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="02829-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02829-127">-Konum</span><span class="sxs-lookup"><span data-stu-id="02829-127">-Location</span></span>
<span data-ttu-id="02829-128">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="02829-128">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02829-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="02829-129">-Name</span></span>
<span data-ttu-id="02829-130">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="02829-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02829-131">-Radiusclientrootcertificatefileslistesi</span><span class="sxs-lookup"><span data-stu-id="02829-131">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="02829-132">RadiusClientRootCertificate dosyalarının yollarının listesi</span><span class="sxs-lookup"><span data-stu-id="02829-132">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02829-133">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="02829-133">-RadiusServerAddress</span></span>
<span data-ttu-id="02829-134">P2S dış RADIUS sunucusu adresi.</span><span class="sxs-lookup"><span data-stu-id="02829-134">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02829-135">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="02829-135">-RadiusServerList</span></span>
<span data-ttu-id="02829-136">Dış çoklu RADIUS sunucularını P2S.</span><span class="sxs-lookup"><span data-stu-id="02829-136">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02829-137">-Radiusserverrootcertificatefileslistesi</span><span class="sxs-lookup"><span data-stu-id="02829-137">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="02829-138">RadiusClientRootCertificate dosyalarının yollarının listesi</span><span class="sxs-lookup"><span data-stu-id="02829-138">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02829-139">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="02829-139">-RadiusServerSecret</span></span>
<span data-ttu-id="02829-140">Dış RADIUS sunucusu gizliliğini P2S.</span><span class="sxs-lookup"><span data-stu-id="02829-140">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02829-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02829-141">-ResourceGroupName</span></span>
<span data-ttu-id="02829-142">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="02829-142">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02829-143">Etiketli</span><span class="sxs-lookup"><span data-stu-id="02829-143">-Tag</span></span>
<span data-ttu-id="02829-144">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="02829-144">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="02829-145">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="02829-145">-VpnAuthenticationType</span></span>
<span data-ttu-id="02829-146">P2S VPN istemci tünel protokollerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="02829-146">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="02829-147">-Vpnclientıpsecpolicy</span><span class="sxs-lookup"><span data-stu-id="02829-147">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="02829-148">VpnServerConfiguration için IPSec ilkelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="02829-148">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02829-149">-Vpnclientgeri</span><span class="sxs-lookup"><span data-stu-id="02829-149">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="02829-150">Dosyaların yollarını iptal edilecek VpnClientCertificates listesi</span><span class="sxs-lookup"><span data-stu-id="02829-150">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02829-151">-Vpnclientrootcertificatefileslistesi</span><span class="sxs-lookup"><span data-stu-id="02829-151">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="02829-152">Dosya yollarının ekleneceği VpnClientRootCertificates listesi</span><span class="sxs-lookup"><span data-stu-id="02829-152">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02829-153">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="02829-153">-VpnProtocol</span></span>
<span data-ttu-id="02829-154">P2S VPN istemci tünel protokollerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="02829-154">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="02829-155">-Onay</span><span class="sxs-lookup"><span data-stu-id="02829-155">-Confirm</span></span>
<span data-ttu-id="02829-156">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="02829-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02829-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02829-157">-WhatIf</span></span>
<span data-ttu-id="02829-158">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="02829-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02829-159">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="02829-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02829-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02829-160">CommonParameters</span></span>
<span data-ttu-id="02829-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02829-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02829-162">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="02829-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02829-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02829-163">INPUTS</span></span>

### <span data-ttu-id="02829-164">Microsoft. Azure. Commands. Network. model. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="02829-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="02829-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02829-165">OUTPUTS</span></span>

### <span data-ttu-id="02829-166">Microsoft. Azure. Commands. Network. model. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="02829-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="02829-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02829-167">NOTES</span></span>

## <span data-ttu-id="02829-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02829-168">RELATED LINKS</span></span>
