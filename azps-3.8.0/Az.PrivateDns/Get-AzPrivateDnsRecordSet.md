---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
ms.openlocfilehash: ade9d95b6388a667f55df24db107a2326fa001ed
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097960"
---
# <span data-ttu-id="0da0f-101">Get-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0da0f-101">Get-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="0da0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0da0f-102">SYNOPSIS</span></span>
<span data-ttu-id="0da0f-103">Özel bir DNS bölgesinden kayıt kümesi alır.</span><span class="sxs-lookup"><span data-stu-id="0da0f-103">Gets a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="0da0f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0da0f-104">SYNTAX</span></span>

### <span data-ttu-id="0da0f-105">Noname (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0da0f-105">FieldsWithNoName (Default)</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0da0f-106">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="0da0f-106">Fields</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0da0f-107">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="0da0f-107">Object</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0da0f-108">ObjectWithNoName</span><span class="sxs-lookup"><span data-stu-id="0da0f-108">ObjectWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0da0f-109">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="0da0f-109">ResourceId</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0da0f-110">Resourceıdwithnoname</span><span class="sxs-lookup"><span data-stu-id="0da0f-110">ResourceIdWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0da0f-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="0da0f-111">DESCRIPTION</span></span>
<span data-ttu-id="0da0f-112">Get-AzPrivateDnsRecordSet cmdlet 'i belirtilen özel bölgedeki özel etki alanı adı sistemi (DNS) kayıt kümesini belirtilen ad ve türle alır.</span><span class="sxs-lookup"><span data-stu-id="0da0f-112">The Get-AzPrivateDnsRecordSet cmdlet gets the Private Domain Name System (DNS) record set with the specified name and type, in the specified private zone.</span></span> <span data-ttu-id="0da0f-113">Name veya RecordType parametrelerini belirtmezseniz, bu cmdlet özel bölgedeki belirtilen türdeki tüm kayıt kümelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0da0f-113">If you do not specify the Name or RecordType parameters, this cmdlet returns all record sets of the specified type in the private zone.</span></span> <span data-ttu-id="0da0f-114">Kayıt türü parametresini belirtirseniz ancak name parametresini belirtmezseniz, bu cmdlet belirtilen kayıt türünün tüm kayıt kümelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0da0f-114">If you specify the RecordType parameter but not the Name parameter, this cmdlet returns all record sets of the specified record type.</span></span> <span data-ttu-id="0da0f-115">Pipeline işlecini kullanarak, bir PSPrivateDnsZone nesnesini bu cmdlet 'e geçirebilir veya bölge parametresi olarak bir PSPrivateDnsZone nesnesi geçirebilirsiniz veya bölge ve kaynak grubunu adıyla belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0da0f-115">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or alternatively you can specify the zone and resource group by name.</span></span> <span data-ttu-id="0da0f-116">Özel bölgesini özel bölgesinin kaynak kimliğini kullanarak da belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0da0f-116">You can also specify the private zone using the Resource Id of the private zone.</span></span>

## <span data-ttu-id="0da0f-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0da0f-117">EXAMPLES</span></span>

