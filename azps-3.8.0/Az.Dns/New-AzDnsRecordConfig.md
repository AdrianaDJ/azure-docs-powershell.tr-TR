---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
ms.openlocfilehash: cd503905cb36d14b0a0537978f02786da7189c33
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096916"
---
# <span data-ttu-id="9a208-101">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="9a208-101">New-AzDnsRecordConfig</span></span>

## <span data-ttu-id="9a208-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a208-102">SYNOPSIS</span></span>
<span data-ttu-id="9a208-103">Yeni bir DNS kaydı yerel nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9a208-103">Creates a new DNS record local object.</span></span>

## <span data-ttu-id="9a208-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9a208-104">SYNTAX</span></span>

### <span data-ttu-id="9a208-105">Bir</span><span class="sxs-lookup"><span data-stu-id="9a208-105">A</span></span>
```
New-AzDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a208-106">Aaaa</span><span class="sxs-lookup"><span data-stu-id="9a208-106">Aaaa</span></span>
```
New-AzDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a208-107">Seç</span><span class="sxs-lookup"><span data-stu-id="9a208-107">Ns</span></span>
```
New-AzDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a208-108">Dosyasına</span><span class="sxs-lookup"><span data-stu-id="9a208-108">Mx</span></span>
```
New-AzDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9a208-109">PTR</span><span class="sxs-lookup"><span data-stu-id="9a208-109">Ptr</span></span>
```
New-AzDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a208-110">,</span><span class="sxs-lookup"><span data-stu-id="9a208-110">Txt</span></span>
```
New-AzDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a208-111">SRV</span><span class="sxs-lookup"><span data-stu-id="9a208-111">Srv</span></span>
```
New-AzDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a208-112">Kaydını</span><span class="sxs-lookup"><span data-stu-id="9a208-112">CName</span></span>
```
New-AzDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a208-113">CAA</span><span class="sxs-lookup"><span data-stu-id="9a208-113">Caa</span></span>
```
New-AzDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a208-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="9a208-114">DESCRIPTION</span></span>
<span data-ttu-id="9a208-115">**New-AzDnsRecordConfig** cmdlet 'i yerel bir **dnsRecord** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9a208-115">The **New-AzDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="9a208-116">Bu nesnelerin bir dizisi, kayıt kümesinde oluşturulacak kayıtları belirtmek için *dnsrecords* parametresini kullanarak New-AzDnsRecordSet cmdlet 'ine geçirilir.</span><span class="sxs-lookup"><span data-stu-id="9a208-116">An array of these objects is passed to the New-AzDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="9a208-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9a208-117">EXAMPLES</span></span>

### <span data-ttu-id="9a208-118">Örnek 1: A türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="9a208-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="9a208-119">Bu örnek, Zone myzone.com 'de www adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9a208-119">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="9a208-120">Kayıt kümesi A türünde ve 1 saatlik bir TTL (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="9a208-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9a208-121">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="9a208-121">It contains a single DNS record.</span></span>

### <span data-ttu-id="9a208-122">Örnek 2: AAAA türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="9a208-122">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="9a208-123">Bu örnek, Zone myzone.com 'de www adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9a208-123">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="9a208-124">Kayıt kümesi AAAA türünde ve 1 saatlik bir TTL değeri (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="9a208-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9a208-125">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="9a208-125">It contains a single DNS record.</span></span>
<span data-ttu-id="9a208-126">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="9a208-126">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9a208-127">Örnek 3: CNAME türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="9a208-127">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="9a208-128">Bu örnek, Zone myzone.com 'de www adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9a208-128">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="9a208-129">Kayıt kümesi CNAME türünde ve 1 saat (3600 saniye) TTL değeri vardır.</span><span class="sxs-lookup"><span data-stu-id="9a208-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9a208-130">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="9a208-130">It contains a single DNS record.</span></span>
<span data-ttu-id="9a208-131">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="9a208-131">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9a208-132">Örnek 4: MX türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="9a208-132">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="9a208-133">Bu komut, Zone myzone.com 'de www adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9a208-133">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="9a208-134">Kayıt kümesi MX türünde ve TTL 1 saat (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="9a208-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9a208-135">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="9a208-135">It contains a single DNS record.</span></span>
<span data-ttu-id="9a208-136">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="9a208-136">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9a208-137">Örnek 5: NS türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="9a208-137">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="9a208-138">Bu komut, ns1 adında bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9a208-138">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="9a208-139">Kayıt kümesi NS türünde ve TTL 1 saat (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="9a208-139">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9a208-140">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="9a208-140">It contains a single DNS record.</span></span>
<span data-ttu-id="9a208-141">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="9a208-141">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9a208-142">Örnek 6: PTR türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="9a208-142">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="9a208-143">Bu komut, 3.2.1.in-addr. arpa bölgesinde 4 adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9a208-143">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="9a208-144">Kayıt kümesi PTR türünde ve bir TTL değeri 1 saattir (3600 saniye).</span><span class="sxs-lookup"><span data-stu-id="9a208-144">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9a208-145">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="9a208-145">It contains a single DNS record.</span></span>
<span data-ttu-id="9a208-146">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="9a208-146">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9a208-147">Örnek 7: SRV türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="9a208-147">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="9a208-148">Bu komut, Zone myzone.com 'de _sıp. _tcp adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9a208-148">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="9a208-149">Kayıt kümesi, SRV türünde ve 1 saatlik bir TTL değeri (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="9a208-149">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9a208-150">Tek bir DNS kaydı içerir ve IP adresi 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="9a208-150">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="9a208-151">Hizmet (Sip) ve protokol (TCP), kayıt verilerinin bir parçası olarak değil, kayıt kümesi adının bir parçası olarak belirtilir.</span><span class="sxs-lookup"><span data-stu-id="9a208-151">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="9a208-152">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="9a208-152">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9a208-153">Örnek 8: TXT türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="9a208-153">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="9a208-154">Bu komut, Zone myzone.com 'de metin adlı bir **kayıt kümesi** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9a208-154">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="9a208-155">Kayıt kümesi TXT türünde ve 1 saatlik bir TTL (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="9a208-155">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9a208-156">Tek bir DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="9a208-156">It contains a single DNS record.</span></span>
<span data-ttu-id="9a208-157">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt **kümesi** oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="9a208-157">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="9a208-158">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9a208-158">PARAMETERS</span></span>

### <span data-ttu-id="9a208-159">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="9a208-159">-CaaFlags</span></span>
<span data-ttu-id="9a208-160">Eklenecek CAA kaydının bayrakları.</span><span class="sxs-lookup"><span data-stu-id="9a208-160">The flags for the CAA record to add.</span></span> <span data-ttu-id="9a208-161">0 ile 255 arasında bir sayı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9a208-161">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="9a208-162">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="9a208-162">-CaaTag</span></span>
<span data-ttu-id="9a208-163">Eklenecek CAA kaydının etiket alanı.</span><span class="sxs-lookup"><span data-stu-id="9a208-163">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="9a208-164">-Caadeğer</span><span class="sxs-lookup"><span data-stu-id="9a208-164">-CaaValue</span></span>
<span data-ttu-id="9a208-165">Eklenecek CAA kaydının değer alanı.</span><span class="sxs-lookup"><span data-stu-id="9a208-165">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="9a208-166">-CNAME</span><span class="sxs-lookup"><span data-stu-id="9a208-166">-Cname</span></span>
<span data-ttu-id="9a208-167">Kurallı ad (CNAME) kaydı için etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a208-167">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: System.String
Parameter Sets: CName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a208-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a208-168">-DefaultProfile</span></span>
<span data-ttu-id="9a208-169">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9a208-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a208-170">-Exchange</span><span class="sxs-lookup"><span data-stu-id="9a208-170">-Exchange</span></span>
<span data-ttu-id="9a208-171">Posta alışverişi (MX) kaydı için posta Exchange sunucusu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a208-171">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a208-172">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="9a208-172">-Ipv4Address</span></span>
<span data-ttu-id="9a208-173">Bir kaydın IPv4 adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a208-173">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="9a208-174">-IPv6Adresi</span><span class="sxs-lookup"><span data-stu-id="9a208-174">-Ipv6Address</span></span>
<span data-ttu-id="9a208-175">AAAA kaydı için IPv6 adresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a208-175">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: System.String
Parameter Sets: Aaaa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a208-176">-Nsdadı</span><span class="sxs-lookup"><span data-stu-id="9a208-176">-Nsdname</span></span>
<span data-ttu-id="9a208-177">Ad sunucusu (NS) kaydı için ad sunucusu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a208-177">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Ns
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a208-178">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="9a208-178">-Port</span></span>
<span data-ttu-id="9a208-179">Hizmet (SRV) kaydı için bağlantı noktası belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a208-179">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a208-180">-Tercih</span><span class="sxs-lookup"><span data-stu-id="9a208-180">-Preference</span></span>
<span data-ttu-id="9a208-181">Bir MX kaydı için tercih belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a208-181">Specifies the preference for an MX record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a208-182">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="9a208-182">-Priority</span></span>
<span data-ttu-id="9a208-183">Bir SRV kaydının önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a208-183">Specifies the priority for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a208-184">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="9a208-184">-Ptrdname</span></span>
<span data-ttu-id="9a208-185">İşaretçi kaynağı (PTR) kaydının hedef etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a208-185">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Ptr
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a208-186">-Hedef</span><span class="sxs-lookup"><span data-stu-id="9a208-186">-Target</span></span>
<span data-ttu-id="9a208-187">Bir SRV kaydının hedefini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a208-187">Specifies the target for an SRV record.</span></span>

```yaml
Type: System.String
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a208-188">-Değer</span><span class="sxs-lookup"><span data-stu-id="9a208-188">-Value</span></span>
<span data-ttu-id="9a208-189">Bir TXT kaydının değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a208-189">Specifies the value for a TXT record.</span></span>

