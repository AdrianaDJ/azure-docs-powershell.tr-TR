---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/add-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
ms.openlocfilehash: a5f3871f0ab63d875c2a0389c5585f0871fb0cb9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935918"
---
# <span data-ttu-id="0f4f9-101">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="0f4f9-101">Add-AzDnsRecordConfig</span></span>

## <span data-ttu-id="0f4f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f4f9-102">SYNOPSIS</span></span>
<span data-ttu-id="0f4f9-103">Yerel kayıt kümesi nesnesine bir DNS kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-103">Adds a DNS record to a local record set object.</span></span>

## <span data-ttu-id="0f4f9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f4f9-104">SYNTAX</span></span>

### <span data-ttu-id="0f4f9-105">Bir</span><span class="sxs-lookup"><span data-stu-id="0f4f9-105">A</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="0f4f9-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="0f4f9-106">AAAA</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="0f4f9-107">Seç</span><span class="sxs-lookup"><span data-stu-id="0f4f9-107">NS</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="0f4f9-108">DOSYASıNA</span><span class="sxs-lookup"><span data-stu-id="0f4f9-108">MX</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="0f4f9-109">PTR</span><span class="sxs-lookup"><span data-stu-id="0f4f9-109">PTR</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="0f4f9-110">,</span><span class="sxs-lookup"><span data-stu-id="0f4f9-110">TXT</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="0f4f9-111">SRV</span><span class="sxs-lookup"><span data-stu-id="0f4f9-111">SRV</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="0f4f9-112">KAYDıNı</span><span class="sxs-lookup"><span data-stu-id="0f4f9-112">CNAME</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="0f4f9-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f4f9-113">DESCRIPTION</span></span>
<span data-ttu-id="0f4f9-114">**Add-AzDnsRecordConfig** cmdlet 'ı bir etki alanı adı SISTEMI (DNS) kaydını bir **Recordset** nesnesine ekler.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-114">The **Add-AzDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="0f4f9-115">**Kayıt kümesi** nesnesi bir çevrimdışı nesnedir ve değişiklikleri MICROSOFT Azure DNS hizmeti 'nde kalıcı olarak sürdürmek için Set-AzDnsRecordSet cmdlet 'i çalıştırana kadar DNS yanıtlarını değiştirmiyor.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="0f4f9-116">SOA kayıtları bir DNS bölgesi oluşturulduğunda oluşturulur ve DNS bölgesi silindiğinde kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-116">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="0f4f9-117">SOA kayıtlarını ekleyip kaldıramazsınız, ancak bunları düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-117">You cannot add or remove SOA records, but you can edit them.</span></span>

<span data-ttu-id="0f4f9-118">**Recordset** nesnesini bu cmdlet 'e parametre olarak veya Pipeline işlecini kullanarak geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-118">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="0f4f9-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f4f9-119">EXAMPLES</span></span>

### <span data-ttu-id="0f4f9-120">Örnek 1: kayıt kümesine kayıt ekleme</span><span class="sxs-lookup"><span data-stu-id="0f4f9-120">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="0f4f9-121">Bu örnek, var olan kayıt kümesine bir kayıt ekler.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-121">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="0f4f9-122">Örnek 2: kayıt kümesine AAAA kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="0f4f9-122">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="0f4f9-123">Bu örnek, var olan kayıt kümesine bir AAAA kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-123">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="0f4f9-124">Örnek 3: kayıt kümesine CNAME kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="0f4f9-124">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="0f4f9-125">Bu örnek, var olan kayıt kümesine bir CNAME kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-125">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="0f4f9-126">CNAME kayıt kümesi en çok bir kayıt içerebileceği için, başlangıçta boş bir kayıt kümesi olmalıdır veya var olan kayıtların Remove-AzDnsRecordConfig kullanılarak kaldırılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-126">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzDnsRecordConfig.</span></span>

### <span data-ttu-id="0f4f9-127">Örnek 4: kayıt kümesine bir MX kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="0f4f9-127">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="0f4f9-128">Bu örnek, varolan bir kayıt kümesine bir MX kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-128">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="0f4f9-129">"@" Kayıt adı, bölge Apex bir kayıt kümesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-129">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="0f4f9-130">Örnek 5: kayıt kümesine NS kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="0f4f9-130">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzDnsRecordSet
```

<span data-ttu-id="0f4f9-131">Bu örnek, var olan kayıt kümesine bir NS kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-131">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="0f4f9-132">Örnek 6: kayıt kümesine PTR kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="0f4f9-132">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="0f4f9-133">Bu örnek, varolan bir kayıt kümesine bir PTR kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-133">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="0f4f9-134">Örnek 7: kayıt kümesine SRV kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="0f4f9-134">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="0f4f9-135">Bu örnek, var olan kayıt kümesine bir SRV kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-135">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="0f4f9-136">Örnek 8: kayıt kümesine TXT kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="0f4f9-136">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Value "This is a TXT Record" | Set-AzDnsRecordSet
```

<span data-ttu-id="0f4f9-137">Bu örnek, var olan kayıt kümesine bir TXT kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-137">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="0f4f9-138">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f4f9-138">PARAMETERS</span></span>

