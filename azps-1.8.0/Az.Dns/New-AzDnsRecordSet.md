---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: 54b83995eb923caca301ba6d84d3673071486850
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760892"
---
# <span data-ttu-id="2660b-101">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2660b-101">New-AzDnsRecordSet</span></span>

## <span data-ttu-id="2660b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2660b-102">SYNOPSIS</span></span>
<span data-ttu-id="2660b-103">DNS kayıt kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2660b-103">Creates a DNS record set.</span></span>

## <span data-ttu-id="2660b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2660b-104">SYNTAX</span></span>

### <span data-ttu-id="2660b-105">Alanlar (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2660b-105">Fields (Default)</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2660b-106">Diğerad alanları</span><span class="sxs-lookup"><span data-stu-id="2660b-106">AliasFields</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2660b-107">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="2660b-107">Object</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2660b-108">AliasObject</span><span class="sxs-lookup"><span data-stu-id="2660b-108">AliasObject</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2660b-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="2660b-109">DESCRIPTION</span></span>
<span data-ttu-id="2660b-110">**New-AzDnsRecordSet** cmdlet 'i belirtilen ada sahip yeni bir etki alanı adı SISTEMI (DNS) kaydı oluşturur ve belirtilen bölgeye yazın.</span><span class="sxs-lookup"><span data-stu-id="2660b-110">The **New-AzDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="2660b-111">**Kayıt kümesi** nesnesi aynı adda ve türde bir DNS kaydı kümesidir.</span><span class="sxs-lookup"><span data-stu-id="2660b-111">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="2660b-112">Adın tam adı değil bölgeye göreli olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="2660b-112">Note that the name is relative to the zone and not the fully qualified name.</span></span>
<span data-ttu-id="2660b-113">*Dnskayıtları* parametresi, kayıt kümesindeki kayıtları belirtir.</span><span class="sxs-lookup"><span data-stu-id="2660b-113">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="2660b-114">Bu parametre, New-AzDnsRecordConfig kullanılarak oluşturulan bir dizi DNS kaydını alır.</span><span class="sxs-lookup"><span data-stu-id="2660b-114">This parameter takes an array of DNS records, constructed using New-AzDnsRecordConfig.</span></span>
<span data-ttu-id="2660b-115">Bu cmdlet 'e bir **dnsZone** nesnesi geçirmek için ardışık düzen işlecini kullanabilir veya bir **dnsZone** nesnesini *bölge* parametresi olarak geçirebilirsiniz veya alternatif olarak bölgeyi adıyla belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2660b-115">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>
<span data-ttu-id="2660b-116">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için *Confirm* parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2660b-116">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="2660b-117">Eşleşen bir **kayıt kümesi** zaten varsa (aynı ad ve kayıt türü), *üzerine yazma* parametresini belirtmeniz gerekir, aksi halde cmdlet yeni bir **kayıt kümesi** oluşturmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="2660b-117">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="2660b-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2660b-118">EXAMPLES</span></span>

### <span data-ttu-id="2660b-119">Örnek 1: A türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2660b-119">Example 1: Create a RecordSet of type A</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzDnsRecordConfig to add each record to the $Records array,
# then call New-AzDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="2660b-120">Bu örnek, Zone myzone.com 'de www adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2660b-120">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="2660b-121">Kayıt kümesi A türünde ve 1 saatlik bir TTL (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="2660b-121">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="2660b-122">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="2660b-122">It contains a single DNS record.</span></span>

