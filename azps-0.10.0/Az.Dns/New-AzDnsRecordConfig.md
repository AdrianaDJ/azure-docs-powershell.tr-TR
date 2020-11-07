---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsRecordConfig.md
ms.openlocfilehash: 0bc25aecae445ba18634df578de590f514640c07
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936728"
---
# <span data-ttu-id="8fb68-101">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="8fb68-101">New-AzDnsRecordConfig</span></span>

## <span data-ttu-id="8fb68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fb68-102">SYNOPSIS</span></span>
<span data-ttu-id="8fb68-103">Yeni bir DNS kaydı yerel nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8fb68-103">Creates a new DNS record local object.</span></span>

## <span data-ttu-id="8fb68-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8fb68-104">SYNTAX</span></span>

### <span data-ttu-id="8fb68-105">Bir</span><span class="sxs-lookup"><span data-stu-id="8fb68-105">A</span></span>
```
New-AzDnsRecordConfig -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="8fb68-106">Aaaa</span><span class="sxs-lookup"><span data-stu-id="8fb68-106">Aaaa</span></span>
```
New-AzDnsRecordConfig -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="8fb68-107">Seç</span><span class="sxs-lookup"><span data-stu-id="8fb68-107">Ns</span></span>
```
New-AzDnsRecordConfig -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="8fb68-108">Dosyasına</span><span class="sxs-lookup"><span data-stu-id="8fb68-108">Mx</span></span>
```
New-AzDnsRecordConfig -Exchange <String> -Preference <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="8fb68-109">PTR</span><span class="sxs-lookup"><span data-stu-id="8fb68-109">Ptr</span></span>
```
New-AzDnsRecordConfig -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="8fb68-110">,</span><span class="sxs-lookup"><span data-stu-id="8fb68-110">Txt</span></span>
```
New-AzDnsRecordConfig -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="8fb68-111">SRV</span><span class="sxs-lookup"><span data-stu-id="8fb68-111">Srv</span></span>
```
New-AzDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="8fb68-112">Kaydını</span><span class="sxs-lookup"><span data-stu-id="8fb68-112">CName</span></span>
```
New-AzDnsRecordConfig -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="8fb68-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="8fb68-113">DESCRIPTION</span></span>
<span data-ttu-id="8fb68-114">**New-AzDnsRecordConfig** cmdlet 'i yerel bir **dnsRecord** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8fb68-114">The **New-AzDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="8fb68-115">Bu nesnelerin bir dizisi, kayıt kümesinde oluşturulacak kayıtları belirtmek için *dnsrecords* parametresini kullanarak New-AzDnsRecordSet cmdlet 'ine geçirilir.</span><span class="sxs-lookup"><span data-stu-id="8fb68-115">An array of these objects is passed to the New-AzDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="8fb68-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8fb68-116">EXAMPLES</span></span>

### <span data-ttu-id="8fb68-117">Örnek 1: A türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8fb68-117">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="8fb68-118">Bu örnek, Zone myzone.com 'de www adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8fb68-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="8fb68-119">Kayıt kümesi A türünde ve 1 saatlik bir TTL (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="8fb68-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="8fb68-120">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="8fb68-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="8fb68-121">Örnek 2: AAAA türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8fb68-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="8fb68-122">Bu örnek, Zone myzone.com 'de www adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8fb68-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="8fb68-123">Kayıt kümesi AAAA türünde ve 1 saatlik bir TTL değeri (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="8fb68-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="8fb68-124">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="8fb68-124">It contains a single DNS record.</span></span>

<span data-ttu-id="8fb68-125">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="8fb68-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="8fb68-126">Örnek 3: CNAME türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8fb68-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="8fb68-127">Bu örnek, Zone myzone.com 'de www adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8fb68-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="8fb68-128">Kayıt kümesi CNAME türünde ve 1 saat (3600 saniye) TTL değeri vardır.</span><span class="sxs-lookup"><span data-stu-id="8fb68-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="8fb68-129">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="8fb68-129">It contains a single DNS record.</span></span>

<span data-ttu-id="8fb68-130">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="8fb68-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="8fb68-131">Örnek 4: MX türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8fb68-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="8fb68-132">Bu komut, Zone myzone.com 'de www adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8fb68-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="8fb68-133">Kayıt kümesi MX türünde ve TTL 1 saat (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="8fb68-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="8fb68-134">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="8fb68-134">It contains a single DNS record.</span></span>

<span data-ttu-id="8fb68-135">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="8fb68-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="8fb68-136">Örnek 5: NS türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8fb68-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="8fb68-137">Bu komut, ns1 adında bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8fb68-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="8fb68-138">Kayıt kümesi NS türünde ve TTL 1 saat (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="8fb68-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="8fb68-139">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="8fb68-139">It contains a single DNS record.</span></span>

<span data-ttu-id="8fb68-140">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="8fb68-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="8fb68-141">Örnek 6: PTR türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8fb68-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="8fb68-142">Bu komut, 3.2.1.in-addr. arpa bölgesinde 4 adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8fb68-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="8fb68-143">Kayıt kümesi PTR türünde ve bir TTL değeri 1 saattir (3600 saniye).</span><span class="sxs-lookup"><span data-stu-id="8fb68-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="8fb68-144">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="8fb68-144">It contains a single DNS record.</span></span>

