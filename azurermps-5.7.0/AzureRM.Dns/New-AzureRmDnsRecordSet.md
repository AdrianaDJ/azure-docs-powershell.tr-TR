---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordSet.md
ms.openlocfilehash: 9896a8e1cfd2e3c0dc3887513d93e902260b82c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764031"
---
# <span data-ttu-id="1d900-101">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1d900-101">New-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="1d900-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d900-102">SYNOPSIS</span></span>
<span data-ttu-id="1d900-103">DNS kayıt kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d900-103">Creates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d900-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1d900-104">SYNTAX</span></span>

### <span data-ttu-id="1d900-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="1d900-105">Fields</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d900-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="1d900-106">Object</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d900-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d900-107">DESCRIPTION</span></span>
<span data-ttu-id="1d900-108">**Yeni-AzureRmDnsRecordSet** cmdlet 'i belirtilen ada sahip yeni bir etki alanı adı SISTEMI (DNS) kaydı oluşturur ve belirtilen bölgeye yazın.</span><span class="sxs-lookup"><span data-stu-id="1d900-108">The **New-AzureRmDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="1d900-109">**Kayıt kümesi** nesnesi aynı adda ve türde bir DNS kaydı kümesidir.</span><span class="sxs-lookup"><span data-stu-id="1d900-109">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="1d900-110">Adın tam adı değil bölgeye göreli olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="1d900-110">Note that the name is relative to the zone and not the fully qualified name.</span></span>

<span data-ttu-id="1d900-111">*Dnskayıtları* parametresi, kayıt kümesindeki kayıtları belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d900-111">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="1d900-112">Bu parametre, New-AzureRmDnsRecordConfig kullanılarak oluşturulan bir dizi DNS kaydını alır.</span><span class="sxs-lookup"><span data-stu-id="1d900-112">This parameter takes an array of DNS records, constructed using New-AzureRmDnsRecordConfig.</span></span>

<span data-ttu-id="1d900-113">Bu cmdlet 'e bir **dnsZone** nesnesi geçirmek için ardışık düzen işlecini kullanabilir veya bir **dnsZone** nesnesini *bölge* parametresi olarak geçirebilirsiniz veya alternatif olarak bölgeyi adıyla belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d900-113">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>

<span data-ttu-id="1d900-114">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için *Confirm* parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d900-114">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="1d900-115">Eşleşen bir **kayıt kümesi** zaten varsa (aynı ad ve kayıt türü), *üzerine yazma* parametresini belirtmeniz gerekir, aksi halde cmdlet yeni bir **kayıt kümesi** oluşturmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="1d900-115">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="1d900-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1d900-116">EXAMPLES</span></span>

### <span data-ttu-id="1d900-117">Örnek 1: A türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1d900-117">Example 1: Create a RecordSet of type A</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzureRmDnsRecordConfig to add each record to the $Records array,
# then call New-AzureRmDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="1d900-118">Bu örnek, Zone myzone.com 'de www adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d900-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="1d900-119">Kayıt kümesi A türünde ve 1 saatlik bir TTL (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="1d900-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="1d900-120">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="1d900-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="1d900-121">Örnek 2: AAAA türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1d900-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="1d900-122">Bu örnek, Zone myzone.com 'de www adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d900-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="1d900-123">Kayıt kümesi AAAA türünde ve 1 saatlik bir TTL değeri (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="1d900-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="1d900-124">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="1d900-124">It contains a single DNS record.</span></span>

<span data-ttu-id="1d900-125">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="1d900-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="1d900-126">Örnek 3: CNAME türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1d900-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="1d900-127">Bu örnek, Zone myzone.com 'de www adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d900-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="1d900-128">Kayıt kümesi CNAME türünde ve 1 saat (3600 saniye) TTL değeri vardır.</span><span class="sxs-lookup"><span data-stu-id="1d900-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="1d900-129">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="1d900-129">It contains a single DNS record.</span></span>

<span data-ttu-id="1d900-130">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="1d900-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="1d900-131">Örnek 4: MX türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1d900-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="1d900-132">Bu komut, Zone myzone.com 'de www adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d900-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="1d900-133">Kayıt kümesi MX türünde ve TTL 1 saat (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="1d900-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="1d900-134">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="1d900-134">It contains a single DNS record.</span></span>

