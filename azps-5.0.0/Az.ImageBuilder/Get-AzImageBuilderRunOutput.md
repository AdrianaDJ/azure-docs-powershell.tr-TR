---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
ms.openlocfilehash: 4cc45f3b4cd21e41f1b2e410dd2b76b9571a4431
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319525"
---
# <span data-ttu-id="2edc5-101">Get-AzImageBuilderRunOutput</span><span class="sxs-lookup"><span data-stu-id="2edc5-101">Get-AzImageBuilderRunOutput</span></span>

## <span data-ttu-id="2edc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2edc5-102">SYNOPSIS</span></span>
<span data-ttu-id="2edc5-103">Belirtilen resim şablonu kaynağı için belirtilen çalışma çıktısını alma</span><span class="sxs-lookup"><span data-stu-id="2edc5-103">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="2edc5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2edc5-104">SYNTAX</span></span>

### <span data-ttu-id="2edc5-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2edc5-105">List (Default)</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2edc5-106">Al</span><span class="sxs-lookup"><span data-stu-id="2edc5-106">Get</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2edc5-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="2edc5-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="2edc5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2edc5-108">DESCRIPTION</span></span>
<span data-ttu-id="2edc5-109">Belirtilen resim şablonu kaynağı için belirtilen çalışma çıktısını alma</span><span class="sxs-lookup"><span data-stu-id="2edc5-109">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="2edc5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2edc5-110">EXAMPLES</span></span>

### <span data-ttu-id="2edc5-111">Örnek 1: tüm çalışma sonuçlarını bir şablon altında listeleme</span><span class="sxs-lookup"><span data-stu-id="2edc5-111">Example 1: List all run results under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="2edc5-112">Bu komut, şablonun altındaki tüm çalışma sonuçlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="2edc5-112">This command lists all run results under a template.</span></span>

### <span data-ttu-id="2edc5-113">Örnek 2: bir şablon altında bir çalışma sonucu alma</span><span class="sxs-lookup"><span data-stu-id="2edc5-113">Example 2: Get a run result under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="2edc5-114">Bu komut, şablon altında bir çalışma sonucunu alır.</span><span class="sxs-lookup"><span data-stu-id="2edc5-114">This command gets a run result under a template.</span></span>

### <span data-ttu-id="2edc5-115">Örnek 3: bir şablon altında bir çalışma sonucu alma</span><span class="sxs-lookup"><span data-stu-id="2edc5-115">Example 3: Get a run result under a template</span></span>
```powershell
PS C:\> $result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
PS C:\> Get-AzImageBuilderRunOutput -InputObject $result

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="2edc5-116">Bu komut, şablon altında bir çalışma sonucunu alır.</span><span class="sxs-lookup"><span data-stu-id="2edc5-116">This command gets a run result under a template.</span></span>

## <span data-ttu-id="2edc5-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2edc5-117">PARAMETERS</span></span>

### <span data-ttu-id="2edc5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2edc5-118">-DefaultProfile</span></span>
<span data-ttu-id="2edc5-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2edc5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2edc5-120">-Imagetemplatename</span><span class="sxs-lookup"><span data-stu-id="2edc5-120">-ImageTemplateName</span></span>
<span data-ttu-id="2edc5-121">Resim şablonunun adı</span><span class="sxs-lookup"><span data-stu-id="2edc5-121">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2edc5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2edc5-122">-InputObject</span></span>
<span data-ttu-id="2edc5-123">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2edc5-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2edc5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2edc5-124">-ResourceGroupName</span></span>
<span data-ttu-id="2edc5-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2edc5-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2edc5-126">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="2edc5-126">-RunOutputName</span></span>
<span data-ttu-id="2edc5-127">Çalışma çıkışının adı</span><span class="sxs-lookup"><span data-stu-id="2edc5-127">The name of the run output</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2edc5-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="2edc5-128">-SubscriptionId</span></span>
<span data-ttu-id="2edc5-129">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="2edc5-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2edc5-130">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="2edc5-130">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2edc5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2edc5-131">CommonParameters</span></span>
<span data-ttu-id="2edc5-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2edc5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2edc5-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2edc5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2edc5-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2edc5-134">INPUTS</span></span>

### <span data-ttu-id="2edc5-135">Microsoft. Azure. PowerShell. cmdlet. ımagebuilder. model. ıımagebuilderıdentity</span><span class="sxs-lookup"><span data-stu-id="2edc5-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="2edc5-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2edc5-136">OUTPUTS</span></span>

### <span data-ttu-id="2edc5-137">Microsoft. Azure. PowerShell. cmdlet. ımagebuilder. modeller. Api20200214. ırunoutput</span><span class="sxs-lookup"><span data-stu-id="2edc5-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span></span>

## <span data-ttu-id="2edc5-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2edc5-138">NOTES</span></span>

<span data-ttu-id="2edc5-139">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="2edc5-139">ALIASES</span></span>

<span data-ttu-id="2edc5-140">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="2edc5-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2edc5-141">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2edc5-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2edc5-142">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2edc5-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2edc5-143">INPUTOBJECT <IImageBuilderIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="2edc5-143">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2edc5-144">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="2edc5-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2edc5-145">`[ImageTemplateName <String>]`: Resim şablonunun adı</span><span class="sxs-lookup"><span data-stu-id="2edc5-145">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="2edc5-146">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2edc5-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="2edc5-147">`[RunOutputName <String>]`: Çalışma çıkışının adı</span><span class="sxs-lookup"><span data-stu-id="2edc5-147">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="2edc5-148">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="2edc5-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2edc5-149">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="2edc5-149">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2edc5-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2edc5-150">RELATED LINKS</span></span>

