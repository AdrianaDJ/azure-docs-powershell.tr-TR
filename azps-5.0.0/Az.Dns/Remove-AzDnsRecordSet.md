---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: f5d7075322bb2b5a4b61635400664f0e909f126d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277469"
---
# <span data-ttu-id="1711d-101">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1711d-101">Remove-AzDnsRecordSet</span></span>

## <span data-ttu-id="1711d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1711d-102">SYNOPSIS</span></span>
<span data-ttu-id="1711d-103">Kayıt kümesini siler.</span><span class="sxs-lookup"><span data-stu-id="1711d-103">Deletes a record set.</span></span>

## <span data-ttu-id="1711d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1711d-104">SYNTAX</span></span>

### <span data-ttu-id="1711d-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="1711d-105">Fields</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1711d-106">Karıştır</span><span class="sxs-lookup"><span data-stu-id="1711d-106">Mixed</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1711d-107">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="1711d-107">Object</span></span>
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1711d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1711d-108">DESCRIPTION</span></span>
<span data-ttu-id="1711d-109">**Remove-AzDnsRecordSet** cmdlet 'i belirtilen bölgeden belirtilen kayıt kümesini siler.</span><span class="sxs-lookup"><span data-stu-id="1711d-109">The **Remove-AzDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="1711d-110">Bölge Apex otomatik olarak oluşturulan SOA veya ad sunucusu (NS) kayıtlarını silemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="1711d-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>
<span data-ttu-id="1711d-111">Bir **Recordset** nesnesini, ardışık düzen işlecini veya parametre olarak bu cmdlet 'e geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1711d-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="1711d-112">Ad ve kayıt **kümesi** **nesnesi kullanmadan** bir kayıt kümesi tanımlamak için, bu cmdlet 'e, ardışık düzen işlecini veya parametre olarak kullanarak bölgeyi Bu cmdlet 'e geçirmelisiniz ya da *BölgeAdı* ve *resourcegroupname* parametrelerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1711d-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="1711d-113">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için Confirm parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1711d-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="1711d-114">Kayıt **kümesini kayıt kümesi nesnesi kullanarak** belirtirken, yerel **kayıt** kümesi NESNESI alındıktan sonra Azure DNS 'de değiştirilmişse kayıt kümesi silinmez.</span><span class="sxs-lookup"><span data-stu-id="1711d-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="1711d-115">Bu, eşzamanlı değişiklikler için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="1711d-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="1711d-116">Bunu, yinelenen değişikliklerden bağımsız olarak kayıt kümesini silen *overwrite* parametresini kullanarak kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1711d-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="1711d-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1711d-117">EXAMPLES</span></span>

### <span data-ttu-id="1711d-118">Örnek 1: kayıt kümesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="1711d-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="1711d-119">İlk komut belirtilen kayıt kümesini alır ve $RecordSet değişkeninde depolar. İkinci komut $RecordSet 'da kayıt kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1711d-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="1711d-120">Örnek 2: kayıt kümesini kaldırma ve tüm onayı gösterme</span><span class="sxs-lookup"><span data-stu-id="1711d-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="1711d-121">İlk komut belirtilen kayıt kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="1711d-121">The first command gets the specified record set.</span></span>
<span data-ttu-id="1711d-122">İkinci komut, bu arada değişmiş olsa bile kayıt kümesini siler.</span><span class="sxs-lookup"><span data-stu-id="1711d-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="1711d-123">Onay istemlerinin bastırılması</span><span class="sxs-lookup"><span data-stu-id="1711d-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="1711d-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1711d-124">PARAMETERS</span></span>

### <span data-ttu-id="1711d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1711d-125">-DefaultProfile</span></span>
<span data-ttu-id="1711d-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1711d-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1711d-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="1711d-127">-Name</span></span>
<span data-ttu-id="1711d-128">Kaldırılacak **kayıt kümesinin** adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1711d-128">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="1711d-129">Ada göre kayıt kümesi belirtildiğinde, DNS bölgesi, *bölge* parametresi veya *BölgeAdı* ve *resourcegroupname* parametreleri kullanılarak belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="1711d-129">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="1711d-130">Alternatif olarak, kayıt kümesi, *Recordset* parametresi kullanılarak geçirilen bir **Recordset** nesnesi kullanılarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="1711d-130">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1711d-131">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="1711d-131">-Overwrite</span></span>
<span data-ttu-id="1711d-132">Kayıt **kümesini kayıt kümesi nesnesi kullanarak** belirtirken, yerel **kayıt** kümesi NESNESI alındıktan sonra Azure DNS 'de değiştirilmişse kayıt kümesi silinmez.</span><span class="sxs-lookup"><span data-stu-id="1711d-132">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="1711d-133">Bu, eşzamanlı değişiklikler için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="1711d-133">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="1711d-134">Bu, yinelenen değişikliklerden bağımsız olarak kayıt kümesini silen, *overwrite* parametresi kullanılarak bastırılabilir.</span><span class="sxs-lookup"><span data-stu-id="1711d-134">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1711d-135">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1711d-135">-PassThru</span></span>
<span data-ttu-id="1711d-136">geçiş</span><span class="sxs-lookup"><span data-stu-id="1711d-136">passthru</span></span>

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

