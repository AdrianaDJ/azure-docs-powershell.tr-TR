---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: fc5686e22167613550b236bd234c649317ba8cca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933090"
---
# <span data-ttu-id="98f27-101">New-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="98f27-101">New-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="98f27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98f27-102">SYNOPSIS</span></span>
<span data-ttu-id="98f27-103">Yeni bir özel DNS kaydı yerel nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98f27-103">Creates a new Private DNS record local object.</span></span>

## <span data-ttu-id="98f27-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="98f27-104">SYNTAX</span></span>

### <span data-ttu-id="98f27-105">A (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="98f27-105">A (Default)</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98f27-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="98f27-106">AAAA</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98f27-107">DOSYASıNA</span><span class="sxs-lookup"><span data-stu-id="98f27-107">MX</span></span>
```
New-AzPrivateDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98f27-108">PTR</span><span class="sxs-lookup"><span data-stu-id="98f27-108">PTR</span></span>
```
New-AzPrivateDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98f27-109">,</span><span class="sxs-lookup"><span data-stu-id="98f27-109">TXT</span></span>
```
New-AzPrivateDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98f27-110">SRV</span><span class="sxs-lookup"><span data-stu-id="98f27-110">SRV</span></span>
```
New-AzPrivateDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98f27-111">KAYDıNı</span><span class="sxs-lookup"><span data-stu-id="98f27-111">CNAME</span></span>
```
New-AzPrivateDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98f27-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="98f27-112">DESCRIPTION</span></span>
<span data-ttu-id="98f27-113">New-AzPrivateDnsRecordConfig cmdlet 'i yerel bir PSPrivateDnsRecord nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98f27-113">The New-AzPrivateDnsRecordConfig cmdlet creates a local PSPrivateDnsRecord object.</span></span> <span data-ttu-id="98f27-114">Bu nesnelerin bir dizisi, kayıt kümesinde oluşturulacak kayıtları belirtmek için PrivateDnsRecord parametresini kullanarak New-AzPrivateDnsRecordSet cmdlet 'ine geçirilir.</span><span class="sxs-lookup"><span data-stu-id="98f27-114">An array of these objects is passed to the New-AzPrivateDnsRecordSet cmdlet using the PrivateDnsRecord parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="98f27-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="98f27-115">EXAMPLES</span></span>

### <span data-ttu-id="98f27-116">Örnek 1: A türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="98f27-116">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="98f27-117">Bu örnek, özel bölge myzone.com ' da www adlı bir kayıt kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98f27-117">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="98f27-118">Kayıt kümesi A türünde ve 1 saatlik bir TTL (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="98f27-118">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="98f27-119">Tek bir özel DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="98f27-119">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="98f27-120">Örnek 2: AAAA türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="98f27-120">Example 2: Create a RecordSet of type AAAA</span></span>
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

<span data-ttu-id="98f27-121">Bu örnek, özel bölge myzone.com ' da www adlı bir kayıt kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98f27-121">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="98f27-122">Kayıt kümesi AAAA türünde ve 1 saatlik bir TTL değeri (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="98f27-122">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="98f27-123">Tek bir özel DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="98f27-123">It contains a single Private DNS record.</span></span> <span data-ttu-id="98f27-124">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt kümesi oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="98f27-124">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="98f27-125">Örnek 3: CNAME türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="98f27-125">Example 3: Create a RecordSet of type CNAME</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="98f27-126">Bu örnek, özel bölge myzone.com ' da www adlı bir kayıt kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98f27-126">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="98f27-127">Kayıt kümesi CNAME türünde ve 1 saat (3600 saniye) TTL değeri vardır.</span><span class="sxs-lookup"><span data-stu-id="98f27-127">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="98f27-128">Tek bir özel DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="98f27-128">It contains a single Private DNS record.</span></span> <span data-ttu-id="98f27-129">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt kümesi oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="98f27-129">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="98f27-130">Örnek 4: MX türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="98f27-130">Example 4: Create a RecordSet of type MX</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="98f27-131">Bu komut, özel myzone.com.</span><span class="sxs-lookup"><span data-stu-id="98f27-131">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="98f27-132">Kayıt kümesi MX türünde ve TTL 1 saat (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="98f27-132">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="98f27-133">Tek bir özel DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="98f27-133">It contains a single Private DNS record.</span></span> <span data-ttu-id="98f27-134">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt kümesi oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="98f27-134">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="98f27-135">Örnek 5: PTR türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="98f27-135">Example 5: Create a RecordSet of type PTR</span></span>
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

<span data-ttu-id="98f27-136">Bu komut, 3.2.1.in-addr. arpa özel bölgesinde 4 adlı bir kayıt kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98f27-136">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="98f27-137">Kayıt kümesi PTR türünde ve bir TTL değeri 1 saattir (3600 saniye).</span><span class="sxs-lookup"><span data-stu-id="98f27-137">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="98f27-138">Tek bir özel DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="98f27-138">It contains a single Private DNS record.</span></span> <span data-ttu-id="98f27-139">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt kümesi oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="98f27-139">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="98f27-140">Örnek 6: SRV türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="98f27-140">Example 6: Create a RecordSet of type SRV</span></span>
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

<span data-ttu-id="98f27-141">Bu komut, özel myzone.com. _tcp adlı bir kayıt kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98f27-141">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="98f27-142">Kayıt kümesi, SRV türünde ve 1 saatlik bir TTL değeri (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="98f27-142">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="98f27-143">2001.2.3.4 IP adresi üzerine gelerek tek bir özel DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="98f27-143">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="98f27-144">Hizmet (Sip) ve protokol (TCP), kayıt verilerinin bir parçası olarak değil, kayıt kümesi adının bir parçası olarak belirtilir.</span><span class="sxs-lookup"><span data-stu-id="98f27-144">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="98f27-145">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt kümesi oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="98f27-145">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="98f27-146">Örnek 7: TXT türünde bir kayıt kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="98f27-146">Example 7: Create a RecordSet of type TXT</span></span>
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

<span data-ttu-id="98f27-147">Bu komut, özel myzone.com adlı bir kayıt kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98f27-147">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="98f27-148">Kayıt kümesi TXT türünde ve 1 saatlik bir TTL (3600 saniye) olur.</span><span class="sxs-lookup"><span data-stu-id="98f27-148">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="98f27-149">Tek bir özel DNS kaydı içerir.</span><span class="sxs-lookup"><span data-stu-id="98f27-149">It contains a single Private DNS record.</span></span> <span data-ttu-id="98f27-150">Tek bir pn_PowerShell_short veya birden çok kayıtla kayıt kümesi oluşturmak için bir kayıt kümesi oluşturmak için, bkz.</span><span class="sxs-lookup"><span data-stu-id="98f27-150">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="98f27-151">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="98f27-151">PARAMETERS</span></span>

### <span data-ttu-id="98f27-152">-CNAME</span><span class="sxs-lookup"><span data-stu-id="98f27-152">-Cname</span></span>
<span data-ttu-id="98f27-153">Eklenecek CNAME kaydının kurallı adı.</span><span class="sxs-lookup"><span data-stu-id="98f27-153">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="98f27-154">Bölgenin adına göreli olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="98f27-154">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="98f27-155">Sonlandırıcı nokta olmamalıdır</span><span class="sxs-lookup"><span data-stu-id="98f27-155">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="98f27-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98f27-156">-DefaultProfile</span></span>
<span data-ttu-id="98f27-157">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="98f27-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98f27-158">-Exchange</span><span class="sxs-lookup"><span data-stu-id="98f27-158">-Exchange</span></span>
<span data-ttu-id="98f27-159">Eklenecek MX kaydının posta Exchange ana bilgisayarı.</span><span class="sxs-lookup"><span data-stu-id="98f27-159">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="98f27-160">Bölgenin adına göreli olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="98f27-160">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="98f27-161">Sonlandırıcı nokta olmamalıdır</span><span class="sxs-lookup"><span data-stu-id="98f27-161">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="98f27-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="98f27-162">-Ipv4Address</span></span>
<span data-ttu-id="98f27-163">Eklenecek A kaydının IPv4 adresi.</span><span class="sxs-lookup"><span data-stu-id="98f27-163">The IPv4 address for the A record to add.</span></span>

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

### <span data-ttu-id="98f27-164">-IPv6Adresi</span><span class="sxs-lookup"><span data-stu-id="98f27-164">-Ipv6Address</span></span>
<span data-ttu-id="98f27-165">Eklenecek AAAA kaydının IPv6 adresi.</span><span class="sxs-lookup"><span data-stu-id="98f27-165">The IPv6 address for the AAAA record to add.</span></span>

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

### <span data-ttu-id="98f27-166">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="98f27-166">-Port</span></span>
<span data-ttu-id="98f27-167">Eklenecek SRV kaydının bağlantı noktası numarası.</span><span class="sxs-lookup"><span data-stu-id="98f27-167">The port number for the SRV record to add.</span></span>

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

### <span data-ttu-id="98f27-168">-Tercih</span><span class="sxs-lookup"><span data-stu-id="98f27-168">-Preference</span></span>
<span data-ttu-id="98f27-169">Eklenecek MX kaydının tercih değeri.</span><span class="sxs-lookup"><span data-stu-id="98f27-169">The preference value for the MX record to add.</span></span>

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

### <span data-ttu-id="98f27-170">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="98f27-170">-Priority</span></span>
<span data-ttu-id="98f27-171">Eklenecek öncelik değeri SRV kaydı.</span><span class="sxs-lookup"><span data-stu-id="98f27-171">The priority value SRV record to add.</span></span>

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

### <span data-ttu-id="98f27-172">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="98f27-172">-Ptrdname</span></span>
<span data-ttu-id="98f27-173">Eklenecek PTR kaydının hedef ana bilgisayarı.</span><span class="sxs-lookup"><span data-stu-id="98f27-173">The target host for the PTR record to add.</span></span>
<span data-ttu-id="98f27-174">Bölgenin adına göreli olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="98f27-174">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="98f27-175">Sonlandırıcı nokta olmamalıdır</span><span class="sxs-lookup"><span data-stu-id="98f27-175">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="98f27-176">-Hedef</span><span class="sxs-lookup"><span data-stu-id="98f27-176">-Target</span></span>
<span data-ttu-id="98f27-177">Eklenecek SRV kaydının hedef ana bilgisayarı.</span><span class="sxs-lookup"><span data-stu-id="98f27-177">The target host for the SRV record to add.</span></span>
<span data-ttu-id="98f27-178">Bölgenin adına göreli olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="98f27-178">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="98f27-179">Sonlandırıcı nokta olmamalıdır</span><span class="sxs-lookup"><span data-stu-id="98f27-179">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="98f27-180">-Değer</span><span class="sxs-lookup"><span data-stu-id="98f27-180">-Value</span></span>
<span data-ttu-id="98f27-181">Eklenecek TXT kaydının metin değeri.</span><span class="sxs-lookup"><span data-stu-id="98f27-181">The text value for the TXT record to add.</span></span>

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

### <span data-ttu-id="98f27-182">-Kalınlık</span><span class="sxs-lookup"><span data-stu-id="98f27-182">-Weight</span></span>
<span data-ttu-id="98f27-183">Eklenecek SRV kaydının ağırlık değeri.</span><span class="sxs-lookup"><span data-stu-id="98f27-183">The weight value for the SRV record to add.</span></span>

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

### <span data-ttu-id="98f27-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f27-184">CommonParameters</span></span>
<span data-ttu-id="98f27-185">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="98f27-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f27-186">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98f27-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f27-187">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="98f27-187">INPUTS</span></span>

### <span data-ttu-id="98f27-188">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="98f27-188">None</span></span>

## <span data-ttu-id="98f27-189">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="98f27-189">OUTPUTS</span></span>

### <span data-ttu-id="98f27-190">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="98f27-190">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="98f27-191">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="98f27-191">NOTES</span></span>

## <span data-ttu-id="98f27-192">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="98f27-192">RELATED LINKS</span></span>