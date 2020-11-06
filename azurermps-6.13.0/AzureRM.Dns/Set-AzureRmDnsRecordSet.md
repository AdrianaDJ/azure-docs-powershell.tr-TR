---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/set-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsRecordSet.md
ms.openlocfilehash: d0a7451db664d80240250984fcc1c0f8e1aaefe9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591963"
---
# <span data-ttu-id="fbd6a-101">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="fbd6a-101">Set-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="fbd6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbd6a-102">SYNOPSIS</span></span>
<span data-ttu-id="fbd6a-103">DNS kayıt kümesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-103">Updates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbd6a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fbd6a-104">SYNTAX</span></span>

```
Set-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbd6a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fbd6a-105">DESCRIPTION</span></span>
<span data-ttu-id="fbd6a-106">**Set-AzureRmDnsRecordSet** cmdlet 'i, yerel bir **RECORDSET** nesnesinden Azure DNS hizmetinde bir kayıt güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-106">The **Set-AzureRmDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>
<span data-ttu-id="fbd6a-107">Bir **Recordset** nesnesini parametre olarak veya Pipeline işlecini kullanarak geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>
<span data-ttu-id="fbd6a-108">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için *Confirm* parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="fbd6a-109">Yerel **kayıt** kümesi nesnesi alındıktan sonra Azure DNS 'de değiştirilmişse kayıt kümesi güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="fbd6a-110">Bu, eşzamanlı değişiklikler için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="fbd6a-111">Bu davranışı, yinelenen değişikliklerden bağımsız olarak kayıt kümesini güncelleştiren, *overwrite* parametresini kullanarak kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="fbd6a-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fbd6a-112">EXAMPLES</span></span>

### <span data-ttu-id="fbd6a-113">Örnek 1: kayıt kümesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="fbd6a-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzureRmDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzureRmDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="fbd6a-114">İlk komut, Get-AzureRmDnsRecordSet cmdlet 'ini kullanarak belirtilen kayıt kümesini alır ve $RecordSet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-114">The first command uses the Get-AzureRmDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="fbd6a-115">İkinci ve üçüncü komutlar, kayıt kümesine iki kayıt eklemek için satır dışı operasyonlardır.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>
<span data-ttu-id="fbd6a-116">Son komutu, güncelleştirmeyi kaydetmek için **set-AzureRmDnsRecordSet** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-116">The final command uses the **Set-AzureRmDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="fbd6a-117">Örnek 2: SOA kaydını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="fbd6a-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="fbd6a-118">İlk komut **Get-AzureRmDnsRecordset** cmdlet 'ini kullanarak belirtilen kayıt kümesini alır ve $Recordset değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-118">The first command uses the **Get-AzureRmDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="fbd6a-119">İkinci komut $RecordSet 'da belirtilen SOA kaydını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-119">The second command updates the specified SOA record in $RecordSet.</span></span>
<span data-ttu-id="fbd6a-120">Son komutu, $RecordSet güncelleştirmeyi yaymak için **set-AzureRmDnsRecordSet** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-120">The final command uses the **Set-AzureRmDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="fbd6a-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fbd6a-121">PARAMETERS</span></span>

### <span data-ttu-id="fbd6a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbd6a-122">-DefaultProfile</span></span>
<span data-ttu-id="fbd6a-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fbd6a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbd6a-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="fbd6a-124">-Overwrite</span></span>
<span data-ttu-id="fbd6a-125">Yinelenen değişikliklere bakılmaksızın kayıt kümesinin güncelleştirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-125">Indicates to update the record set regardless of concurrent changes.</span></span>
<span data-ttu-id="fbd6a-126">Yerel **kayıt** kümesi nesnesi alındıktan sonra Azure DNS 'de değiştirilmişse kayıt kümesi güncelleştirilmeyecek.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-126">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="fbd6a-127">Bu, eşzamanlı değişiklikler için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-127">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="fbd6a-128">Bu davranışı bastırmak için, *üzerine yazma* parametresini kullanarak, yinelenen değişikliklere bakılmaksızın kayıt kümesi güncellenir.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-128">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="fbd6a-129">-Kayıt kümesi</span><span class="sxs-lookup"><span data-stu-id="fbd6a-129">-RecordSet</span></span>
<span data-ttu-id="fbd6a-130">Güncelleştirilecek **kayıt kümesini** belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-130">Specifies the **RecordSet** to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbd6a-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="fbd6a-131">-Confirm</span></span>
<span data-ttu-id="fbd6a-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbd6a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbd6a-133">-WhatIf</span></span>
<span data-ttu-id="fbd6a-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fbd6a-135">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fbd6a-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbd6a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbd6a-137">CommonParameters</span></span>
<span data-ttu-id="fbd6a-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbd6a-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbd6a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbd6a-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fbd6a-140">INPUTS</span></span>

### <span data-ttu-id="fbd6a-141">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="fbd6a-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="fbd6a-142">Parametreler: RecordSet (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fbd6a-142">Parameters: RecordSet (ByValue)</span></span>

## <span data-ttu-id="fbd6a-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fbd6a-143">OUTPUTS</span></span>

### <span data-ttu-id="fbd6a-144">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="fbd6a-144">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="fbd6a-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fbd6a-145">NOTES</span></span>
<span data-ttu-id="fbd6a-146">*Confirm* parametresini kullanarak, bu cmdlet 'in onayınızı isteyip istemediğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-146">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="fbd6a-147">Varsayılan olarak, $ConfirmPreference Windows PowerShell değişkeninde orta veya düşük bir değer varsa cmdlet onay ister.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-147">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="fbd6a-148">*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-148">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="fbd6a-149">*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-149">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="fbd6a-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fbd6a-150">RELATED LINKS</span></span>

[<span data-ttu-id="fbd6a-151">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="fbd6a-151">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="fbd6a-152">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="fbd6a-152">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="fbd6a-153">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="fbd6a-153">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)
