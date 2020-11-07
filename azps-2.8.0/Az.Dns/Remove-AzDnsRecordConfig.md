---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
ms.openlocfilehash: acf81459fd62e3f86c8e4ad02bfdefd0055db270
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752031"
---
# <span data-ttu-id="d6037-101">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="d6037-101">Remove-AzDnsRecordConfig</span></span>

## <span data-ttu-id="d6037-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6037-102">SYNOPSIS</span></span>
<span data-ttu-id="d6037-103">Yerel kayıt kümesi nesnesinden DNS kaydını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d6037-103">Removes a DNS record from a local record set object.</span></span>

## <span data-ttu-id="d6037-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d6037-104">SYNTAX</span></span>

### <span data-ttu-id="d6037-105">Bir</span><span class="sxs-lookup"><span data-stu-id="d6037-105">A</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6037-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="d6037-106">AAAA</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6037-107">Seç</span><span class="sxs-lookup"><span data-stu-id="d6037-107">NS</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6037-108">DOSYASıNA</span><span class="sxs-lookup"><span data-stu-id="d6037-108">MX</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6037-109">PTR</span><span class="sxs-lookup"><span data-stu-id="d6037-109">PTR</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6037-110">,</span><span class="sxs-lookup"><span data-stu-id="d6037-110">TXT</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6037-111">SRV</span><span class="sxs-lookup"><span data-stu-id="d6037-111">SRV</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6037-112">KAYDıNı</span><span class="sxs-lookup"><span data-stu-id="d6037-112">CNAME</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6037-113">CAA</span><span class="sxs-lookup"><span data-stu-id="d6037-113">Caa</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6037-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="d6037-114">DESCRIPTION</span></span>
<span data-ttu-id="d6037-115">**Remove-AzDnsRecordConfig** cmdlet 'i, bir kayıt kümesinden etki alanı adı SISTEMI (DNS) kaydını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d6037-115">The **Remove-AzDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="d6037-116">**Kayıt kümesi** nesnesi bir çevrimdışı nesnedir ve değişiklikleri MICROSOFT Azure DNS hizmeti 'nde kalıcı olarak sürdürmek için Set-AzDnsRecordSet cmdlet 'i çalıştırana kadar DNS yanıtlarını değiştirmiyor.</span><span class="sxs-lookup"><span data-stu-id="d6037-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="d6037-117">Kaydı kaldırmak için, bu kayıt türü için tüm alanların tam olarak eşleşmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="d6037-117">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="d6037-118">SOA kayıtlarını ekleyemezsiniz veya kaldıramazsınız.</span><span class="sxs-lookup"><span data-stu-id="d6037-118">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="d6037-119">SOA kayıtları, DNS bölgesi oluşturulduğunda ve DNS bölgesi silindiğinde otomatik olarak silindiğinde otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d6037-119">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>
<span data-ttu-id="d6037-120">**Recordset** nesnesini bu cmdlet 'e parametre olarak veya Pipeline işlecini kullanarak geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d6037-120">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="d6037-121">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d6037-121">EXAMPLES</span></span>

