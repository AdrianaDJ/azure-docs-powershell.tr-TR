---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4b0e8642feb208c9ed7ab0a91a31ebe7bd0f7cf8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939732"
---
# <span data-ttu-id="6f5b7-101">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="6f5b7-101">Remove-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="6f5b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f5b7-102">SYNOPSIS</span></span>
<span data-ttu-id="6f5b7-103">Yerel kayıt kümesi nesnesinden DNS kaydını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-103">Removes a DNS record from a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f5b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f5b7-104">SYNTAX</span></span>

### <span data-ttu-id="6f5b7-105">Bir</span><span class="sxs-lookup"><span data-stu-id="6f5b7-105">A</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="6f5b7-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="6f5b7-106">AAAA</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="6f5b7-107">Seç</span><span class="sxs-lookup"><span data-stu-id="6f5b7-107">NS</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="6f5b7-108">DOSYASıNA</span><span class="sxs-lookup"><span data-stu-id="6f5b7-108">MX</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="6f5b7-109">PTR</span><span class="sxs-lookup"><span data-stu-id="6f5b7-109">PTR</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="6f5b7-110">,</span><span class="sxs-lookup"><span data-stu-id="6f5b7-110">TXT</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="6f5b7-111">SRV</span><span class="sxs-lookup"><span data-stu-id="6f5b7-111">SRV</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="6f5b7-112">KAYDıNı</span><span class="sxs-lookup"><span data-stu-id="6f5b7-112">CNAME</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="6f5b7-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f5b7-113">DESCRIPTION</span></span>
<span data-ttu-id="6f5b7-114">**Remove-AzureRmDnsRecordConfig** cmdlet 'i, bir kayıt kümesinden etki alanı adı SISTEMI (DNS) kaydını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-114">The **Remove-AzureRmDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="6f5b7-115">**Kayıt kümesi** nesnesi bir çevrimdışı nesnedir ve değişiklikleri MICROSOFT Azure DNS hizmeti 'nde kalıcı olarak sürdürmek için Set-AzureRmDnsRecordSet cmdlet 'i çalıştırana kadar DNS yanıtlarını değiştirmiyor.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="6f5b7-116">Kaydı kaldırmak için, bu kayıt türü için tüm alanların tam olarak eşleşmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-116">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="6f5b7-117">SOA kayıtlarını ekleyemezsiniz veya kaldıramazsınız.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-117">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="6f5b7-118">SOA kayıtları, DNS bölgesi oluşturulduğunda ve DNS bölgesi silindiğinde otomatik olarak silindiğinde otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-118">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>

<span data-ttu-id="6f5b7-119">**Recordset** nesnesini bu cmdlet 'e parametre olarak veya Pipeline işlecini kullanarak geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="6f5b7-120">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f5b7-120">EXAMPLES</span></span>

### <span data-ttu-id="6f5b7-121">Örnek 1: kayıt kümesinden kayıt kaldırma</span><span class="sxs-lookup"><span data-stu-id="6f5b7-121">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="6f5b7-122">Bu örnekte, var olan kayıt kümesinden bir kayıt kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-122">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="6f5b7-123">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-123">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="6f5b7-124">Kayıt kümesini tümüyle kaldırmak için Remove-AzureRmDnsRecordSet ' e bakın.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-124">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="6f5b7-125">Örnek 2: kayıt kümesinden AAAA kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="6f5b7-125">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="6f5b7-126">Bu örnekte, varolan bir kayıt kümesinden AAAA kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-126">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="6f5b7-127">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-127">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="6f5b7-128">Kayıt kümesini tümüyle kaldırmak için Remove-AzureRmDnsRecordSet ' e bakın.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-128">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="6f5b7-129">Örnek 3: kayıt kümesinden CNAME kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="6f5b7-129">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="6f5b7-130">Bu örnekte, var olan kayıt kümesinden bir CNAME kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-130">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="6f5b7-131">CNAME kayıt kümesi en çok bir kayıt içerebileceğinden, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-131">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="6f5b7-132">Örnek 4: kayıt kümesinden bir MX kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="6f5b7-132">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="6f5b7-133">Bu örnekte, var olan kayıt kümesinden bir MX kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-133">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="6f5b7-134">"@" Kayıt adı, bölge Apex bir kayıt kümesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-134">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="6f5b7-135">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-135">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="6f5b7-136">Kayıt kümesini tümüyle kaldırmak için Remove-AzureRmDnsRecordSet ' e bakın.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-136">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="6f5b7-137">Örnek 5: kayıt kümesinden NS kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="6f5b7-137">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="6f5b7-138">Bu örnekte, var olan kayıt kümesinden NS kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-138">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="6f5b7-139">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-139">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="6f5b7-140">Kayıt kümesini tümüyle kaldırmak için Remove-AzureRmDnsRecordSet ' e bakın.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-140">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="6f5b7-141">Örnek 6: kayıt kümesinden PTR kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="6f5b7-141">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="6f5b7-142">Bu örnekte, var olan kayıt kümesinden bir PTR kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-142">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="6f5b7-143">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-143">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="6f5b7-144">Kayıt kümesini tümüyle kaldırmak için Remove-AzureRmDnsRecordSet ' e bakın.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-144">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="6f5b7-145">Örnek 7: kayıt kümesinden SRV kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="6f5b7-145">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="6f5b7-146">Bu örnekte, var olan kayıt kümesinden bir SRV kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-146">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="6f5b7-147">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-147">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="6f5b7-148">Kayıt kümesini tümüyle kaldırmak için Remove-AzureRmDnsRecordSet ' e bakın.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-148">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="6f5b7-149">Örnek 8: kayıt kümesinden TXT kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="6f5b7-149">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Value "This is a TXT Record"  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="6f5b7-150">Bu örnekte, var olan kayıt kümesinden bir TXT kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-150">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="6f5b7-151">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-151">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="6f5b7-152">Kayıt kümesini tümüyle kaldırmak için Remove-AzureRmDnsRecordSet ' e bakın.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-152">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

