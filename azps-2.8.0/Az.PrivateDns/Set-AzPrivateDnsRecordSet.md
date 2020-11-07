---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsRecordSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 7c4f76b9731e82bd134be7ae38461a7d74e31e6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933078"
---
# <span data-ttu-id="cd501-101">Set-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="cd501-101">Set-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="cd501-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd501-102">SYNOPSIS</span></span>
<span data-ttu-id="cd501-103">Özel bir DNS bölgesinde bir kayıt kümesini güncelleştirir/ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cd501-103">Updates/Sets a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="cd501-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd501-104">SYNTAX</span></span>

```
Set-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd501-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd501-105">DESCRIPTION</span></span>
<span data-ttu-id="cd501-106">Set-AzPrivateDnsRecordSet cmdlet 'i, yerel bir RecordSet nesnesinden Azure özel DNS hizmetinde ayarlanan bir kaydı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="cd501-106">The Set-AzPrivateDnsRecordSet cmdlet updates a record set in the Azure Private DNS service from a local RecordSet object.</span></span> <span data-ttu-id="cd501-107">Bir RecordSet nesnesini parametre olarak veya Pipeline işlecini kullanarak geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cd501-107">You can pass a RecordSet object as a parameter or by using the pipeline operator.</span></span> <span data-ttu-id="cd501-108">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için Confirm parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cd501-108">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="cd501-109">Yerel kayıt kümesi nesnesi alındıktan sonra Azure özel DNS 'de değiştirilmişse kayıt kümesi güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="cd501-109">The record set is not updated if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="cd501-110">Bu, eşzamanlı değişiklikler için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="cd501-110">This provides protection for concurrent changes.</span></span> <span data-ttu-id="cd501-111">Bu davranışı, yinelenen değişikliklerden bağımsız olarak kayıt kümesini güncelleştiren, overwrite parametresini kullanarak kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cd501-111">You can suppress this behavior using the Overwrite parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="cd501-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd501-112">EXAMPLES</span></span>

### <span data-ttu-id="cd501-113">Örnek 1: kayıt kümesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="cd501-113">Example 1: Update a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 172.16.0.0, 172.31.255.255}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="cd501-114">İlk komut, Get-AzPrivateDnsRecordSet cmdlet 'ini kullanarak belirtilen kayıt kümesini alır ve $RecordSet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cd501-114">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="cd501-115">İkinci ve üçüncü komutlar, kayıt kümesine iki kayıt eklemek için satır dışı operasyonlardır.</span><span class="sxs-lookup"><span data-stu-id="cd501-115">The second and third commands are off-line operations to add two A records to the record set.</span></span> <span data-ttu-id="cd501-116">Son komutu, güncelleştirmeyi yürütmek için Set-AzPrivateDnsRecordSet cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="cd501-116">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to commit the update.</span></span>

### <span data-ttu-id="cd501-117">Örnek 2: SOA kaydını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="cd501-117">Example 2: Update an SOA record</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SOA/@
Name              : @
ZoneName          : myzone.com
ResourceGroupName : Myresourcegroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SOA
Records           : {[internal.cloudapp.net,admin.myzone.com,3600,300,2419200,300]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="cd501-118">İlk komut, Get-AzPrivateDnsRecordSet cmdlet 'ini kullanarak belirtilen kayıt kümesini alır ve $RecordSet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cd501-118">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="cd501-119">İkinci komut $RecordSet 'da belirtilen SOA kaydını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="cd501-119">The second command updates the specified SOA record in $RecordSet.</span></span> <span data-ttu-id="cd501-120">Son komutu $RecordSet güncelleştirmeyi yaymak için Set-AzPrivateDnsRecordSet cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="cd501-120">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="cd501-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd501-121">PARAMETERS</span></span>

### <span data-ttu-id="cd501-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd501-122">-DefaultProfile</span></span>
<span data-ttu-id="cd501-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cd501-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd501-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="cd501-124">-Overwrite</span></span>
<span data-ttu-id="cd501-125">İyimser eşzamanlılık denetimleri için kayıt kümesi parametresinin ETag alanını kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="cd501-125">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="cd501-126">-Kayıt kümesi</span><span class="sxs-lookup"><span data-stu-id="cd501-126">-RecordSet</span></span>
<span data-ttu-id="cd501-127">Kaydın ekleneceği kayıt kümesi.</span><span class="sxs-lookup"><span data-stu-id="cd501-127">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="cd501-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="cd501-128">-Confirm</span></span>
<span data-ttu-id="cd501-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cd501-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd501-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd501-130">-WhatIf</span></span>
<span data-ttu-id="cd501-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cd501-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd501-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cd501-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd501-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd501-133">CommonParameters</span></span>
<span data-ttu-id="cd501-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd501-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd501-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd501-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd501-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd501-136">INPUTS</span></span>

### <span data-ttu-id="cd501-137">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="cd501-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="cd501-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd501-138">OUTPUTS</span></span>

### <span data-ttu-id="cd501-139">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="cd501-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="cd501-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd501-140">NOTES</span></span>

## <span data-ttu-id="cd501-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd501-141">RELATED LINKS</span></span>
