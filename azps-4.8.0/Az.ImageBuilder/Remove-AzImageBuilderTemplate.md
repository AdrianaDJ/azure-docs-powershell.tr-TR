---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/remove-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
ms.openlocfilehash: 998c4f05e8b6a03749a4872e3f4b069e29ef634d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108083"
---
# <span data-ttu-id="c42db-101">Remove-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="c42db-101">Remove-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="c42db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c42db-102">SYNOPSIS</span></span>
<span data-ttu-id="c42db-103">Sanal makine görüntü şablonunu silme</span><span class="sxs-lookup"><span data-stu-id="c42db-103">Delete a virtual machine image template</span></span>

## <span data-ttu-id="c42db-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c42db-104">SYNTAX</span></span>

### <span data-ttu-id="c42db-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c42db-105">Delete (Default)</span></span>
```
Remove-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c42db-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="c42db-106">DeleteViaIdentity</span></span>
```
Remove-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c42db-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c42db-107">DESCRIPTION</span></span>
<span data-ttu-id="c42db-108">Sanal makine görüntü şablonunu silme</span><span class="sxs-lookup"><span data-stu-id="c42db-108">Delete a virtual machine image template</span></span>

## <span data-ttu-id="c42db-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c42db-109">EXAMPLES</span></span>

### <span data-ttu-id="c42db-110">Örnek 1: resim şablonunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="c42db-110">Example 1: Remove a image template</span></span>
```powershell
PS C:\> Remove-AzImageBuilderTemplate -ImageTemplateName template-name-dmt6ze -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="c42db-111">Bu komut, resim şablonunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c42db-111">This command removes a image template.</span></span>

### <span data-ttu-id="c42db-112">Örnek 2: resim şablonunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="c42db-112">Example 2: Remove a image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ImageTemplateName template-name-3uo8p6 -ResourceGroupName wyunchi-imagebuilder
PS C:\> Remove-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="c42db-113">Bu komut, resim şablonunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c42db-113">This command removes a image template.</span></span>

## <span data-ttu-id="c42db-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c42db-114">PARAMETERS</span></span>

### <span data-ttu-id="c42db-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="c42db-115">-AsJob</span></span>
<span data-ttu-id="c42db-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="c42db-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c42db-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c42db-117">-DefaultProfile</span></span>
<span data-ttu-id="c42db-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c42db-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c42db-119">-Imagetemplatename</span><span class="sxs-lookup"><span data-stu-id="c42db-119">-ImageTemplateName</span></span>
<span data-ttu-id="c42db-120">Resim şablonunun adı</span><span class="sxs-lookup"><span data-stu-id="c42db-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42db-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c42db-121">-InputObject</span></span>
<span data-ttu-id="c42db-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c42db-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c42db-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c42db-123">-NoWait</span></span>
<span data-ttu-id="c42db-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="c42db-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c42db-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c42db-125">-PassThru</span></span>
<span data-ttu-id="c42db-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="c42db-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c42db-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c42db-127">-ResourceGroupName</span></span>
<span data-ttu-id="c42db-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c42db-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="c42db-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c42db-129">-SubscriptionId</span></span>
<span data-ttu-id="c42db-130">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="c42db-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c42db-131">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="c42db-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c42db-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="c42db-132">-Confirm</span></span>
<span data-ttu-id="c42db-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c42db-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c42db-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c42db-134">-WhatIf</span></span>
<span data-ttu-id="c42db-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c42db-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c42db-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c42db-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c42db-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c42db-137">CommonParameters</span></span>
<span data-ttu-id="c42db-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c42db-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c42db-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c42db-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c42db-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c42db-140">INPUTS</span></span>

### <span data-ttu-id="c42db-141">Microsoft. Azure. PowerShell. cmdlet. ımagebuilder. model. ıımagebuilderıdentity</span><span class="sxs-lookup"><span data-stu-id="c42db-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="c42db-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c42db-142">OUTPUTS</span></span>

### <span data-ttu-id="c42db-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c42db-143">System.Boolean</span></span>

## <span data-ttu-id="c42db-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c42db-144">NOTES</span></span>

<span data-ttu-id="c42db-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="c42db-145">ALIASES</span></span>

<span data-ttu-id="c42db-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="c42db-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c42db-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c42db-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c42db-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c42db-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c42db-149">INPUTOBJECT <IImageBuilderIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="c42db-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c42db-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="c42db-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c42db-151">`[ImageTemplateName <String>]`: Resim şablonunun adı</span><span class="sxs-lookup"><span data-stu-id="c42db-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="c42db-152">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c42db-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c42db-153">`[RunOutputName <String>]`: Çalışma çıkışının adı</span><span class="sxs-lookup"><span data-stu-id="c42db-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="c42db-154">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="c42db-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c42db-155">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="c42db-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c42db-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c42db-156">RELATED LINKS</span></span>

