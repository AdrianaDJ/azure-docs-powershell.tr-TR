---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 0b54ebe9650ba8dcd382afd308b21e7c48d1062d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933083"
---
# <span data-ttu-id="4f52d-101">Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4f52d-101">Remove-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="4f52d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f52d-102">SYNOPSIS</span></span>
<span data-ttu-id="4f52d-103">Özel bir DNS bölgesinden kayıt kümesi siler.</span><span class="sxs-lookup"><span data-stu-id="4f52d-103">Deletes a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="4f52d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f52d-104">SYNTAX</span></span>

### <span data-ttu-id="4f52d-105">Alanlar (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4f52d-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f52d-106">Karıştır</span><span class="sxs-lookup"><span data-stu-id="4f52d-106">Mixed</span></span>
```
Remove-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f52d-107">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="4f52d-107">Object</span></span>
```
Remove-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f52d-108">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="4f52d-108">ResourceId</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f52d-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f52d-109">DESCRIPTION</span></span>
<span data-ttu-id="4f52d-110">Remove-AzPrivateDnsRecordSet cmdlet 'i belirtilen bölgeden belirtilen kayıt kümesini siler.</span><span class="sxs-lookup"><span data-stu-id="4f52d-110">The Remove-AzPrivateDnsRecordSet cmdlet deletes the specified record set from the specified zone.</span></span> <span data-ttu-id="4f52d-111">Özel bölge Apex otomatik olarak oluşturulan SOA kayıtlarını silemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f52d-111">You cannot delete SOA records that are automatically created at the private zone apex.</span></span> <span data-ttu-id="4f52d-112">Bir RecordSet nesnesini, Pipeline işlecini veya bir parametre olarak veya bir RESOURCEID olarak kullanarak bu cmdlet 'e geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f52d-112">You can pass a RecordSet object to this cmdlet by using the pipeline operator or as a parameter or as a ResourceId.</span></span> <span data-ttu-id="4f52d-113">Ad ve kayıt kümesi nesnesini kullanmadan bir kaydı belirlemek için, bu cmdlet 'i, ardışık düzen işlecini veya parametre olarak kullanarak bu cmdlet 'e bir PSPrivateDnsZone nesnesi olarak geçirmelisiniz veya bir alternatif olarak, Bölgebirleştir ve ResourceGroupName parametrelerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f52d-113">To identify a record set by name and type without using a RecordSet object, you must pass the zone as a PSPrivateDnsZone object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the ZoneName and ResourceGroupName parameters.</span></span> <span data-ttu-id="4f52d-114">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için Confirm parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f52d-114">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="4f52d-115">Kayıt kümesini kayıt kümesi nesnesi kullanarak belirtirken, yerel kayıt kümesi nesnesi alındıktan sonra Azure özel DNS 'de değiştirilmişse kayıt kümesi silinmez.</span><span class="sxs-lookup"><span data-stu-id="4f52d-115">When specifying the record set using a RecordSet object, the record set is not deleted if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="4f52d-116">Bu, eşzamanlı değişiklikler için koruma sağlar.</span><span class="sxs-lookup"><span data-stu-id="4f52d-116">This provides protection for concurrent changes.</span></span> <span data-ttu-id="4f52d-117">Bunu, yinelenen değişikliklerden bağımsız olarak kayıt kümesini silen overwrite parametresini kullanarak kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f52d-117">You can suppress this by using the Overwrite parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="4f52d-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f52d-118">EXAMPLES</span></span>

### <span data-ttu-id="4f52d-119">Örnek 1: kayıt kümesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="4f52d-119">Example 1: Remove a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="4f52d-120">İlk komut belirtilen kayıt kümesini alır ve $RecordSet değişkeninde depolar. İkinci komut $RecordSet 'da kayıt kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4f52d-120">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="4f52d-121">Örnek 2: kayıt kümesini kaldırma ve tüm onayı gösterme</span><span class="sxs-lookup"><span data-stu-id="4f52d-121">Example 2: Remove a record set and suppress all confirmation</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="4f52d-122">İlk komut belirtilen kayıt kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="4f52d-122">The first command gets the specified record set.</span></span> <span data-ttu-id="4f52d-123">İkinci komut, bu arada değişmiş olsa bile kayıt kümesini siler.</span><span class="sxs-lookup"><span data-stu-id="4f52d-123">The second command deletes the record set, even if it has changed in the meantime.</span></span> <span data-ttu-id="4f52d-124">Onay istemlerinin bastırılması</span><span class="sxs-lookup"><span data-stu-id="4f52d-124">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="4f52d-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f52d-125">PARAMETERS</span></span>