```yaml
Type: System.String
Parameter Sets: Txt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a208-190">-Kalınlık</span><span class="sxs-lookup"><span data-stu-id="9a208-190">-Weight</span></span>
<span data-ttu-id="9a208-191">Bir SRV kaydı için ağırlığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a208-191">Specifies the weight for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a208-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a208-192">CommonParameters</span></span>
<span data-ttu-id="9a208-193">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9a208-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a208-194">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a208-194">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a208-195">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9a208-195">INPUTS</span></span>

### <span data-ttu-id="9a208-196">System. String</span><span class="sxs-lookup"><span data-stu-id="9a208-196">System.String</span></span>

### <span data-ttu-id="9a208-197">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="9a208-197">System.UInt16</span></span>

### <span data-ttu-id="9a208-198">System. Byte</span><span class="sxs-lookup"><span data-stu-id="9a208-198">System.Byte</span></span>

## <span data-ttu-id="9a208-199">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9a208-199">OUTPUTS</span></span>

### <span data-ttu-id="9a208-200">Microsoft. Azure. Commands. DNS. DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="9a208-200">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="9a208-201">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9a208-201">NOTES</span></span>

## <span data-ttu-id="9a208-202">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9a208-202">RELATED LINKS</span></span>

[<span data-ttu-id="9a208-203">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="9a208-203">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="9a208-204">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9a208-204">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="9a208-205">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="9a208-205">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)