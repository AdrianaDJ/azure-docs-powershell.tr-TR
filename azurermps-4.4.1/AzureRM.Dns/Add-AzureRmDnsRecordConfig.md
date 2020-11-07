---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Add-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Add-AzureRmDnsRecordConfig.md
ms.openlocfilehash: 65ab77c7ad94224e3ab2c72072834c43ef1434a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764068"
---
# <span data-ttu-id="ce83a-101">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="ce83a-101">Add-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="ce83a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce83a-102">SYNOPSIS</span></span>
<span data-ttu-id="ce83a-103">Yerel kayıt kümesi nesnesine bir DNS kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="ce83a-103">Adds a DNS record to a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce83a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ce83a-104">SYNTAX</span></span>

### <span data-ttu-id="ce83a-105">Bir</span><span class="sxs-lookup"><span data-stu-id="ce83a-105">A</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce83a-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="ce83a-106">AAAA</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce83a-107">Seç</span><span class="sxs-lookup"><span data-stu-id="ce83a-107">NS</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce83a-108">DOSYASıNA</span><span class="sxs-lookup"><span data-stu-id="ce83a-108">MX</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce83a-109">PTR</span><span class="sxs-lookup"><span data-stu-id="ce83a-109">PTR</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce83a-110">,</span><span class="sxs-lookup"><span data-stu-id="ce83a-110">TXT</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ce83a-111">SRV</span><span class="sxs-lookup"><span data-stu-id="ce83a-111">SRV</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce83a-112">KAYDıNı</span><span class="sxs-lookup"><span data-stu-id="ce83a-112">CNAME</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce83a-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce83a-113">DESCRIPTION</span></span>
<span data-ttu-id="ce83a-114">**Add-AzureRmDnsRecordConfig** cmdlet 'ı bir etki alanı adı SISTEMI (DNS) kaydını bir **Recordset** nesnesine ekler.</span><span class="sxs-lookup"><span data-stu-id="ce83a-114">The **Add-AzureRmDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="ce83a-115">**Kayıt kümesi** nesnesi bir çevrimdışı nesnedir ve değişiklikleri MICROSOFT Azure DNS hizmeti 'nde kalıcı olarak sürdürmek için Set-AzureRmDnsRecordSet cmdlet 'i çalıştırana kadar DNS yanıtlarını değiştirmiyor.</span><span class="sxs-lookup"><span data-stu-id="ce83a-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="ce83a-116">SOA kayıtları bir DNS bölgesi oluşturulduğunda oluşturulur ve DNS bölgesi silindiğinde kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="ce83a-116">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="ce83a-117">SOA kayıtlarını ekleyip kaldıramazsınız, ancak bunları düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce83a-117">You cannot add or remove SOA records, but you can edit them.</span></span>

<span data-ttu-id="ce83a-118">**Recordset** nesnesini bu cmdlet 'e parametre olarak veya Pipeline işlecini kullanarak geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce83a-118">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="ce83a-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ce83a-119">EXAMPLES</span></span>

### <span data-ttu-id="ce83a-120">Örnek 1: kayıt kümesine kayıt ekleme</span><span class="sxs-lookup"><span data-stu-id="ce83a-120">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="ce83a-121">Bu örnek, var olan kayıt kümesine bir kayıt ekler.</span><span class="sxs-lookup"><span data-stu-id="ce83a-121">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="ce83a-122">Örnek 2: kayıt kümesine AAAA kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="ce83a-122">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="ce83a-123">Bu örnek, var olan kayıt kümesine bir AAAA kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="ce83a-123">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="ce83a-124">Örnek 3: kayıt kümesine CNAME kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="ce83a-124">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="ce83a-125">Bu örnek, var olan kayıt kümesine bir CNAME kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="ce83a-125">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="ce83a-126">CNAME kayıt kümesi en fazla bir kayıt içerebileceğinden, başlangıçta boş bir kayıt kümesi olmalıdır veya var olan kayıtların Remove-AzureRmDnsRecordConfig kullanılarak kaldırılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ce83a-126">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzureRmDnsRecordConfig.</span></span>

### <span data-ttu-id="ce83a-127">Örnek 4: kayıt kümesine bir MX kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="ce83a-127">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="ce83a-128">Bu örnek, varolan bir kayıt kümesine bir MX kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="ce83a-128">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="ce83a-129">"@" Kayıt adı, bölge Apex bir kayıt kümesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce83a-129">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="ce83a-130">Örnek 5: kayıt kümesine NS kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="ce83a-130">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="ce83a-131">Bu örnek, var olan kayıt kümesine bir NS kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="ce83a-131">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="ce83a-132">Örnek 6: kayıt kümesine PTR kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="ce83a-132">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="ce83a-133">Bu örnek, varolan bir kayıt kümesine bir PTR kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="ce83a-133">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="ce83a-134">Örnek 7: kayıt kümesine SRV kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="ce83a-134">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="ce83a-135">Bu örnek, var olan kayıt kümesine bir SRV kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="ce83a-135">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="ce83a-136">Örnek 8: kayıt kümesine TXT kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="ce83a-136">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Value "This is a TXT Record" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="ce83a-137">Bu örnek, var olan kayıt kümesine bir TXT kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="ce83a-137">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="ce83a-138">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ce83a-138">PARAMETERS</span></span>

