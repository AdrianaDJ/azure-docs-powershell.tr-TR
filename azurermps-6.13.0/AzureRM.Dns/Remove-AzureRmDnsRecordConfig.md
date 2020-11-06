---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordConfig.md
ms.openlocfilehash: f4521b50d338d18eaa3c811ee64c5cff20dcf54a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590947"
---
# <span data-ttu-id="a65d6-101">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="a65d6-101">Remove-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="a65d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a65d6-102">SYNOPSIS</span></span>
<span data-ttu-id="a65d6-103">Yerel kayıt kümesi nesnesinden DNS kaydını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a65d6-103">Removes a DNS record from a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a65d6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a65d6-104">SYNTAX</span></span>

### <span data-ttu-id="a65d6-105">Bir</span><span class="sxs-lookup"><span data-stu-id="a65d6-105">A</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a65d6-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="a65d6-106">AAAA</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a65d6-107">Seç</span><span class="sxs-lookup"><span data-stu-id="a65d6-107">NS</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a65d6-108">DOSYASıNA</span><span class="sxs-lookup"><span data-stu-id="a65d6-108">MX</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a65d6-109">PTR</span><span class="sxs-lookup"><span data-stu-id="a65d6-109">PTR</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a65d6-110">,</span><span class="sxs-lookup"><span data-stu-id="a65d6-110">TXT</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a65d6-111">SRV</span><span class="sxs-lookup"><span data-stu-id="a65d6-111">SRV</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a65d6-112">KAYDıNı</span><span class="sxs-lookup"><span data-stu-id="a65d6-112">CNAME</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a65d6-113">CAA</span><span class="sxs-lookup"><span data-stu-id="a65d6-113">Caa</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a65d6-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="a65d6-114">DESCRIPTION</span></span>
<span data-ttu-id="a65d6-115">**Remove-AzureRmDnsRecordConfig** cmdlet 'i, bir kayıt kümesinden etki alanı adı SISTEMI (DNS) kaydını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a65d6-115">The **Remove-AzureRmDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="a65d6-116">**Kayıt kümesi** nesnesi bir çevrimdışı nesnedir ve değişiklikleri MICROSOFT Azure DNS hizmeti 'nde kalıcı olarak sürdürmek için Set-AzureRmDnsRecordSet cmdlet 'i çalıştırana kadar DNS yanıtlarını değiştirmiyor.</span><span class="sxs-lookup"><span data-stu-id="a65d6-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="a65d6-117">Kaydı kaldırmak için, bu kayıt türü için tüm alanların tam olarak eşleşmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="a65d6-117">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="a65d6-118">SOA kayıtlarını ekleyemezsiniz veya kaldıramazsınız.</span><span class="sxs-lookup"><span data-stu-id="a65d6-118">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="a65d6-119">SOA kayıtları, DNS bölgesi oluşturulduğunda ve DNS bölgesi silindiğinde otomatik olarak silindiğinde otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a65d6-119">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>
<span data-ttu-id="a65d6-120">**Recordset** nesnesini bu cmdlet 'e parametre olarak veya Pipeline işlecini kullanarak geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a65d6-120">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="a65d6-121">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a65d6-121">EXAMPLES</span></span>

