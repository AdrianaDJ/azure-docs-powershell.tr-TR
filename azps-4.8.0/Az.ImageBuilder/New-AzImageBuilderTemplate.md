---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderTemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
ms.openlocfilehash: 337584fb7f960f64ee94c5206f9bf60b0cc6c21a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267391"
---
# <span data-ttu-id="55c35-101">New-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="55c35-101">New-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="55c35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55c35-102">SYNOPSIS</span></span>
<span data-ttu-id="55c35-103">Sanal makine görüntü şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="55c35-103">Create a virtual machine image template</span></span>

## <span data-ttu-id="55c35-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55c35-104">SYNTAX</span></span>

```
New-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 -Distribute <IImageTemplateDistributor[]> -Source <IImageTemplateSource> -UserAssignedIdentityId <String>
 [-SubscriptionId <String>] [-BuildTimeoutInMinute <Int32>] [-Customize <IImageTemplateCustomizer[]>]
 [-LastRunStatusEndTime <DateTime>] [-LastRunStatusMessage <String>] [-LastRunStatusRunState <RunState>]
 [-LastRunStatusRunSubState <RunSubState>] [-LastRunStatusStartTime <DateTime>] [-Location <String>]
 [-ProvisioningErrorCode <ProvisioningErrorCode>] [-ProvisioningErrorMessage <String>] [-Tag <Hashtable>]
 [-VMProfileOsdiskSizeInGb <Int32>] [-VMProfileVmSize <String>] [-VnetConfigSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="55c35-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="55c35-105">DESCRIPTION</span></span>
<span data-ttu-id="55c35-106">Sanal makine görüntü şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="55c35-106">Create a virtual machine image template</span></span>

## <span data-ttu-id="55c35-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55c35-107">EXAMPLES</span></span>

### <span data-ttu-id="55c35-108">Örnek 1: sanal makine görüntü şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="55c35-108">Example 1: Create a virtual machine image template</span></span>
```powershell
PS C:\> $srcPlatform = New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical'  -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'
PS C:\> $disSharedImg = New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/testsharedgallery/images/imagedefinition-linux/versions/1.0.0' -ReplicationRegion 'eastus2' -RunOutputName 'runoutput-01'  -ExcludeFromLatest $false
PS C:\> $customizer = New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName 'CheckSumCompareShellScript' -ScriptUri 'https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh' -Sha256Checksum 'ade4c5214c3c675e92c66e2d067a870c5b81b9844b3de3cc72c49ff36425fc93'
PS C:\> $userAssignedIdentity = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/wyunchi-imagebuilder/providers/Microsoft.ManagedIdentity/userAssignedIdentities/image-builder-user-assign-identity'
PS C:\> New-AzImageBuilderTemplate -ImageTemplateName platform-shared-img -ResourceGroupName wyunchi-imagebuilder -Source $srcPlatform -Distribute $disSharedImg -Customize $customizer -Location eastus  -UserAssignedIdentityId $userAssignedIdentity

