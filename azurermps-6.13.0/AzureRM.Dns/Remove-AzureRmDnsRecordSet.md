---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
ms.openlocfilehash: 129177c93d48b55cf8dfe5675d7ffc30ec7f46ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593670"
---
# <span data-ttu-id="f79b4-101">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f79b4-101">Remove-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="f79b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f79b4-102">SYNOPSIS</span></span>
<span data-ttu-id="f79b4-103">Kayıt kümesini siler.</span><span class="sxs-lookup"><span data-stu-id="f79b4-103">Deletes a record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f79b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f79b4-104">SYNTAX</span></span>

### <span data-ttu-id="f79b4-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="f79b4-105">Fields</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f79b4-106">Karıştır</span><span class="sxs-lookup"><span data-stu-id="f79b4-106">Mixed</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f79b4-107">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="f79b4-107">Object</span></span>
```
Remove-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f79b4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f79b4-108">DESCRIPTION</span></span>
<span data-ttu-id="f79b4-109">**Remove-AzureRmDnsRecordSet** cmdlet 'i belirtilen bölgeden belirtilen kayıt kümesini siler.</span><span class="sxs-lookup"><span data-stu-id="f79b4-109">The **Remove-AzureRmDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="f79b4-110">Bölge Apex otomatik olarak oluşturulan SOA veya ad sunucusu (NS) kayıtlarını silemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="f79b4-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>
<span data-ttu-id="f79b4-111">Bir **Recordset** nesnesini, ardışık düzen işlecini veya parametre olarak bu cmdlet 'e geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f79b4-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="f79b4-112">Ad ve kayıt **kümesi** **nesnesi kullanmadan** bir kayıt kümesi tanımlamak için, bu cmdlet 'e, ardışık düzen işlecini veya parametre olarak kullanarak bölgeyi Bu cmdlet 'e geçirmelisiniz ya da *BölgeAdı* ve *resourcegroupname* parametrelerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f79b4-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="f79b4-113">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için Confirm parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f79b4-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="f79b4-114">Kayıt **kümesini kayıt kümesi nesnesi kullanarak** belirtirken, yerel **kayıt** kümesi NESNESI alındıktan sonra Azure DNS 'de değiştirilmişse kayıt kümesi silinmez.</span><span class="sxs-lookup"><span data-stu-id="f79b4-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="f79b4-115">Bu, eşzamanlı değişiklikler için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="f79b4-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="f79b4-116">Bunu, yinelenen değişikliklerden bağımsız olarak kayıt kümesini silen *overwrite* parametresini kullanarak kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f79b4-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="f79b4-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f79b4-117">EXAMPLES</span></span>

### <span data-ttu-id="f79b4-118">Örnek 1: kayıt kümesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="f79b4-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="f79b4-119">İlk komut belirtilen kayıt kümesini alır ve $RecordSet değişkeninde depolar. İkinci komut $RecordSet 'da kayıt kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f79b4-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="f79b4-120">Örnek 2: kayıt kümesini kaldırma ve tüm onayı gösterme</span><span class="sxs-lookup"><span data-stu-id="f79b4-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="f79b4-121">İlk komut belirtilen kayıt kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="f79b4-121">The first command gets the specified record set.</span></span>
<span data-ttu-id="f79b4-122">İkinci komut, bu arada değişmiş olsa bile kayıt kümesini siler.</span><span class="sxs-lookup"><span data-stu-id="f79b4-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="f79b4-123">Onay istemlerinin bastırılması</span><span class="sxs-lookup"><span data-stu-id="f79b4-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="f79b4-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f79b4-124">PARAMETERS</span></span>

### <span data-ttu-id="f79b4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f79b4-125">-DefaultProfile</span></span>
<span data-ttu-id="f79b4-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f79b4-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f79b4-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="f79b4-127">-Name</span></span>
<span data-ttu-id="f79b4-128">Kaldırılacak **kayıt kümesinin** adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f79b4-128">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="f79b4-129">Ada göre kayıt kümesi belirtildiğinde, DNS bölgesi, *bölge* parametresi veya *BölgeAdı* ve *resourcegroupname* parametreleri kullanılarak belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="f79b4-129">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="f79b4-130">Alternatif olarak, kayıt kümesi, *Recordset* parametresi kullanılarak geçirilen bir **Recordset** nesnesi kullanılarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="f79b4-130">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

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

### <span data-ttu-id="f79b4-131">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="f79b4-131">-Overwrite</span></span>
<span data-ttu-id="f79b4-132">Kayıt **kümesini kayıt kümesi nesnesi kullanarak** belirtirken, yerel **kayıt** kümesi NESNESI alındıktan sonra Azure DNS 'de değiştirilmişse kayıt kümesi silinmez.</span><span class="sxs-lookup"><span data-stu-id="f79b4-132">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="f79b4-133">Bu, eşzamanlı değişiklikler için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="f79b4-133">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="f79b4-134">Bu, yinelenen değişikliklerden bağımsız olarak kayıt kümesini silen, *overwrite* parametresi kullanılarak bastırılabilir.</span><span class="sxs-lookup"><span data-stu-id="f79b4-134">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="f79b4-135">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f79b4-135">-PassThru</span></span>
<span data-ttu-id="f79b4-136">geçiş</span><span class="sxs-lookup"><span data-stu-id="f79b4-136">passthru</span></span>

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

### <span data-ttu-id="f79b4-137">-Kayıt kümesi</span><span class="sxs-lookup"><span data-stu-id="f79b4-137">-RecordSet</span></span>
<span data-ttu-id="f79b4-138">Kaldırılacak **kayıt kümesi** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f79b4-138">Specifies the **RecordSet** object to remove.</span></span>
<span data-ttu-id="f79b4-139">Alternatif olarak, kayıt kümesi *ad* ve *bölge* parametreleri kullanılarak veya *Name, BölgeAdı* ve *resourcegroupname* parametrelerini kullanarak *ZoneName* belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="f79b4-139">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="f79b4-140">-RecordType</span><span class="sxs-lookup"><span data-stu-id="f79b4-140">-RecordType</span></span>
<span data-ttu-id="f79b4-141">DNS kaydı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f79b4-141">Specifies the type of DNS record.</span></span>
<span data-ttu-id="f79b4-142">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="f79b4-142">Valid values are:</span></span>
- <span data-ttu-id="f79b4-143">Bir</span><span class="sxs-lookup"><span data-stu-id="f79b4-143">A</span></span>
- <span data-ttu-id="f79b4-144">AAAA</span><span class="sxs-lookup"><span data-stu-id="f79b4-144">AAAA</span></span>
- <span data-ttu-id="f79b4-145">KAYDıNı</span><span class="sxs-lookup"><span data-stu-id="f79b4-145">CNAME</span></span>
- <span data-ttu-id="f79b4-146">DOSYASıNA</span><span class="sxs-lookup"><span data-stu-id="f79b4-146">MX</span></span>
- <span data-ttu-id="f79b4-147">Seç</span><span class="sxs-lookup"><span data-stu-id="f79b4-147">NS</span></span>
- <span data-ttu-id="f79b4-148">PTR</span><span class="sxs-lookup"><span data-stu-id="f79b4-148">PTR</span></span>
- <span data-ttu-id="f79b4-149">SRV</span><span class="sxs-lookup"><span data-stu-id="f79b4-149">SRV</span></span>
- <span data-ttu-id="f79b4-150">Bölge silindiğinde TXT SOA kayıtları otomatik olarak silinir.</span><span class="sxs-lookup"><span data-stu-id="f79b4-150">TXT SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="f79b4-151">SOA kayıtlarını el ile silemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="f79b4-151">You cannot manually delete SOA records.</span></span>

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

### <span data-ttu-id="f79b4-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f79b4-152">-ResourceGroupName</span></span>
<span data-ttu-id="f79b4-153">Silinecek **kayıt kümesini** içeren DNS bölgesini içeren kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f79b4-153">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="f79b4-154">Bu parametre yalnızca, kayıt kümesi ve DNS bölgesi ad ve *BölgeAdı* kullanılarak belirtildiğinde uygulanabilir *Name* .</span><span class="sxs-lookup"><span data-stu-id="f79b4-154">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>
<span data-ttu-id="f79b4-155">Alternatif olarak, kayıt *kümesini kayıt kümesi parametresini veya* *ad* ve *bölge* parametrelerini kullanarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f79b4-155">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="f79b4-156">-Bölge</span><span class="sxs-lookup"><span data-stu-id="f79b4-156">-Zone</span></span>
<span data-ttu-id="f79b4-157">Silinecek **kayıt kümesini** içeren DNS bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f79b4-157">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="f79b4-158">Bu parametre yalnızca *Name* parametresi kullanılarak kayıt kümesi belirtildiğinde uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="f79b4-158">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>
<span data-ttu-id="f79b4-159">Alternatif olarak, kayıt *kümesini kayıt kümesi parametresini veya* *Name, BölgeAdı* ve *resourcegroupname* parametrelerini kullanarak *ZoneName* belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f79b4-159">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="f79b4-160">-BölgeAdı</span><span class="sxs-lookup"><span data-stu-id="f79b4-160">-ZoneName</span></span>
<span data-ttu-id="f79b4-161">Silinecek **kayıt kümesini** içeren bölgenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f79b4-161">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="f79b4-162">*Name* ve *resourcegroupname* parametrelerini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f79b4-162">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="f79b4-163">Alternatif olarak, kayıt kümesi, kayıt *kümesi* parametresi veya *ad* ve *bölge* parametreleriyle belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="f79b4-163">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="f79b4-164">-Onay</span><span class="sxs-lookup"><span data-stu-id="f79b4-164">-Confirm</span></span>
<span data-ttu-id="f79b4-165">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f79b4-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f79b4-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f79b4-166">-WhatIf</span></span>
<span data-ttu-id="f79b4-167">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f79b4-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f79b4-168">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f79b4-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f79b4-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f79b4-169">CommonParameters</span></span>
<span data-ttu-id="f79b4-170">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f79b4-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f79b4-171">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f79b4-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f79b4-172">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f79b4-172">INPUTS</span></span>

### <span data-ttu-id="f79b4-173">Microsoft. Azure. Management. DNS. modeller. RecordType</span><span class="sxs-lookup"><span data-stu-id="f79b4-173">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="f79b4-174">System. String</span><span class="sxs-lookup"><span data-stu-id="f79b4-174">System.String</span></span>

### <span data-ttu-id="f79b4-175">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="f79b4-175">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="f79b4-176">Parametreler: bölge (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f79b4-176">Parameters: Zone (ByValue)</span></span>

### <span data-ttu-id="f79b4-177">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f79b4-177">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="f79b4-178">Parametreler: RecordSet (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f79b4-178">Parameters: RecordSet (ByValue)</span></span>

## <span data-ttu-id="f79b4-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f79b4-179">OUTPUTS</span></span>

### <span data-ttu-id="f79b4-180">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f79b4-180">System.Boolean</span></span>

## <span data-ttu-id="f79b4-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f79b4-181">NOTES</span></span>
<span data-ttu-id="f79b4-182">*Confirm* parametresini kullanarak, bu cmdlet 'in onayınızı isteyip istemediğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="f79b4-182">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="f79b4-183">Varsayılan olarak, $ConfirmPreference Windows PowerShell değişkeninde orta veya düşük bir değer varsa cmdlet onay ister.</span><span class="sxs-lookup"><span data-stu-id="f79b4-183">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="f79b4-184">*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="f79b4-184">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="f79b4-185">*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="f79b4-185">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f79b4-186">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f79b4-186">RELATED LINKS</span></span>

[<span data-ttu-id="f79b4-187">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f79b4-187">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="f79b4-188">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f79b4-188">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="f79b4-189">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f79b4-189">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)