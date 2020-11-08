---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
ms.openlocfilehash: accf225acfb05fdcaf49eb5dde4d1bae0332d300
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267937"
---
# <span data-ttu-id="1a10a-101">Remove-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="1a10a-101">Remove-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="1a10a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a10a-102">SYNOPSIS</span></span>
<span data-ttu-id="1a10a-103">Özel bulutu silme</span><span class="sxs-lookup"><span data-stu-id="1a10a-103">Delete a private cloud</span></span>

## <span data-ttu-id="1a10a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a10a-104">SYNTAX</span></span>

### <span data-ttu-id="1a10a-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1a10a-105">Delete (Default)</span></span>
```
Remove-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1a10a-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="1a10a-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1a10a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a10a-107">DESCRIPTION</span></span>
<span data-ttu-id="1a10a-108">Özel bulutu silme</span><span class="sxs-lookup"><span data-stu-id="1a10a-108">Delete a private cloud</span></span>

## <span data-ttu-id="1a10a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a10a-109">EXAMPLES</span></span>

### <span data-ttu-id="1a10a-110">Örnek 1: özel bulutu silme</span><span class="sxs-lookup"><span data-stu-id="1a10a-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="1a10a-111">Özel bulutu silme</span><span class="sxs-lookup"><span data-stu-id="1a10a-111">Delete private cloud</span></span>

## <span data-ttu-id="1a10a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a10a-112">PARAMETERS</span></span>

### <span data-ttu-id="1a10a-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="1a10a-113">-AsJob</span></span>
<span data-ttu-id="1a10a-114">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="1a10a-114">Run the command as a job</span></span>

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

### <span data-ttu-id="1a10a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a10a-115">-DefaultProfile</span></span>
<span data-ttu-id="1a10a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1a10a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a10a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a10a-117">-InputObject</span></span>
<span data-ttu-id="1a10a-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1a10a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a10a-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="1a10a-119">-Name</span></span>
<span data-ttu-id="1a10a-120">Özel bulutun adı</span><span class="sxs-lookup"><span data-stu-id="1a10a-120">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a10a-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1a10a-121">-NoWait</span></span>
<span data-ttu-id="1a10a-122">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="1a10a-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1a10a-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1a10a-123">-PassThru</span></span>
<span data-ttu-id="1a10a-124">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="1a10a-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1a10a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a10a-125">-ResourceGroupName</span></span>
<span data-ttu-id="1a10a-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1a10a-126">The name of the resource group.</span></span>
<span data-ttu-id="1a10a-127">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="1a10a-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a10a-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="1a10a-128">-SubscriptionId</span></span>
<span data-ttu-id="1a10a-129">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1a10a-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a10a-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="1a10a-130">-Confirm</span></span>
<span data-ttu-id="1a10a-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1a10a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a10a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a10a-132">-WhatIf</span></span>
<span data-ttu-id="1a10a-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a10a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a10a-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1a10a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a10a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a10a-135">CommonParameters</span></span>
<span data-ttu-id="1a10a-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a10a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a10a-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1a10a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a10a-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a10a-138">INPUTS</span></span>

### <span data-ttu-id="1a10a-139">Microsoft. Azure. PowerShell. cmdlet. VMWare. modeller. ıvmwareıdentity</span><span class="sxs-lookup"><span data-stu-id="1a10a-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="1a10a-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a10a-140">OUTPUTS</span></span>

### <span data-ttu-id="1a10a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1a10a-141">System.Boolean</span></span>

## <span data-ttu-id="1a10a-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a10a-142">NOTES</span></span>

<span data-ttu-id="1a10a-143">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="1a10a-143">ALIASES</span></span>

<span data-ttu-id="1a10a-144">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="1a10a-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1a10a-145">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1a10a-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1a10a-146">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1a10a-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1a10a-147">INPUTOBJECT <IVMWareIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="1a10a-147">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1a10a-148">`[AuthorizationName <String>]`: Özel bulutta ExpressRoute devresi yetkilendirmesi adı</span><span class="sxs-lookup"><span data-stu-id="1a10a-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="1a10a-149">`[ClusterName <String>]`: Özel buluttaki kümenin adı</span><span class="sxs-lookup"><span data-stu-id="1a10a-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="1a10a-150">`[HcxEnterpriseSiteName <String>]`: Özel bulutta HCX kurumsal sitesinin adı</span><span class="sxs-lookup"><span data-stu-id="1a10a-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="1a10a-151">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="1a10a-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1a10a-152">`[Location <String>]`: Azure bölgesi</span><span class="sxs-lookup"><span data-stu-id="1a10a-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="1a10a-153">`[PrivateCloudName <String>]`: Özel bulutun adı</span><span class="sxs-lookup"><span data-stu-id="1a10a-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="1a10a-154">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1a10a-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1a10a-155">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="1a10a-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="1a10a-156">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1a10a-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="1a10a-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a10a-157">RELATED LINKS</span></span>

