---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: 1b2ee31c136c24478ddd69d58c264ce44886c057
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935915"
---
# <span data-ttu-id="8e29d-101">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8e29d-101">Set-AzDnsRecordSet</span></span>

## <span data-ttu-id="8e29d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e29d-102">SYNOPSIS</span></span>
<span data-ttu-id="8e29d-103">DNS kayıt kümesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8e29d-103">Updates a DNS record set.</span></span>

## <span data-ttu-id="8e29d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8e29d-104">SYNTAX</span></span>

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e29d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e29d-105">DESCRIPTION</span></span>
<span data-ttu-id="8e29d-106">**Set-AzDnsRecordSet** cmdlet 'i, yerel bir **RECORDSET** nesnesinden Azure DNS hizmetinde bir kayıt güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8e29d-106">The **Set-AzDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>

<span data-ttu-id="8e29d-107">Bir **Recordset** nesnesini parametre olarak veya Pipeline işlecini kullanarak geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e29d-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>

<span data-ttu-id="8e29d-108">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için *Confirm* parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e29d-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="8e29d-109">Yerel **kayıt** kümesi nesnesi alındıktan sonra Azure DNS 'de değiştirilmişse kayıt kümesi güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="8e29d-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="8e29d-110">Bu, eşzamanlı değişiklikler için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="8e29d-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="8e29d-111">Bu davranışı, yinelenen değişikliklerden bağımsız olarak kayıt kümesini güncelleştiren, *overwrite* parametresini kullanarak kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e29d-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="8e29d-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8e29d-112">EXAMPLES</span></span>

### <span data-ttu-id="8e29d-113">Örnek 1: kayıt kümesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="8e29d-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

<span data-ttu-id="8e29d-114">İlk komut, Get-AzDnsRecordSet cmdlet 'ini kullanarak belirtilen kayıt kümesini alır ve $RecordSet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8e29d-114">The first command uses the Get-AzDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="8e29d-115">İkinci ve üçüncü komutlar, kayıt kümesine iki kayıt eklemek için satır dışı operasyonlardır.</span><span class="sxs-lookup"><span data-stu-id="8e29d-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>

<span data-ttu-id="8e29d-116">Final komutu, güncelleştirmeyi kaydetmek için **set-AzDnsRecordSet** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="8e29d-116">The final command uses the **Set-AzDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="8e29d-117">Örnek 2: SOA kaydını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="8e29d-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="8e29d-118">İlk komut, **Get-AzDnsRecordset** cmdlet 'ini kullanarak belirtilen kayıt kümesini alır ve ardından $Recordset değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8e29d-118">The first command uses the **Get-AzDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="8e29d-119">İkinci komut $RecordSet 'da belirtilen SOA kaydını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8e29d-119">The second command updates the specified SOA record in $RecordSet.</span></span>

<span data-ttu-id="8e29d-120">Son komutu, $RecordSet güncelleştirmeyi yaymak için **set-AzDnsRecordSet** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="8e29d-120">The final command uses the **Set-AzDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="8e29d-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8e29d-121">PARAMETERS</span></span>

### <span data-ttu-id="8e29d-122">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="8e29d-122">-Overwrite</span></span>
<span data-ttu-id="8e29d-123">Yinelenen değişikliklere bakılmaksızın kayıt kümesinin güncelleştirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e29d-123">Indicates to update the record set regardless of concurrent changes.</span></span>

<span data-ttu-id="8e29d-124">Yerel **kayıt** kümesi nesnesi alındıktan sonra Azure DNS 'de değiştirilmişse kayıt kümesi güncelleştirilmeyecek.</span><span class="sxs-lookup"><span data-stu-id="8e29d-124">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="8e29d-125">Bu, eşzamanlı değişiklikler için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="8e29d-125">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="8e29d-126">Bu davranışı bastırmak için, *üzerine yazma* parametresini kullanarak, yinelenen değişikliklere bakılmaksızın kayıt kümesi güncellenir.</span><span class="sxs-lookup"><span data-stu-id="8e29d-126">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e29d-127">-Kayıt kümesi</span><span class="sxs-lookup"><span data-stu-id="8e29d-127">-RecordSet</span></span>
<span data-ttu-id="8e29d-128">Güncelleştirilecek **kayıt kümesini** belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e29d-128">Specifies the **RecordSet** to update.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e29d-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="8e29d-129">-Confirm</span></span>
<span data-ttu-id="8e29d-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8e29d-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e29d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e29d-131">-WhatIf</span></span>
<span data-ttu-id="8e29d-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e29d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e29d-133">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e29d-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e29d-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8e29d-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e29d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e29d-135">CommonParameters</span></span>
<span data-ttu-id="8e29d-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8e29d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e29d-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e29d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e29d-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8e29d-138">INPUTS</span></span>

### <span data-ttu-id="8e29d-139">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8e29d-139">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="8e29d-140">Bir **Recordset** nesnesini bu cmdlet 'e geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e29d-140">You can pass a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="8e29d-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8e29d-141">OUTPUTS</span></span>

### <span data-ttu-id="8e29d-142">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8e29d-142">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="8e29d-143">Bu cmdlet, güncelleştirilmiş **Recordset** nesnesini temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="8e29d-143">This cmdlet returns an object that represents the updated **RecordSet** object.</span></span>

## <span data-ttu-id="8e29d-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8e29d-144">NOTES</span></span>
<span data-ttu-id="8e29d-145">*Confirm* parametresini kullanarak, bu cmdlet 'in onayınızı isteyip istemediğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="8e29d-145">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="8e29d-146">Varsayılan olarak, $ConfirmPreference Windows PowerShell değişkeninde orta veya düşük bir değer varsa cmdlet onay ister.</span><span class="sxs-lookup"><span data-stu-id="8e29d-146">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="8e29d-147">*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="8e29d-147">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="8e29d-148">*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="8e29d-148">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="8e29d-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8e29d-149">RELATED LINKS</span></span>

[<span data-ttu-id="8e29d-150">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8e29d-150">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="8e29d-151">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8e29d-151">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="8e29d-152">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8e29d-152">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)