<span data-ttu-id="1d900-135">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="1d900-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="1d900-136">Örnek 5: NS türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1d900-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="1d900-137">Bu komut, ns1 adında bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d900-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="1d900-138">Kayıt kümesi NS türünde ve TTL 1 saat (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="1d900-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="1d900-139">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="1d900-139">It contains a single DNS record.</span></span>

<span data-ttu-id="1d900-140">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="1d900-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="1d900-141">Örnek 6: PTR türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1d900-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="1d900-142">Bu komut, 3.2.1.in-addr. arpa bölgesinde 4 adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d900-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="1d900-143">Kayıt kümesi PTR türünde ve bir TTL değeri 1 saattir (3600 saniye).</span><span class="sxs-lookup"><span data-stu-id="1d900-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="1d900-144">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="1d900-144">It contains a single DNS record.</span></span>

<span data-ttu-id="1d900-145">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="1d900-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="1d900-146">Örnek 7: SRV türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1d900-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="1d900-147">Bu komut, Zone myzone.com 'de _sıp. _tcp adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d900-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="1d900-148">Kayıt kümesi, SRV türünde ve 1 saatlik bir TTL değeri (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="1d900-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="1d900-149">Tek bir DNS kaydı içerir ve IP adresi 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="1d900-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="1d900-150">Hizmet (Sip) ve protokol (TCP), kayıt verilerinin bir parçası olarak değil, kayıt kümesi adının bir parçası olarak belirtilir.</span><span class="sxs-lookup"><span data-stu-id="1d900-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="1d900-151">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="1d900-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="1d900-152">Örnek 8: TXT türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1d900-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="1d900-153">Bu komut, Zone myzone.com 'de metin adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d900-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="1d900-154">Kayıt kümesi TXT türünde ve 1 saatlik bir TTL (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="1d900-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="1d900-155">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="1d900-155">It contains a single DNS record.</span></span>

<span data-ttu-id="1d900-156">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="1d900-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="1d900-157">Örnek 9: bölgede kayıt kümesi Apex</span><span class="sxs-lookup"><span data-stu-id="1d900-157">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="1d900-158">Bu komut, Apex (veya kökünde) bir **kayıt kümesi** oluşturur MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="1d900-158">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="1d900-159">Bunu yapmak için, kayıt kümesi adı "@" (çift tırnak işaretleri dahil) olarak belirtilir.</span><span class="sxs-lookup"><span data-stu-id="1d900-159">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>

<span data-ttu-id="1d900-160">Bir bölgenin Apex CNAME kayıtları oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="1d900-160">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="1d900-161">Bu, DNS standartlarının bir kısıtlamadır; Azure DNS 'nin bir sınırlaması değildir.</span><span class="sxs-lookup"><span data-stu-id="1d900-161">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>

<span data-ttu-id="1d900-162">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="1d900-162">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="1d900-163">Örnek 10: joker karakter kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1d900-163">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="1d900-164">Bu komut, Zone myzone.com adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d900-164">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="1d900-165">Bu, joker karakter kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="1d900-165">This is a wildcard record set.</span></span>

