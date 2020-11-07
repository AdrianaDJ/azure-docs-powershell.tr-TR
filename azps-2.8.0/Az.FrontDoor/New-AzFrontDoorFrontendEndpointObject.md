---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: 3684c7d0cf28c0814178ea234f9368d138fc78d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751902"
---
# <span data-ttu-id="d26e5-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="d26e5-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="d26e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d26e5-102">SYNOPSIS</span></span>
<span data-ttu-id="d26e5-103">Ön kapı oluşturmak için Psfrontendenvseçpoint nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="d26e5-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="d26e5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d26e5-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-ProtocolType <String>]
 [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>] [-CertificateType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d26e5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d26e5-105">DESCRIPTION</span></span>
<span data-ttu-id="d26e5-106">Ön kapı oluşturmak için Psfrontendenvseçpoint nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="d26e5-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="d26e5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d26e5-107">EXAMPLES</span></span>

### <span data-ttu-id="d26e5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d26e5-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName $hostName


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

<span data-ttu-id="d26e5-109">Ön kapı oluşturmak için Psfrontendenvseçpoint nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="d26e5-109">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="d26e5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d26e5-110">PARAMETERS</span></span>

### <span data-ttu-id="d26e5-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="d26e5-111">-CertificateSource</span></span>
<span data-ttu-id="d26e5-112">SSL sertifikasının kaynağı</span><span class="sxs-lookup"><span data-stu-id="d26e5-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="d26e5-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="d26e5-113">-CertificateType</span></span>
<span data-ttu-id="d26e5-114">bir Frontendenvseçma güvenli bağlantılarında kullanılan sertifika türü</span><span class="sxs-lookup"><span data-stu-id="d26e5-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="d26e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d26e5-115">-DefaultProfile</span></span>
<span data-ttu-id="d26e5-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d26e5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d26e5-117">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="d26e5-117">-HostName</span></span>
<span data-ttu-id="d26e5-118">Frontendenvseçpunto ana bilgisayar adı.</span><span class="sxs-lookup"><span data-stu-id="d26e5-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="d26e5-119">Bir etki alanı adı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d26e5-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="d26e5-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="d26e5-120">-Name</span></span>
<span data-ttu-id="d26e5-121">Ön uç uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="d26e5-121">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="d26e5-122">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="d26e5-122">-ProtocolType</span></span>
<span data-ttu-id="d26e5-123">Güvenli teslim için kullanılan TLS uzantısı Protokolü</span><span class="sxs-lookup"><span data-stu-id="d26e5-123">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="d26e5-124">-SecretName</span><span class="sxs-lookup"><span data-stu-id="d26e5-124">-SecretName</span></span>
<span data-ttu-id="d26e5-125">Tam sertifika PFX 'yi temsil eden Anahtar Kasası parolasının adı</span><span class="sxs-lookup"><span data-stu-id="d26e5-125">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="d26e5-126">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="d26e5-126">-SecretVersion</span></span>
<span data-ttu-id="d26e5-127">Tam sertifika PFX 'yi temsil eden Anahtar Kasası parolasının sürümü</span><span class="sxs-lookup"><span data-stu-id="d26e5-127">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="d26e5-128">-Sessionbenzeşeyenil durumu</span><span class="sxs-lookup"><span data-stu-id="d26e5-128">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="d26e5-129">Bu konakta oturum benzeşimi izni verip vermeyeceği.</span><span class="sxs-lookup"><span data-stu-id="d26e5-129">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="d26e5-130">Varsayılan değer devre dışı</span><span class="sxs-lookup"><span data-stu-id="d26e5-130">Default value is Disabled</span></span>

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

### <span data-ttu-id="d26e5-131">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="d26e5-131">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="d26e5-132">Varsa, oturum benzeşimi için saniye cinsinden kullanılacak TTL.</span><span class="sxs-lookup"><span data-stu-id="d26e5-132">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="d26e5-133">Varsayılan değer 0 ' dır</span><span class="sxs-lookup"><span data-stu-id="d26e5-133">Default value is 0</span></span>

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

### <span data-ttu-id="d26e5-134">-Kasa</span><span class="sxs-lookup"><span data-stu-id="d26e5-134">-Vault</span></span>
<span data-ttu-id="d26e5-135">SSL sertifikasını içeren Anahtar Kasası</span><span class="sxs-lookup"><span data-stu-id="d26e5-135">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="d26e5-136">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="d26e5-136">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="d26e5-137">Her ana bilgisayar için Web uygulaması güvenlik duvarı ilkesinin kaynak kimliği (uygulanabilirse)</span><span class="sxs-lookup"><span data-stu-id="d26e5-137">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="d26e5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d26e5-138">CommonParameters</span></span>
<span data-ttu-id="d26e5-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d26e5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d26e5-140">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d26e5-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d26e5-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d26e5-141">INPUTS</span></span>

### <span data-ttu-id="d26e5-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d26e5-142">None</span></span>

## <span data-ttu-id="d26e5-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d26e5-143">OUTPUTS</span></span>

### <span data-ttu-id="d26e5-144">Microsoft. Azure. Commands. Frontkapısı. modeller. Psfrontendenvseçpoint</span><span class="sxs-lookup"><span data-stu-id="d26e5-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="d26e5-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d26e5-145">NOTES</span></span>

## <span data-ttu-id="d26e5-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d26e5-146">RELATED LINKS</span></span>

<span data-ttu-id="d26e5-147">[Yeni-azön kapı](./New-AzFrontDoor.md) 
 [Set-Azfrontkapısı](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="d26e5-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