### <span data-ttu-id="2660b-123">Örnek 2: AAAA türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2660b-123">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="2660b-124">Bu örnek, Zone myzone.com 'de www adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2660b-124">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="2660b-125">Kayıt kümesi AAAA türünde ve 1 saatlik bir TTL değeri (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="2660b-125">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="2660b-126">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="2660b-126">It contains a single DNS record.</span></span>
<span data-ttu-id="2660b-127">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="2660b-127">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="2660b-128">Örnek 3: CNAME türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2660b-128">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="2660b-129">Bu örnek, Zone myzone.com 'de www adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2660b-129">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="2660b-130">Kayıt kümesi CNAME türünde ve 1 saat (3600 saniye) TTL değeri vardır.</span><span class="sxs-lookup"><span data-stu-id="2660b-130">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="2660b-131">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="2660b-131">It contains a single DNS record.</span></span>
<span data-ttu-id="2660b-132">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="2660b-132">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="2660b-133">Örnek 4: MX türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2660b-133">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="2660b-134">Bu komut, Zone myzone.com 'de www adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2660b-134">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="2660b-135">Kayıt kümesi MX türünde ve TTL 1 saat (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="2660b-135">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="2660b-136">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="2660b-136">It contains a single DNS record.</span></span>
<span data-ttu-id="2660b-137">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="2660b-137">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="2660b-138">Örnek 5: NS türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2660b-138">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="2660b-139">Bu komut, ns1 adında bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2660b-139">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="2660b-140">Kayıt kümesi NS türünde ve TTL 1 saat (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="2660b-140">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="2660b-141">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="2660b-141">It contains a single DNS record.</span></span>
<span data-ttu-id="2660b-142">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="2660b-142">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="2660b-143">Örnek 6: PTR türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2660b-143">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="2660b-144">Bu komut, 3.2.1.in-addr. arpa bölgesinde 4 adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2660b-144">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="2660b-145">Kayıt kümesi PTR türünde ve bir TTL değeri 1 saattir (3600 saniye).</span><span class="sxs-lookup"><span data-stu-id="2660b-145">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="2660b-146">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="2660b-146">It contains a single DNS record.</span></span>
<span data-ttu-id="2660b-147">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="2660b-147">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="2660b-148">Örnek 7: SRV türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2660b-148">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="2660b-149">Bu komut, Zone myzone.com 'de _sıp. _tcp adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2660b-149">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="2660b-150">Kayıt kümesi, SRV türünde ve 1 saatlik bir TTL değeri (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="2660b-150">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="2660b-151">Tek bir DNS kaydı içerir ve IP adresi 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="2660b-151">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="2660b-152">Hizmet (Sip) ve protokol (TCP), kayıt verilerinin bir parçası olarak değil, kayıt kümesi adının bir parçası olarak belirtilir.</span><span class="sxs-lookup"><span data-stu-id="2660b-152">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="2660b-153">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="2660b-153">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="2660b-154">Örnek 8: TXT türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2660b-154">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="2660b-155">Bu komut, Zone myzone.com 'de metin adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2660b-155">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="2660b-156">Kayıt kümesi TXT türünde ve 1 saatlik bir TTL (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="2660b-156">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="2660b-157">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="2660b-157">It contains a single DNS record.</span></span>
<span data-ttu-id="2660b-158">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="2660b-158">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="2660b-159">Örnek 9: bölgede kayıt kümesi Apex</span><span class="sxs-lookup"><span data-stu-id="2660b-159">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="2660b-160">Bu komut, Apex (veya kökünde) bir **kayıt kümesi** oluşturur MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="2660b-160">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="2660b-161">Bunu yapmak için, kayıt kümesi adı "@" (çift tırnak işaretleri dahil) olarak belirtilir.</span><span class="sxs-lookup"><span data-stu-id="2660b-161">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>
<span data-ttu-id="2660b-162">Bir bölgenin Apex CNAME kayıtları oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="2660b-162">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="2660b-163">Bu, DNS standartlarının bir kısıtlamadır; Azure DNS 'nin bir sınırlaması değildir.</span><span class="sxs-lookup"><span data-stu-id="2660b-163">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>
<span data-ttu-id="2660b-164">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="2660b-164">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="2660b-165">Örnek 10: joker karakter kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2660b-165">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="2660b-166">Bu komut, Zone myzone.com adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2660b-166">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="2660b-167">Bu, joker karakter kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="2660b-167">This is a wildcard record set.</span></span>
<span data-ttu-id="2660b-168">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="2660b-168">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="2660b-169">Örnek 11: boş bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2660b-169">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="2660b-170">Bu komut, Zone myzone.com 'de www adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2660b-170">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="2660b-171">Kayıt kümesi A türünde ve 1 saatlik bir TTL (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="2660b-171">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="2660b-172">Bu, daha sonra kayıt ekleyebileceğiniz bir yer tutucu görevi gören boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="2660b-172">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="2660b-173">Örnek 12: kayıt kümesi oluşturma ve tüm onayı gösterme</span><span class="sxs-lookup"><span data-stu-id="2660b-173">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="2660b-174">Bu komut bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2660b-174">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="2660b-175">Overwrite parametresi, bu kayıt kümesinin aynı ada ve türe sahip önceden var olan herhangi bir kayıt kümesinin üzerine *yazılmasını* sağlar (Bu kayıt kümesinde varolan kayıtlar kaybolur).</span><span class="sxs-lookup"><span data-stu-id="2660b-175">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="2660b-176">$False değeri olan *Confirm* parametresi, onay istemini bastırır.</span><span class="sxs-lookup"><span data-stu-id="2660b-176">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="2660b-177">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2660b-177">PARAMETERS</span></span>

### <span data-ttu-id="2660b-178">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2660b-178">-DefaultProfile</span></span>
<span data-ttu-id="2660b-179">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2660b-179">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2660b-180">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="2660b-180">-DnsRecords</span></span>
<span data-ttu-id="2660b-181">Kayıt kümesine eklenecek DNS kayıtlarının dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2660b-181">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="2660b-182">DNS kayıt nesneleri oluşturmak için New-AzDnsRecordConfig cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2660b-182">You can use the New-AzDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="2660b-183">Daha fazla bilgi için örneklere bakın.</span><span class="sxs-lookup"><span data-stu-id="2660b-183">See the examples for more information.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordBase[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2660b-184">-Metadata</span><span class="sxs-lookup"><span data-stu-id="2660b-184">-Metadata</span></span>
<span data-ttu-id="2660b-185">Kayıt kümesiyle ilişkilendirilecek meta veri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2660b-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="2660b-186">Meta veriler, karma tablolar olarak temsil edilen ad değeri çiftleri kullanılarak belirtilmiştir (örneğin @ (@ {"Name" = "Bölüm"; "Değer" = "alışveriş"}, @ {"ad" = "env"; "Değer" = "üretim"}).</span><span class="sxs-lookup"><span data-stu-id="2660b-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @(@{"Name"="dept"; "Value"="shopping"}, @{"Name"="env"; "Value"="production"}).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2660b-187">-Ad</span><span class="sxs-lookup"><span data-stu-id="2660b-187">-Name</span></span>
<span data-ttu-id="2660b-188">Oluşturulacak **kayıt kümesinin** adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2660b-188">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="2660b-189">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="2660b-189">-Overwrite</span></span>
<span data-ttu-id="2660b-190">Zaten varsa, bu cmdlet 'in belirtilen **kayıt kümesini** üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2660b-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2660b-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="2660b-191">-RecordType</span></span>
<span data-ttu-id="2660b-192">Oluşturulacak DNS kaydı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2660b-192">Specifies the type of DNS record to create.</span></span>
<span data-ttu-id="2660b-193">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="2660b-193">Valid values are:</span></span>
- <span data-ttu-id="2660b-194">Bir</span><span class="sxs-lookup"><span data-stu-id="2660b-194">A</span></span>
- <span data-ttu-id="2660b-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="2660b-195">AAAA</span></span>
- <span data-ttu-id="2660b-196">KAYDıNı</span><span class="sxs-lookup"><span data-stu-id="2660b-196">CNAME</span></span>
- <span data-ttu-id="2660b-197">DOSYASıNA</span><span class="sxs-lookup"><span data-stu-id="2660b-197">MX</span></span>
- <span data-ttu-id="2660b-198">Seç</span><span class="sxs-lookup"><span data-stu-id="2660b-198">NS</span></span>
- <span data-ttu-id="2660b-199">PTR</span><span class="sxs-lookup"><span data-stu-id="2660b-199">PTR</span></span>
- <span data-ttu-id="2660b-200">SRV</span><span class="sxs-lookup"><span data-stu-id="2660b-200">SRV</span></span>
- <span data-ttu-id="2660b-201">Bölge oluşturulduğunda ve el ile oluşturuoluşturuoluşturumıyorsa TXT SOA kayıtları otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2660b-201">TXT SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2660b-202">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2660b-202">-ResourceGroupName</span></span>
<span data-ttu-id="2660b-203">DNS bölgesini içeren kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2660b-203">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="2660b-204">Bölge adını belirtmek için de *BölgeAdı* parametresini belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2660b-204">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>
<span data-ttu-id="2660b-205">Alternatif olarak, bölge ve kaynak grubunu, *bölge* parametresini kullanarak bir DNS bölgesi nesnesini geçirerek belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2660b-205">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2660b-206">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="2660b-206">-TargetResourceId</span></span>
<span data-ttu-id="2660b-207">Diğer ad hedef kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="2660b-207">Alias Target Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2660b-208">-TTL</span><span class="sxs-lookup"><span data-stu-id="2660b-208">-Ttl</span></span>
<span data-ttu-id="2660b-209">DNS kayıt kümesi için yaşam süresi (TTL) belirtir.</span><span class="sxs-lookup"><span data-stu-id="2660b-209">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: Fields, Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2660b-210">-Bölge</span><span class="sxs-lookup"><span data-stu-id="2660b-210">-Zone</span></span>
<span data-ttu-id="2660b-211">**Kayıt kümesinin** oluşturulacağı dnsZone öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2660b-211">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="2660b-212">Alternatif olarak, bölgeyi *BölgeAdı* ve *resourcegroupname* parametrelerini kullanarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2660b-212">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2660b-213">-BölgeAdı</span><span class="sxs-lookup"><span data-stu-id="2660b-213">-ZoneName</span></span>
<span data-ttu-id="2660b-214">**Kayıt kümesinin** oluşturulacağı bölgenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2660b-214">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="2660b-215">Ayrıca, *Resourcegroupname* parametresini kullanarak bölgeyi içeren kaynak grubunu da belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2660b-215">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="2660b-216">Alternatif olarak, bölge ve kaynak grubunu, *bölge* parametresini kullanarak bir DNS bölgesi nesnesini geçirerek belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2660b-216">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2660b-217">-Onay</span><span class="sxs-lookup"><span data-stu-id="2660b-217">-Confirm</span></span>
<span data-ttu-id="2660b-218">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2660b-218">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2660b-219">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2660b-219">-WhatIf</span></span>
<span data-ttu-id="2660b-220">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2660b-220">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2660b-221">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2660b-221">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2660b-222">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2660b-222">CommonParameters</span></span>
<span data-ttu-id="2660b-223">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2660b-223">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2660b-224">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2660b-224">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2660b-225">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2660b-225">INPUTS</span></span>

### <span data-ttu-id="2660b-226">System. String</span><span class="sxs-lookup"><span data-stu-id="2660b-226">System.String</span></span>

### <span data-ttu-id="2660b-227">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="2660b-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="2660b-228">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="2660b-228">System.UInt32</span></span>

### <span data-ttu-id="2660b-229">Microsoft. Azure. Management. DNS. modeller. RecordType</span><span class="sxs-lookup"><span data-stu-id="2660b-229">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="2660b-230">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2660b-230">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2660b-231">Microsoft. Azure. Commands. DNS. DnsRecordBase []</span><span class="sxs-lookup"><span data-stu-id="2660b-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span></span>

## <span data-ttu-id="2660b-232">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2660b-232">OUTPUTS</span></span>

### <span data-ttu-id="2660b-233">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2660b-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="2660b-234">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2660b-234">NOTES</span></span>
<span data-ttu-id="2660b-235">*Confirm* parametresini kullanarak, bu cmdlet 'in onayınızı isteyip istemediğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="2660b-235">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="2660b-236">Varsayılan olarak, $ConfirmPreference Windows PowerShell değişkeninde orta veya düşük bir değer varsa cmdlet onay ister.</span><span class="sxs-lookup"><span data-stu-id="2660b-236">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="2660b-237">*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="2660b-237">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="2660b-238">*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="2660b-238">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="2660b-239">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2660b-239">RELATED LINKS</span></span>

[<span data-ttu-id="2660b-240">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="2660b-240">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="2660b-241">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2660b-241">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="2660b-242">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="2660b-242">New-AzDnsRecordConfig</span></span>](./New-AzDnsRecordConfig.md)

[<span data-ttu-id="2660b-243">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2660b-243">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="2660b-244">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2660b-244">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)