### <span data-ttu-id="0f4f9-139">-CNAME</span><span class="sxs-lookup"><span data-stu-id="0f4f9-139">-Cname</span></span>
<span data-ttu-id="0f4f9-140">Kurallı ad (CNAME) kaydı için etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-140">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: String
Parameter Sets: CNAME
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4f9-141">-Exchange</span><span class="sxs-lookup"><span data-stu-id="0f4f9-141">-Exchange</span></span>
<span data-ttu-id="0f4f9-142">Posta alışverişi (MX) kaydı için posta Exchange sunucusu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-142">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: String
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4f9-143">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="0f4f9-143">-Ipv4Address</span></span>
<span data-ttu-id="0f4f9-144">Bir kaydın IPv4 adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-144">Specifies an IPv4 address for an A record.</span></span>

```yaml
Type: String
Parameter Sets: A
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4f9-145">-IPv6Adresi</span><span class="sxs-lookup"><span data-stu-id="0f4f9-145">-Ipv6Address</span></span>
<span data-ttu-id="0f4f9-146">AAAA kaydı için IPv6 adresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-146">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: String
Parameter Sets: AAAA
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4f9-147">-Nsdadı</span><span class="sxs-lookup"><span data-stu-id="0f4f9-147">-Nsdname</span></span>
<span data-ttu-id="0f4f9-148">Ad sunucusu (NS) kaydı için ad sunucusu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-148">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: String
Parameter Sets: NS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4f9-149">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="0f4f9-149">-Port</span></span>
<span data-ttu-id="0f4f9-150">Hizmet (SRV) kaydı için bağlantı noktası belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-150">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4f9-151">-Tercih</span><span class="sxs-lookup"><span data-stu-id="0f4f9-151">-Preference</span></span>
<span data-ttu-id="0f4f9-152">Bir MX kaydı için tercih belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-152">Specifies the preference for an MX record.</span></span>

```yaml
Type: UInt16
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4f9-153">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="0f4f9-153">-Priority</span></span>
<span data-ttu-id="0f4f9-154">Bir SRV kaydının önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-154">Specifies the priority for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4f9-155">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="0f4f9-155">-Ptrdname</span></span>
<span data-ttu-id="0f4f9-156">İşaretçi kaynağı (PTR) kaydının hedef etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-156">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: String
Parameter Sets: PTR
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4f9-157">-Kayıt kümesi</span><span class="sxs-lookup"><span data-stu-id="0f4f9-157">-RecordSet</span></span>
<span data-ttu-id="0f4f9-158">Düzenlenecek **kayıt kümesi** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-158">Specifies the **RecordSet** object to edit.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4f9-159">-Hedef</span><span class="sxs-lookup"><span data-stu-id="0f4f9-159">-Target</span></span>
<span data-ttu-id="0f4f9-160">Bir SRV kaydının hedefini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-160">Specifies the target for an SRV record.</span></span>

```yaml
Type: String
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4f9-161">-Değer</span><span class="sxs-lookup"><span data-stu-id="0f4f9-161">-Value</span></span>
<span data-ttu-id="0f4f9-162">Bir TXT kaydının değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-162">Specifies the value for a TXT record.</span></span>

```yaml
Type: String
Parameter Sets: TXT
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4f9-163">-Kalınlık</span><span class="sxs-lookup"><span data-stu-id="0f4f9-163">-Weight</span></span>
<span data-ttu-id="0f4f9-164">Bir SRV kaydı için ağırlığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-164">Specifies the weight for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4f9-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f4f9-165">CommonParameters</span></span>
<span data-ttu-id="0f4f9-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f4f9-167">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f4f9-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f4f9-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f4f9-168">INPUTS</span></span>

### <span data-ttu-id="0f4f9-169">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0f4f9-169">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="0f4f9-170">Bir **Recordset** nesnesini bu cmdlet 'e boru yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-170">You can pipe a **RecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="0f4f9-171">Bu, **kayıt kümesinin** çevrimdışı temsilidir ve Set-AzDnsRecordSet cmdlet 'i ÇALıŞTıRANA kadar DNS yanıtlarını değiştirmiyor.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-171">This is an offline representation of the **RecordSet** , and changes to it do not change DNS responses until after you run the Set-AzDnsRecordSet cmdlet.</span></span>

## <span data-ttu-id="0f4f9-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f4f9-172">OUTPUTS</span></span>

### <span data-ttu-id="0f4f9-173">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0f4f9-173">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="0f4f9-174">Bu cmdlet değiştirilmiş **Recordset** nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-174">This cmdlet returns the modified **RecordSet** object.</span></span>
<span data-ttu-id="0f4f9-175">Ayrıca, geçirilen nesne doğrudan değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-175">In addition, the object passed in is modified directly.</span></span>

## <span data-ttu-id="0f4f9-176">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f4f9-176">NOTES</span></span>

## <span data-ttu-id="0f4f9-177">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f4f9-177">RELATED LINKS</span></span>

[<span data-ttu-id="0f4f9-178">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0f4f9-178">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="0f4f9-179">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="0f4f9-179">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

[<span data-ttu-id="0f4f9-180">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0f4f9-180">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
