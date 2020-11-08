---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: 06b8a8bd7027b95d7f51e186b0184707ffd296a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096480"
---
# <span data-ttu-id="73611-101">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="73611-101">Set-AzPrivateDnsZone</span></span>

## <span data-ttu-id="73611-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73611-102">SYNOPSIS</span></span>
<span data-ttu-id="73611-103">Kaynak grubundan özel bir DNS bölgesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="73611-103">Updates a Private DNS zone from a resource group.</span></span>

## <span data-ttu-id="73611-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="73611-104">SYNTAX</span></span>

### <span data-ttu-id="73611-105">Alanlar (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="73611-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73611-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="73611-106">ResourceId</span></span>
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73611-107">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="73611-107">Object</span></span>
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73611-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="73611-108">DESCRIPTION</span></span>
<span data-ttu-id="73611-109">**Set-AzPrivateDnsZone** cmdlet 'i, belirli bir kaynak grubundan özel bir etki alanı adı SISTEMI (DNS) bölgesini kalıcı olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="73611-109">The **Set-AzPrivateDnsZone** cmdlet permanently updates a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="73611-110">*Privatezone* parametresini veya Pipeline işlecini kullanarak bir **PrivateDnsZone** nesnesi geçirebilir ya da *Name* ve *resourcegroupname* parametrelerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="73611-110">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="73611-111">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için Confirm parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="73611-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="73611-112">Bir **PrivateDnsZone** nesnesi (ardışık düzen veya *bölge* parametresi aracılığıyla geçirilir) kullanarak bölgeyi belirtirken, yerel **PrivateDnsZone** nesnesinin alındığı bu yana Azure DNS 'de DEĞIŞIKLIK yapıldığında bölge güncelleştirilmez (yalnızca DNS bölge kaynak sayısı değiştiğinde, bölgedeki kayıt kümeleri üzerinde bulunan işlemler).</span><span class="sxs-lookup"><span data-stu-id="73611-112">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="73611-113">Bu, eşzamanlı bölge değişiklikleri için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="73611-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="73611-114">Bu, yinelenen değişikliklerden bağımsız olarak bölgeyi güncelleştiren, *overwrite* parametresi kullanılarak bastırılabilir.</span><span class="sxs-lookup"><span data-stu-id="73611-114">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="73611-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="73611-115">EXAMPLES</span></span>

### <span data-ttu-id="73611-116">Örnek 1: özel bölgeyi güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="73611-116">Example 1: Updates a private zone</span></span>
```
PS C:\>Set-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup" -Tag @{tag1="value1";tag2="value2"}


This command updates the zone named myzone.com from the resource group named MyResourceGroup with the tags provided. Use Get-AzPrivateDnsZone to retrieve the updated zone. Updated zone would look something like this:

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {tag1="value1";tag2="value2"}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## <span data-ttu-id="73611-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="73611-117">PARAMETERS</span></span>

### <span data-ttu-id="73611-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73611-118">-DefaultProfile</span></span>
<span data-ttu-id="73611-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="73611-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73611-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="73611-120">-Name</span></span>
<span data-ttu-id="73611-121">Bu cmdlet 'in güncelleştirdiği özel DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="73611-121">Specifies the name of the Private DNS zone that this cmdlet updates.</span></span>
<span data-ttu-id="73611-122">*Resourcegroupname* parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="73611-122">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="73611-123">Alternatif olarak, *bölge* parametresini kullanarak özel DNS bölgesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="73611-123">Alternatively, you can specify the private DNS zone using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73611-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="73611-124">-Overwrite</span></span>
<span data-ttu-id="73611-125">Bir **PrivateDnsZone** nesnesi (ardışık düzen veya *bölge* parametresi aracılığıyla geçirilir) kullanarak bölgeyi belirtirken, yerel **dnsZone** nesnesinin alındığı bu yana Azure DNS 'de DEĞIŞTIRILDIYSE bölge güncelleştirilmez (yalnızca DNS bölge kaynak sayısı değiştiğinde, bölgedeki kayıt kümelerindeki işlemler).</span><span class="sxs-lookup"><span data-stu-id="73611-125">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="73611-126">Bu, eşzamanlı bölge değişiklikleri için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="73611-126">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="73611-127">Bu, yinelenen değişikliklerden bağımsız olarak bölgeyi güncelleştiren, *overwrite* parametresi kullanılarak bastırılabilir.</span><span class="sxs-lookup"><span data-stu-id="73611-127">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="73611-128">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="73611-128">-PrivateZone</span></span>
<span data-ttu-id="73611-129">Ayarlanacak bölge nesnesi.</span><span class="sxs-lookup"><span data-stu-id="73611-129">The zone object to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73611-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73611-130">-ResourceGroupName</span></span>
<span data-ttu-id="73611-131">Güncelleştirilecek bölgeyi içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="73611-131">Specifies the name of the resource group that contains the zone to be updated.</span></span>
<span data-ttu-id="73611-132">Ayrıca, *BölgeAdı* parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="73611-132">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="73611-133">Alternatif olarak, özel DNS bölgesini, potansiyel satış veya *bölge* parametresinden geçen bir **dnsZone** nesnesi kullanarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="73611-133">Alternatively, you can specify the private DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73611-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="73611-134">-ResourceId</span></span>
<span data-ttu-id="73611-135">Özel DNS bölge RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="73611-135">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73611-136">Etiketli</span><span class="sxs-lookup"><span data-stu-id="73611-136">-Tag</span></span>
<span data-ttu-id="73611-137">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="73611-137">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73611-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="73611-138">-Confirm</span></span>
<span data-ttu-id="73611-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="73611-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73611-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73611-140">-WhatIf</span></span>
<span data-ttu-id="73611-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="73611-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73611-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="73611-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73611-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73611-143">CommonParameters</span></span>
<span data-ttu-id="73611-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="73611-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73611-145">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73611-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73611-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="73611-146">INPUTS</span></span>

### <span data-ttu-id="73611-147">System. String</span><span class="sxs-lookup"><span data-stu-id="73611-147">System.String</span></span>

### <span data-ttu-id="73611-148">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="73611-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="73611-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="73611-149">OUTPUTS</span></span>

### <span data-ttu-id="73611-150">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="73611-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="73611-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="73611-151">NOTES</span></span>

## <span data-ttu-id="73611-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="73611-152">RELATED LINKS</span></span>

[<span data-ttu-id="73611-153">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="73611-153">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="73611-154">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="73611-154">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="73611-155">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="73611-155">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
