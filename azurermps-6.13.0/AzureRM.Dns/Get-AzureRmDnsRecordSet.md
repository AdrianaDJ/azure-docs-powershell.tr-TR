---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/get-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
ms.openlocfilehash: c45fc33ec45ce0843fe7ef832a70ec622b14af8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592314"
---
# <span data-ttu-id="b566d-101">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b566d-101">Get-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="b566d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b566d-102">SYNOPSIS</span></span>
<span data-ttu-id="b566d-103">DNS kayıt kümesi alır.</span><span class="sxs-lookup"><span data-stu-id="b566d-103">Gets a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b566d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b566d-104">SYNTAX</span></span>

### <span data-ttu-id="b566d-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="b566d-105">Fields</span></span>
```
Get-AzureRmDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b566d-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="b566d-106">Object</span></span>
```
Get-AzureRmDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b566d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b566d-107">DESCRIPTION</span></span>
<span data-ttu-id="b566d-108">**Get-AzureRmDnsRecordSet** cmdlet 'i belirtilen ad ve türüyle belirtilen bölgedeki etki alanı adı SISTEMI (DNS) kayıt kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="b566d-108">The **Get-AzureRmDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>
<span data-ttu-id="b566d-109">*Name* veya *RecordType* parametrelerini belirtmezseniz, bu cmdlet bölgedeki belirtilen türdeki tüm kayıt kümelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b566d-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="b566d-110">*Kayıt türü* parametresini belirtirseniz ancak *Name* parametresini belirtmezseniz, bu cmdlet belirtilen kayıt türünün tüm kayıt kümelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b566d-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>
<span data-ttu-id="b566d-111">Bu cmdlet 'e bir **dnsZone** nesnesi geçirmek için Pipeline işlecini kullanabilir veya bir **dnsZone** nesnesini *bölge* parametresi olarak geçirebilirsiniz ya da bölge ve kaynak grubunu adıyla belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b566d-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="b566d-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b566d-112">EXAMPLES</span></span>

