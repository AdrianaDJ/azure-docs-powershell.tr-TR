---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: 37cd1f7b00cbfae6421b5dab06ce87c0f462434c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760898"
---
# <span data-ttu-id="f9dff-101">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f9dff-101">Get-AzDnsRecordSet</span></span>

## <span data-ttu-id="f9dff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9dff-102">SYNOPSIS</span></span>
<span data-ttu-id="f9dff-103">DNS kayıt kümesi alır.</span><span class="sxs-lookup"><span data-stu-id="f9dff-103">Gets a DNS record set.</span></span>

## <span data-ttu-id="f9dff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f9dff-104">SYNTAX</span></span>

### <span data-ttu-id="f9dff-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="f9dff-105">Fields</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9dff-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="f9dff-106">Object</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9dff-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f9dff-107">DESCRIPTION</span></span>
<span data-ttu-id="f9dff-108">**Get-AzDnsRecordSet** cmdlet 'i belirtilen ad ve türüyle belirtilen bölgedeki etki alanı adı SISTEMI (DNS) kayıt kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="f9dff-108">The **Get-AzDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>
<span data-ttu-id="f9dff-109">*Name* veya *RecordType* parametrelerini belirtmezseniz, bu cmdlet bölgedeki belirtilen türdeki tüm kayıt kümelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="f9dff-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="f9dff-110">*Kayıt türü* parametresini belirtirseniz ancak *Name* parametresini belirtmezseniz, bu cmdlet belirtilen kayıt türünün tüm kayıt kümelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="f9dff-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>
<span data-ttu-id="f9dff-111">Bu cmdlet 'e bir **dnsZone** nesnesi geçirmek için Pipeline işlecini kullanabilir veya bir **dnsZone** nesnesini *bölge* parametresi olarak geçirebilirsiniz ya da bölge ve kaynak grubunu adıyla belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9dff-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="f9dff-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f9dff-112">EXAMPLES</span></span>

### <span data-ttu-id="f9dff-113">Örnek 1: belirtilen ad ve türde kayıt kümelerini alma</span><span class="sxs-lookup"><span data-stu-id="f9dff-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="f9dff-114">Bu komut, kayıt türü kayıt kümesini belirtilen kaynak grubu ve bölgesinde alır ve $RecordSet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f9dff-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="f9dff-115">*Name* ve *RecordType* parametreleri belirtildiğinden, yalnızca bir **Recordset** nesnesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="f9dff-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="f9dff-116">Örnek 2: belirtilen türde kayıt kümelerini alma</span><span class="sxs-lookup"><span data-stu-id="f9dff-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="f9dff-117">Bu komut MyResourceGroup adındaki kaynak grubundaki myzone.com adlı bölgedeki kayıt türü kayıt kümesinin bir dizisini alır ve ardından $RecordSets değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f9dff-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="f9dff-118">Örnek 3: bölgedeki tüm kayıt kümelerini alma</span><span class="sxs-lookup"><span data-stu-id="f9dff-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="f9dff-119">Bu komut, MyResourceGroup adındaki kaynak grubundaki myzone.com adlı bölgedeki tüm kayıt kümelerinin bir dizisini alır ve ardından $RecordSets değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f9dff-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="f9dff-120">Örnek 4: DnsZone nesnesini kullanarak bölgedeki tüm kayıt kümelerini alma</span><span class="sxs-lookup"><span data-stu-id="f9dff-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

<span data-ttu-id="f9dff-121">Bu örnek, yukarıdaki örnek 3 ile eşdeğerdir.</span><span class="sxs-lookup"><span data-stu-id="f9dff-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="f9dff-122">Bu kez bölge, bölge nesnesi kullanılarak belirtilir.</span><span class="sxs-lookup"><span data-stu-id="f9dff-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="f9dff-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f9dff-123">PARAMETERS</span></span>

### <span data-ttu-id="f9dff-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9dff-124">-DefaultProfile</span></span>
<span data-ttu-id="f9dff-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f9dff-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9dff-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="f9dff-126">-Name</span></span>
<span data-ttu-id="f9dff-127">Alınacak **kayıt kümesinin** adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9dff-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="f9dff-128">*Name* parametresini belirtmezseniz, belirtilen türdeki tüm kayıt kümeleri döndürülür.</span><span class="sxs-lookup"><span data-stu-id="f9dff-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

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

