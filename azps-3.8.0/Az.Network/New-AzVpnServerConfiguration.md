---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: de0806585cee16eed19291766ab29696a9a1b960
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938072"
---
# <span data-ttu-id="a7f0a-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7f0a-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="a7f0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f0a-103">Site bağlantısı noktası için yeni bir VpnServerConfiguration oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a7f0a-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="a7f0a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7f0a-104">SYNTAX</span></span>

### <span data-ttu-id="a7f0a-105">ByVpnServerConfigurationNameByCertificateAuthentication (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a7f0a-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7f0a-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="a7f0a-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7f0a-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="a7f0a-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>]
 [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7f0a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7f0a-108">DESCRIPTION</span></span>
<span data-ttu-id="a7f0a-109">**New-AzVpnServerConfiguration** cmdlet 'ı farklı Vpnprotocols, VpnAuthenticationTypes, ıpsecpolicies ile yeni bir Vpnserveryapılandırması oluşturmanıza ve Seçilen VPN kimlik doğrulaması türüyle ilgili parametrelerin, site bağlantısının üzerine gelmek için müşterinin gereksinimlerine göre ayarlanmasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="a7f0a-109">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="a7f0a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7f0a-110">EXAMPLES</span></span>

### <span data-ttu-id="a7f0a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a7f0a-111">Example 1</span></span>
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

<span data-ttu-id="a7f0a-112">Yukarıdaki komut, VpnAuthenticationType ile Certificate olarak yeni bir VpnServerConfiguration oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a7f0a-112">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

## <span data-ttu-id="a7f0a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7f0a-113">PARAMETERS</span></span>

### <span data-ttu-id="a7f0a-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="a7f0a-114">-AadAudience</span></span>
<span data-ttu-id="a7f0a-115">P2S AAD kimlik doğrulaması için AAD izleyiciyi.</span><span class="sxs-lookup"><span data-stu-id="a7f0a-115">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f0a-116">-Aadıssuer</span><span class="sxs-lookup"><span data-stu-id="a7f0a-116">-AadIssuer</span></span>
<span data-ttu-id="a7f0a-117">P2S AAD kimlik doğrulaması için AAD vericisi.</span><span class="sxs-lookup"><span data-stu-id="a7f0a-117">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f0a-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="a7f0a-118">-AadTenant</span></span>
<span data-ttu-id="a7f0a-119">P2S AAD kimlik doğrulaması için AAD kiracısı.</span><span class="sxs-lookup"><span data-stu-id="a7f0a-119">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f0a-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="a7f0a-120">-AsJob</span></span>
<span data-ttu-id="a7f0a-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a7f0a-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7f0a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f0a-122">-DefaultProfile</span></span>
<span data-ttu-id="a7f0a-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a7f0a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7f0a-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="a7f0a-124">-Location</span></span>
<span data-ttu-id="a7f0a-125">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="a7f0a-125">The resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f0a-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="a7f0a-126">-Name</span></span>
<span data-ttu-id="a7f0a-127">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="a7f0a-127">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f0a-128">-Radiusclientrootcertificatefileslistesi</span><span class="sxs-lookup"><span data-stu-id="a7f0a-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="a7f0a-129">RadiusClientRootCertificate dosyalarının yollarının listesi</span><span class="sxs-lookup"><span data-stu-id="a7f0a-129">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f0a-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="a7f0a-130">-RadiusServerAddress</span></span>
<span data-ttu-id="a7f0a-131">P2S dış RADIUS sunucusu adresi.</span><span class="sxs-lookup"><span data-stu-id="a7f0a-131">P2S External Radius server address.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f0a-132">-Radiusserverrootcertificatefileslistesi</span><span class="sxs-lookup"><span data-stu-id="a7f0a-132">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="a7f0a-133">RadiusClientRootCertificate dosyalarının yollarının listesi</span><span class="sxs-lookup"><span data-stu-id="a7f0a-133">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f0a-134">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="a7f0a-134">-RadiusServerSecret</span></span>
<span data-ttu-id="a7f0a-135">Dış RADIUS sunucusu gizliliğini P2S.</span><span class="sxs-lookup"><span data-stu-id="a7f0a-135">P2S External Radius server secret.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f0a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7f0a-136">-ResourceGroupName</span></span>
<span data-ttu-id="a7f0a-137">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a7f0a-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f0a-138">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a7f0a-138">-Tag</span></span>
<span data-ttu-id="a7f0a-139">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="a7f0a-139">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a7f0a-140">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="a7f0a-140">-VpnAuthenticationType</span></span>
<span data-ttu-id="a7f0a-141">P2S VPN istemci tünel protokollerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="a7f0a-141">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="a7f0a-142">-Vpnclientıpsecpolicy</span><span class="sxs-lookup"><span data-stu-id="a7f0a-142">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="a7f0a-143">VpnServerConfiguration için IPSec ilkelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="a7f0a-143">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7f0a-144">-Vpnclientgeri</span><span class="sxs-lookup"><span data-stu-id="a7f0a-144">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="a7f0a-145">Dosyaların yollarını iptal edilecek VpnClientCertificates listesi</span><span class="sxs-lookup"><span data-stu-id="a7f0a-145">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f0a-146">-Vpnclientrootcertificatefileslistesi</span><span class="sxs-lookup"><span data-stu-id="a7f0a-146">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="a7f0a-147">Dosya yollarının ekleneceği VpnClientRootCertificates listesi</span><span class="sxs-lookup"><span data-stu-id="a7f0a-147">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f0a-148">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="a7f0a-148">-VpnProtocol</span></span>
<span data-ttu-id="a7f0a-149">P2S VPN istemci tünel protokollerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="a7f0a-149">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="a7f0a-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="a7f0a-150">-Confirm</span></span>
<span data-ttu-id="a7f0a-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a7f0a-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7f0a-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7f0a-152">-WhatIf</span></span>
<span data-ttu-id="a7f0a-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a7f0a-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7f0a-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a7f0a-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7f0a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f0a-155">CommonParameters</span></span>
<span data-ttu-id="a7f0a-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7f0a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f0a-157">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7f0a-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f0a-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7f0a-158">INPUTS</span></span>

### <span data-ttu-id="a7f0a-159">Microsoft. Azure. Commands. Network. model. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="a7f0a-159">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="a7f0a-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7f0a-160">OUTPUTS</span></span>

### <span data-ttu-id="a7f0a-161">Microsoft. Azure. Commands. Network. model. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7f0a-161">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="a7f0a-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7f0a-162">NOTES</span></span>

## <span data-ttu-id="a7f0a-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7f0a-163">RELATED LINKS</span></span>