### <span data-ttu-id="1711d-137">-Kayıt kümesi</span><span class="sxs-lookup"><span data-stu-id="1711d-137">-RecordSet</span></span>
<span data-ttu-id="1711d-138">Kaldırılacak **kayıt kümesi** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1711d-138">Specifies the **RecordSet** object to remove.</span></span>
<span data-ttu-id="1711d-139">Alternatif olarak, kayıt kümesi *ad* ve *bölge* parametreleri kullanılarak veya *Name, BölgeAdı* ve *resourcegroupname* parametrelerini kullanarak *ZoneName* belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="1711d-139">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1711d-140">-RecordType</span><span class="sxs-lookup"><span data-stu-id="1711d-140">-RecordType</span></span>
<span data-ttu-id="1711d-141">DNS kaydı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1711d-141">Specifies the type of DNS record.</span></span>
<span data-ttu-id="1711d-142">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="1711d-142">Valid values are:</span></span>
- <span data-ttu-id="1711d-143">Bir</span><span class="sxs-lookup"><span data-stu-id="1711d-143">A</span></span>
- <span data-ttu-id="1711d-144">AAAA</span><span class="sxs-lookup"><span data-stu-id="1711d-144">AAAA</span></span>
- <span data-ttu-id="1711d-145">KAYDıNı</span><span class="sxs-lookup"><span data-stu-id="1711d-145">CNAME</span></span>
- <span data-ttu-id="1711d-146">DOSYASıNA</span><span class="sxs-lookup"><span data-stu-id="1711d-146">MX</span></span>
- <span data-ttu-id="1711d-147">Seç</span><span class="sxs-lookup"><span data-stu-id="1711d-147">NS</span></span>
- <span data-ttu-id="1711d-148">PTR</span><span class="sxs-lookup"><span data-stu-id="1711d-148">PTR</span></span>
- <span data-ttu-id="1711d-149">SRV</span><span class="sxs-lookup"><span data-stu-id="1711d-149">SRV</span></span>
- <span data-ttu-id="1711d-150">Bölge silindiğinde TXT SOA kayıtları otomatik olarak silinir.</span><span class="sxs-lookup"><span data-stu-id="1711d-150">TXT SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="1711d-151">SOA kayıtlarını el ile silemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="1711d-151">You cannot manually delete SOA records.</span></span>

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1711d-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1711d-152">-ResourceGroupName</span></span>
<span data-ttu-id="1711d-153">Silinecek **kayıt kümesini** içeren DNS bölgesini içeren kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1711d-153">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="1711d-154">Bu parametre yalnızca, kayıt kümesi ve DNS bölgesi ad ve *BölgeAdı* kullanılarak belirtildiğinde uygulanabilir *Name* .</span><span class="sxs-lookup"><span data-stu-id="1711d-154">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>
<span data-ttu-id="1711d-155">Alternatif olarak, kayıt *kümesini kayıt kümesi parametresini veya* *ad* ve *bölge* parametrelerini kullanarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1711d-155">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="1711d-156">-Bölge</span><span class="sxs-lookup"><span data-stu-id="1711d-156">-Zone</span></span>
<span data-ttu-id="1711d-157">Silinecek **kayıt kümesini** içeren DNS bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1711d-157">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="1711d-158">Bu parametre yalnızca *Name* parametresi kullanılarak kayıt kümesi belirtildiğinde uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="1711d-158">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>
<span data-ttu-id="1711d-159">Alternatif olarak, kayıt *kümesini kayıt kümesi parametresini veya* *Name, BölgeAdı* ve *resourcegroupname* parametrelerini kullanarak *ZoneName* belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1711d-159">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1711d-160">-BölgeAdı</span><span class="sxs-lookup"><span data-stu-id="1711d-160">-ZoneName</span></span>
<span data-ttu-id="1711d-161">Silinecek **kayıt kümesini** içeren bölgenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1711d-161">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="1711d-162">*Name* ve *resourcegroupname* parametrelerini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1711d-162">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="1711d-163">Alternatif olarak, kayıt kümesi, kayıt *kümesi* parametresi veya *ad* ve *bölge* parametreleriyle belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="1711d-163">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="1711d-164">-Onay</span><span class="sxs-lookup"><span data-stu-id="1711d-164">-Confirm</span></span>
<span data-ttu-id="1711d-165">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1711d-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1711d-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1711d-166">-WhatIf</span></span>
<span data-ttu-id="1711d-167">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1711d-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1711d-168">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1711d-168">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1711d-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1711d-169">CommonParameters</span></span>
<span data-ttu-id="1711d-170">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1711d-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1711d-171">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1711d-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1711d-172">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1711d-172">INPUTS</span></span>

### <span data-ttu-id="1711d-173">Microsoft. Azure. Management. DNS. modeller. RecordType</span><span class="sxs-lookup"><span data-stu-id="1711d-173">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="1711d-174">System. String</span><span class="sxs-lookup"><span data-stu-id="1711d-174">System.String</span></span>

### <span data-ttu-id="1711d-175">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="1711d-175">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="1711d-176">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1711d-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="1711d-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1711d-177">OUTPUTS</span></span>

### <span data-ttu-id="1711d-178">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1711d-178">System.Boolean</span></span>

## <span data-ttu-id="1711d-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1711d-179">NOTES</span></span>
<span data-ttu-id="1711d-180">*Confirm* parametresini kullanarak, bu cmdlet 'in onayınızı isteyip istemediğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="1711d-180">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="1711d-181">Varsayılan olarak, $ConfirmPreference Windows PowerShell değişkeninde orta veya düşük bir değer varsa cmdlet onay ister.</span><span class="sxs-lookup"><span data-stu-id="1711d-181">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="1711d-182">*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="1711d-182">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="1711d-183">*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="1711d-183">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="1711d-184">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1711d-184">RELATED LINKS</span></span>

[<span data-ttu-id="1711d-185">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1711d-185">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="1711d-186">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1711d-186">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="1711d-187">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1711d-187">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
