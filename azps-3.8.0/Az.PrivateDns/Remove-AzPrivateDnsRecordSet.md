---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 865ab4ab3cca9d921fc8c40e9c6ae5cd03eaf00a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096492"
---
# <span data-ttu-id="b2c3e-101">Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b2c3e-101">Remove-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="b2c3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2c3e-102">SYNOPSIS</span></span>
<span data-ttu-id="b2c3e-103">Özel bir DNS bölgesinden kayıt kümesi siler.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-103">Deletes a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="b2c3e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b2c3e-104">SYNTAX</span></span>

### <span data-ttu-id="b2c3e-105">Alanlar (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b2c3e-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2c3e-106">Karıştır</span><span class="sxs-lookup"><span data-stu-id="b2c3e-106">Mixed</span></span>
```
Remove-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2c3e-107">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="b2c3e-107">Object</span></span>
```
Remove-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2c3e-108">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="b2c3e-108">ResourceId</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2c3e-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b2c3e-109">DESCRIPTION</span></span>
<span data-ttu-id="b2c3e-110">Remove-AzPrivateDnsRecordSet cmdlet 'i belirtilen bölgeden belirtilen kayıt kümesini siler.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-110">The Remove-AzPrivateDnsRecordSet cmdlet deletes the specified record set from the specified zone.</span></span> <span data-ttu-id="b2c3e-111">Özel bölge Apex otomatik olarak oluşturulan SOA kayıtlarını silemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-111">You cannot delete SOA records that are automatically created at the private zone apex.</span></span> <span data-ttu-id="b2c3e-112">Bir RecordSet nesnesini, Pipeline işlecini veya bir parametre olarak veya bir RESOURCEID olarak kullanarak bu cmdlet 'e geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-112">You can pass a RecordSet object to this cmdlet by using the pipeline operator or as a parameter or as a ResourceId.</span></span> <span data-ttu-id="b2c3e-113">Ad ve kayıt kümesi nesnesini kullanmadan bir kaydı belirlemek için, bu cmdlet 'i, ardışık düzen işlecini veya parametre olarak kullanarak bu cmdlet 'e bir PSPrivateDnsZone nesnesi olarak geçirmelisiniz veya bir alternatif olarak, Bölgebirleştir ve ResourceGroupName parametrelerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-113">To identify a record set by name and type without using a RecordSet object, you must pass the zone as a PSPrivateDnsZone object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the ZoneName and ResourceGroupName parameters.</span></span> <span data-ttu-id="b2c3e-114">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için Confirm parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-114">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="b2c3e-115">Kayıt kümesini kayıt kümesi nesnesi kullanarak belirtirken, yerel kayıt kümesi nesnesi alındıktan sonra Azure özel DNS 'de değiştirilmişse kayıt kümesi silinmez.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-115">When specifying the record set using a RecordSet object, the record set is not deleted if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="b2c3e-116">Bu, eşzamanlı değişiklikler için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-116">This provides protection for concurrent changes.</span></span> <span data-ttu-id="b2c3e-117">Bunu, yinelenen değişikliklerden bağımsız olarak kayıt kümesini silen overwrite parametresini kullanarak kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-117">You can suppress this by using the Overwrite parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="b2c3e-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b2c3e-118">EXAMPLES</span></span>

### <span data-ttu-id="b2c3e-119">Örnek 1: kayıt kümesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="b2c3e-119">Example 1: Remove a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="b2c3e-120">İlk komut belirtilen kayıt kümesini alır ve $RecordSet değişkeninde depolar. İkinci komut $RecordSet 'da kayıt kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-120">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="b2c3e-121">Örnek 2: kayıt kümesini kaldırma ve tüm onayı gösterme</span><span class="sxs-lookup"><span data-stu-id="b2c3e-121">Example 2: Remove a record set and suppress all confirmation</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="b2c3e-122">İlk komut belirtilen kayıt kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-122">The first command gets the specified record set.</span></span> <span data-ttu-id="b2c3e-123">İkinci komut, bu arada değişmiş olsa bile kayıt kümesini siler.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-123">The second command deletes the record set, even if it has changed in the meantime.</span></span> <span data-ttu-id="b2c3e-124">Onay istemlerinin bastırılması</span><span class="sxs-lookup"><span data-stu-id="b2c3e-124">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="b2c3e-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b2c3e-125">PARAMETERS</span></span>

