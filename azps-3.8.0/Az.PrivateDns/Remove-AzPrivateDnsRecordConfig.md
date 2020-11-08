---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: 1e3362850880f02c648fb3318db226515fc95eef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096494"
---
# <span data-ttu-id="f840c-101">Remove-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="f840c-101">Remove-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="f840c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f840c-102">SYNOPSIS</span></span>
<span data-ttu-id="f840c-103">Yerel kayıt kümesi nesnesinden özel bir DNS kaydını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f840c-103">Removes a Private DNS record from a local record set object.</span></span>

## <span data-ttu-id="f840c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f840c-104">SYNTAX</span></span>

### <span data-ttu-id="f840c-105">A (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f840c-105">A (Default)</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f840c-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="f840c-106">AAAA</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f840c-107">DOSYASıNA</span><span class="sxs-lookup"><span data-stu-id="f840c-107">MX</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f840c-108">PTR</span><span class="sxs-lookup"><span data-stu-id="f840c-108">PTR</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f840c-109">,</span><span class="sxs-lookup"><span data-stu-id="f840c-109">TXT</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f840c-110">SRV</span><span class="sxs-lookup"><span data-stu-id="f840c-110">SRV</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f840c-111">KAYDıNı</span><span class="sxs-lookup"><span data-stu-id="f840c-111">CNAME</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f840c-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="f840c-112">DESCRIPTION</span></span>
<span data-ttu-id="f840c-113">Remove-AzPrivateDnsRecordConfig cmdlet 'i bir kayıt kümesinden özel bir etki alanı adı sistemi (DNS) kaydını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f840c-113">The Remove-AzPrivateDnsRecordConfig cmdlet removes a Private Domain Name System (DNS) record from a record set.</span></span> <span data-ttu-id="f840c-114">Kayıt kümesi nesnesi bir çevrimdışı nesnedir ve değişiklikleri Microsoft Azure özel DNS hizmetine kalıcı hale getirmek için Set-AzPrivateDnsRecordSet cmdlet 'i çalıştırana kadar, özel DNS yanıtlarını değiştirmiyor.</span><span class="sxs-lookup"><span data-stu-id="f840c-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="f840c-115">Kaydı kaldırmak için, bu kayıt türü için tüm alanların tam olarak eşleşmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="f840c-115">To remove a record, all the fields for that record type must match exactly.</span></span> <span data-ttu-id="f840c-116">SOA kayıtlarını ekleyemezsiniz veya kaldıramazsınız.</span><span class="sxs-lookup"><span data-stu-id="f840c-116">You cannot add or remove SOA records.</span></span> <span data-ttu-id="f840c-117">SOA kayıtları, özel bir DNS bölgesi oluşturulduğunda ve özel DNS bölgesi silindiğinde otomatik olarak silindiğinde otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f840c-117">SOA records are automatically created when a Private DNS zone is created and automatically deleted when the Private DNS zone is deleted.</span></span> <span data-ttu-id="f840c-118">RecordSet nesnesini bu cmdlet 'e parametre olarak veya Pipeline işlecini kullanarak geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f840c-118">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="f840c-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f840c-119">EXAMPLES</span></span>

