---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/stop-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
ms.openlocfilehash: 01fd95dd41a7ee76c06f0423d33c4aba34329c18
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277371"
---
# <span data-ttu-id="c61ff-101">Stop-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="c61ff-101">Stop-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="c61ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c61ff-102">SYNOPSIS</span></span>
<span data-ttu-id="c61ff-103">Görüntü şablonunu temel alan uzun süren görüntü oluşturmayı iptal etme</span><span class="sxs-lookup"><span data-stu-id="c61ff-103">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="c61ff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c61ff-104">SYNTAX</span></span>

### <span data-ttu-id="c61ff-105">İptal (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c61ff-105">Cancel (Default)</span></span>
```
Stop-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c61ff-106">Cancelviaıdentity</span><span class="sxs-lookup"><span data-stu-id="c61ff-106">CancelViaIdentity</span></span>
```
Stop-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c61ff-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c61ff-107">DESCRIPTION</span></span>
<span data-ttu-id="c61ff-108">Görüntü şablonunu temel alan uzun süren görüntü oluşturmayı iptal etme</span><span class="sxs-lookup"><span data-stu-id="c61ff-108">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="c61ff-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c61ff-109">EXAMPLES</span></span>

### <span data-ttu-id="c61ff-110">Örnek 1: resim şablonunu durdurma oluşturma</span><span class="sxs-lookup"><span data-stu-id="c61ff-110">Example 1: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> Stop-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="c61ff-111">Bu komut, resim şablonu oluşturmayı durdurur.</span><span class="sxs-lookup"><span data-stu-id="c61ff-111">This command stops image template creation.</span></span>

### <span data-ttu-id="c61ff-112">Örnek 2: resim şablonu oluşturmayı durdurma</span><span class="sxs-lookup"><span data-stu-id="c61ff-112">Example 2: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Stop-AzImageBuilderTemplate -InputObject $template 

```

<span data-ttu-id="c61ff-113">Bu komut, resim şablonu oluşturmayı durdurur.</span><span class="sxs-lookup"><span data-stu-id="c61ff-113">This command stops image template creation.</span></span>

## <span data-ttu-id="c61ff-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c61ff-114">PARAMETERS</span></span>

### <span data-ttu-id="c61ff-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="c61ff-115">-AsJob</span></span>
<span data-ttu-id="c61ff-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="c61ff-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c61ff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c61ff-117">-DefaultProfile</span></span>
<span data-ttu-id="c61ff-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c61ff-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c61ff-119">-Imagetemplatename</span><span class="sxs-lookup"><span data-stu-id="c61ff-119">-ImageTemplateName</span></span>
<span data-ttu-id="c61ff-120">Resim şablonunun adı</span><span class="sxs-lookup"><span data-stu-id="c61ff-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c61ff-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c61ff-121">-InputObject</span></span>
<span data-ttu-id="c61ff-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c61ff-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: CancelViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c61ff-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c61ff-123">-NoWait</span></span>
<span data-ttu-id="c61ff-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="c61ff-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c61ff-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c61ff-125">-PassThru</span></span>
<span data-ttu-id="c61ff-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="c61ff-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c61ff-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c61ff-127">-ResourceGroupName</span></span>
<span data-ttu-id="c61ff-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c61ff-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c61ff-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c61ff-129">-SubscriptionId</span></span>
<span data-ttu-id="c61ff-130">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="c61ff-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c61ff-131">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="c61ff-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c61ff-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="c61ff-132">-Confirm</span></span>
<span data-ttu-id="c61ff-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c61ff-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c61ff-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c61ff-134">-WhatIf</span></span>
<span data-ttu-id="c61ff-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c61ff-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c61ff-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c61ff-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c61ff-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c61ff-137">CommonParameters</span></span>
<span data-ttu-id="c61ff-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c61ff-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c61ff-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c61ff-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c61ff-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c61ff-140">INPUTS</span></span>

### <span data-ttu-id="c61ff-141">Microsoft. Azure. PowerShell. cmdlet. ımagebuilder. model. ıımagebuilderıdentity</span><span class="sxs-lookup"><span data-stu-id="c61ff-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="c61ff-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c61ff-142">OUTPUTS</span></span>

### <span data-ttu-id="c61ff-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c61ff-143">System.Boolean</span></span>

## <span data-ttu-id="c61ff-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c61ff-144">NOTES</span></span>

<span data-ttu-id="c61ff-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="c61ff-145">ALIASES</span></span>

<span data-ttu-id="c61ff-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="c61ff-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c61ff-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c61ff-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c61ff-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c61ff-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c61ff-149">INPUTOBJECT <IImageBuilderIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="c61ff-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c61ff-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="c61ff-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c61ff-151">`[ImageTemplateName <String>]`: Resim şablonunun adı</span><span class="sxs-lookup"><span data-stu-id="c61ff-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="c61ff-152">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c61ff-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c61ff-153">`[RunOutputName <String>]`: Çalışma çıkışının adı</span><span class="sxs-lookup"><span data-stu-id="c61ff-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="c61ff-154">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="c61ff-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c61ff-155">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="c61ff-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c61ff-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c61ff-156">RELATED LINKS</span></span>