### <span data-ttu-id="4f52d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f52d-126">-DefaultProfile</span></span>
<span data-ttu-id="4f52d-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4f52d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f52d-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="4f52d-128">-Name</span></span>
<span data-ttu-id="4f52d-129">Kayıt kümesindeki kayıtların adı (bölgenin adına ve sonlandırma noktası olmadan).</span><span class="sxs-lookup"><span data-stu-id="4f52d-129">The name of the records in the record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="4f52d-130">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="4f52d-130">-Overwrite</span></span>
<span data-ttu-id="4f52d-131">İyimser eşzamanlılık denetimleri için kayıt kümesi parametresinin ETag alanını kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="4f52d-131">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="4f52d-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4f52d-132">-PassThru</span></span>
<span data-ttu-id="4f52d-133">İşlemin sonucunu geçirmek için kullanılır özel bölgesini daha aşağı doğru silme.</span><span class="sxs-lookup"><span data-stu-id="4f52d-133">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="4f52d-134">-Kayıt kümesi</span><span class="sxs-lookup"><span data-stu-id="4f52d-134">-RecordSet</span></span>
<span data-ttu-id="4f52d-135">Kaydın ekleneceği kayıt kümesi.</span><span class="sxs-lookup"><span data-stu-id="4f52d-135">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="4f52d-136">-RecordType</span><span class="sxs-lookup"><span data-stu-id="4f52d-136">-RecordType</span></span>
<span data-ttu-id="4f52d-137">Kayıt kümesindeki özel DNS kayıtlarının türü.</span><span class="sxs-lookup"><span data-stu-id="4f52d-137">The type of Private DNS records in the record set.</span></span>

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

### <span data-ttu-id="4f52d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f52d-138">-ResourceGroupName</span></span>
<span data-ttu-id="4f52d-139">Bölgenin ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="4f52d-139">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="4f52d-140">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4f52d-140">-ResourceId</span></span>
<span data-ttu-id="4f52d-141">Özel DNS kayıt kümesi RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="4f52d-141">Private DNS RecordSet ResourceID.</span></span>

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

### <span data-ttu-id="4f52d-142">-Bölge</span><span class="sxs-lookup"><span data-stu-id="4f52d-142">-Zone</span></span>
<span data-ttu-id="4f52d-143">Kayıt kümesinin oluşturulacağı bölgeyi temsil eden PrivateDnsZone nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4f52d-143">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

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

### <span data-ttu-id="4f52d-144">-BölgeAdı</span><span class="sxs-lookup"><span data-stu-id="4f52d-144">-ZoneName</span></span>
<span data-ttu-id="4f52d-145">Kayıt kümesinin varolduğu bölge (Sonlandırıcı nokta olmadan).</span><span class="sxs-lookup"><span data-stu-id="4f52d-145">The zone in which the record set exists (without a terminating dot).</span></span>

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

### <span data-ttu-id="4f52d-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="4f52d-146">-Confirm</span></span>
<span data-ttu-id="4f52d-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4f52d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f52d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f52d-148">-WhatIf</span></span>
<span data-ttu-id="4f52d-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f52d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f52d-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4f52d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f52d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f52d-151">CommonParameters</span></span>
<span data-ttu-id="4f52d-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f52d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f52d-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f52d-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f52d-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f52d-154">INPUTS</span></span>

### <span data-ttu-id="4f52d-155">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="4f52d-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="4f52d-156">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4f52d-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

### <span data-ttu-id="4f52d-157">System. String</span><span class="sxs-lookup"><span data-stu-id="4f52d-157">System.String</span></span>

## <span data-ttu-id="4f52d-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f52d-158">OUTPUTS</span></span>

### <span data-ttu-id="4f52d-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4f52d-159">System.Boolean</span></span>

## <span data-ttu-id="4f52d-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f52d-160">NOTES</span></span>

## <span data-ttu-id="4f52d-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f52d-161">RELATED LINKS</span></span>