### <span data-ttu-id="f840c-120">Örnek 1: kayıt kümesinden kayıt kaldırma</span><span class="sxs-lookup"><span data-stu-id="f840c-120">Example 1: Remove an A record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f840c-121">Bu örnekte, var olan kayıt kümesinden bir kayıt kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="f840c-121">This example removes an A record from an existing record set.</span></span> <span data-ttu-id="f840c-122">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="f840c-122">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="f840c-123">Kayıt kümesini tümüyle kaldırmak için bkz: Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="f840c-123">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="f840c-124">Örnek 2: kayıt kümesinden AAAA kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="f840c-124">Example 2: Remove an AAAA record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f840c-125">Bu örnekte, varolan bir kayıt kümesinden AAAA kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="f840c-125">This example removes an AAAA record from an existing record set.</span></span> <span data-ttu-id="f840c-126">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="f840c-126">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="f840c-127">Kayıt kümesini tümüyle kaldırmak için bkz: Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="f840c-127">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="f840c-128">Örnek 3: kayıt kümesinden CNAME kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="f840c-128">Example 3: Remove a CNAME record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f840c-129">Bu örnekte, var olan kayıt kümesinden bir CNAME kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="f840c-129">This example removes a CNAME record from an existing record set.</span></span> <span data-ttu-id="f840c-130">CNAME kayıt kümesi en çok bir kayıt içerebileceğinden, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="f840c-130">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="f840c-131">Örnek 4: kayıt kümesinden bir MX kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="f840c-131">Example 4: Remove a MX record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f840c-132">Bu örnekte, var olan kayıt kümesinden bir MX kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="f840c-132">This example removes an MX record from an existing record set.</span></span> <span data-ttu-id="f840c-133">"@" Kayıt adı, bölge Apex bir kayıt kümesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f840c-133">The record name "@" indicates a record set at the zone apex.</span></span> <span data-ttu-id="f840c-134">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="f840c-134">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="f840c-135">Kayıt kümesini tümüyle kaldırmak için bkz: Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="f840c-135">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="f840c-136">Örnek 5: kayıt kümesinden PTR kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="f840c-136">Example 5: Remove a PTR record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f840c-137">Bu örnekte, var olan kayıt kümesinden bir PTR kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="f840c-137">This example removes a PTR record from an existing record set.</span></span> <span data-ttu-id="f840c-138">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="f840c-138">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="f840c-139">Kayıt kümesini tümüyle kaldırmak için bkz: Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="f840c-139">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="f840c-140">Örnek 6: kayıt kümesinden SRV kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="f840c-140">Example 6: Remove a SRV record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f840c-141">Bu örnekte, var olan kayıt kümesinden bir SRV kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="f840c-141">This example removes an SRV record from an existing record set.</span></span> <span data-ttu-id="f840c-142">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="f840c-142">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="f840c-143">Kayıt kümesini tümüyle kaldırmak için bkz: Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="f840c-143">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="f840c-144">Örnek 7: kayıt kümesinden TXT kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="f840c-144">Example 7: Remove a TXT record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Value "This is a TXT Record"  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f840c-145">Bu örnekte, var olan kayıt kümesinden bir TXT kaydı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="f840c-145">This example removes a TXT record from an existing record set.</span></span> <span data-ttu-id="f840c-146">Bu, kayıt kümesindeki tek kayıttır, sonuç boş bir kayıt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="f840c-146">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="f840c-147">Kayıt kümesini tümüyle kaldırmak için bkz: Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="f840c-147">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

## <span data-ttu-id="f840c-148">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f840c-148">PARAMETERS</span></span>

### <span data-ttu-id="f840c-149">-CNAME</span><span class="sxs-lookup"><span data-stu-id="f840c-149">-Cname</span></span>
<span data-ttu-id="f840c-150">Kaldırılacak CNAME kaydının kurallı adı.</span><span class="sxs-lookup"><span data-stu-id="f840c-150">The canonical name of the CNAME record to remove.</span></span>
<span data-ttu-id="f840c-151">Bölgenin adına göreli olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="f840c-151">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f840c-152">Sonlandırıcı nokta olmamalıdır</span><span class="sxs-lookup"><span data-stu-id="f840c-152">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="f840c-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f840c-153">-DefaultProfile</span></span>
<span data-ttu-id="f840c-154">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f840c-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f840c-155">-Exchange</span><span class="sxs-lookup"><span data-stu-id="f840c-155">-Exchange</span></span>
<span data-ttu-id="f840c-156">Kaldırılacak MX kaydının posta Exchange ana bilgisayarı.</span><span class="sxs-lookup"><span data-stu-id="f840c-156">The mail exchange host of the MX record to remove.</span></span>
<span data-ttu-id="f840c-157">Bölgenin adına göreli olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="f840c-157">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f840c-158">Sonlandırıcı nokta olmamalıdır</span><span class="sxs-lookup"><span data-stu-id="f840c-158">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="f840c-159">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="f840c-159">-Ipv4Address</span></span>
<span data-ttu-id="f840c-160">Kaldırılacak kaydın IPv4 adresi.</span><span class="sxs-lookup"><span data-stu-id="f840c-160">The IPv4 address of the A record to remove.</span></span>

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

