---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/stop-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
ms.openlocfilehash: 01fd95dd41a7ee76c06f0423d33c4aba34329c18
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268232"
---
# <span data-ttu-id="29dc8-101">Stop-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="29dc8-101">Stop-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="29dc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="29dc8-103">Görüntü şablonunu temel alan uzun süren görüntü oluşturmayı iptal etme</span><span class="sxs-lookup"><span data-stu-id="29dc8-103">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="29dc8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="29dc8-104">SYNTAX</span></span>

### <span data-ttu-id="29dc8-105">İptal (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="29dc8-105">Cancel (Default)</span></span>
```
Stop-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="29dc8-106">Cancelviaıdentity</span><span class="sxs-lookup"><span data-stu-id="29dc8-106">CancelViaIdentity</span></span>
```
Stop-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="29dc8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="29dc8-107">DESCRIPTION</span></span>
<span data-ttu-id="29dc8-108">Görüntü şablonunu temel alan uzun süren görüntü oluşturmayı iptal etme</span><span class="sxs-lookup"><span data-stu-id="29dc8-108">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="29dc8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="29dc8-109">EXAMPLES</span></span>

### <span data-ttu-id="29dc8-110">Örnek 1: resim şablonunu durdurma oluşturma</span><span class="sxs-lookup"><span data-stu-id="29dc8-110">Example 1: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> Stop-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="29dc8-111">Bu komut, resim şablonu oluşturmayı durdurur.</span><span class="sxs-lookup"><span data-stu-id="29dc8-111">This command stops image template creation.</span></span>

### <span data-ttu-id="29dc8-112">Örnek 2: resim şablonu oluşturmayı durdurma</span><span class="sxs-lookup"><span data-stu-id="29dc8-112">Example 2: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Stop-AzImageBuilderTemplate -InputObject $template 

```

<span data-ttu-id="29dc8-113">Bu komut, resim şablonu oluşturmayı durdurur.</span><span class="sxs-lookup"><span data-stu-id="29dc8-113">This command stops image template creation.</span></span>

## <span data-ttu-id="29dc8-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="29dc8-114">PARAMETERS</span></span>

### <span data-ttu-id="29dc8-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="29dc8-115">-AsJob</span></span>
<span data-ttu-id="29dc8-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="29dc8-116">Run the command as a job</span></span>

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

### <span data-ttu-id="29dc8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29dc8-117">-DefaultProfile</span></span>
<span data-ttu-id="29dc8-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="29dc8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29dc8-119">-Imagetemplatename</span><span class="sxs-lookup"><span data-stu-id="29dc8-119">-ImageTemplateName</span></span>
<span data-ttu-id="29dc8-120">Resim şablonunun adı</span><span class="sxs-lookup"><span data-stu-id="29dc8-120">The name of the image Template</span></span>

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

### <span data-ttu-id="29dc8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29dc8-121">-InputObject</span></span>
<span data-ttu-id="29dc8-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="29dc8-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="29dc8-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="29dc8-123">-NoWait</span></span>
<span data-ttu-id="29dc8-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="29dc8-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="29dc8-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="29dc8-125">-PassThru</span></span>
<span data-ttu-id="29dc8-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="29dc8-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="29dc8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29dc8-127">-ResourceGroupName</span></span>
<span data-ttu-id="29dc8-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="29dc8-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="29dc8-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="29dc8-129">-SubscriptionId</span></span>
<span data-ttu-id="29dc8-130">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="29dc8-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="29dc8-131">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="29dc8-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="29dc8-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="29dc8-132">-Confirm</span></span>
<span data-ttu-id="29dc8-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="29dc8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29dc8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29dc8-134">-WhatIf</span></span>
<span data-ttu-id="29dc8-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="29dc8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29dc8-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="29dc8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29dc8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29dc8-137">CommonParameters</span></span>
<span data-ttu-id="29dc8-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="29dc8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29dc8-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="29dc8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29dc8-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="29dc8-140">INPUTS</span></span>

### <span data-ttu-id="29dc8-141">Microsoft. Azure. PowerShell. cmdlet. ımagebuilder. model. ıımagebuilderıdentity</span><span class="sxs-lookup"><span data-stu-id="29dc8-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="29dc8-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="29dc8-142">OUTPUTS</span></span>

### <span data-ttu-id="29dc8-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="29dc8-143">System.Boolean</span></span>

## <span data-ttu-id="29dc8-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="29dc8-144">NOTES</span></span>

<span data-ttu-id="29dc8-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="29dc8-145">ALIASES</span></span>

<span data-ttu-id="29dc8-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="29dc8-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="29dc8-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="29dc8-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="29dc8-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="29dc8-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="29dc8-149">INPUTOBJECT <IImageBuilderIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="29dc8-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="29dc8-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="29dc8-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="29dc8-151">`[ImageTemplateName <String>]`: Resim şablonunun adı</span><span class="sxs-lookup"><span data-stu-id="29dc8-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="29dc8-152">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="29dc8-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="29dc8-153">`[RunOutputName <String>]`: Çalışma çıkışının adı</span><span class="sxs-lookup"><span data-stu-id="29dc8-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="29dc8-154">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="29dc8-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="29dc8-155">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="29dc8-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="29dc8-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="29dc8-156">RELATED LINKS</span></span>

