---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/start-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
ms.openlocfilehash: 710c39adca3f3a82b91b1e27a7f63e0ef1f6b693
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268234"
---
# <span data-ttu-id="54f83-101">Start-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="54f83-101">Start-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="54f83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54f83-102">SYNOPSIS</span></span>
<span data-ttu-id="54f83-103">Var olan bir resim şablonundan yapılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="54f83-103">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="54f83-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54f83-104">SYNTAX</span></span>

### <span data-ttu-id="54f83-105">Çalışma (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="54f83-105">Run (Default)</span></span>
```
Start-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="54f83-106">Runviaıdentity</span><span class="sxs-lookup"><span data-stu-id="54f83-106">RunViaIdentity</span></span>
```
Start-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="54f83-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="54f83-107">DESCRIPTION</span></span>
<span data-ttu-id="54f83-108">Var olan bir resim şablonundan yapılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="54f83-108">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="54f83-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54f83-109">EXAMPLES</span></span>

### <span data-ttu-id="54f83-110">Örnek 1: resim şablonu başlatma</span><span class="sxs-lookup"><span data-stu-id="54f83-110">Example 1: Start an image template</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg

```

<span data-ttu-id="54f83-111">Bu komut, resim şablonunu başlatır.</span><span class="sxs-lookup"><span data-stu-id="54f83-111">This command starts an image template.</span></span>

### <span data-ttu-id="54f83-112">Örnek 2: resim şablonu başlatma</span><span class="sxs-lookup"><span data-stu-id="54f83-112">Example 2: Start an image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Start-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="54f83-113">Bu komut, resim şablonunu başlatır.</span><span class="sxs-lookup"><span data-stu-id="54f83-113">This command starts an image template.</span></span>

## <span data-ttu-id="54f83-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54f83-114">PARAMETERS</span></span>

### <span data-ttu-id="54f83-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="54f83-115">-AsJob</span></span>
<span data-ttu-id="54f83-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="54f83-116">Run the command as a job</span></span>

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

### <span data-ttu-id="54f83-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54f83-117">-DefaultProfile</span></span>
<span data-ttu-id="54f83-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="54f83-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54f83-119">-Imagetemplatename</span><span class="sxs-lookup"><span data-stu-id="54f83-119">-ImageTemplateName</span></span>
<span data-ttu-id="54f83-120">Resim şablonunun adı</span><span class="sxs-lookup"><span data-stu-id="54f83-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54f83-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54f83-121">-InputObject</span></span>
<span data-ttu-id="54f83-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54f83-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: RunViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54f83-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="54f83-123">-NoWait</span></span>
<span data-ttu-id="54f83-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="54f83-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="54f83-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="54f83-125">-PassThru</span></span>
<span data-ttu-id="54f83-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="54f83-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="54f83-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54f83-127">-ResourceGroupName</span></span>
<span data-ttu-id="54f83-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="54f83-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54f83-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="54f83-129">-SubscriptionId</span></span>
<span data-ttu-id="54f83-130">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="54f83-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="54f83-131">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="54f83-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54f83-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="54f83-132">-Confirm</span></span>
<span data-ttu-id="54f83-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="54f83-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54f83-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54f83-134">-WhatIf</span></span>
<span data-ttu-id="54f83-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="54f83-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54f83-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="54f83-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54f83-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54f83-137">CommonParameters</span></span>
<span data-ttu-id="54f83-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54f83-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54f83-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="54f83-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54f83-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54f83-140">INPUTS</span></span>

### <span data-ttu-id="54f83-141">Microsoft. Azure. PowerShell. cmdlet. ımagebuilder. model. ıımagebuilderıdentity</span><span class="sxs-lookup"><span data-stu-id="54f83-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="54f83-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54f83-142">OUTPUTS</span></span>

### <span data-ttu-id="54f83-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="54f83-143">System.Boolean</span></span>

## <span data-ttu-id="54f83-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54f83-144">NOTES</span></span>

<span data-ttu-id="54f83-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="54f83-145">ALIASES</span></span>

<span data-ttu-id="54f83-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="54f83-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="54f83-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="54f83-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="54f83-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="54f83-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="54f83-149">INPUTOBJECT <IImageBuilderIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="54f83-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="54f83-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="54f83-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="54f83-151">`[ImageTemplateName <String>]`: Resim şablonunun adı</span><span class="sxs-lookup"><span data-stu-id="54f83-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="54f83-152">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="54f83-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="54f83-153">`[RunOutputName <String>]`: Çalışma çıkışının adı</span><span class="sxs-lookup"><span data-stu-id="54f83-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="54f83-154">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="54f83-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="54f83-155">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="54f83-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="54f83-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54f83-156">RELATED LINKS</span></span>

