---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: 11b18f0a0f12a82e88694fd91ce89956951a4eb6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278522"
---
# <span data-ttu-id="6c1a6-101">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c1a6-101">New-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="6c1a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c1a6-102">SYNOPSIS</span></span>
<span data-ttu-id="6c1a6-103">Bu komut, kullanıcıların VPN ağ geçidinde önceden yapılandırılmış VPN ayarları temelinde, örneğin bazı kök sertifikaları için kullanıcıların yapılandırması gerekebilecek bazı ek ayarlara ek olarak VPN profili paketini oluşturmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="6c1a6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6c1a6-104">SYNTAX</span></span>

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c1a6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6c1a6-105">DESCRIPTION</span></span>
<span data-ttu-id="6c1a6-106">Bu, kullanıcıların VPN ağ geçidinde önceden yapılandırılmış VPN ayarları temelinde, örneğin bazı kök sertifikaları için kullanıcıların yapılandırması gerekebilecek bazı ek ayarlara ek olarak VPN profili paketini oluşturmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="6c1a6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6c1a6-107">EXAMPLES</span></span>

### <span data-ttu-id="6c1a6-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6c1a6-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="6c1a6-109">Bu cmdlet, "ContosoResourceGroup" tablosunda "ContosoVirtualNetworkGateway" için bir VPN istemci profili ZIP dosyası oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="6c1a6-110">Profil, VpnProfileRadiusCert sertifika dosyasıyla "EAPTLS" kimlik doğrulama yöntemini kullanacak şekilde yapılandırılmış önceden yapılandırılmış bir RADIUS sunucusu için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="6c1a6-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6c1a6-111">PARAMETERS</span></span>

### <span data-ttu-id="6c1a6-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="6c1a6-112">-AuthenticationMethod</span></span>
<span data-ttu-id="6c1a6-113">Kimlik doğrulama yöntemi EAPMSCHAPv2 veya EAPTLS değerlerini alabilir.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="6c1a6-114">EAPMSCHAPv2 belirtildiğinde cmdlet, EAP-MSCHAPv2 kimlik doğrulama protokolünü kullanan Kullanıcı adı/parola kimlik doğrulaması için bir istemci yapılandırması yükleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="6c1a6-115">EAPTLS belirtilmişse cmdlet, EAP-TLS protokolünü kullanan sertifika kimlik doğrulaması için bir istemci yapılandırması yükleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="6c1a6-116">"EapTls" seçeneği, hem RADIUS tabanlı sertifika kimlik doğrulaması hem de sanal ağ geçidi tarafından gerçekleştirilen sertifika kimlik doğrulaması için, güvenilen kök yükleyerek kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="6c1a6-117">Cmdlet, nelerin yapılandırıldığını otomatik olarak algılar.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-117">The cmdlet automatically detects what is configured.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c1a6-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="6c1a6-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="6c1a6-119">İstemci kök sertifikası yollarının listesi</span><span class="sxs-lookup"><span data-stu-id="6c1a6-119">A list of client root certificate paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c1a6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c1a6-120">-DefaultProfile</span></span>
<span data-ttu-id="6c1a6-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c1a6-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="6c1a6-122">-Name</span></span>
<span data-ttu-id="6c1a6-123">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c1a6-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="6c1a6-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="6c1a6-125">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="6c1a6-125">ProcessorArchitecture</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c1a6-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="6c1a6-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="6c1a6-127">RADIUS sunucusu kök sertifikası yolu.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-127">Radius server root certificate path.</span></span> <span data-ttu-id="6c1a6-128">Bu, RADIUS kimlik doğrulaması kullanılan EAP-TLS kullanıldığında belirtilmesi gereken zorunlu bir parametredir.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="6c1a6-129">Bu, istemcinin kimlik doğrulama sırasında RADIUS sunucusunu doğrulamak için kullandığı RADIUS kök sertifikasını içeren tam yol adıdır.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c1a6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c1a6-130">-ResourceGroupName</span></span>
<span data-ttu-id="6c1a6-131">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c1a6-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="6c1a6-132">-Confirm</span></span>
<span data-ttu-id="6c1a6-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c1a6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c1a6-134">-WhatIf</span></span>
<span data-ttu-id="6c1a6-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c1a6-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c1a6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c1a6-137">CommonParameters</span></span>
<span data-ttu-id="6c1a6-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c1a6-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c1a6-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c1a6-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6c1a6-140">INPUTS</span></span>

### <span data-ttu-id="6c1a6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6c1a6-141">System.String</span></span>

### <span data-ttu-id="6c1a6-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="6c1a6-142">System.String[]</span></span>

## <span data-ttu-id="6c1a6-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6c1a6-143">OUTPUTS</span></span>

### <span data-ttu-id="6c1a6-144">Microsoft. Azure. Commands. Network. model. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="6c1a6-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="6c1a6-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6c1a6-145">NOTES</span></span>

## <span data-ttu-id="6c1a6-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6c1a6-146">RELATED LINKS</span></span>

[<span data-ttu-id="6c1a6-147">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c1a6-147">Get-AzVpnClientConfiguration</span></span>](./Get-AzVpnClientConfiguration.md)
