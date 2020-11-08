---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/add-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
ms.openlocfilehash: c9390514ad7680a047ca145c8fe71feda0ab1b51
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097819"
---
# <span data-ttu-id="e3775-101">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="e3775-101">Add-AzDnsRecordConfig</span></span>

## <span data-ttu-id="e3775-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3775-102">SYNOPSIS</span></span>
<span data-ttu-id="e3775-103">Yerel kayıt kümesi nesnesine bir DNS kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="e3775-103">Adds a DNS record to a local record set object.</span></span>

## <span data-ttu-id="e3775-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3775-104">SYNTAX</span></span>

### <span data-ttu-id="e3775-105">Bir</span><span class="sxs-lookup"><span data-stu-id="e3775-105">A</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3775-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="e3775-106">AAAA</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3775-107">Seç</span><span class="sxs-lookup"><span data-stu-id="e3775-107">NS</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3775-108">DOSYASıNA</span><span class="sxs-lookup"><span data-stu-id="e3775-108">MX</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3775-109">PTR</span><span class="sxs-lookup"><span data-stu-id="e3775-109">PTR</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3775-110">,</span><span class="sxs-lookup"><span data-stu-id="e3775-110">TXT</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3775-111">SRV</span><span class="sxs-lookup"><span data-stu-id="e3775-111">SRV</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3775-112">KAYDıNı</span><span class="sxs-lookup"><span data-stu-id="e3775-112">CNAME</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3775-113">CAA</span><span class="sxs-lookup"><span data-stu-id="e3775-113">Caa</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3775-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3775-114">DESCRIPTION</span></span>
<span data-ttu-id="e3775-115">**Add-AzDnsRecordConfig** cmdlet 'ı bir etki alanı adı SISTEMI (DNS) kaydını bir **Recordset** nesnesine ekler.</span><span class="sxs-lookup"><span data-stu-id="e3775-115">The **Add-AzDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="e3775-116">**Kayıt kümesi** nesnesi bir çevrimdışı nesnedir ve değişiklikleri MICROSOFT Azure DNS hizmeti 'nde kalıcı olarak sürdürmek için Set-AzDnsRecordSet cmdlet 'i çalıştırana kadar DNS yanıtlarını değiştirmiyor.</span><span class="sxs-lookup"><span data-stu-id="e3775-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="e3775-117">SOA kayıtları bir DNS bölgesi oluşturulduğunda oluşturulur ve DNS bölgesi silindiğinde kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="e3775-117">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="e3775-118">SOA kayıtlarını ekleyip kaldıramazsınız, ancak bunları düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e3775-118">You cannot add or remove SOA records, but you can edit them.</span></span>
<span data-ttu-id="e3775-119">**Recordset** nesnesini bu cmdlet 'e parametre olarak veya Pipeline işlecini kullanarak geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e3775-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="e3775-120">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3775-120">EXAMPLES</span></span>

### <span data-ttu-id="e3775-121">Örnek 1: kayıt kümesine kayıt ekleme</span><span class="sxs-lookup"><span data-stu-id="e3775-121">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="e3775-122">Bu örnek, var olan kayıt kümesine bir kayıt ekler.</span><span class="sxs-lookup"><span data-stu-id="e3775-122">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="e3775-123">Örnek 2: kayıt kümesine AAAA kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="e3775-123">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="e3775-124">Bu örnek, var olan kayıt kümesine bir AAAA kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="e3775-124">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="e3775-125">Örnek 3: kayıt kümesine CNAME kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="e3775-125">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="e3775-126">Bu örnek, var olan kayıt kümesine bir CNAME kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="e3775-126">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="e3775-127">CNAME kayıt kümesi en çok bir kayıt içerebileceği için, başlangıçta boş bir kayıt kümesi olmalıdır veya var olan kayıtların Remove-AzDnsRecordConfig kullanılarak kaldırılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="e3775-127">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzDnsRecordConfig.</span></span>

### <span data-ttu-id="e3775-128">Örnek 4: kayıt kümesine bir MX kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="e3775-128">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="e3775-129">Bu örnek, varolan bir kayıt kümesine bir MX kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="e3775-129">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="e3775-130">"@" Kayıt adı, bölge Apex bir kayıt kümesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e3775-130">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="e3775-131">Örnek 5: kayıt kümesine NS kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="e3775-131">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzDnsRecordSet
```

<span data-ttu-id="e3775-132">Bu örnek, var olan kayıt kümesine bir NS kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="e3775-132">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="e3775-133">Örnek 6: kayıt kümesine PTR kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="e3775-133">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="e3775-134">Bu örnek, varolan bir kayıt kümesine bir PTR kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="e3775-134">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="e3775-135">Örnek 7: kayıt kümesine SRV kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="e3775-135">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="e3775-136">Bu örnek, var olan kayıt kümesine bir SRV kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="e3775-136">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="e3775-137">Örnek 8: kayıt kümesine TXT kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="e3775-137">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Value "This is a TXT Record" | Set-AzDnsRecordSet
```

<span data-ttu-id="e3775-138">Bu örnek, var olan kayıt kümesine bir TXT kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="e3775-138">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="e3775-139">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3775-139">PARAMETERS</span></span>

