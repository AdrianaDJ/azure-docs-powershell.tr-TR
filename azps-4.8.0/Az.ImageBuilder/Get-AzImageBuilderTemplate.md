---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
ms.openlocfilehash: d159a59f6fb94523868b4aa6109553900f1b289d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268851"
---
# <span data-ttu-id="d3643-101">Get-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="d3643-101">Get-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="d3643-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3643-102">SYNOPSIS</span></span>
<span data-ttu-id="d3643-103">Sanal makine görüntü şablonuyla ilgili bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="d3643-103">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="d3643-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3643-104">SYNTAX</span></span>

### <span data-ttu-id="d3643-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d3643-105">List (Default)</span></span>
```
Get-AzImageBuilderTemplate [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d3643-106">Al</span><span class="sxs-lookup"><span data-stu-id="d3643-106">Get</span></span>
```
Get-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d3643-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="d3643-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3643-108">List1</span><span class="sxs-lookup"><span data-stu-id="d3643-108">List1</span></span>
```
Get-AzImageBuilderTemplate -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d3643-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3643-109">DESCRIPTION</span></span>
<span data-ttu-id="d3643-110">Sanal makine görüntü şablonuyla ilgili bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="d3643-110">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="d3643-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3643-111">EXAMPLES</span></span>

### <span data-ttu-id="d3643-112">Örnek 1: aboneliğin altındaki tüm şablonları listeleme</span><span class="sxs-lookup"><span data-stu-id="d3643-112">Example 1: List all template under a subscription</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate

Location Name                      Type
-------- ----                      ----
eastus   HelloImageTemplateLinux01 Microsoft.VirtualMachineImages/imageTemplates
eastus   lucas-imagetemplate       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder         Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="d3643-113">Bu komut, bir aboneliğin altındaki tüm şablonları listeler.</span><span class="sxs-lookup"><span data-stu-id="d3643-113">This command lists all template under a subscription.</span></span>

### <span data-ttu-id="d3643-114">Örnek 2: kaynak grubu altındaki tüm şablonları listeleme</span><span class="sxs-lookup"><span data-stu-id="d3643-114">Example 2: List all template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                       Type
-------- ----                       ----
eastus   HelloImageTemplateLinux01  Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ax01b7       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ep5z7v       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-klcuav       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-u7gjqx       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder          Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-managedimg-managedimg Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-platform-managed      Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-shareimg-managedimg   Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="d3643-115">Bu komut, kaynak grubu altındaki tüm şablonları listeler.</span><span class="sxs-lookup"><span data-stu-id="d3643-115">This command lists all template under a resource group.</span></span>

### <span data-ttu-id="d3643-116">Örnek 3: kaynak grubu altında şablon alma</span><span class="sxs-lookup"><span data-stu-id="d3643-116">Example 3: Get a template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                Type
-------- ----                ----
eastus   lucas-imagetemplate Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="d3643-117">Bu komut, kaynak grubu altında bir şablon alır.</span><span class="sxs-lookup"><span data-stu-id="d3643-117">This command gets a template under a resource group.</span></span>

### <span data-ttu-id="d3643-118">Örnek 4: kaynak grubu altında şablon alma</span><span class="sxs-lookup"><span data-stu-id="d3643-118">Example 4: Get a template under a resource group</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -ImageTemplateName template-name-ep5z7v
PS C:\> Get-AzImageBuilderTemplate -InputObject $template

Location Name                 Type
-------- ----                 ----
eastus   template-name-ep5z7v Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="d3643-119">Bu komut, kaynak grubu altında bir şablon alır.</span><span class="sxs-lookup"><span data-stu-id="d3643-119">This command gets a template under a resource group.</span></span>

## <span data-ttu-id="d3643-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3643-120">PARAMETERS</span></span>

### <span data-ttu-id="d3643-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3643-121">-DefaultProfile</span></span>
<span data-ttu-id="d3643-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d3643-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3643-123">-Imagetemplatename</span><span class="sxs-lookup"><span data-stu-id="d3643-123">-ImageTemplateName</span></span>
<span data-ttu-id="d3643-124">Resim şablonunun adı</span><span class="sxs-lookup"><span data-stu-id="d3643-124">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3643-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3643-125">-InputObject</span></span>
<span data-ttu-id="d3643-126">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d3643-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d3643-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3643-127">-ResourceGroupName</span></span>
<span data-ttu-id="d3643-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d3643-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3643-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d3643-129">-SubscriptionId</span></span>
<span data-ttu-id="d3643-130">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="d3643-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d3643-131">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="d3643-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3643-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3643-132">CommonParameters</span></span>
<span data-ttu-id="d3643-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3643-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3643-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d3643-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3643-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3643-135">INPUTS</span></span>

### <span data-ttu-id="d3643-136">Microsoft. Azure. PowerShell. cmdlet. ımagebuilder. model. ıımagebuilderıdentity</span><span class="sxs-lookup"><span data-stu-id="d3643-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="d3643-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3643-137">OUTPUTS</span></span>

### <span data-ttu-id="d3643-138">Microsoft. Azure. PowerShell. cmdlet. ımagebuilder. modeller. Api20200214. ıımagetemplate</span><span class="sxs-lookup"><span data-stu-id="d3643-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="d3643-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3643-139">NOTES</span></span>

<span data-ttu-id="d3643-140">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="d3643-140">ALIASES</span></span>

<span data-ttu-id="d3643-141">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="d3643-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d3643-142">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d3643-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d3643-143">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d3643-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d3643-144">INPUTOBJECT <IImageBuilderIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="d3643-144">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d3643-145">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="d3643-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d3643-146">`[ImageTemplateName <String>]`: Resim şablonunun adı</span><span class="sxs-lookup"><span data-stu-id="d3643-146">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="d3643-147">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d3643-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="d3643-148">`[RunOutputName <String>]`: Çalışma çıkışının adı</span><span class="sxs-lookup"><span data-stu-id="d3643-148">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="d3643-149">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="d3643-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d3643-150">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="d3643-150">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d3643-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3643-151">RELATED LINKS</span></span>