<span data-ttu-id="1d900-166">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="1d900-166">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="1d900-167">Örnek 11: boş bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1d900-167">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="1d900-168">Bu komut, Zone myzone.com 'de www adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d900-168">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="1d900-169">Kayıt kümesi A türünde ve 1 saatlik bir TTL (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="1d900-169">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="1d900-170">Bu, daha sonra kayıt ekleyebileceğiniz bir yer tutucu görevi gören boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="1d900-170">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="1d900-171">Örnek 12: kayıt kümesi oluşturma ve tüm onayı gösterme</span><span class="sxs-lookup"><span data-stu-id="1d900-171">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="1d900-172">Bu komut bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d900-172">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="1d900-173">Overwrite parametresi, bu kayıt kümesinin aynı ada ve türe sahip önceden var olan herhangi bir kayıt kümesinin üzerine *yazılmasını* sağlar (Bu kayıt kümesinde varolan kayıtlar kaybolur).</span><span class="sxs-lookup"><span data-stu-id="1d900-173">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="1d900-174">$False değeri olan *Confirm* parametresi, onay istemini bastırır.</span><span class="sxs-lookup"><span data-stu-id="1d900-174">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="1d900-175">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1d900-175">PARAMETERS</span></span>

### <span data-ttu-id="1d900-176">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d900-176">-DefaultProfile</span></span>
<span data-ttu-id="1d900-177">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1d900-177">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d900-178">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="1d900-178">-DnsRecords</span></span>
<span data-ttu-id="1d900-179">Kayıt kümesine eklenecek DNS kayıtlarının dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d900-179">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="1d900-180">DNS kayıt nesneleri oluşturmak için New-AzureRmDnsRecordConfig cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d900-180">You can use the New-AzureRmDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="1d900-181">Daha fazla bilgi için örneklere bakın.</span><span class="sxs-lookup"><span data-stu-id="1d900-181">See the examples for more information.</span></span>

```yaml
Type: DnsRecordBase[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d900-182">-Force</span><span class="sxs-lookup"><span data-stu-id="1d900-182">-Force</span></span>
<span data-ttu-id="1d900-183">Bu parametre bu cmdlet için onaylanmaz.</span><span class="sxs-lookup"><span data-stu-id="1d900-183">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="1d900-184">Gelecek sürümde kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="1d900-184">It will be removed in a future release.</span></span>

<span data-ttu-id="1d900-185">Bu cmdlet 'in sizi sorana isteyip istemediğini kontrol etmek için, *Confirm* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1d900-185">To control whether this cmdlet prompts you for comfirmation, use the *Confirm* parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d900-186">-Metadata</span><span class="sxs-lookup"><span data-stu-id="1d900-186">-Metadata</span></span>
<span data-ttu-id="1d900-187">Kayıt kümesiyle ilişkilendirilecek meta veri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d900-187">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="1d900-188">Meta veriler, karma tablolar olarak temsil edilen ad değeri çiftleri kullanılarak belirtilmiştir (örneğin @ (@ {"Name" = "Bölüm"; "Değer" = "alışveriş"}, @ {"ad" = "env"; "Değer" = "üretim"}).</span><span class="sxs-lookup"><span data-stu-id="1d900-188">Metadata is specified using name-value pairs that are represented as hash tables, for example @(@{"Name"="dept"; "Value"="shopping"}, @{"Name"="env"; "Value"="production"}).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d900-189">-Ad</span><span class="sxs-lookup"><span data-stu-id="1d900-189">-Name</span></span>
<span data-ttu-id="1d900-190">Oluşturulacak **kayıt kümesinin** adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d900-190">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="1d900-191">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="1d900-191">-Overwrite</span></span>
<span data-ttu-id="1d900-192">Zaten varsa, bu cmdlet 'in belirtilen **kayıt kümesini** üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d900-192">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d900-193">-RecordType</span><span class="sxs-lookup"><span data-stu-id="1d900-193">-RecordType</span></span>
<span data-ttu-id="1d900-194">Oluşturulacak DNS kaydı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d900-194">Specifies the type of DNS record to create.</span></span>

<span data-ttu-id="1d900-195">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="1d900-195">Valid values are:</span></span>

- <span data-ttu-id="1d900-196">Bir</span><span class="sxs-lookup"><span data-stu-id="1d900-196">A</span></span>
- <span data-ttu-id="1d900-197">AAAA</span><span class="sxs-lookup"><span data-stu-id="1d900-197">AAAA</span></span>
- <span data-ttu-id="1d900-198">KAYDıNı</span><span class="sxs-lookup"><span data-stu-id="1d900-198">CNAME</span></span>
- <span data-ttu-id="1d900-199">DOSYASıNA</span><span class="sxs-lookup"><span data-stu-id="1d900-199">MX</span></span>
- <span data-ttu-id="1d900-200">Seç</span><span class="sxs-lookup"><span data-stu-id="1d900-200">NS</span></span>
- <span data-ttu-id="1d900-201">PTR</span><span class="sxs-lookup"><span data-stu-id="1d900-201">PTR</span></span>
- <span data-ttu-id="1d900-202">SRV</span><span class="sxs-lookup"><span data-stu-id="1d900-202">SRV</span></span>
- <span data-ttu-id="1d900-203">,</span><span class="sxs-lookup"><span data-stu-id="1d900-203">TXT</span></span>

<span data-ttu-id="1d900-204">SOA kayıtları bölge oluşturulduğunda otomatik olarak oluşturulur ve el ile oluşturulamaz.</span><span class="sxs-lookup"><span data-stu-id="1d900-204">SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d900-205">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d900-205">-ResourceGroupName</span></span>
<span data-ttu-id="1d900-206">DNS bölgesini içeren kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d900-206">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="1d900-207">Bölge adını belirtmek için de *BölgeAdı* parametresini belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1d900-207">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>

<span data-ttu-id="1d900-208">Alternatif olarak, bölge ve kaynak grubunu, *bölge* parametresini kullanarak bir DNS bölgesi nesnesini geçirerek belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d900-208">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d900-209">-TTL</span><span class="sxs-lookup"><span data-stu-id="1d900-209">-Ttl</span></span>
<span data-ttu-id="1d900-210">DNS kayıt kümesi için yaşam süresi (TTL) belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d900-210">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d900-211">-Bölge</span><span class="sxs-lookup"><span data-stu-id="1d900-211">-Zone</span></span>
<span data-ttu-id="1d900-212">**Kayıt kümesinin** oluşturulacağı dnsZone öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d900-212">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="1d900-213">Alternatif olarak, bölgeyi *BölgeAdı* ve *resourcegroupname* parametrelerini kullanarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d900-213">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d900-214">-BölgeAdı</span><span class="sxs-lookup"><span data-stu-id="1d900-214">-ZoneName</span></span>
<span data-ttu-id="1d900-215">**Kayıt kümesinin** oluşturulacağı bölgenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d900-215">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="1d900-216">Ayrıca, *Resourcegroupname* parametresini kullanarak bölgeyi içeren kaynak grubunu da belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1d900-216">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="1d900-217">Alternatif olarak, bölge ve kaynak grubunu, *bölge* parametresini kullanarak bir DNS bölgesi nesnesini geçirerek belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d900-217">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d900-218">-Onay</span><span class="sxs-lookup"><span data-stu-id="1d900-218">-Confirm</span></span>
<span data-ttu-id="1d900-219">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1d900-219">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d900-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d900-220">-WhatIf</span></span>
<span data-ttu-id="1d900-221">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d900-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d900-222">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1d900-222">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d900-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d900-223">CommonParameters</span></span>
<span data-ttu-id="1d900-224">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1d900-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d900-225">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d900-225">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d900-226">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1d900-226">INPUTS</span></span>

### <span data-ttu-id="1d900-227">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="1d900-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="1d900-228">Bir DnsZone nesnesini bu cmdlet 'e boru edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d900-228">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="1d900-229">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1d900-229">OUTPUTS</span></span>

### <span data-ttu-id="1d900-230">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1d900-230">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="1d900-231">Bu cmdlet bir **Recordset** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="1d900-231">This cmdlet returns a **RecordSet** object.</span></span>

## <span data-ttu-id="1d900-232">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1d900-232">NOTES</span></span>
<span data-ttu-id="1d900-233">*Confirm* parametresini kullanarak, bu cmdlet 'in onayınızı isteyip istemediğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="1d900-233">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="1d900-234">Varsayılan olarak, $ConfirmPreference Windows PowerShell değişkeninde orta veya düşük bir değer varsa cmdlet onay ister.</span><span class="sxs-lookup"><span data-stu-id="1d900-234">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="1d900-235">*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="1d900-235">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="1d900-236">*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="1d900-236">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="1d900-237">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1d900-237">RELATED LINKS</span></span>

[<span data-ttu-id="1d900-238">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="1d900-238">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="1d900-239">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1d900-239">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="1d900-240">Yeni-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="1d900-240">New-AzureRmDnsRecordConfig</span></span>](./New-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="1d900-241">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1d900-241">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="1d900-242">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1d900-242">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)