### <span data-ttu-id="0da0f-118">Örnek 1: belirtilen ad ve türde kayıt kümelerini alma</span><span class="sxs-lookup"><span data-stu-id="0da0f-118">Example 1: Get record sets with a specified name and type</span></span>
```powershell
PS C:\>$RecordSet = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
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

<span data-ttu-id="0da0f-119">Bu komut, kayıt türü kayıt kümesini belirtilen kaynak grubunda ve özel bölgesinde alır ve $RecordSet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0da0f-119">This command gets the record set of record type A named www in the specified resource group and private zone, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="0da0f-120">Name ve RecordType parametreleri belirtildiğinden, yalnızca bir RecordSet nesnesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="0da0f-120">Because the Name and RecordType parameters are specified, only one RecordSet object is returned.</span></span>

### <span data-ttu-id="0da0f-121">Örnek 2: belirtilen türde kayıt kümelerini alma</span><span class="sxs-lookup"><span data-stu-id="0da0f-121">Example 2: Get record sets of a specified type</span></span>
```powershell
PS C:\>$RecordSets = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www2
Name              : www2
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {2.3.4.5}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="0da0f-122">Bu komut MyResourceGroup adlı kaynak grubundaki myzone.com adlı özel bölgedeki kayıt türündeki tüm kayıt kümesi dizisini alır ve $RecordSets değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0da0f-122">This command gets an array of all record sets of record type A in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="0da0f-123">Örnek 3: özel bir bölgedeki tüm kayıt kümelerini alma</span><span class="sxs-lookup"><span data-stu-id="0da0f-123">Example 3: Get all record sets in a private zone</span></span>
```powershell
PS C:\>$RecordSets = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="0da0f-124">Bu komut, MyResourceGroup adındaki kaynak grubundaki myzone.com adlı özel bölgedeki tüm kayıt kümelerinin bir dizisini alır ve sonra bunları $RecordSets değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0da0f-124">This command gets an array of all record sets in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="0da0f-125">Örnek 4: PSPrivateDnsZone nesnesini kullanarak özel bir bölgedeki tüm kayıt kümelerini alma</span><span class="sxs-lookup"><span data-stu-id="0da0f-125">Example 4: Get all record sets in a private zone, using a PSPrivateDnsZone object</span></span>
```powershell
PS C:\> $Zone = Get-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzPrivateDnsRecordSet -Zone $Zone

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="0da0f-126">Bu örnek, yukarıdaki örnek 3 ile eşdeğerdir.</span><span class="sxs-lookup"><span data-stu-id="0da0f-126">This example is equivalent to Example 3 above.</span></span> <span data-ttu-id="0da0f-127">Bu kez, özel bölge özel bir bölge nesnesi kullanılarak belirtilir.</span><span class="sxs-lookup"><span data-stu-id="0da0f-127">This time, the private zone is specified using a private zone object.</span></span>

## <span data-ttu-id="0da0f-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0da0f-128">PARAMETERS</span></span>

### <span data-ttu-id="0da0f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da0f-129">-DefaultProfile</span></span>
<span data-ttu-id="0da0f-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0da0f-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0da0f-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="0da0f-131">-Name</span></span>
<span data-ttu-id="0da0f-132">Bu kayıt kümesindeki kayıtların adı (bölgenin adına ve sonlandırma noktası olmadan).</span><span class="sxs-lookup"><span data-stu-id="0da0f-132">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Object, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da0f-133">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="0da0f-133">-ParentResourceId</span></span>
<span data-ttu-id="0da0f-134">Özel DNS bölge RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="0da0f-134">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId, ResourceIdWithNoName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0da0f-135">-RecordType</span><span class="sxs-lookup"><span data-stu-id="0da0f-135">-RecordType</span></span>
<span data-ttu-id="0da0f-136">Bu kayıt kümesindeki DNS kayıtlarının türü.</span><span class="sxs-lookup"><span data-stu-id="0da0f-136">The type of DNS records in this record set.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.PrivateDns.Models.RecordType]
Parameter Sets: FieldsWithNoName, ObjectWithNoName, ResourceIdWithNoName
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.PrivateDns.Models.RecordType]
Parameter Sets: Fields, Object, ResourceId
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da0f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0da0f-137">-ResourceGroupName</span></span>
<span data-ttu-id="0da0f-138">Bölgenin ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="0da0f-138">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: FieldsWithNoName, Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da0f-139">-Bölge</span><span class="sxs-lookup"><span data-stu-id="0da0f-139">-Zone</span></span>
<span data-ttu-id="0da0f-140">Kayıt kümesinin oluşturulacağı bölgeyi temsil eden DnsZone nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0da0f-140">The DnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object, ObjectWithNoName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0da0f-141">-BölgeAdı</span><span class="sxs-lookup"><span data-stu-id="0da0f-141">-ZoneName</span></span>
<span data-ttu-id="0da0f-142">Kayıt kümesinin oluşturulacağı bölge (Sonlandırıcı nokta olmadan).</span><span class="sxs-lookup"><span data-stu-id="0da0f-142">The zone in which to create the record set (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: FieldsWithNoName, Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da0f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da0f-143">CommonParameters</span></span>
<span data-ttu-id="0da0f-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0da0f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da0f-145">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0da0f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da0f-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0da0f-146">INPUTS</span></span>

### <span data-ttu-id="0da0f-147">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="0da0f-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="0da0f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="0da0f-148">System.String</span></span>

## <span data-ttu-id="0da0f-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0da0f-149">OUTPUTS</span></span>

### <span data-ttu-id="0da0f-150">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0da0f-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="0da0f-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0da0f-151">NOTES</span></span>

## <span data-ttu-id="0da0f-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0da0f-152">RELATED LINKS</span></span>
