---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: efb32f3fa73fac50e5f96100ed895c2ca7d4a83e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274947"
---
# <span data-ttu-id="d2255-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="d2255-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="d2255-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2255-102">SYNOPSIS</span></span>
<span data-ttu-id="d2255-103">Ön kapı oluşturmak için Psfrontendenvseçpoint nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="d2255-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="d2255-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2255-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-MinimumTlsVersion <String>]
 [-ProtocolType <String>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2255-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2255-105">DESCRIPTION</span></span>
<span data-ttu-id="d2255-106">Ön kapı oluşturmak için Psfrontendenvseçpoint nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="d2255-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="d2255-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2255-107">EXAMPLES</span></span>

### <span data-ttu-id="d2255-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d2255-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName "frontendendpoint1"


HostName                         : frontendendpoint1
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     :
CustomHttpsProvisioningSubstate  :
CertificateSource                :
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    :
Id                               :
Name                             : frontendendpoint1
Type                             :
ProtocolType                     : ServerNameIndication
```

<span data-ttu-id="d2255-109">Ön kapı oluşturmak için Psfrontendenvseçpoint nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d2255-109">Create a PSFrontendEndpoint Object for Front Door creation.</span></span>

## <span data-ttu-id="d2255-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2255-110">PARAMETERS</span></span>

### <span data-ttu-id="d2255-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="d2255-111">-CertificateSource</span></span>
<span data-ttu-id="d2255-112">SSL sertifikasının kaynağı</span><span class="sxs-lookup"><span data-stu-id="d2255-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="d2255-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="d2255-113">-CertificateType</span></span>
<span data-ttu-id="d2255-114">bir Frontendenvseçma güvenli bağlantılarında kullanılan sertifika türü</span><span class="sxs-lookup"><span data-stu-id="d2255-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="d2255-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2255-115">-DefaultProfile</span></span>
<span data-ttu-id="d2255-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d2255-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2255-117">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="d2255-117">-HostName</span></span>
<span data-ttu-id="d2255-118">Frontendenvseçpunto ana bilgisayar adı.</span><span class="sxs-lookup"><span data-stu-id="d2255-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="d2255-119">Bir etki alanı adı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d2255-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="d2255-120">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="d2255-120">-MinimumTlsVersion</span></span>
<span data-ttu-id="d2255-121">Ön kapılı bir SSL el sıkışması oluşturmak için, istemcilerden gereken minimum TLS sürümü.</span><span class="sxs-lookup"><span data-stu-id="d2255-121">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="d2255-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="d2255-122">-Name</span></span>
<span data-ttu-id="d2255-123">Ön uç uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="d2255-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="d2255-124">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="d2255-124">-ProtocolType</span></span>
<span data-ttu-id="d2255-125">Güvenli teslim için kullanılan TLS uzantısı Protokolü</span><span class="sxs-lookup"><span data-stu-id="d2255-125">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="d2255-126">-SecretName</span><span class="sxs-lookup"><span data-stu-id="d2255-126">-SecretName</span></span>
<span data-ttu-id="d2255-127">Tam sertifika PFX 'yi temsil eden Anahtar Kasası parolasının adı</span><span class="sxs-lookup"><span data-stu-id="d2255-127">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="d2255-128">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="d2255-128">-SecretVersion</span></span>
<span data-ttu-id="d2255-129">Tam sertifika PFX 'yi temsil eden Anahtar Kasası parolasının sürümü</span><span class="sxs-lookup"><span data-stu-id="d2255-129">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="d2255-130">-Sessionbenzeşeyenil durumu</span><span class="sxs-lookup"><span data-stu-id="d2255-130">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="d2255-131">Bu konakta oturum benzeşimi izni verip vermeyeceği.</span><span class="sxs-lookup"><span data-stu-id="d2255-131">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="d2255-132">Varsayılan değer devre dışı</span><span class="sxs-lookup"><span data-stu-id="d2255-132">Default value is Disabled</span></span>

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

### <span data-ttu-id="d2255-133">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="d2255-133">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="d2255-134">Varsa, oturum benzeşimi için saniye cinsinden kullanılacak TTL.</span><span class="sxs-lookup"><span data-stu-id="d2255-134">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="d2255-135">Varsayılan değer 0 ' dır</span><span class="sxs-lookup"><span data-stu-id="d2255-135">Default value is 0</span></span>

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

### <span data-ttu-id="d2255-136">-Kasa</span><span class="sxs-lookup"><span data-stu-id="d2255-136">-Vault</span></span>
<span data-ttu-id="d2255-137">SSL sertifikasını içeren Anahtar Kasası</span><span class="sxs-lookup"><span data-stu-id="d2255-137">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="d2255-138">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="d2255-138">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="d2255-139">Her ana bilgisayar için Web uygulaması güvenlik duvarı ilkesinin kaynak kimliği (uygulanabilirse)</span><span class="sxs-lookup"><span data-stu-id="d2255-139">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="d2255-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2255-140">CommonParameters</span></span>
<span data-ttu-id="d2255-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2255-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2255-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d2255-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2255-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2255-143">INPUTS</span></span>

### <span data-ttu-id="d2255-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d2255-144">None</span></span>
## <span data-ttu-id="d2255-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2255-145">OUTPUTS</span></span>

### <span data-ttu-id="d2255-146">Microsoft. Azure. Commands. Frontkapısı. modeller. Psfrontendenvseçpoint</span><span class="sxs-lookup"><span data-stu-id="d2255-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="d2255-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2255-147">NOTES</span></span>

## <span data-ttu-id="d2255-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2255-148">RELATED LINKS</span></span>

<span data-ttu-id="d2255-149">[Yeni-azön kapı](./New-AzFrontDoor.md) 
 [Set-Azfrontkapısı](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="d2255-149">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