### <span data-ttu-id="b566d-113">Örnek 1: belirtilen ad ve türde kayıt kümelerini alma</span><span class="sxs-lookup"><span data-stu-id="b566d-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="b566d-114">Bu komut, kayıt türü kayıt kümesini belirtilen kaynak grubu ve bölgesinde alır ve $RecordSet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b566d-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="b566d-115">*Name* ve *RecordType* parametreleri belirtildiğinden, yalnızca bir **Recordset** nesnesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="b566d-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="b566d-116">Örnek 2: belirtilen türde kayıt kümelerini alma</span><span class="sxs-lookup"><span data-stu-id="b566d-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="b566d-117">Bu komut MyResourceGroup adındaki kaynak grubundaki myzone.com adlı bölgedeki kayıt türü kayıt kümesinin bir dizisini alır ve ardından $RecordSets değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b566d-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="b566d-118">Örnek 3: bölgedeki tüm kayıt kümelerini alma</span><span class="sxs-lookup"><span data-stu-id="b566d-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="b566d-119">Bu komut, MyResourceGroup adındaki kaynak grubundaki myzone.com adlı bölgedeki tüm kayıt kümelerinin bir dizisini alır ve ardından $RecordSets değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b566d-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="b566d-120">Örnek 4: DnsZone nesnesini kullanarak bölgedeki tüm kayıt kümelerini alma</span><span class="sxs-lookup"><span data-stu-id="b566d-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzureRmDnsRecordSet -Zone $Zone
```

<span data-ttu-id="b566d-121">Bu örnek, yukarıdaki örnek 3 ile eşdeğerdir.</span><span class="sxs-lookup"><span data-stu-id="b566d-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="b566d-122">Bu kez bölge, bölge nesnesi kullanılarak belirtilir.</span><span class="sxs-lookup"><span data-stu-id="b566d-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="b566d-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b566d-123">PARAMETERS</span></span>

### <span data-ttu-id="b566d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b566d-124">-DefaultProfile</span></span>
<span data-ttu-id="b566d-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b566d-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b566d-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="b566d-126">-Name</span></span>
<span data-ttu-id="b566d-127">Alınacak **kayıt kümesinin** adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b566d-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="b566d-128">*Name* parametresini belirtmezseniz, belirtilen türdeki tüm kayıt kümeleri döndürülür.</span><span class="sxs-lookup"><span data-stu-id="b566d-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b566d-129">-RecordType</span><span class="sxs-lookup"><span data-stu-id="b566d-129">-RecordType</span></span>
<span data-ttu-id="b566d-130">Bu cmdlet 'in aldığı DNS kaydının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b566d-130">Specifies the type of DNS record that this cmdlet gets.</span></span>
<span data-ttu-id="b566d-131">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="b566d-131">Valid values are:</span></span> 
- <span data-ttu-id="b566d-132">Bir</span><span class="sxs-lookup"><span data-stu-id="b566d-132">A</span></span>
- <span data-ttu-id="b566d-133">AAAA</span><span class="sxs-lookup"><span data-stu-id="b566d-133">AAAA</span></span>
- <span data-ttu-id="b566d-134">KAYDıNı</span><span class="sxs-lookup"><span data-stu-id="b566d-134">CNAME</span></span>
- <span data-ttu-id="b566d-135">DOSYASıNA</span><span class="sxs-lookup"><span data-stu-id="b566d-135">MX</span></span>
- <span data-ttu-id="b566d-136">Seç</span><span class="sxs-lookup"><span data-stu-id="b566d-136">NS</span></span>
- <span data-ttu-id="b566d-137">PTR</span><span class="sxs-lookup"><span data-stu-id="b566d-137">PTR</span></span>
- <span data-ttu-id="b566d-138">SOA</span><span class="sxs-lookup"><span data-stu-id="b566d-138">SOA</span></span>
- <span data-ttu-id="b566d-139">SRV</span><span class="sxs-lookup"><span data-stu-id="b566d-139">SRV</span></span>
- <span data-ttu-id="b566d-140">TXT *RecordType* parametresini belirtmezseniz, *Name* parametresini de atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b566d-140">TXT If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="b566d-141">Bu cmdlet, bölgedeki tüm kayıt kümelerini (tüm adlarda ve türlerinde) döndürür.</span><span class="sxs-lookup"><span data-stu-id="b566d-141">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.RecordType]
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b566d-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b566d-142">-ResourceGroupName</span></span>
<span data-ttu-id="b566d-143">DNS bölgesini içeren kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b566d-143">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="b566d-144">Bölge adı da belirtilmelidir ve *BölgeAdı* da belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="b566d-144">The zone name must also be specified, using the *ZoneName* parameter.</span></span>
<span data-ttu-id="b566d-145">Alternatif olarak, bölge parametresini kullanarak bir **dnsZone** nesnesini *geçirerek bölgeyi ve* kaynak grubunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b566d-145">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b566d-146">-Bölge</span><span class="sxs-lookup"><span data-stu-id="b566d-146">-Zone</span></span>
<span data-ttu-id="b566d-147">Bu cmdlet 'in aldığı kayıt kümesini içeren DNS bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b566d-147">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="b566d-148">Alternatif olarak, bölgeyi *BölgeAdı* ve *resourcegroupname* parametrelerini kullanarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b566d-148">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b566d-149">-BölgeAdı</span><span class="sxs-lookup"><span data-stu-id="b566d-149">-ZoneName</span></span>
<span data-ttu-id="b566d-150">Alınacak kayıt kümesini içeren DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b566d-150">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="b566d-151">Bölgeyi içeren kaynak grubunun da belirtilmesi için, *Resourcegroupname* parametresi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b566d-151">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="b566d-152">Alternatif olarak, bölge ve kaynak grubunu, *bölge* parametresini kullanarak bir DNS bölgesi nesnesini geçirerek belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b566d-152">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b566d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b566d-153">CommonParameters</span></span>
<span data-ttu-id="b566d-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b566d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b566d-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b566d-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b566d-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b566d-156">INPUTS</span></span>

### <span data-ttu-id="b566d-157">System. String</span><span class="sxs-lookup"><span data-stu-id="b566d-157">System.String</span></span>

### <span data-ttu-id="b566d-158">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="b566d-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="b566d-159">Parametreler: bölge (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b566d-159">Parameters: Zone (ByValue)</span></span>

### <span data-ttu-id="b566d-160">System. Nullable ' 1 [[Microsoft. Azure. Management. DNS. modeller. RecordType, Microsoft. Azure. Management. DNS, Version = 2.1.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b566d-160">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=2.1.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="b566d-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b566d-161">OUTPUTS</span></span>

### <span data-ttu-id="b566d-162">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b566d-162">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="b566d-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b566d-163">NOTES</span></span>

## <span data-ttu-id="b566d-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b566d-164">RELATED LINKS</span></span>

[<span data-ttu-id="b566d-165">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b566d-165">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="b566d-166">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b566d-166">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="b566d-167">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b566d-167">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)