### <span data-ttu-id="a65d6-122">Örnek 1: kayıt kümesinden kayıt kaldırma</span><span class="sxs-lookup"><span data-stu-id="a65d6-122">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a65d6-123">Bu örnekte, var olan kayıt kümesinden bir kayıt kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="a65d6-123">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="a65d6-124">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="a65d6-124">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="a65d6-125">Kayıt kümesini tümüyle kaldırmak için Remove-AzureRmDnsRecordSet ' e bakın.</span><span class="sxs-lookup"><span data-stu-id="a65d6-125">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="a65d6-126">Örnek 2: kayıt kümesinden AAAA kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="a65d6-126">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a65d6-127">Bu örnekte, varolan bir kayıt kümesinden AAAA kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="a65d6-127">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="a65d6-128">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="a65d6-128">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="a65d6-129">Kayıt kümesini tümüyle kaldırmak için Remove-AzureRmDnsRecordSet ' e bakın.</span><span class="sxs-lookup"><span data-stu-id="a65d6-129">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="a65d6-130">Örnek 3: kayıt kümesinden CNAME kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="a65d6-130">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a65d6-131">Bu örnekte, var olan kayıt kümesinden bir CNAME kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="a65d6-131">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="a65d6-132">CNAME kayıt kümesi en çok bir kayıt içerebileceğinden, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="a65d6-132">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="a65d6-133">Örnek 4: kayıt kümesinden bir MX kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="a65d6-133">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a65d6-134">Bu örnekte, var olan kayıt kümesinden bir MX kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="a65d6-134">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="a65d6-135">"@" Kayıt adı, bölge Apex bir kayıt kümesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a65d6-135">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="a65d6-136">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="a65d6-136">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="a65d6-137">Kayıt kümesini tümüyle kaldırmak için Remove-AzureRmDnsRecordSet ' e bakın.</span><span class="sxs-lookup"><span data-stu-id="a65d6-137">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="a65d6-138">Örnek 5: kayıt kümesinden NS kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="a65d6-138">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a65d6-139">Bu örnekte, var olan kayıt kümesinden NS kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="a65d6-139">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="a65d6-140">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="a65d6-140">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="a65d6-141">Kayıt kümesini tümüyle kaldırmak için Remove-AzureRmDnsRecordSet ' e bakın.</span><span class="sxs-lookup"><span data-stu-id="a65d6-141">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="a65d6-142">Örnek 6: kayıt kümesinden PTR kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="a65d6-142">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a65d6-143">Bu örnekte, var olan kayıt kümesinden bir PTR kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="a65d6-143">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="a65d6-144">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="a65d6-144">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="a65d6-145">Kayıt kümesini tümüyle kaldırmak için Remove-AzureRmDnsRecordSet ' e bakın.</span><span class="sxs-lookup"><span data-stu-id="a65d6-145">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="a65d6-146">Örnek 7: kayıt kümesinden SRV kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="a65d6-146">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a65d6-147">Bu örnekte, var olan kayıt kümesinden bir SRV kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="a65d6-147">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="a65d6-148">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="a65d6-148">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="a65d6-149">Kayıt kümesini tümüyle kaldırmak için Remove-AzureRmDnsRecordSet ' e bakın.</span><span class="sxs-lookup"><span data-stu-id="a65d6-149">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="a65d6-150">Örnek 8: kayıt kümesinden TXT kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="a65d6-150">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Value "This is a TXT Record"  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a65d6-151">Bu örnekte, var olan kayıt kümesinden bir TXT kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="a65d6-151">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="a65d6-152">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="a65d6-152">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="a65d6-153">Kayıt kümesini tümüyle kaldırmak için Remove-AzureRmDnsRecordSet ' e bakın.</span><span class="sxs-lookup"><span data-stu-id="a65d6-153">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

## <span data-ttu-id="a65d6-154">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a65d6-154">PARAMETERS</span></span>

### <span data-ttu-id="a65d6-155">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="a65d6-155">-CaaFlags</span></span>
<span data-ttu-id="a65d6-156">Eklenecek CAA kaydının bayrakları.</span><span class="sxs-lookup"><span data-stu-id="a65d6-156">The flags for the CAA record to add.</span></span> <span data-ttu-id="a65d6-157">0 ile 255 arasında bir sayı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a65d6-157">Must be a number between 0 and 255.</span></span>