### <span data-ttu-id="d6037-122">Örnek 1: kayıt kümesinden kayıt kaldırma</span><span class="sxs-lookup"><span data-stu-id="d6037-122">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="d6037-123">Bu örnekte, var olan kayıt kümesinden bir kayıt kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="d6037-123">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="d6037-124">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="d6037-124">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="d6037-125">Kayıt kümesini tümüyle kaldırmak için Remove-AzDnsRecordSet ' e bakın.</span><span class="sxs-lookup"><span data-stu-id="d6037-125">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="d6037-126">Örnek 2: kayıt kümesinden AAAA kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d6037-126">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="d6037-127">Bu örnekte, varolan bir kayıt kümesinden AAAA kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="d6037-127">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="d6037-128">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="d6037-128">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="d6037-129">Kayıt kümesini tümüyle kaldırmak için Remove-AzDnsRecordSet ' e bakın.</span><span class="sxs-lookup"><span data-stu-id="d6037-129">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="d6037-130">Örnek 3: kayıt kümesinden CNAME kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d6037-130">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="d6037-131">Bu örnekte, var olan kayıt kümesinden bir CNAME kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="d6037-131">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="d6037-132">CNAME kayıt kümesi en çok bir kayıt içerebileceğinden, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="d6037-132">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="d6037-133">Örnek 4: kayıt kümesinden bir MX kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d6037-133">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="d6037-134">Bu örnekte, var olan kayıt kümesinden bir MX kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="d6037-134">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="d6037-135">"@" Kayıt adı, bölge Apex bir kayıt kümesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="d6037-135">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="d6037-136">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="d6037-136">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="d6037-137">Kayıt kümesini tümüyle kaldırmak için Remove-AzDnsRecordSet ' e bakın.</span><span class="sxs-lookup"><span data-stu-id="d6037-137">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="d6037-138">Örnek 5: kayıt kümesinden NS kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d6037-138">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzDnsRecordSet
```

<span data-ttu-id="d6037-139">Bu örnekte, var olan kayıt kümesinden NS kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="d6037-139">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="d6037-140">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="d6037-140">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="d6037-141">Kayıt kümesini tümüyle kaldırmak için Remove-AzDnsRecordSet ' e bakın.</span><span class="sxs-lookup"><span data-stu-id="d6037-141">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="d6037-142">Örnek 6: kayıt kümesinden PTR kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d6037-142">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="d6037-143">Bu örnekte, var olan kayıt kümesinden bir PTR kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="d6037-143">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="d6037-144">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="d6037-144">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="d6037-145">Kayıt kümesini tümüyle kaldırmak için Remove-AzDnsRecordSet ' e bakın.</span><span class="sxs-lookup"><span data-stu-id="d6037-145">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="d6037-146">Örnek 7: kayıt kümesinden SRV kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d6037-146">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="d6037-147">Bu örnekte, var olan kayıt kümesinden bir SRV kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="d6037-147">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="d6037-148">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="d6037-148">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="d6037-149">Kayıt kümesini tümüyle kaldırmak için Remove-AzDnsRecordSet ' e bakın.</span><span class="sxs-lookup"><span data-stu-id="d6037-149">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="d6037-150">Örnek 8: kayıt kümesinden TXT kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d6037-150">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Value "This is a TXT Record"  | Set-AzDnsRecordSet
```

<span data-ttu-id="d6037-151">Bu örnekte, var olan kayıt kümesinden bir TXT kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="d6037-151">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="d6037-152">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="d6037-152">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="d6037-153">Kayıt kümesini tümüyle kaldırmak için Remove-AzDnsRecordSet ' e bakın.</span><span class="sxs-lookup"><span data-stu-id="d6037-153">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

## <span data-ttu-id="d6037-154">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d6037-154">PARAMETERS</span></span>

### <span data-ttu-id="d6037-155">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="d6037-155">-CaaFlags</span></span>
<span data-ttu-id="d6037-156">Eklenecek CAA kaydının bayrakları.</span><span class="sxs-lookup"><span data-stu-id="d6037-156">The flags for the CAA record to add.</span></span> <span data-ttu-id="d6037-157">0 ile 255 arasında bir sayı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d6037-157">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="d6037-158">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="d6037-158">-CaaTag</span></span>
<span data-ttu-id="d6037-159">Eklenecek CAA kaydının etiket alanı.</span><span class="sxs-lookup"><span data-stu-id="d6037-159">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="d6037-160">-Caadeğer</span><span class="sxs-lookup"><span data-stu-id="d6037-160">-CaaValue</span></span>
<span data-ttu-id="d6037-161">Eklenecek CAA kaydının değer alanı.</span><span class="sxs-lookup"><span data-stu-id="d6037-161">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="d6037-162">-CNAME</span><span class="sxs-lookup"><span data-stu-id="d6037-162">-Cname</span></span>
<span data-ttu-id="d6037-163">Kurallı ad (CNAME) kaydı için etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6037-163">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="d6037-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6037-164">-DefaultProfile</span></span>
<span data-ttu-id="d6037-165">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d6037-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6037-166">-Exchange</span><span class="sxs-lookup"><span data-stu-id="d6037-166">-Exchange</span></span>
<span data-ttu-id="d6037-167">Posta alışverişi (MX) kaydı için posta Exchange sunucusu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6037-167">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="d6037-168">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="d6037-168">-Ipv4Address</span></span>
<span data-ttu-id="d6037-169">Bir kaydın IPv4 adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6037-169">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="d6037-170">-IPv6Adresi</span><span class="sxs-lookup"><span data-stu-id="d6037-170">-Ipv6Address</span></span>
<span data-ttu-id="d6037-171">AAAA kaydı için IPv6 adresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6037-171">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="d6037-172">-Nsdadı</span><span class="sxs-lookup"><span data-stu-id="d6037-172">-Nsdname</span></span>
<span data-ttu-id="d6037-173">Ad sunucusu (NS) kaydı için ad sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6037-173">Specifies the name server for a name server (NS) record.</span></span>

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