## <span data-ttu-id="6f5b7-153">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f5b7-153">PARAMETERS</span></span>

### <span data-ttu-id="6f5b7-154">-CNAME</span><span class="sxs-lookup"><span data-stu-id="6f5b7-154">-Cname</span></span>
<span data-ttu-id="6f5b7-155">Kurallı ad (CNAME) kaydı için etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-155">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="6f5b7-156">-Exchange</span><span class="sxs-lookup"><span data-stu-id="6f5b7-156">-Exchange</span></span>
<span data-ttu-id="6f5b7-157">Posta alışverişi (MX) kaydı için posta Exchange sunucusu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-157">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="6f5b7-158">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="6f5b7-158">-Ipv4Address</span></span>
<span data-ttu-id="6f5b7-159">Bir kaydın IPv4 adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-159">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="6f5b7-160">-IPv6Adresi</span><span class="sxs-lookup"><span data-stu-id="6f5b7-160">-Ipv6Address</span></span>
<span data-ttu-id="6f5b7-161">AAAA kaydı için IPv6 adresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-161">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="6f5b7-162">-Nsdadı</span><span class="sxs-lookup"><span data-stu-id="6f5b7-162">-Nsdname</span></span>
<span data-ttu-id="6f5b7-163">Ad sunucusu (NS) kaydı için ad sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-163">Specifies the name server for a name server (NS) record.</span></span>

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

### <span data-ttu-id="6f5b7-164">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="6f5b7-164">-Port</span></span>
<span data-ttu-id="6f5b7-165">Hizmet (SRV) kaydı için bağlantı noktası belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-165">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="6f5b7-166">-Tercih</span><span class="sxs-lookup"><span data-stu-id="6f5b7-166">-Preference</span></span>
<span data-ttu-id="6f5b7-167">Bir MX kaydı için tercih belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-167">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="6f5b7-168">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="6f5b7-168">-Priority</span></span>
<span data-ttu-id="6f5b7-169">Bir SRV kaydının önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-169">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="6f5b7-170">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="6f5b7-170">-Ptrdname</span></span>
<span data-ttu-id="6f5b7-171">Bir işaretçi (PTR) kaydının hedef etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-171">Specifies the target domain name of a pointer (PTR) record.</span></span>

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

### <span data-ttu-id="6f5b7-172">-Kayıt kümesi</span><span class="sxs-lookup"><span data-stu-id="6f5b7-172">-RecordSet</span></span>
<span data-ttu-id="6f5b7-173">Kaldırılacak kaydı içeren **kayıt kümesi** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-173">Specifies the **RecordSet** object that contains the record to remove.</span></span>

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

### <span data-ttu-id="6f5b7-174">-Hedef</span><span class="sxs-lookup"><span data-stu-id="6f5b7-174">-Target</span></span>
<span data-ttu-id="6f5b7-175">Bir SRV kaydının hedefini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-175">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="6f5b7-176">-Değer</span><span class="sxs-lookup"><span data-stu-id="6f5b7-176">-Value</span></span>
<span data-ttu-id="6f5b7-177">Bir TXT kaydının değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-177">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="6f5b7-178">-Kalınlık</span><span class="sxs-lookup"><span data-stu-id="6f5b7-178">-Weight</span></span>
<span data-ttu-id="6f5b7-179">Bir SRV kaydı için ağırlığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-179">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="6f5b7-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f5b7-180">CommonParameters</span></span>
<span data-ttu-id="6f5b7-181">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f5b7-182">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f5b7-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f5b7-183">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f5b7-183">INPUTS</span></span>

### <span data-ttu-id="6f5b7-184">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6f5b7-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="6f5b7-185">Bir **Dnsrecordset** nesnesini bu cmdlet 'e boru edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-185">You can pipe a **DnsRecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="6f5b7-186">Bu, kayıt kümesinin çevrimdışı bir temsilidir ve bu sunucudaki güncelleştirmeler, set-AzureRmDnsRecordSet 'i çalıştırana kadar DNS yanıtlarını değiştirmiyor.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-186">This is an offline representation of the record set and updates to it do not change DNS responses until after you run Set-AzureRmDnsRecordSet.</span></span>

## <span data-ttu-id="6f5b7-187">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f5b7-187">OUTPUTS</span></span>

### <span data-ttu-id="6f5b7-188">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6f5b7-188">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="6f5b7-189">Bu cmdlet değiştirilmiş **Recordset** nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-189">This cmdlet returns the modified **RecordSet** object.</span></span>

## <span data-ttu-id="6f5b7-190">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f5b7-190">NOTES</span></span>

## <span data-ttu-id="6f5b7-191">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f5b7-191">RELATED LINKS</span></span>

[<span data-ttu-id="6f5b7-192">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="6f5b7-192">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="6f5b7-193">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6f5b7-193">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="6f5b7-194">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6f5b7-194">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