```yaml
Type: System.Byte
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a65d6-158">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="a65d6-158">-CaaTag</span></span>
<span data-ttu-id="a65d6-159">Eklenecek CAA kaydının etiket alanı.</span><span class="sxs-lookup"><span data-stu-id="a65d6-159">The tag field of the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a65d6-160">-Caadeğer</span><span class="sxs-lookup"><span data-stu-id="a65d6-160">-CaaValue</span></span>
<span data-ttu-id="a65d6-161">Eklenecek CAA kaydının değer alanı.</span><span class="sxs-lookup"><span data-stu-id="a65d6-161">The value field for the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a65d6-162">-CNAME</span><span class="sxs-lookup"><span data-stu-id="a65d6-162">-Cname</span></span>
<span data-ttu-id="a65d6-163">Kurallı ad (CNAME) kaydı için etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a65d6-163">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="a65d6-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a65d6-164">-DefaultProfile</span></span>
<span data-ttu-id="a65d6-165">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a65d6-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a65d6-166">-Exchange</span><span class="sxs-lookup"><span data-stu-id="a65d6-166">-Exchange</span></span>
<span data-ttu-id="a65d6-167">Posta alışverişi (MX) kaydı için posta Exchange sunucusu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a65d6-167">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="a65d6-168">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="a65d6-168">-Ipv4Address</span></span>
<span data-ttu-id="a65d6-169">Bir kaydın IPv4 adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a65d6-169">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="a65d6-170">-IPv6Adresi</span><span class="sxs-lookup"><span data-stu-id="a65d6-170">-Ipv6Address</span></span>
<span data-ttu-id="a65d6-171">AAAA kaydı için IPv6 adresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a65d6-171">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="a65d6-172">-Nsdadı</span><span class="sxs-lookup"><span data-stu-id="a65d6-172">-Nsdname</span></span>
<span data-ttu-id="a65d6-173">Ad sunucusu (NS) kaydı için ad sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a65d6-173">Specifies the name server for a name server (NS) record.</span></span>

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

### <span data-ttu-id="a65d6-174">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="a65d6-174">-Port</span></span>
<span data-ttu-id="a65d6-175">Hizmet (SRV) kaydı için bağlantı noktası belirtir.</span><span class="sxs-lookup"><span data-stu-id="a65d6-175">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="a65d6-176">-Tercih</span><span class="sxs-lookup"><span data-stu-id="a65d6-176">-Preference</span></span>
<span data-ttu-id="a65d6-177">Bir MX kaydı için tercih belirtir.</span><span class="sxs-lookup"><span data-stu-id="a65d6-177">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="a65d6-178">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="a65d6-178">-Priority</span></span>
<span data-ttu-id="a65d6-179">Bir SRV kaydının önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a65d6-179">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="a65d6-180">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="a65d6-180">-Ptrdname</span></span>
<span data-ttu-id="a65d6-181">Bir işaretçi (PTR) kaydının hedef etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a65d6-181">Specifies the target domain name of a pointer (PTR) record.</span></span>

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

### <span data-ttu-id="a65d6-182">-Kayıt kümesi</span><span class="sxs-lookup"><span data-stu-id="a65d6-182">-RecordSet</span></span>
<span data-ttu-id="a65d6-183">Kaldırılacak kaydı içeren **kayıt kümesi** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a65d6-183">Specifies the **RecordSet** object that contains the record to remove.</span></span>

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

### <span data-ttu-id="a65d6-184">-Hedef</span><span class="sxs-lookup"><span data-stu-id="a65d6-184">-Target</span></span>
<span data-ttu-id="a65d6-185">Bir SRV kaydının hedefini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a65d6-185">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="a65d6-186">-Değer</span><span class="sxs-lookup"><span data-stu-id="a65d6-186">-Value</span></span>
<span data-ttu-id="a65d6-187">Bir TXT kaydının değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a65d6-187">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="a65d6-188">-Kalınlık</span><span class="sxs-lookup"><span data-stu-id="a65d6-188">-Weight</span></span>
<span data-ttu-id="a65d6-189">Bir SRV kaydı için ağırlığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="a65d6-189">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="a65d6-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a65d6-190">CommonParameters</span></span>
<span data-ttu-id="a65d6-191">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a65d6-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a65d6-192">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a65d6-192">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a65d6-193">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a65d6-193">INPUTS</span></span>

### <span data-ttu-id="a65d6-194">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a65d6-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="a65d6-195">Parametreler: RecordSet (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a65d6-195">Parameters: RecordSet (ByValue)</span></span>

### <span data-ttu-id="a65d6-196">System. String</span><span class="sxs-lookup"><span data-stu-id="a65d6-196">System.String</span></span>

### <span data-ttu-id="a65d6-197">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="a65d6-197">System.UInt16</span></span>

### <span data-ttu-id="a65d6-198">System. Byte</span><span class="sxs-lookup"><span data-stu-id="a65d6-198">System.Byte</span></span>

## <span data-ttu-id="a65d6-199">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a65d6-199">OUTPUTS</span></span>

### <span data-ttu-id="a65d6-200">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a65d6-200">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="a65d6-201">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a65d6-201">NOTES</span></span>

## <span data-ttu-id="a65d6-202">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a65d6-202">RELATED LINKS</span></span>

[<span data-ttu-id="a65d6-203">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="a65d6-203">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="a65d6-204">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a65d6-204">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="a65d6-205">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a65d6-205">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
