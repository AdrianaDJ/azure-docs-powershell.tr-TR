---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/resume-azsupdaterun
schema: 2.0.0
ms.openlocfilehash: 65d2b3a045d38435cdd709d47c0be88f7fc98af0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935196"
---
# <span data-ttu-id="0cc23-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="0cc23-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="0cc23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cc23-102">SYNOPSIS</span></span>
<span data-ttu-id="0cc23-103">Başarısız güncelleştirmeyi sürdürün.</span><span class="sxs-lookup"><span data-stu-id="0cc23-103">Resume a failed update.</span></span>

## <span data-ttu-id="0cc23-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0cc23-104">SYNTAX</span></span>

### <span data-ttu-id="0cc23-105">Yeniden çalıştır (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0cc23-105">Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0cc23-106">Yeniden yönlendirme kimliği</span><span class="sxs-lookup"><span data-stu-id="0cc23-106">RerunViaIdentity</span></span>
```
Resume-AzsUpdateRun -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0cc23-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0cc23-107">DESCRIPTION</span></span>
<span data-ttu-id="0cc23-108">Başarısız güncelleştirmeyi sürdürün.</span><span class="sxs-lookup"><span data-stu-id="0cc23-108">Resume a failed update.</span></span>

## <span data-ttu-id="0cc23-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0cc23-109">EXAMPLES</span></span>

### <span data-ttu-id="0cc23-110">Örnek 1: ada ve Güncelleştirile Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="0cc23-110">Example 1: Resume-AzsUpdateRun By Name and UpdateName</span></span>
```powershell
PS C:\> Resume-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10 -Name 45aaeb26-805b-495b-9c8c-d5da5542dbf4

```

<span data-ttu-id="0cc23-111">Command, belirli bir başarısız güncelleştirme çalıştırmasını yeniden çalıştırmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="0cc23-111">Commandlet allows you to rerun a specific failed update run.</span></span>
<span data-ttu-id="0cc23-112">Güncelleştirme sürümünün geçerli sürümden kesinlikle daha büyük olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="0cc23-112">Note that there is a requirement that the update version is strictly greater than the current version.</span></span>

## <span data-ttu-id="0cc23-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0cc23-113">PARAMETERS</span></span>

### <span data-ttu-id="0cc23-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cc23-114">-DefaultProfile</span></span>
<span data-ttu-id="0cc23-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0cc23-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0cc23-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0cc23-116">-InputObject</span></span>
<span data-ttu-id="0cc23-117">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0cc23-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: RerunViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="0cc23-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="0cc23-118">-Location</span></span>
<span data-ttu-id="0cc23-119">Güncelleştirme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="0cc23-119">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0cc23-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="0cc23-120">-Name</span></span>
<span data-ttu-id="0cc23-121">Çalışma tanımlayıcısını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="0cc23-121">Update run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0cc23-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0cc23-122">-PassThru</span></span>
<span data-ttu-id="0cc23-123">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="0cc23-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0cc23-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cc23-124">-ResourceGroupName</span></span>
<span data-ttu-id="0cc23-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0cc23-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0cc23-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="0cc23-126">-SubscriptionId</span></span>
<span data-ttu-id="0cc23-127">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="0cc23-127">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0cc23-128">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0cc23-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0cc23-129">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="0cc23-129">-UpdateName</span></span>
<span data-ttu-id="0cc23-130">Güncelleştirmenin adı.</span><span class="sxs-lookup"><span data-stu-id="0cc23-130">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0cc23-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="0cc23-131">-Confirm</span></span>
<span data-ttu-id="0cc23-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0cc23-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cc23-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cc23-133">-WhatIf</span></span>
<span data-ttu-id="0cc23-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0cc23-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cc23-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0cc23-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cc23-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cc23-136">CommonParameters</span></span>
<span data-ttu-id="0cc23-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0cc23-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cc23-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0cc23-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cc23-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0cc23-139">INPUTS</span></span>

### <span data-ttu-id="0cc23-140">Microsoft. Azure. PowerShell. cmdlet. UpdateAdmin. modeller. ıupdateadminıdentity</span><span class="sxs-lookup"><span data-stu-id="0cc23-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="0cc23-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0cc23-141">OUTPUTS</span></span>

### <span data-ttu-id="0cc23-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0cc23-142">System.Boolean</span></span>



## <span data-ttu-id="0cc23-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0cc23-143">NOTES</span></span>

<span data-ttu-id="0cc23-144">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0cc23-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0cc23-145">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0cc23-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="0cc23-146">INPUTOBJECT <IUpdateAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="0cc23-146">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0cc23-147">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="0cc23-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0cc23-148">`[ResourceGroupName <String>]`: Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0cc23-148">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="0cc23-149">`[RunName <String>]`: Güncelleştirme çalıştırması tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="0cc23-149">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="0cc23-150">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="0cc23-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="0cc23-151">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0cc23-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="0cc23-152">`[UpdateLocation <String>]`: Güncelleştirme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="0cc23-152">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="0cc23-153">`[UpdateName <String>]`: Güncelleştirmenin adı.</span><span class="sxs-lookup"><span data-stu-id="0cc23-153">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="0cc23-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0cc23-154">RELATED LINKS</span></span>