### <span data-ttu-id="e3775-140">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="e3775-140">-CaaFlags</span></span>
<span data-ttu-id="e3775-141">Eklenecek CAA kaydının bayrakları.</span><span class="sxs-lookup"><span data-stu-id="e3775-141">The flags for the CAA record to add.</span></span> <span data-ttu-id="e3775-142">0 ile 255 arasında bir sayı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e3775-142">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="e3775-143">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="e3775-143">-CaaTag</span></span>
<span data-ttu-id="e3775-144">Eklenecek CAA kaydının etiket alanı.</span><span class="sxs-lookup"><span data-stu-id="e3775-144">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="e3775-145">-Caadeğer</span><span class="sxs-lookup"><span data-stu-id="e3775-145">-CaaValue</span></span>
<span data-ttu-id="e3775-146">Eklenecek CAA kaydının değer alanı.</span><span class="sxs-lookup"><span data-stu-id="e3775-146">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="e3775-147">-CNAME</span><span class="sxs-lookup"><span data-stu-id="e3775-147">-Cname</span></span>
<span data-ttu-id="e3775-148">Kurallı ad (CNAME) kaydı için etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3775-148">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="e3775-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3775-149">-DefaultProfile</span></span>
<span data-ttu-id="e3775-150">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e3775-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3775-151">-Exchange</span><span class="sxs-lookup"><span data-stu-id="e3775-151">-Exchange</span></span>
<span data-ttu-id="e3775-152">Posta alışverişi (MX) kaydı için posta Exchange sunucusu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3775-152">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="e3775-153">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="e3775-153">-Ipv4Address</span></span>
<span data-ttu-id="e3775-154">Bir kaydın IPv4 adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3775-154">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="e3775-155">-IPv6Adresi</span><span class="sxs-lookup"><span data-stu-id="e3775-155">-Ipv6Address</span></span>
<span data-ttu-id="e3775-156">AAAA kaydı için IPv6 adresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3775-156">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="e3775-157">-Nsdadı</span><span class="sxs-lookup"><span data-stu-id="e3775-157">-Nsdname</span></span>
<span data-ttu-id="e3775-158">Ad sunucusu (NS) kaydı için ad sunucusu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3775-158">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="e3775-159">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="e3775-159">-Port</span></span>
<span data-ttu-id="e3775-160">Hizmet (SRV) kaydı için bağlantı noktası belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3775-160">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="e3775-161">-Tercih</span><span class="sxs-lookup"><span data-stu-id="e3775-161">-Preference</span></span>
<span data-ttu-id="e3775-162">Bir MX kaydı için tercih belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3775-162">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="e3775-163">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="e3775-163">-Priority</span></span>
<span data-ttu-id="e3775-164">Bir SRV kaydının önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3775-164">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="e3775-165">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="e3775-165">-Ptrdname</span></span>
<span data-ttu-id="e3775-166">İşaretçi kaynağı (PTR) kaydının hedef etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3775-166">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="e3775-167">-Kayıt kümesi</span><span class="sxs-lookup"><span data-stu-id="e3775-167">-RecordSet</span></span>
<span data-ttu-id="e3775-168">Düzenlenecek **kayıt kümesi** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3775-168">Specifies the **RecordSet** object to edit.</span></span>

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

### <span data-ttu-id="e3775-169">-Hedef</span><span class="sxs-lookup"><span data-stu-id="e3775-169">-Target</span></span>
<span data-ttu-id="e3775-170">Bir SRV kaydının hedefini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3775-170">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="e3775-171">-Değer</span><span class="sxs-lookup"><span data-stu-id="e3775-171">-Value</span></span>
<span data-ttu-id="e3775-172">Bir TXT kaydının değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3775-172">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="e3775-173">-Kalınlık</span><span class="sxs-lookup"><span data-stu-id="e3775-173">-Weight</span></span>
<span data-ttu-id="e3775-174">Bir SRV kaydı için ağırlığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3775-174">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="e3775-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3775-175">CommonParameters</span></span>
<span data-ttu-id="e3775-176">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3775-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3775-177">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3775-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3775-178">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3775-178">INPUTS</span></span>

### <span data-ttu-id="e3775-179">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e3775-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="e3775-180">System. String</span><span class="sxs-lookup"><span data-stu-id="e3775-180">System.String</span></span>

### <span data-ttu-id="e3775-181">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="e3775-181">System.UInt16</span></span>

### <span data-ttu-id="e3775-182">System. Byte</span><span class="sxs-lookup"><span data-stu-id="e3775-182">System.Byte</span></span>

## <span data-ttu-id="e3775-183">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3775-183">OUTPUTS</span></span>

### <span data-ttu-id="e3775-184">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e3775-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="e3775-185">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3775-185">NOTES</span></span>

## <span data-ttu-id="e3775-186">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3775-186">RELATED LINKS</span></span>

[<span data-ttu-id="e3775-187">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e3775-187">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="e3775-188">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="e3775-188">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

[<span data-ttu-id="e3775-189">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e3775-189">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
