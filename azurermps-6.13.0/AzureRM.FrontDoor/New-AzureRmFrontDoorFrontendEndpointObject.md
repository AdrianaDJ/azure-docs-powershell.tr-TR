---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: 638617cfe55e01121b46c7fe283d3664948e76b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572757"
---
# <span data-ttu-id="92b1b-101">New-AzureRmFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="92b1b-101">New-AzureRmFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="92b1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="92b1b-103">Ön kapı oluşturmak için Psfrontendenvseçpoint nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="92b1b-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92b1b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="92b1b-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <PSCertificateSource>]
 [-ProtocolType <PSProtocolType>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <PSCertificateType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92b1b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="92b1b-105">DESCRIPTION</span></span>
<span data-ttu-id="92b1b-106">Ön kapı oluşturmak için Psfrontendenvseçpoint nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="92b1b-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="92b1b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="92b1b-107">EXAMPLES</span></span>

### <span data-ttu-id="92b1b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="92b1b-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName $hostName


HostName                         : frontdoor5.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     :
CustomHttpsProvisioningSubstate  :
CertificateSource                : AzureKeyVault
ProtocolType                     : ServerNameIndication
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  : Shared
ResourceState                    :
Id                               :
Name                             : frontendendpoint1
Type                             :
```

<span data-ttu-id="92b1b-109">Ön kapı oluşturmak için Psfrontendenvseçpoint nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="92b1b-109">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="92b1b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="92b1b-110">PARAMETERS</span></span>

### <span data-ttu-id="92b1b-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="92b1b-111">-CertificateSource</span></span>
<span data-ttu-id="92b1b-112">SSL sertifikasının kaynağı</span><span class="sxs-lookup"><span data-stu-id="92b1b-112">The source of the SSL certificate</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCertificateSource
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, FrontDoor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b1b-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="92b1b-113">-CertificateType</span></span>
<span data-ttu-id="92b1b-114">bir Frontendenvseçma güvenli bağlantılarında kullanılan sertifika türü</span><span class="sxs-lookup"><span data-stu-id="92b1b-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCertificateType
Parameter Sets: (All)
Aliases:
Accepted values: Shared, Dedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92b1b-115">-DefaultProfile</span></span>
<span data-ttu-id="92b1b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="92b1b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b1b-117">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="92b1b-117">-HostName</span></span>
<span data-ttu-id="92b1b-118">Frontendenvseçpunto ana bilgisayar adı.</span><span class="sxs-lookup"><span data-stu-id="92b1b-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="92b1b-119">Bir etki alanı adı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="92b1b-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="92b1b-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="92b1b-120">-Name</span></span>
<span data-ttu-id="92b1b-121">Ön uç uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="92b1b-121">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="92b1b-122">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="92b1b-122">-ProtocolType</span></span>
<span data-ttu-id="92b1b-123">Güvenli teslim için kullanılan TLS uzantısı Protokolü</span><span class="sxs-lookup"><span data-stu-id="92b1b-123">The TLS extension protocol that is used for secure delivery</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocolType
Parameter Sets: (All)
Aliases:
Accepted values: ServerNameIndication, IPBased

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b1b-124">-SecretName</span><span class="sxs-lookup"><span data-stu-id="92b1b-124">-SecretName</span></span>
<span data-ttu-id="92b1b-125">Tam sertifika PFX 'yi temsil eden Anahtar Kasası parolasının adı</span><span class="sxs-lookup"><span data-stu-id="92b1b-125">The name of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b1b-126">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="92b1b-126">-SecretVersion</span></span>
<span data-ttu-id="92b1b-127">Tam sertifika PFX 'yi temsil eden Anahtar Kasası parolasının sürümü</span><span class="sxs-lookup"><span data-stu-id="92b1b-127">The version of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b1b-128">-Sessionbenzeşeyenil durumu</span><span class="sxs-lookup"><span data-stu-id="92b1b-128">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="92b1b-129">Bu konakta oturum benzeşimi izni verip vermeyeceği.</span><span class="sxs-lookup"><span data-stu-id="92b1b-129">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="92b1b-130">Varsayılan değer devre dışı</span><span class="sxs-lookup"><span data-stu-id="92b1b-130">Default value is Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b1b-131">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="92b1b-131">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="92b1b-132">Varsa, oturum benzeşimi için saniye cinsinden kullanılacak TTL.</span><span class="sxs-lookup"><span data-stu-id="92b1b-132">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="92b1b-133">Varsayılan değer 0 ' dır</span><span class="sxs-lookup"><span data-stu-id="92b1b-133">Default value is 0</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b1b-134">-Kasa</span><span class="sxs-lookup"><span data-stu-id="92b1b-134">-Vault</span></span>
<span data-ttu-id="92b1b-135">SSL sertifikasını içeren Anahtar Kasası</span><span class="sxs-lookup"><span data-stu-id="92b1b-135">The Key Vault containing the SSL certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b1b-136">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="92b1b-136">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="92b1b-137">Her ana bilgisayar için Web uygulaması güvenlik duvarı ilkesinin kaynak kimliği (uygulanabilirse)</span><span class="sxs-lookup"><span data-stu-id="92b1b-137">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b1b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92b1b-138">CommonParameters</span></span>
<span data-ttu-id="92b1b-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="92b1b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92b1b-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92b1b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92b1b-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="92b1b-141">INPUTS</span></span>

### <span data-ttu-id="92b1b-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="92b1b-142">None</span></span>

## <span data-ttu-id="92b1b-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="92b1b-143">OUTPUTS</span></span>

### <span data-ttu-id="92b1b-144">Microsoft. Azure. Commands. Frontkapısı. modeller. Psfrontendenvseçpoint</span><span class="sxs-lookup"><span data-stu-id="92b1b-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="92b1b-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="92b1b-145">NOTES</span></span>

## <span data-ttu-id="92b1b-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="92b1b-146">RELATED LINKS</span></span>

<span data-ttu-id="92b1b-147">[Yeni-Azurermfrontkapısı](./New-AzureRmFrontDoor.md) 
 [Set-Azurermfrontkapısı](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="92b1b-147">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