<span data-ttu-id="8fb68-145">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="8fb68-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="8fb68-146">Örnek 7: SRV türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8fb68-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="8fb68-147">Bu komut, Zone myzone.com 'de _sıp. _tcp adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8fb68-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="8fb68-148">Kayıt kümesi, SRV türünde ve 1 saatlik bir TTL değeri (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="8fb68-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="8fb68-149">Tek bir DNS kaydı içerir ve IP adresi 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="8fb68-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="8fb68-150">Hizmet (Sip) ve protokol (TCP), kayıt verilerinin bir parçası olarak değil, kayıt kümesi adının bir parçası olarak belirtilir.</span><span class="sxs-lookup"><span data-stu-id="8fb68-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="8fb68-151">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="8fb68-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="8fb68-152">Örnek 8: TXT türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8fb68-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="8fb68-153">Bu komut, Zone myzone.com 'de metin adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8fb68-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="8fb68-154">Kayıt kümesi TXT türünde ve 1 saatlik bir TTL (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="8fb68-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="8fb68-155">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="8fb68-155">It contains a single DNS record.</span></span>

<span data-ttu-id="8fb68-156">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="8fb68-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="8fb68-157">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8fb68-157">PARAMETERS</span></span>

### <span data-ttu-id="8fb68-158">-CNAME</span><span class="sxs-lookup"><span data-stu-id="8fb68-158">-Cname</span></span>
<span data-ttu-id="8fb68-159">Kurallı ad (CNAME) kaydı için etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb68-159">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: String
Parameter Sets: CName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fb68-160">-Exchange</span><span class="sxs-lookup"><span data-stu-id="8fb68-160">-Exchange</span></span>
<span data-ttu-id="8fb68-161">Posta alışverişi (MX) kaydı için posta Exchange sunucusu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb68-161">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: String
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fb68-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="8fb68-162">-Ipv4Address</span></span>
<span data-ttu-id="8fb68-163">Bir kaydın IPv4 adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb68-163">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="8fb68-164">-IPv6Adresi</span><span class="sxs-lookup"><span data-stu-id="8fb68-164">-Ipv6Address</span></span>
<span data-ttu-id="8fb68-165">AAAA kaydı için IPv6 adresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb68-165">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: String
Parameter Sets: Aaaa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fb68-166">-Nsdadı</span><span class="sxs-lookup"><span data-stu-id="8fb68-166">-Nsdname</span></span>
<span data-ttu-id="8fb68-167">Ad sunucusu (NS) kaydı için ad sunucusu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb68-167">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: String
Parameter Sets: Ns
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fb68-168">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="8fb68-168">-Port</span></span>
<span data-ttu-id="8fb68-169">Hizmet (SRV) kaydı için bağlantı noktası belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb68-169">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fb68-170">-Tercih</span><span class="sxs-lookup"><span data-stu-id="8fb68-170">-Preference</span></span>
<span data-ttu-id="8fb68-171">Bir MX kaydı için tercih belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb68-171">Specifies the preference for an MX record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fb68-172">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="8fb68-172">-Priority</span></span>
<span data-ttu-id="8fb68-173">Bir SRV kaydının önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb68-173">Specifies the priority for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fb68-174">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="8fb68-174">-Ptrdname</span></span>
<span data-ttu-id="8fb68-175">İşaretçi kaynağı (PTR) kaydının hedef etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb68-175">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: String
Parameter Sets: Ptr
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fb68-176">-Hedef</span><span class="sxs-lookup"><span data-stu-id="8fb68-176">-Target</span></span>
<span data-ttu-id="8fb68-177">Bir SRV kaydının hedefini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb68-177">Specifies the target for an SRV record.</span></span>

```yaml
Type: String
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fb68-178">-Değer</span><span class="sxs-lookup"><span data-stu-id="8fb68-178">-Value</span></span>
<span data-ttu-id="8fb68-179">Bir TXT kaydının değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb68-179">Specifies the value for a TXT record.</span></span>

```yaml
Type: String
Parameter Sets: Txt
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fb68-180">-Kalınlık</span><span class="sxs-lookup"><span data-stu-id="8fb68-180">-Weight</span></span>
<span data-ttu-id="8fb68-181">Bir SRV kaydı için ağırlığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb68-181">Specifies the weight for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fb68-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fb68-182">CommonParameters</span></span>
<span data-ttu-id="8fb68-183">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8fb68-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fb68-184">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fb68-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fb68-185">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8fb68-185">INPUTS</span></span>

### <span data-ttu-id="8fb68-186">Yabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8fb68-186">None.</span></span>

## <span data-ttu-id="8fb68-187">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8fb68-187">OUTPUTS</span></span>

### <span data-ttu-id="8fb68-188">Microsoft. Azure. Commands. DNS. DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="8fb68-188">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="8fb68-189">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8fb68-189">NOTES</span></span>

## <span data-ttu-id="8fb68-190">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8fb68-190">RELATED LINKS</span></span>

[<span data-ttu-id="8fb68-191">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="8fb68-191">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="8fb68-192">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8fb68-192">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="8fb68-193">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="8fb68-193">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)
