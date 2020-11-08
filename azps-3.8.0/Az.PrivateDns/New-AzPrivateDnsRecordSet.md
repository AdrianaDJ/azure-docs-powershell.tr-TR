---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 1a7042c94457f23302aa8d2899475d7b117e65b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104738"
---
# <span data-ttu-id="166d0-101">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="166d0-101">New-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="166d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="166d0-102">SYNOPSIS</span></span>
<span data-ttu-id="166d0-103">Özel bir DNS bölgesinde kayıt kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="166d0-103">Creates a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="166d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="166d0-104">SYNTAX</span></span>

### <span data-ttu-id="166d0-105">Alanlar (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="166d0-105">Fields (Default)</span></span>
```
New-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> -Ttl <UInt32> [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="166d0-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="166d0-106">Object</span></span>
```
New-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="166d0-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="166d0-107">ResourceId</span></span>
```
New-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="166d0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="166d0-108">DESCRIPTION</span></span>
<span data-ttu-id="166d0-109">New-AzPrivateDnsRecordSet cmdlet 'i belirtilen adda bir özel etki alanı adı sistemi (DNS) kaydı oluşturur ve belirtilen özel bölgeye yazın.</span><span class="sxs-lookup"><span data-stu-id="166d0-109">The New-AzPrivateDnsRecordSet cmdlet creates a new Private Domain Name System (DNS) record set with the specified name and type in the specified private zone.</span></span> <span data-ttu-id="166d0-110">Kayıt kümesi nesnesi, aynı adda ve türde bir özel DNS kaydı kümesidir.</span><span class="sxs-lookup"><span data-stu-id="166d0-110">A RecordSet object is a set of Private DNS records with the same name and type.</span></span> <span data-ttu-id="166d0-111">Adın, özel bir bölgeye göreli olduğunu ve tam adı olmadığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="166d0-111">Note that the name is relative to the private zone and not the fully qualified name.</span></span> <span data-ttu-id="166d0-112">PrivateDnsRecord parametresi, kayıt kümesindeki kayıtları belirtir.</span><span class="sxs-lookup"><span data-stu-id="166d0-112">The PrivateDnsRecord parameter specifies the records in the record set.</span></span> <span data-ttu-id="166d0-113">Bu parametre, New-AzPrivateDnsRecordConfig kullanılarak oluşturulan özel DNS kayıtları dizisini alır.</span><span class="sxs-lookup"><span data-stu-id="166d0-113">This parameter takes an array of Private DNS records, constructed using New-AzPrivateDnsRecordConfig.</span></span> <span data-ttu-id="166d0-114">Pipeline işlecini kullanarak, bir PSPrivateDnsZone nesnesini bu cmdlet 'e geçirebilir ya da bölge parametresi olarak bir PSPrivateDnsZone nesnesi geçirebilirsiniz veya bölgeyi RESOURCEID ile belirtebilirsiniz veya alternatif olarak bölgeyi adıyla belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="166d0-114">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or you can specify the zone by its ResourceId, or alternatively you can specify the zone by name.</span></span> <span data-ttu-id="166d0-115">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için Confirm parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="166d0-115">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="166d0-116">Eşleşen bir kayıt kümesi zaten varsa (aynı ad ve kayıt türü), üzerine yazma parametresini belirtmeniz gerekir, aksi halde cmdlet yeni bir kayıt kümesi oluşturmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="166d0-116">If a matching RecordSet already exists (same name and record type), you must specify the Overwrite parameter, otherwise the cmdlet will not create a new RecordSet .</span></span>

## <span data-ttu-id="166d0-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="166d0-117">EXAMPLES</span></span>

### <span data-ttu-id="166d0-118">Örnek 1: A türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="166d0-118">Example 1: Create a RecordSet of type A</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4)

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :


# To create a record set containing multiple records, use New-AzPrivateDnsRecordConfig to add each record to the $Records array,
# then call New-AzPrivateDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 5.6.7.8}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="166d0-119">Bu örnek, özel bölge myzone.com ' da www adlı bir kayıt kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="166d0-119">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="166d0-120">Kayıt kümesi A türünde ve 1 saatlik bir TTL (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="166d0-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="166d0-121">Tek bir özel DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="166d0-121">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="166d0-122">Örnek 2: AAAA türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="166d0-122">Example 2: Create a RecordSet of type AAAA</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:db8::1}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="166d0-123">Bu örnek, özel bölge myzone.com ' da www adlı bir kayıt kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="166d0-123">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="166d0-124">Kayıt kümesi AAAA türünde ve 1 saatlik bir TTL değeri (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="166d0-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="166d0-125">Tek bir özel DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="166d0-125">It contains a single Private DNS record.</span></span> <span data-ttu-id="166d0-126">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt kümesi oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="166d0-126">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="166d0-127">Örnek 3: CNAME türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="166d0-127">Example 3: Create a RecordSet of type CNAME</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="166d0-128">Bu örnek, özel bölge myzone.com ' da www adlı bir kayıt kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="166d0-128">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="166d0-129">Kayıt kümesi CNAME türünde ve 1 saat (3600 saniye) TTL değeri vardır.</span><span class="sxs-lookup"><span data-stu-id="166d0-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="166d0-130">Tek bir özel DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="166d0-130">It contains a single Private DNS record.</span></span> <span data-ttu-id="166d0-131">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt kümesi oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="166d0-131">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="166d0-132">Örnek 4: MX türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="166d0-132">Example 4: Create a RecordSet of type MX</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="166d0-133">Bu komut, özel myzone.com.</span><span class="sxs-lookup"><span data-stu-id="166d0-133">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="166d0-134">Kayıt kümesi MX türünde ve TTL 1 saat (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="166d0-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="166d0-135">Tek bir özel DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="166d0-135">It contains a single Private DNS record.</span></span> <span data-ttu-id="166d0-136">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt kümesi oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="166d0-136">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="166d0-137">Örnek 5: PTR türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="166d0-137">Example 5: Create a RecordSet of type PTR</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -PrivateDnsRecords $Records

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

<span data-ttu-id="166d0-138">Bu komut, 3.2.1.in-addr. arpa özel bölgesinde 4 adlı bir kayıt kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="166d0-138">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="166d0-139">Kayıt kümesi PTR türünde ve bir TTL değeri 1 saattir (3600 saniye).</span><span class="sxs-lookup"><span data-stu-id="166d0-139">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="166d0-140">Tek bir özel DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="166d0-140">It contains a single Private DNS record.</span></span> <span data-ttu-id="166d0-141">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt kümesi oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="166d0-141">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="166d0-142">Örnek 6: SRV türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="166d0-142">Example 6: Create a RecordSet of type SRV</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="166d0-143">Bu komut, özel myzone.com. _tcp adlı bir kayıt kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="166d0-143">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="166d0-144">Kayıt kümesi, SRV türünde ve 1 saatlik bir TTL değeri (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="166d0-144">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="166d0-145">2001.2.3.4 IP adresi üzerine gelerek tek bir özel DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="166d0-145">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="166d0-146">Hizmet (Sip) ve protokol (TCP), kayıt verilerinin bir parçası olarak değil, kayıt kümesi adının bir parçası olarak belirtilir.</span><span class="sxs-lookup"><span data-stu-id="166d0-146">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="166d0-147">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt kümesi oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="166d0-147">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="166d0-148">Örnek 7: TXT türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="166d0-148">Example 7: Create a RecordSet of type TXT</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="166d0-149">Bu komut, özel myzone.com adlı bir kayıt kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="166d0-149">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="166d0-150">Kayıt kümesi TXT türünde ve 1 saatlik bir TTL (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="166d0-150">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="166d0-151">Tek bir özel DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="166d0-151">It contains a single Private DNS record.</span></span> <span data-ttu-id="166d0-152">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt kümesi oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="166d0-152">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="166d0-153">Örnek 8: bölgede kayıt kümesi Apex</span><span class="sxs-lookup"><span data-stu-id="166d0-153">Example 8:  Create a RecordSet at the zone apex</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : @
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="166d0-154">Bu komut, özel myzone.com Apex (veya kökü) üzerinde bir RecordSet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="166d0-154">This command creates a RecordSet at the apex (or root) of the private zone myzone.com.</span></span> <span data-ttu-id="166d0-155">Bunu yapmak için, kayıt kümesi adı "@" (çift tırnak işaretleri dahil) olarak belirtilir.</span><span class="sxs-lookup"><span data-stu-id="166d0-155">To do this, the record set name is specified as "@" (including the double-quotes).</span></span> <span data-ttu-id="166d0-156">Bir bölgenin Apex CNAME kayıtları oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="166d0-156">You cannot create CNAME records at the apex of a zone.</span></span> <span data-ttu-id="166d0-157">Bu, DNS standartlarının bir kısıtlamadır; Azure özel DNS 'nin bir sınırlaması değildir.</span><span class="sxs-lookup"><span data-stu-id="166d0-157">This is a constraint of the DNS standards; it is not a limitation of Azure Private DNS.</span></span> <span data-ttu-id="166d0-158">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt kümesi oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="166d0-158">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="166d0-159">Örnek 9: joker karakter kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="166d0-159">Example 9:  Create a wildcard Record Set</span></span>

```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : *
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="166d0-160">Bu komut, myzone.com adında bir kayıt kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="166d0-160">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="166d0-161">Bu, joker karakter kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="166d0-161">This is a wildcard record set.</span></span> <span data-ttu-id="166d0-162">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt kümesi oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="166d0-162">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="166d0-163">Örnek 10: boş bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="166d0-163">Example 10:  Create an empty Record Set</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords @()

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : *
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="166d0-164">Bu komut, myzone.com adında bir kayıt kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="166d0-164">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="166d0-165">Kayıt kümesi A türünde ve 1 saatlik bir TTL (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="166d0-165">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="166d0-166">Bu, daha sonra kayıt ekleyebileceğiniz bir yer tutucu görevi gören boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="166d0-166">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="166d0-167">Örnek 11: kayıt kümesi oluşturma ve tüm onayı gösterme</span><span class="sxs-lookup"><span data-stu-id="166d0-167">Example 11:  Create a record set and suppress all confirmation</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="166d0-168">Bu komut bir kayıt kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="166d0-168">This command creates a RecordSet.</span></span> <span data-ttu-id="166d0-169">Overwrite parametresi, bu kayıt kümesinin aynı ada ve türe sahip önceden var olan herhangi bir kayıt kümesinin üzerine yazılmasını sağlar (Bu kayıt kümesinde varolan kayıtlar kaybolur).</span><span class="sxs-lookup"><span data-stu-id="166d0-169">The Overwrite parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span> <span data-ttu-id="166d0-170">$False değeri olan Confirm parametresi, onay istemini bastırır.</span><span class="sxs-lookup"><span data-stu-id="166d0-170">The Confirm parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="166d0-171">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="166d0-171">PARAMETERS</span></span>

### <span data-ttu-id="166d0-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="166d0-172">-DefaultProfile</span></span>
<span data-ttu-id="166d0-173">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="166d0-173">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="166d0-174">-Metadata</span><span class="sxs-lookup"><span data-stu-id="166d0-174">-Metadata</span></span>
<span data-ttu-id="166d0-175">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="166d0-175">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="166d0-176">-Ad</span><span class="sxs-lookup"><span data-stu-id="166d0-176">-Name</span></span>
<span data-ttu-id="166d0-177">Bu kayıt kümesindeki kayıtların adı (bölgenin adına ve sonlandırma noktası olmadan).</span><span class="sxs-lookup"><span data-stu-id="166d0-177">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="166d0-178">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="166d0-178">-Overwrite</span></span>
<span data-ttu-id="166d0-179">Kayıt kümesi zaten varsa başarısız olmaz.</span><span class="sxs-lookup"><span data-stu-id="166d0-179">Do not fail if the record set already exists.</span></span>

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

### <span data-ttu-id="166d0-180">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="166d0-180">-ParentResourceId</span></span>
<span data-ttu-id="166d0-181">Özel DNS bölge RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="166d0-181">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="166d0-182">-PrivateDnsRecord</span><span class="sxs-lookup"><span data-stu-id="166d0-182">-PrivateDnsRecord</span></span>
<span data-ttu-id="166d0-183">Bu kayıt kümesinin parçası olan özel DNS kayıtları.</span><span class="sxs-lookup"><span data-stu-id="166d0-183">The private dns records that are part of this record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordBase[]
Parameter Sets: (All)
Aliases: PrivateDnsRecords

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="166d0-184">-RecordType</span><span class="sxs-lookup"><span data-stu-id="166d0-184">-RecordType</span></span>
<span data-ttu-id="166d0-185">Bu kayıt kümesindeki özel DNS kayıtlarının türü.</span><span class="sxs-lookup"><span data-stu-id="166d0-185">The type of Private DNS records in this record set.</span></span>

```yaml
Type: Microsoft.Azure.Management.PrivateDns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="166d0-186">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="166d0-186">-ResourceGroupName</span></span>
<span data-ttu-id="166d0-187">Bölgenin ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="166d0-187">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="166d0-188">-TTL</span><span class="sxs-lookup"><span data-stu-id="166d0-188">-Ttl</span></span>
<span data-ttu-id="166d0-189">Bu kayıt kümesindeki tüm kayıtların TTL değeri.</span><span class="sxs-lookup"><span data-stu-id="166d0-189">The TTL value of all the records in this record set.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="166d0-190">-Bölge</span><span class="sxs-lookup"><span data-stu-id="166d0-190">-Zone</span></span>
<span data-ttu-id="166d0-191">Kayıt kümesinin oluşturulacağı bölgeyi temsil eden PrivateDnsZone nesnesi.</span><span class="sxs-lookup"><span data-stu-id="166d0-191">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="166d0-192">-BölgeAdı</span><span class="sxs-lookup"><span data-stu-id="166d0-192">-ZoneName</span></span>
<span data-ttu-id="166d0-193">Kayıt kümesinin oluşturulacağı bölge (Sonlandırıcı nokta olmadan).</span><span class="sxs-lookup"><span data-stu-id="166d0-193">The zone in which to create the record set (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="166d0-194">-Onay</span><span class="sxs-lookup"><span data-stu-id="166d0-194">-Confirm</span></span>
<span data-ttu-id="166d0-195">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="166d0-195">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="166d0-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="166d0-196">-WhatIf</span></span>
<span data-ttu-id="166d0-197">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="166d0-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="166d0-198">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="166d0-198">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="166d0-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="166d0-199">CommonParameters</span></span>
<span data-ttu-id="166d0-200">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="166d0-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="166d0-201">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="166d0-201">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="166d0-202">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="166d0-202">INPUTS</span></span>

### <span data-ttu-id="166d0-203">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="166d0-203">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="166d0-204">System. String</span><span class="sxs-lookup"><span data-stu-id="166d0-204">System.String</span></span>

## <span data-ttu-id="166d0-205">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="166d0-205">OUTPUTS</span></span>

### <span data-ttu-id="166d0-206">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="166d0-206">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="166d0-207">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="166d0-207">NOTES</span></span>

## <span data-ttu-id="166d0-208">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="166d0-208">RELATED LINKS</span></span>