Location Name                Type
-------- ----                ----
PlanInfoPlanName      :
PlanInfoPlanPublisher :
Sku                   : 18.04-LTS
Version               : latest
PlanInfo              : Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.PlatformImagePurchasePlan
```

<span data-ttu-id="55c35-109">Bu komut, bir sanal makine görüntü şablonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="55c35-109">This commands creates a virtual machine image template.</span></span>

## <span data-ttu-id="55c35-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55c35-110">PARAMETERS</span></span>

### <span data-ttu-id="55c35-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="55c35-111">-AsJob</span></span>
<span data-ttu-id="55c35-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="55c35-112">Run the command as a job</span></span>

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

### <span data-ttu-id="55c35-113">-Buildtimeoutınminute</span><span class="sxs-lookup"><span data-stu-id="55c35-113">-BuildTimeoutInMinute</span></span>
<span data-ttu-id="55c35-114">Resim şablonunu oluştururken beklenecek süre üst sınırı.</span><span class="sxs-lookup"><span data-stu-id="55c35-114">Maximum duration to wait while building the image template.</span></span>
<span data-ttu-id="55c35-115">Varsayılanı (4 saat) kullanmak için 0 değerini atlayın veya belirtin.</span><span class="sxs-lookup"><span data-stu-id="55c35-115">Omit or specify 0 to use the default (4 hours).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c35-116">-Özelleştir</span><span class="sxs-lookup"><span data-stu-id="55c35-116">-Customize</span></span>
<span data-ttu-id="55c35-117">Resim kaynağı gibi resmin özelleştirme adımlarını açıklamak için kullanılan özellikleri belirtir. Oluşturmak için, özellikleri ÖZELLEŞTIRME ve karma tablo oluşturma başlıklı Notlar bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="55c35-117">Specifies the properties used to describe the customization steps of the image, like Image source etc. To construct, see NOTES section for CUSTOMIZE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c35-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55c35-118">-DefaultProfile</span></span>
<span data-ttu-id="55c35-119">Region HideParameter Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55c35-119">region HideParameter The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55c35-120">-Dağıt</span><span class="sxs-lookup"><span data-stu-id="55c35-120">-Distribute</span></span>
<span data-ttu-id="55c35-121">Görüntü çıkışının gideceği dağıtım hedefleri.</span><span class="sxs-lookup"><span data-stu-id="55c35-121">The distribution targets where the image output needs to go to.</span></span>
<span data-ttu-id="55c35-122">Oluşturmak için, özellikleri DAĞıTMA ve karma tablo oluşturma başlıklı Notlar bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="55c35-122">To construct, see NOTES section for DISTRIBUTE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c35-123">-Imagetemplatename</span><span class="sxs-lookup"><span data-stu-id="55c35-123">-ImageTemplateName</span></span>
<span data-ttu-id="55c35-124">Resim şablonunun adı.</span><span class="sxs-lookup"><span data-stu-id="55c35-124">The name of the image Template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c35-125">-Lastrunstatusbitişsaati</span><span class="sxs-lookup"><span data-stu-id="55c35-125">-LastRunStatusEndTime</span></span>
<span data-ttu-id="55c35-126">Son çalıştırmanın bitiş saati (UTC).</span><span class="sxs-lookup"><span data-stu-id="55c35-126">End time of the last run (UTC).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c35-127">-LastRunStatusMessage</span><span class="sxs-lookup"><span data-stu-id="55c35-127">-LastRunStatusMessage</span></span>
<span data-ttu-id="55c35-128">Son çalışma durumuyla ilgili ayrıntılı bilgi.</span><span class="sxs-lookup"><span data-stu-id="55c35-128">Verbose information about the last run state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c35-129">-Lastrundurumtümü</span><span class="sxs-lookup"><span data-stu-id="55c35-129">-LastRunStatusRunState</span></span>
<span data-ttu-id="55c35-130">Son çalıştırmanın durumu.</span><span class="sxs-lookup"><span data-stu-id="55c35-130">State of the last run.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.RunState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c35-131">-LastRunStatusRunSubState</span><span class="sxs-lookup"><span data-stu-id="55c35-131">-LastRunStatusRunSubState</span></span>
<span data-ttu-id="55c35-132">Son çalıştırmanın alt durumu.</span><span class="sxs-lookup"><span data-stu-id="55c35-132">Sub-state of the last run.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.RunSubState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c35-133">-Lastrundurumbaşlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="55c35-133">-LastRunStatusStartTime</span></span>
<span data-ttu-id="55c35-134">Son çalıştırmanın başlangıç saati (UTC).</span><span class="sxs-lookup"><span data-stu-id="55c35-134">Start time of the last run (UTC).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c35-135">-Konum</span><span class="sxs-lookup"><span data-stu-id="55c35-135">-Location</span></span>
<span data-ttu-id="55c35-136">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="55c35-136">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c35-137">-NoWait</span><span class="sxs-lookup"><span data-stu-id="55c35-137">-NoWait</span></span>
<span data-ttu-id="55c35-138">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="55c35-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="55c35-139">-ProvisioningErrorCode</span><span class="sxs-lookup"><span data-stu-id="55c35-139">-ProvisioningErrorCode</span></span>
<span data-ttu-id="55c35-140">Hazırlama hatasının hata kodu.</span><span class="sxs-lookup"><span data-stu-id="55c35-140">Error code of the provisioning failure.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.ProvisioningErrorCode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c35-141">-ProvisioningErrorMessage</span><span class="sxs-lookup"><span data-stu-id="55c35-141">-ProvisioningErrorMessage</span></span>
<span data-ttu-id="55c35-142">Hazırlama hatası hakkında ayrıntılı hata iletisi.</span><span class="sxs-lookup"><span data-stu-id="55c35-142">Verbose error message about the provisioning failure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c35-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55c35-143">-ResourceGroupName</span></span>
<span data-ttu-id="55c35-144">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="55c35-144">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c35-145">-Kaynak</span><span class="sxs-lookup"><span data-stu-id="55c35-145">-Source</span></span>
<span data-ttu-id="55c35-146">Oluşturmak, özelleştirmek ve dağıtmak için sanal makine görüntü kaynağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="55c35-146">Describes a virtual machine image source for building, customizing and distributing.</span></span>
<span data-ttu-id="55c35-147">Oluşturmak için, kaynak özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="55c35-147">To construct, see NOTES section for SOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c35-148">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="55c35-148">-SubscriptionId</span></span>
<span data-ttu-id="55c35-149">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="55c35-149">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c35-150">Etiketli</span><span class="sxs-lookup"><span data-stu-id="55c35-150">-Tag</span></span>
<span data-ttu-id="55c35-151">Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="55c35-151">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c35-152">-Useratandidentityıd</span><span class="sxs-lookup"><span data-stu-id="55c35-152">-UserAssignedIdentityId</span></span>
<span data-ttu-id="55c35-153">Kullanıcının atadığı kimlik.</span><span class="sxs-lookup"><span data-stu-id="55c35-153">The id of user assigned identity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c35-154">-VMProfileOsdiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="55c35-154">-VMProfileOsdiskSizeInGb</span></span>
<span data-ttu-id="55c35-155">GB cinsinden işletim sistemi diskinin boyutu.</span><span class="sxs-lookup"><span data-stu-id="55c35-155">Size of the OS disk in GB.</span></span>
<span data-ttu-id="55c35-156">Azure 'un varsayılan işletim sistemi disk boyutunu kullanmak için 0 değerini atlayın veya belirtin.</span><span class="sxs-lookup"><span data-stu-id="55c35-156">Omit or specify 0 to use Azure's default OS disk size.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c35-157">-VMProfileVmSize</span><span class="sxs-lookup"><span data-stu-id="55c35-157">-VMProfileVmSize</span></span>
<span data-ttu-id="55c35-158">Görüntü oluşturmak, özelleştirmek ve yakalamak için kullanılan sanal makinenin boyutu.</span><span class="sxs-lookup"><span data-stu-id="55c35-158">Size of the virtual machine used to build, customize and capture images.</span></span>
<span data-ttu-id="55c35-159">Varsayılanı (Standard_D1_v2) kullanmak için boş dize atlayın veya belirtin.</span><span class="sxs-lookup"><span data-stu-id="55c35-159">Omit or specify empty string to use the default (Standard_D1_v2).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c35-160">-VnetConfigSubnetId</span><span class="sxs-lookup"><span data-stu-id="55c35-160">-VnetConfigSubnetId</span></span>
<span data-ttu-id="55c35-161">Önceden var olan bir alt ağın kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="55c35-161">Resource id of a pre-existing subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c35-162">-Onay</span><span class="sxs-lookup"><span data-stu-id="55c35-162">-Confirm</span></span>
<span data-ttu-id="55c35-163">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="55c35-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55c35-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55c35-164">-WhatIf</span></span>
<span data-ttu-id="55c35-165">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="55c35-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55c35-166">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="55c35-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55c35-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55c35-167">CommonParameters</span></span>
<span data-ttu-id="55c35-168">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55c35-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55c35-169">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="55c35-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55c35-170">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55c35-170">INPUTS</span></span>

## <span data-ttu-id="55c35-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55c35-171">OUTPUTS</span></span>

### <span data-ttu-id="55c35-172">Microsoft. Azure. PowerShell. cmdlet. ımagebuilder. modeller. Api20200214. ıımagetemplate</span><span class="sxs-lookup"><span data-stu-id="55c35-172">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="55c35-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55c35-173">NOTES</span></span>

<span data-ttu-id="55c35-174">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="55c35-174">ALIASES</span></span>

<span data-ttu-id="55c35-175">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="55c35-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="55c35-176">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="55c35-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="55c35-177">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="55c35-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="55c35-178"><ıımagetemplateözelleştirici [] >: resim kaynağı gibi resmin özelleştirme adımlarını açıklamak için kullanılan özellikleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="55c35-178">CUSTOMIZE <IImageTemplateCustomizer[]>: Specifies the properties used to describe the customization steps of the image, like Image source etc.</span></span>
  - <span data-ttu-id="55c35-179">`Type <String>`: Görüntüde kullanmak istediğiniz özelleştirme aracı türü.</span><span class="sxs-lookup"><span data-stu-id="55c35-179">`Type <String>`: The type of customization tool you want to use on the Image.</span></span> <span data-ttu-id="55c35-180">Örneğin, "Shell" kabuk Özelleştirici olabilir</span><span class="sxs-lookup"><span data-stu-id="55c35-180">For example, "Shell" can be shell customizer</span></span>
  - <span data-ttu-id="55c35-181">`[Name <String>]`: Bu özelleştirme adımında bağlam sağlamak için kolay ad</span><span class="sxs-lookup"><span data-stu-id="55c35-181">`[Name <String>]`: Friendly Name to provide context on what this customization step does</span></span>

<span data-ttu-id="55c35-182"><ıımagetemplatedağıtıcıyı DAĞıTMA [] >: resim çıkışının gideceği dağıtım hedefleri.</span><span class="sxs-lookup"><span data-stu-id="55c35-182">DISTRIBUTE <IImageTemplateDistributor[]>: The distribution targets where the image output needs to go to.</span></span>
  - <span data-ttu-id="55c35-183">`RunOutputName <String>`: İlişkili RunOutput için kullanılacak ad.</span><span class="sxs-lookup"><span data-stu-id="55c35-183">`RunOutputName <String>`: The name to be used for the associated RunOutput.</span></span>
  - <span data-ttu-id="55c35-184">`Type <String>`: Dağıtım türü.</span><span class="sxs-lookup"><span data-stu-id="55c35-184">`Type <String>`: Type of distribution.</span></span>
  - <span data-ttu-id="55c35-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Dağıtıcı tarafından oluşturulduktan/güncelleştirildikten sonra yapıya uygulanacak Etiketler.</span><span class="sxs-lookup"><span data-stu-id="55c35-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>
    - <span data-ttu-id="55c35-186">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="55c35-186">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="55c35-187">KAYNAK <IImageTemplateSource> : oluşturmak, özelleştirmek ve dağıtmak için sanal makine görüntü kaynağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="55c35-187">SOURCE <IImageTemplateSource>: Describes a virtual machine image source for building, customizing and distributing.</span></span>
  - <span data-ttu-id="55c35-188">`Type <String>`: Başlamak istediğiniz kaynak görüntünün türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="55c35-188">`Type <String>`: Specifies the type of source image you want to start with.</span></span>

## <span data-ttu-id="55c35-189">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55c35-189">RELATED LINKS</span></span>

