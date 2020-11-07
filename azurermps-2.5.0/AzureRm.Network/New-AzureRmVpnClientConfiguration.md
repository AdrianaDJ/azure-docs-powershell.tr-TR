---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientconfiguration
schema: 2.0.0
ms.openlocfilehash: d49078e18b6082473c398c9f4aa7ac01f41909ca
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939700"
---
# <span data-ttu-id="4c10a-101">New-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c10a-101">New-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="4c10a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c10a-102">SYNOPSIS</span></span>
<span data-ttu-id="4c10a-103">Bu komut, kullanıcıların VPN ağ geçidinde önceden yapılandırılmış VPN ayarları temelinde, örneğin bazı kök sertifikaları için kullanıcıların yapılandırması gerekebilecek bazı ek ayarlara ek olarak VPN profili paketini oluşturmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="4c10a-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c10a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c10a-104">SYNTAX</span></span>

```
New-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-ProcessorArchitecture <String>] -AuthenticationMethod <String> [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c10a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c10a-105">DESCRIPTION</span></span>
<span data-ttu-id="4c10a-106">Bu, kullanıcıların VPN ağ geçidinde önceden yapılandırılmış VPN ayarları temelinde, örneğin bazı kök sertifikaları için kullanıcıların yapılandırması gerekebilecek bazı ek ayarlara ek olarak VPN profili paketini oluşturmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="4c10a-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="4c10a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c10a-107">EXAMPLES</span></span>

### <span data-ttu-id="4c10a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4c10a-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="4c10a-109">Bu cmdlet, "ContosoResourceGroup" tablosunda "ContosoVirtualNetworkGateway" için bir VPN istemci profili ZIP dosyası oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4c10a-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="4c10a-110">Profil, VpnProfileRadiusCert sertifika dosyasıyla "EAPTLS" kimlik doğrulama yöntemini kullanacak şekilde yapılandırılmış önceden yapılandırılmış bir RADIUS sunucusu için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4c10a-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="4c10a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c10a-111">PARAMETERS</span></span>

### <span data-ttu-id="4c10a-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="4c10a-112">-AuthenticationMethod</span></span>
<span data-ttu-id="4c10a-113">Kimlik doğrulama yöntemi EAPMSCHAPv2 veya EAPTLS değerlerini alabilir.</span><span class="sxs-lookup"><span data-stu-id="4c10a-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="4c10a-114">EAPMSCHAPv2 belirtildiğinde cmdlet, EAP-MSCHAPv2 kimlik doğrulama protokolünü kullanan Kullanıcı adı/parola kimlik doğrulaması için bir istemci yapılandırması yükleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4c10a-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="4c10a-115">EAPTLS belirtilmişse cmdlet, EAP-TLS protokolünü kullanan sertifika kimlik doğrulaması için bir istemci yapılandırması yükleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4c10a-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="4c10a-116">"EapTls" seçeneği, hem RADIUS tabanlı sertifika kimlik doğrulaması hem de sanal ağ geçidi tarafından gerçekleştirilen sertifika kimlik doğrulaması için, güvenilen kök yükleyerek kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4c10a-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="4c10a-117">Cmdlet, nelerin yapılandırıldığını otomatik olarak algılar.</span><span class="sxs-lookup"><span data-stu-id="4c10a-117">The cmdlet automatically detects what is configured.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: EAPTLS, EAPMSCHAPv2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c10a-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="4c10a-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="4c10a-119">İstemci kök sertifikası yollarının listesi</span><span class="sxs-lookup"><span data-stu-id="4c10a-119">A list of client root certificate paths</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c10a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c10a-120">-DefaultProfile</span></span>
<span data-ttu-id="4c10a-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4c10a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c10a-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="4c10a-122">-Name</span></span>
<span data-ttu-id="4c10a-123">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="4c10a-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c10a-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="4c10a-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="4c10a-125">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="4c10a-125">ProcessorArchitecture</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c10a-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="4c10a-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="4c10a-127">RADIUS sunucusu kök sertifikası yolu.</span><span class="sxs-lookup"><span data-stu-id="4c10a-127">Radius server root certificate path.</span></span> <span data-ttu-id="4c10a-128">Bu, RADIUS kimlik doğrulaması kullanılan EAP-TLS kullanıldığında belirtilmesi gereken zorunlu bir parametredir.</span><span class="sxs-lookup"><span data-stu-id="4c10a-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="4c10a-129">Bu, istemcinin kimlik doğrulama sırasında RADIUS sunucusunu doğrulamak için kullandığı RADIUS kök sertifikasını içeren tam yol adıdır.</span><span class="sxs-lookup"><span data-stu-id="4c10a-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c10a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c10a-130">-ResourceGroupName</span></span>
<span data-ttu-id="4c10a-131">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4c10a-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c10a-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="4c10a-132">-Confirm</span></span>
<span data-ttu-id="4c10a-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4c10a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c10a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c10a-134">-WhatIf</span></span>
<span data-ttu-id="4c10a-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c10a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c10a-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4c10a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c10a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c10a-137">CommonParameters</span></span>
<span data-ttu-id="4c10a-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c10a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c10a-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c10a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c10a-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c10a-140">INPUTS</span></span>

### <span data-ttu-id="4c10a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4c10a-141">System.String</span></span>
<span data-ttu-id="4c10a-142">System. Koleksiyonlar. Generic. LIST ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4c10a-142">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="4c10a-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c10a-143">OUTPUTS</span></span>

### <span data-ttu-id="4c10a-144">Microsoft. Azure. Commands. Network. model. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="4c10a-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="4c10a-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c10a-145">NOTES</span></span>

## <span data-ttu-id="4c10a-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c10a-146">RELATED LINKS</span></span>

