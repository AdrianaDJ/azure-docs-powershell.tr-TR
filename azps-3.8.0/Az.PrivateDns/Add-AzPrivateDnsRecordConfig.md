---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/add-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: a6150f6f54db57abbcd643c99729d41254db7d27
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096378"
---
# <span data-ttu-id="409cf-101">Add-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="409cf-101">Add-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="409cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="409cf-102">SYNOPSIS</span></span>
<span data-ttu-id="409cf-103">Yerel kayıt kümesi nesnesine özel bir DNS kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="409cf-103">Adds a Private DNS record to a local record set object.</span></span>

## <span data-ttu-id="409cf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="409cf-104">SYNTAX</span></span>

### <span data-ttu-id="409cf-105">A (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="409cf-105">A (Default)</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="409cf-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="409cf-106">AAAA</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="409cf-107">DOSYASıNA</span><span class="sxs-lookup"><span data-stu-id="409cf-107">MX</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="409cf-108">PTR</span><span class="sxs-lookup"><span data-stu-id="409cf-108">PTR</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="409cf-109">,</span><span class="sxs-lookup"><span data-stu-id="409cf-109">TXT</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="409cf-110">SRV</span><span class="sxs-lookup"><span data-stu-id="409cf-110">SRV</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="409cf-111">KAYDıNı</span><span class="sxs-lookup"><span data-stu-id="409cf-111">CNAME</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="409cf-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="409cf-112">DESCRIPTION</span></span>
<span data-ttu-id="409cf-113">Add-AzPrivateDnsRecordConfig cmdlet 'i bir RecordSet nesnesine özel bir etki alanı adı sistemi (DNS) kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="409cf-113">The Add-AzPrivateDnsRecordConfig cmdlet adds a Private Domain Name System (DNS) record to a RecordSet object.</span></span> <span data-ttu-id="409cf-114">Kayıt kümesi nesnesi bir çevrimdışı nesnedir ve değişiklikleri Microsoft Azure özel DNS hizmetine kalıcı hale getirmek için Set-AzPrivateDnsRecordSet cmdlet 'i çalıştırana kadar, özel DNS yanıtlarını değiştirmiyor.</span><span class="sxs-lookup"><span data-stu-id="409cf-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="409cf-115">SOA kayıtları özel bir DNS bölgesi oluşturulduğunda oluşturulur ve özel DNS bölgesi silindiğinde kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="409cf-115">SOA records are created when a Private DNS zone is created, and are removed when the Private DNS zone is deleted.</span></span> <span data-ttu-id="409cf-116">SOA kayıtlarını ekleyip kaldıramazsınız, ancak bunları düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="409cf-116">You cannot add or remove SOA records, but you can edit them.</span></span> <span data-ttu-id="409cf-117">RecordSet nesnesini bu cmdlet 'e parametre olarak veya Pipeline işlecini kullanarak geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="409cf-117">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="409cf-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="409cf-118">EXAMPLES</span></span>

### <span data-ttu-id="409cf-119">Örnek 1: kayıt kümesine kayıt ekleme</span><span class="sxs-lookup"><span data-stu-id="409cf-119">Example 1: Add an A record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType A -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType A -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="409cf-120">Bu örnek, var olan kayıt kümesine bir kayıt ekler.</span><span class="sxs-lookup"><span data-stu-id="409cf-120">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="409cf-121">Örnek 2: kayıt kümesine AAAA kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="409cf-121">Example 2: Add an AAAA record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType AAAAA -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType AAAAA -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="409cf-122">Bu örnek, var olan kayıt kümesine bir AAAAA kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="409cf-122">This example adds an AAAAA record to an existing record set.</span></span>

### <span data-ttu-id="409cf-123">Örnek 3: kayıt kümesine CNAME kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="409cf-123">Example 3: Add a CNAME record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType CNAME -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType CNAME -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="409cf-124">Bu örnek, var olan kayıt kümesine bir CNAME kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="409cf-124">This example adds a CNAME record to an existing record set.</span></span>

### <span data-ttu-id="409cf-125">Örnek 4: kayıt kümesine MX kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="409cf-125">Example 4: Add a MX record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name @ -RecordType MX -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {[5,mail.microsoft.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="409cf-126">Bu örnek, var olan kayıt kümesine bir MX kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="409cf-126">This example adds a MX record to an existing record set.</span></span>

### <span data-ttu-id="409cf-127">Örnek 5: kayıt kümesine PTR kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="409cf-127">Example 5: Add a PTR record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name 4 -RecordType PTR -ResourceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name 4 -RecordType PTR -ResourceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="409cf-128">Bu örnek, varolan bir kayıt kümesine bir PTR kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="409cf-128">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="409cf-129">Örnek 6: kayıt kümesine SRV kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="409cf-129">Example 6: Add a SRV record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name _sip._tcp -RecordType SRV -ResourceGroupName MyResourceGroup-ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name _sip._tcp -RecordType SRV -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {[0,5,8080,sipservice.contoso.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="409cf-130">Bu örnek, var olan kayıt kümesine bir SRV kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="409cf-130">This example adds a SRV record to an existing record set.</span></span>

### <span data-ttu-id="409cf-131">Örnek 7: kayıt kümesine TXT kaydı ekleme</span><span class="sxs-lookup"><span data-stu-id="409cf-131">Example 7: Add a TXT record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name text -RecordType TXT -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name text -RecordType TXT -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Value "This is a TXT Record" | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {This is a TXT Record}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="409cf-132">Bu örnek, var olan kayıt kümesine bir TXT kaydı ekler.</span><span class="sxs-lookup"><span data-stu-id="409cf-132">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="409cf-133">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="409cf-133">PARAMETERS</span></span>