### <span data-ttu-id="d6037-174">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="d6037-174">-Port</span></span>
<span data-ttu-id="d6037-175">Hizmet (SRV) kaydı için bağlantı noktası belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6037-175">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="d6037-176">-Tercih</span><span class="sxs-lookup"><span data-stu-id="d6037-176">-Preference</span></span>
<span data-ttu-id="d6037-177">Bir MX kaydı için tercih belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6037-177">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="d6037-178">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="d6037-178">-Priority</span></span>
<span data-ttu-id="d6037-179">Bir SRV kaydının önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6037-179">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="d6037-180">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="d6037-180">-Ptrdname</span></span>
<span data-ttu-id="d6037-181">Bir işaretçi (PTR) kaydının hedef etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6037-181">Specifies the target domain name of a pointer (PTR) record.</span></span>

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

### <span data-ttu-id="d6037-182">-Kayıt kümesi</span><span class="sxs-lookup"><span data-stu-id="d6037-182">-RecordSet</span></span>
<span data-ttu-id="d6037-183">Kaldırılacak kaydı içeren **kayıt kümesi** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6037-183">Specifies the **RecordSet** object that contains the record to remove.</span></span>

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

### <span data-ttu-id="d6037-184">-Hedef</span><span class="sxs-lookup"><span data-stu-id="d6037-184">-Target</span></span>
<span data-ttu-id="d6037-185">Bir SRV kaydının hedefini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6037-185">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="d6037-186">-Değer</span><span class="sxs-lookup"><span data-stu-id="d6037-186">-Value</span></span>
<span data-ttu-id="d6037-187">Bir TXT kaydının değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6037-187">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="d6037-188">-Kalınlık</span><span class="sxs-lookup"><span data-stu-id="d6037-188">-Weight</span></span>
<span data-ttu-id="d6037-189">Bir SRV kaydı için ağırlığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6037-189">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="d6037-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6037-190">CommonParameters</span></span>
<span data-ttu-id="d6037-191">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d6037-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6037-192">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6037-192">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6037-193">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d6037-193">INPUTS</span></span>

### <span data-ttu-id="d6037-194">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d6037-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="d6037-195">System. String</span><span class="sxs-lookup"><span data-stu-id="d6037-195">System.String</span></span>

### <span data-ttu-id="d6037-196">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="d6037-196">System.UInt16</span></span>

### <span data-ttu-id="d6037-197">System. Byte</span><span class="sxs-lookup"><span data-stu-id="d6037-197">System.Byte</span></span>

## <span data-ttu-id="d6037-198">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d6037-198">OUTPUTS</span></span>

### <span data-ttu-id="d6037-199">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d6037-199">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="d6037-200">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d6037-200">NOTES</span></span>

## <span data-ttu-id="d6037-201">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d6037-201">RELATED LINKS</span></span>

[<span data-ttu-id="d6037-202">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="d6037-202">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="d6037-203">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d6037-203">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="d6037-204">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d6037-204">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)