### <span data-ttu-id="f840c-161">-IPv6Adresi</span><span class="sxs-lookup"><span data-stu-id="f840c-161">-Ipv6Address</span></span>
<span data-ttu-id="f840c-162">Kaldırılacak AAAA kaydının IPv6 adresi.</span><span class="sxs-lookup"><span data-stu-id="f840c-162">The IPv6 address of the AAAA record to remove.</span></span>

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

### <span data-ttu-id="f840c-163">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="f840c-163">-Port</span></span>
<span data-ttu-id="f840c-164">Kaldırılacak SRV kaydının bağlantı noktası numarası.</span><span class="sxs-lookup"><span data-stu-id="f840c-164">The port number of the SRV record to remove.</span></span>

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

### <span data-ttu-id="f840c-165">-Tercih</span><span class="sxs-lookup"><span data-stu-id="f840c-165">-Preference</span></span>
<span data-ttu-id="f840c-166">Kaldırılacak MX kaydının tercih değeri.</span><span class="sxs-lookup"><span data-stu-id="f840c-166">The preference value of the MX record to remove.</span></span>

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

### <span data-ttu-id="f840c-167">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="f840c-167">-Priority</span></span>
<span data-ttu-id="f840c-168">Kaldırılacak SRV kaydının öncelik değeri.</span><span class="sxs-lookup"><span data-stu-id="f840c-168">The priority value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="f840c-169">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="f840c-169">-Ptrdname</span></span>
<span data-ttu-id="f840c-170">Kaldırılacak PTR kaydının hedef ana bilgisayarı.</span><span class="sxs-lookup"><span data-stu-id="f840c-170">The target host of the PTR record to remove.</span></span>
<span data-ttu-id="f840c-171">Bölgenin adına göreli olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="f840c-171">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f840c-172">Sonlandırıcı nokta olmamalıdır</span><span class="sxs-lookup"><span data-stu-id="f840c-172">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="f840c-173">-Kayıt kümesi</span><span class="sxs-lookup"><span data-stu-id="f840c-173">-RecordSet</span></span>
<span data-ttu-id="f840c-174">Kaydın kaldırılacağı kayıt kümesi.</span><span class="sxs-lookup"><span data-stu-id="f840c-174">The record set from which to remove the record.</span></span>

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

### <span data-ttu-id="f840c-175">-Hedef</span><span class="sxs-lookup"><span data-stu-id="f840c-175">-Target</span></span>
<span data-ttu-id="f840c-176">Kaldırılacak SRV kaydının hedef ana bilgisayarı.</span><span class="sxs-lookup"><span data-stu-id="f840c-176">The target host of the SRV record to remove.</span></span>
<span data-ttu-id="f840c-177">Bölgenin adına göreli olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="f840c-177">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f840c-178">Sonlandırıcı nokta olmamalıdır</span><span class="sxs-lookup"><span data-stu-id="f840c-178">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="f840c-179">-Değer</span><span class="sxs-lookup"><span data-stu-id="f840c-179">-Value</span></span>
<span data-ttu-id="f840c-180">Kaldırılacak TXT kaydının metin değeri.</span><span class="sxs-lookup"><span data-stu-id="f840c-180">The text value of the TXT record to remove.</span></span>

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

### <span data-ttu-id="f840c-181">-Kalınlık</span><span class="sxs-lookup"><span data-stu-id="f840c-181">-Weight</span></span>
<span data-ttu-id="f840c-182">Kaldırılacak SRV kaydının ağırlık değeri.</span><span class="sxs-lookup"><span data-stu-id="f840c-182">The weight value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="f840c-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f840c-183">CommonParameters</span></span>
<span data-ttu-id="f840c-184">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f840c-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f840c-185">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f840c-185">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f840c-186">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f840c-186">INPUTS</span></span>

### <span data-ttu-id="f840c-187">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f840c-187">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="f840c-188">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f840c-188">OUTPUTS</span></span>

### <span data-ttu-id="f840c-189">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f840c-189">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="f840c-190">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f840c-190">NOTES</span></span>

## <span data-ttu-id="f840c-191">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f840c-191">RELATED LINKS</span></span>