### <span data-ttu-id="f9dff-129">-RecordType</span><span class="sxs-lookup"><span data-stu-id="f9dff-129">-RecordType</span></span>
<span data-ttu-id="f9dff-130">Bu cmdlet 'in aldığı DNS kaydının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9dff-130">Specifies the type of DNS record that this cmdlet gets.</span></span>
<span data-ttu-id="f9dff-131">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="f9dff-131">Valid values are:</span></span> 
- <span data-ttu-id="f9dff-132">Bir</span><span class="sxs-lookup"><span data-stu-id="f9dff-132">A</span></span>
- <span data-ttu-id="f9dff-133">AAAA</span><span class="sxs-lookup"><span data-stu-id="f9dff-133">AAAA</span></span>
- <span data-ttu-id="f9dff-134">KAYDıNı</span><span class="sxs-lookup"><span data-stu-id="f9dff-134">CNAME</span></span>
- <span data-ttu-id="f9dff-135">DOSYASıNA</span><span class="sxs-lookup"><span data-stu-id="f9dff-135">MX</span></span>
- <span data-ttu-id="f9dff-136">Seç</span><span class="sxs-lookup"><span data-stu-id="f9dff-136">NS</span></span>
- <span data-ttu-id="f9dff-137">PTR</span><span class="sxs-lookup"><span data-stu-id="f9dff-137">PTR</span></span>
- <span data-ttu-id="f9dff-138">SOA</span><span class="sxs-lookup"><span data-stu-id="f9dff-138">SOA</span></span>
- <span data-ttu-id="f9dff-139">SRV</span><span class="sxs-lookup"><span data-stu-id="f9dff-139">SRV</span></span>
- <span data-ttu-id="f9dff-140">TXT *RecordType* parametresini belirtmezseniz, *Name* parametresini de atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9dff-140">TXT If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="f9dff-141">Bu cmdlet, bölgedeki tüm kayıt kümelerini (tüm adlarda ve türlerinde) döndürür.</span><span class="sxs-lookup"><span data-stu-id="f9dff-141">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

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

### <span data-ttu-id="f9dff-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9dff-142">-ResourceGroupName</span></span>
<span data-ttu-id="f9dff-143">DNS bölgesini içeren kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9dff-143">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="f9dff-144">Bölge adı da belirtilmelidir ve *BölgeAdı* da belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="f9dff-144">The zone name must also be specified, using the *ZoneName* parameter.</span></span>
<span data-ttu-id="f9dff-145">Alternatif olarak, bölge parametresini kullanarak bir **dnsZone** nesnesini *geçirerek bölgeyi ve* kaynak grubunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9dff-145">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="f9dff-146">-Bölge</span><span class="sxs-lookup"><span data-stu-id="f9dff-146">-Zone</span></span>
<span data-ttu-id="f9dff-147">Bu cmdlet 'in aldığı kayıt kümesini içeren DNS bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9dff-147">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="f9dff-148">Alternatif olarak, bölgeyi *BölgeAdı* ve *resourcegroupname* parametrelerini kullanarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9dff-148">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="f9dff-149">-BölgeAdı</span><span class="sxs-lookup"><span data-stu-id="f9dff-149">-ZoneName</span></span>
<span data-ttu-id="f9dff-150">Alınacak kayıt kümesini içeren DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9dff-150">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="f9dff-151">Bölgeyi içeren kaynak grubunun da belirtilmesi için, *Resourcegroupname* parametresi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f9dff-151">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="f9dff-152">Alternatif olarak, bölge ve kaynak grubunu, *bölge* parametresini kullanarak bir DNS bölgesi nesnesini geçirerek belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9dff-152">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="f9dff-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9dff-153">CommonParameters</span></span>
<span data-ttu-id="f9dff-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f9dff-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9dff-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9dff-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9dff-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f9dff-156">INPUTS</span></span>

### <span data-ttu-id="f9dff-157">System. String</span><span class="sxs-lookup"><span data-stu-id="f9dff-157">System.String</span></span>

### <span data-ttu-id="f9dff-158">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="f9dff-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="f9dff-159">System. Nullable ' 1 [[Microsoft. Azure. Management. DNS. modeller. RecordType, Microsoft. Azure. Management. DNS, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f9dff-159">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="f9dff-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f9dff-160">OUTPUTS</span></span>

### <span data-ttu-id="f9dff-161">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f9dff-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="f9dff-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f9dff-162">NOTES</span></span>

## <span data-ttu-id="f9dff-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f9dff-163">RELATED LINKS</span></span>

[<span data-ttu-id="f9dff-164">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f9dff-164">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="f9dff-165">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f9dff-165">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="f9dff-166">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f9dff-166">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)