### <span data-ttu-id="409cf-134">-CNAME</span><span class="sxs-lookup"><span data-stu-id="409cf-134">-Cname</span></span>
<span data-ttu-id="409cf-135">Eklenecek CNAME kaydının kurallı adı.</span><span class="sxs-lookup"><span data-stu-id="409cf-135">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="409cf-136">Bölgenin adına göreli olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="409cf-136">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="409cf-137">Sonlandırıcı nokta olmamalıdır</span><span class="sxs-lookup"><span data-stu-id="409cf-137">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409cf-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="409cf-138">-DefaultProfile</span></span>
<span data-ttu-id="409cf-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="409cf-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="409cf-140">-Exchange</span><span class="sxs-lookup"><span data-stu-id="409cf-140">-Exchange</span></span>
<span data-ttu-id="409cf-141">Eklenecek MX kaydının posta Exchange ana bilgisayarı.</span><span class="sxs-lookup"><span data-stu-id="409cf-141">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="409cf-142">Bölgenin adına göreli olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="409cf-142">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="409cf-143">Sonlandırıcı nokta olmamalıdır</span><span class="sxs-lookup"><span data-stu-id="409cf-143">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409cf-144">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="409cf-144">-Ipv4Address</span></span>
<span data-ttu-id="409cf-145">Eklenecek A kaydının IPv4 adresi.</span><span class="sxs-lookup"><span data-stu-id="409cf-145">The IPv4 address for the A record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409cf-146">-IPv6Adresi</span><span class="sxs-lookup"><span data-stu-id="409cf-146">-Ipv6Address</span></span>
<span data-ttu-id="409cf-147">Eklenecek AAAA kaydının IPv6 adresi.</span><span class="sxs-lookup"><span data-stu-id="409cf-147">The IPv6 address for the AAAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409cf-148">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="409cf-148">-Port</span></span>
<span data-ttu-id="409cf-149">Eklenecek SRV kaydının bağlantı noktası numarası.</span><span class="sxs-lookup"><span data-stu-id="409cf-149">The port number for the SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409cf-150">-Tercih</span><span class="sxs-lookup"><span data-stu-id="409cf-150">-Preference</span></span>
<span data-ttu-id="409cf-151">Eklenecek MX kaydının tercih değeri.</span><span class="sxs-lookup"><span data-stu-id="409cf-151">The preference value for the MX record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409cf-152">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="409cf-152">-Priority</span></span>
<span data-ttu-id="409cf-153">Eklenecek öncelik değeri SRV kaydı.</span><span class="sxs-lookup"><span data-stu-id="409cf-153">The priority value SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409cf-154">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="409cf-154">-Ptrdname</span></span>
<span data-ttu-id="409cf-155">Eklenecek PTR kaydının hedef ana bilgisayarı.</span><span class="sxs-lookup"><span data-stu-id="409cf-155">The target host for the PTR record to add.</span></span>
<span data-ttu-id="409cf-156">Bölgenin adına göreli olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="409cf-156">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="409cf-157">Sonlandırıcı nokta olmamalıdır</span><span class="sxs-lookup"><span data-stu-id="409cf-157">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409cf-158">-Kayıt kümesi</span><span class="sxs-lookup"><span data-stu-id="409cf-158">-RecordSet</span></span>
<span data-ttu-id="409cf-159">Kaydın ekleneceği kayıt kümesi.</span><span class="sxs-lookup"><span data-stu-id="409cf-159">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="409cf-160">-Hedef</span><span class="sxs-lookup"><span data-stu-id="409cf-160">-Target</span></span>
<span data-ttu-id="409cf-161">Eklenecek SRV kaydının hedef ana bilgisayarı.</span><span class="sxs-lookup"><span data-stu-id="409cf-161">The target host for the SRV record to add.</span></span>
<span data-ttu-id="409cf-162">Bölgenin adına göreli olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="409cf-162">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="409cf-163">Sonlandırıcı nokta olmamalıdır</span><span class="sxs-lookup"><span data-stu-id="409cf-163">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409cf-164">-Değer</span><span class="sxs-lookup"><span data-stu-id="409cf-164">-Value</span></span>
<span data-ttu-id="409cf-165">Eklenecek TXT kaydının metin değeri.</span><span class="sxs-lookup"><span data-stu-id="409cf-165">The text value for the TXT record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409cf-166">-Kalınlık</span><span class="sxs-lookup"><span data-stu-id="409cf-166">-Weight</span></span>
<span data-ttu-id="409cf-167">Eklenecek SRV kaydının ağırlık değeri.</span><span class="sxs-lookup"><span data-stu-id="409cf-167">The weight value for the SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409cf-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="409cf-168">CommonParameters</span></span>
<span data-ttu-id="409cf-169">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="409cf-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="409cf-170">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="409cf-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="409cf-171">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="409cf-171">INPUTS</span></span>

### <span data-ttu-id="409cf-172">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="409cf-172">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="409cf-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="409cf-173">OUTPUTS</span></span>

### <span data-ttu-id="409cf-174">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="409cf-174">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="409cf-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="409cf-175">NOTES</span></span>

## <span data-ttu-id="409cf-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="409cf-176">RELATED LINKS</span></span>