### <span data-ttu-id="b2c3e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2c3e-126">-DefaultProfile</span></span>
<span data-ttu-id="b2c3e-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2c3e-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="b2c3e-128">-Name</span></span>
<span data-ttu-id="b2c3e-129">Kayıt kümesindeki kayıtların adı (bölgenin adına ve sonlandırma noktası olmadan).</span><span class="sxs-lookup"><span data-stu-id="b2c3e-129">The name of the records in the record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="b2c3e-130">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="b2c3e-130">-Overwrite</span></span>
<span data-ttu-id="b2c3e-131">İyimser eşzamanlılık denetimleri için kayıt kümesi parametresinin ETag alanını kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-131">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="b2c3e-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b2c3e-132">-PassThru</span></span>
<span data-ttu-id="b2c3e-133">İşlemin sonucunu geçirmek için kullanılır özel bölgesini daha aşağı doğru silme.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-133">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="b2c3e-134">-Kayıt kümesi</span><span class="sxs-lookup"><span data-stu-id="b2c3e-134">-RecordSet</span></span>
<span data-ttu-id="b2c3e-135">Kaydın ekleneceği kayıt kümesi.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-135">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c3e-136">-RecordType</span><span class="sxs-lookup"><span data-stu-id="b2c3e-136">-RecordType</span></span>
<span data-ttu-id="b2c3e-137">Kayıt kümesindeki özel DNS kayıtlarının türü.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-137">The type of Private DNS records in the record set.</span></span>

```yaml
Type: Microsoft.Azure.Management.PrivateDns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2c3e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2c3e-138">-ResourceGroupName</span></span>
<span data-ttu-id="b2c3e-139">Bölgenin ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-139">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="b2c3e-140">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b2c3e-140">-ResourceId</span></span>
<span data-ttu-id="b2c3e-141">Özel DNS kayıt kümesi RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-141">Private DNS RecordSet ResourceID.</span></span>

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

### <span data-ttu-id="b2c3e-142">-Bölge</span><span class="sxs-lookup"><span data-stu-id="b2c3e-142">-Zone</span></span>
<span data-ttu-id="b2c3e-143">Kayıt kümesinin oluşturulacağı bölgeyi temsil eden PrivateDnsZone nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-143">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c3e-144">-BölgeAdı</span><span class="sxs-lookup"><span data-stu-id="b2c3e-144">-ZoneName</span></span>
<span data-ttu-id="b2c3e-145">Kayıt kümesinin varolduğu bölge (Sonlandırıcı nokta olmadan).</span><span class="sxs-lookup"><span data-stu-id="b2c3e-145">The zone in which the record set exists (without a terminating dot).</span></span>

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

### <span data-ttu-id="b2c3e-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="b2c3e-146">-Confirm</span></span>
<span data-ttu-id="b2c3e-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2c3e-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2c3e-148">-WhatIf</span></span>
<span data-ttu-id="b2c3e-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2c3e-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2c3e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2c3e-151">CommonParameters</span></span>
<span data-ttu-id="b2c3e-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b2c3e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2c3e-153">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2c3e-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2c3e-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b2c3e-154">INPUTS</span></span>

### <span data-ttu-id="b2c3e-155">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="b2c3e-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="b2c3e-156">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b2c3e-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

### <span data-ttu-id="b2c3e-157">System. String</span><span class="sxs-lookup"><span data-stu-id="b2c3e-157">System.String</span></span>

## <span data-ttu-id="b2c3e-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b2c3e-158">OUTPUTS</span></span>

### <span data-ttu-id="b2c3e-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b2c3e-159">System.Boolean</span></span>

## <span data-ttu-id="b2c3e-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b2c3e-160">NOTES</span></span>

## <span data-ttu-id="b2c3e-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b2c3e-161">RELATED LINKS</span></span>
