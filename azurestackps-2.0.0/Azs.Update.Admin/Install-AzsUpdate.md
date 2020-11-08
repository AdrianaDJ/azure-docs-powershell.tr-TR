---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/install-azsupdate
schema: 2.0.0
ms.openlocfilehash: e6fc8ee19443f0861fb867a5e60d0f637642ff62
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935201"
---
# <span data-ttu-id="99c86-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="99c86-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="99c86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99c86-102">SYNOPSIS</span></span>
<span data-ttu-id="99c86-103">Güncelleştirme konumunda belirli bir güncelleştirme uygulayın.</span><span class="sxs-lookup"><span data-stu-id="99c86-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="99c86-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99c86-104">SYNTAX</span></span>

### <span data-ttu-id="99c86-105">Uygula (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="99c86-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="99c86-106">Applyviaıdentity</span><span class="sxs-lookup"><span data-stu-id="99c86-106">ApplyViaIdentity</span></span>
```
Install-AzsUpdate -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="99c86-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="99c86-107">DESCRIPTION</span></span>
<span data-ttu-id="99c86-108">Güncelleştirme konumunda belirli bir güncelleştirme uygulayın.</span><span class="sxs-lookup"><span data-stu-id="99c86-108">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="99c86-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99c86-109">EXAMPLES</span></span>

### <span data-ttu-id="99c86-110">Örnek 1: ada göre Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="99c86-110">Example 1: Install-AzsUpdate By Name</span></span>
```powershell
PS C:\> Install-AzsUpdate -Name Microsoft1.1907.0.10
```

<span data-ttu-id="99c86-111">Command, belirli güncellemeleri ada göre yüklemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="99c86-111">Commandlet allows you to install specific updates by name.</span></span>
<span data-ttu-id="99c86-112">Güncelleştirme sürümünün geçerli sürümden kesinlikle daha büyük olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="99c86-112">Note that there is a requirement that the update version is strictly greater than the current version.</span></span>

## <span data-ttu-id="99c86-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99c86-113">PARAMETERS</span></span>

### <span data-ttu-id="99c86-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="99c86-114">-AsJob</span></span>
<span data-ttu-id="99c86-115">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="99c86-115">Run the command as a job</span></span>

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

### <span data-ttu-id="99c86-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99c86-116">-DefaultProfile</span></span>
<span data-ttu-id="99c86-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="99c86-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99c86-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99c86-118">-InputObject</span></span>
<span data-ttu-id="99c86-119">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="99c86-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: ApplyViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="99c86-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="99c86-120">-Location</span></span>
<span data-ttu-id="99c86-121">Güncelleştirme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="99c86-121">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="99c86-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="99c86-122">-Name</span></span>
<span data-ttu-id="99c86-123">Güncelleştirmenin adı.</span><span class="sxs-lookup"><span data-stu-id="99c86-123">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="99c86-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="99c86-124">-NoWait</span></span>
<span data-ttu-id="99c86-125">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="99c86-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="99c86-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99c86-126">-ResourceGroupName</span></span>
<span data-ttu-id="99c86-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="99c86-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="99c86-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="99c86-128">-SubscriptionId</span></span>
<span data-ttu-id="99c86-129">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="99c86-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="99c86-130">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="99c86-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="99c86-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="99c86-131">-Confirm</span></span>
<span data-ttu-id="99c86-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="99c86-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99c86-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99c86-133">-WhatIf</span></span>
<span data-ttu-id="99c86-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="99c86-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99c86-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="99c86-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99c86-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99c86-136">CommonParameters</span></span>
<span data-ttu-id="99c86-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99c86-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99c86-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="99c86-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99c86-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99c86-139">INPUTS</span></span>

### <span data-ttu-id="99c86-140">Microsoft. Azure. PowerShell. cmdlet. UpdateAdmin. modeller. ıupdateadminıdentity</span><span class="sxs-lookup"><span data-stu-id="99c86-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="99c86-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99c86-141">OUTPUTS</span></span>

### <span data-ttu-id="99c86-142">Microsoft. Azure. PowerShell. cmdlet. UpdateAdmin. modeller. Api20160501. ıupdaterun</span><span class="sxs-lookup"><span data-stu-id="99c86-142">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateRun</span></span>



## <span data-ttu-id="99c86-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99c86-143">NOTES</span></span>

<span data-ttu-id="99c86-144">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="99c86-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="99c86-145">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="99c86-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="99c86-146">INPUTOBJECT <IUpdateAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="99c86-146">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="99c86-147">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="99c86-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="99c86-148">`[ResourceGroupName <String>]`: Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="99c86-148">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="99c86-149">`[RunName <String>]`: Güncelleştirme çalıştırması tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="99c86-149">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="99c86-150">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="99c86-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="99c86-151">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="99c86-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="99c86-152">`[UpdateLocation <String>]`: Güncelleştirme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="99c86-152">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="99c86-153">`[UpdateName <String>]`: Güncelleştirmenin adı.</span><span class="sxs-lookup"><span data-stu-id="99c86-153">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="99c86-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99c86-154">RELATED LINKS</span></span>