### <span data-ttu-id="ce83a-139">-CNAME</span><span class="sxs-lookup"><span data-stu-id="ce83a-139">-Cname</span></span>
<span data-ttu-id="ce83a-140">Kurallı ad (CNAME) kaydı için etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce83a-140">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce83a-141">-Exchange</span><span class="sxs-lookup"><span data-stu-id="ce83a-141">-Exchange</span></span>
<span data-ttu-id="ce83a-142">Posta alışverişi (MX) kaydı için posta Exchange sunucusu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce83a-142">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce83a-143">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="ce83a-143">-Ipv4Address</span></span>
<span data-ttu-id="ce83a-144">Bir kaydın IPv4 adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce83a-144">Specifies an IPv4 address for an A record.</span></span>

```yaml
Type: System.String
Parameter Sets: A
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce83a-145">-IPv6Adresi</span><span class="sxs-lookup"><span data-stu-id="ce83a-145">-Ipv6Address</span></span>
<span data-ttu-id="ce83a-146">AAAA kaydı için IPv6 adresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce83a-146">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce83a-147">-Nsdadı</span><span class="sxs-lookup"><span data-stu-id="ce83a-147">-Nsdname</span></span>
<span data-ttu-id="ce83a-148">Ad sunucusu (NS) kaydı için ad sunucusu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce83a-148">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: System.String
Parameter Sets: NS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce83a-149">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="ce83a-149">-Port</span></span>
<span data-ttu-id="ce83a-150">Hizmet (SRV) kaydı için bağlantı noktası belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce83a-150">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce83a-151">-Tercih</span><span class="sxs-lookup"><span data-stu-id="ce83a-151">-Preference</span></span>
<span data-ttu-id="ce83a-152">Bir MX kaydı için tercih belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce83a-152">Specifies the preference for an MX record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce83a-153">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="ce83a-153">-Priority</span></span>
<span data-ttu-id="ce83a-154">Bir SRV kaydının önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce83a-154">Specifies the priority for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce83a-155">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="ce83a-155">-Ptrdname</span></span>
<span data-ttu-id="ce83a-156">İşaretçi kaynağı (PTR) kaydının hedef etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce83a-156">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce83a-157">-Kayıt kümesi</span><span class="sxs-lookup"><span data-stu-id="ce83a-157">-RecordSet</span></span>
<span data-ttu-id="ce83a-158">Düzenlenecek **kayıt kümesi** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce83a-158">Specifies the **RecordSet** object to edit.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce83a-159">-Hedef</span><span class="sxs-lookup"><span data-stu-id="ce83a-159">-Target</span></span>
<span data-ttu-id="ce83a-160">Bir SRV kaydının hedefini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce83a-160">Specifies the target for an SRV record.</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce83a-161">-Değer</span><span class="sxs-lookup"><span data-stu-id="ce83a-161">-Value</span></span>
<span data-ttu-id="ce83a-162">Bir TXT kaydının değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce83a-162">Specifies the value for a TXT record.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce83a-163">-Kalınlık</span><span class="sxs-lookup"><span data-stu-id="ce83a-163">-Weight</span></span>
<span data-ttu-id="ce83a-164">Bir SRV kaydı için ağırlığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce83a-164">Specifies the weight for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce83a-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce83a-165">-DefaultProfile</span></span>
<span data-ttu-id="ce83a-166">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ce83a-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce83a-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce83a-167">CommonParameters</span></span>
<span data-ttu-id="ce83a-168">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ce83a-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce83a-169">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce83a-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce83a-170">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ce83a-170">INPUTS</span></span>

### <span data-ttu-id="ce83a-171">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ce83a-171">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="ce83a-172">Bir **Recordset** nesnesini bu cmdlet 'e boru yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce83a-172">You can pipe a **RecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="ce83a-173">Bu, **kayıt kümesinin** çevrimdışı temsilidir ve Set-AzureRmDnsRecordSet cmdlet 'i ÇALıŞTıRANA kadar DNS yanıtlarını değiştirmiyor.</span><span class="sxs-lookup"><span data-stu-id="ce83a-173">This is an offline representation of the **RecordSet** , and changes to it do not change DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet.</span></span>

## <span data-ttu-id="ce83a-174">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ce83a-174">OUTPUTS</span></span>

### <span data-ttu-id="ce83a-175">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ce83a-175">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="ce83a-176">Bu cmdlet değiştirilmiş **Recordset** nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ce83a-176">This cmdlet returns the modified **RecordSet** object.</span></span>
<span data-ttu-id="ce83a-177">Ayrıca, geçirilen nesne doğrudan değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="ce83a-177">In addition, the object passed in is modified directly.</span></span>

## <span data-ttu-id="ce83a-178">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ce83a-178">NOTES</span></span>

## <span data-ttu-id="ce83a-179">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ce83a-179">RELATED LINKS</span></span>

[<span data-ttu-id="ce83a-180">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ce83a-180">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="ce83a-181">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="ce83a-181">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="ce83a-182">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ce83a-182">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
