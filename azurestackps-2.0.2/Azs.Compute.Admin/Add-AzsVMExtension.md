---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/add-azsvmextension
schema: 2.0.0
ms.openlocfilehash: a9c5a207d478fe40181150206990cb47ad4e45d5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106929"
---
# <span data-ttu-id="a7110-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="a7110-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="a7110-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7110-102">SYNOPSIS</span></span>
<span data-ttu-id="a7110-103">Publisher sürümü ile sanal makine uzantısı görüntüsü oluşturma.</span><span class="sxs-lookup"><span data-stu-id="a7110-103">Create a Virtual Machine Extension Image with publisher, version.</span></span>

## <span data-ttu-id="a7110-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7110-104">SYNTAX</span></span>

### <span data-ttu-id="a7110-105">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a7110-105">CreateExpanded (Default)</span></span>
```
Add-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-ComputeRole <String>] [-IsSystemExtension] [-PropertiesPublisher <String>]
 [-ProvisioningState <ProvisioningState>] [-SourceBlob <String>] [-SupportMultipleExtensions]
 [-VmOsType <OSType>] [-VMScaleSetEnabled] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a7110-106">Oluturmak</span><span class="sxs-lookup"><span data-stu-id="a7110-106">Create</span></span>
```
Add-AzsVMExtension -Publisher <String> -Type <String> -Version <String> -Extension <IVMExtensionParameters>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a7110-107">Createviaıdentity</span><span class="sxs-lookup"><span data-stu-id="a7110-107">CreateViaIdentity</span></span>
```
Add-AzsVMExtension -InputObject <IComputeAdminIdentity> -Extension <IVMExtensionParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a7110-108">Createviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="a7110-108">CreateViaIdentityExpanded</span></span>
```
Add-AzsVMExtension -InputObject <IComputeAdminIdentity> [-Publisher <String>] [-ComputeRole <String>]
 [-IsSystemExtension] [-ProvisioningState <ProvisioningState>] [-SourceBlob <String>]
 [-SupportMultipleExtensions] [-VmOsType <OSType>] [-VMScaleSetEnabled] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a7110-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7110-109">DESCRIPTION</span></span>
<span data-ttu-id="a7110-110">Publisher sürümü ile sanal makine uzantısı görüntüsü oluşturma.</span><span class="sxs-lookup"><span data-stu-id="a7110-110">Create a Virtual Machine Extension Image with publisher, version.</span></span>

## <span data-ttu-id="a7110-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7110-111">EXAMPLES</span></span>

### <span data-ttu-id="a7110-112">Örnek 1: Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="a7110-112">Example 1: Add-AzsVMExtension</span></span>
```powershell
PS C:\> Add-AzsVMExtension -Location "local" -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"

ExtensionType            : MicroExtension
TypeHandlerVersion       : 0.1.0
ComputeRole              : IaaS
Id                       : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locati
                           ons/local/artifactTypes/VMExtension/publishers/Microsoft/types/MicroExtension/versions/0.1.0
IsSystemExtension        : False
Location                 : local
Name                     :
ProvisioningState        : Creating
Publisher                : Microsoft
SourceBlobUri            : https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip
SupportMultipleExtension : True
Type                     : Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions
VMScaleSetEnabled        : False
VmosType                 : Linux
```

<span data-ttu-id="a7110-113">Uzantının konumunu veya URI 'yi SasUri kullanarak Azure Blob 'a sağlamak için genel olarak erişilebilir bir bağlantı kullanın.</span><span class="sxs-lookup"><span data-stu-id="a7110-113">Use a publicly accessible link to provide the location of the extension, or the URI to an Azure Blob using the SasUri.</span></span>

## <span data-ttu-id="a7110-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7110-114">PARAMETERS</span></span>

### <span data-ttu-id="a7110-115">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="a7110-115">-ComputeRole</span></span>
<span data-ttu-id="a7110-116">Compute role</span><span class="sxs-lookup"><span data-stu-id="a7110-116">Compute role</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a7110-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7110-117">-DefaultProfile</span></span>
<span data-ttu-id="a7110-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a7110-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7110-119">Uzantılı</span><span class="sxs-lookup"><span data-stu-id="a7110-119">-Extension</span></span>
<span data-ttu-id="a7110-120">Yeni sanal makine uzantısı görüntüsü oluşturmak için kullanılan parametreler.</span><span class="sxs-lookup"><span data-stu-id="a7110-120">Parameters used to create a new Virtual Machine Extension Image.</span></span>
<span data-ttu-id="a7110-121">Oluşturmak için, UZANTı özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a7110-121">To construct, see NOTES section for EXTENSION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtensionParameters
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a7110-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7110-122">-InputObject</span></span>
<span data-ttu-id="a7110-123">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a7110-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a7110-124">-Ispsystegeri</span><span class="sxs-lookup"><span data-stu-id="a7110-124">-IsSystemExtension</span></span>
<span data-ttu-id="a7110-125">Uzantının sistem için olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a7110-125">Indicates if the extension is for the system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a7110-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="a7110-126">-Location</span></span>
<span data-ttu-id="a7110-127">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="a7110-127">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a7110-128">-PropertiesPublisher</span><span class="sxs-lookup"><span data-stu-id="a7110-128">-PropertiesPublisher</span></span>
<span data-ttu-id="a7110-129">VM uzantısının yayıncısı</span><span class="sxs-lookup"><span data-stu-id="a7110-129">The publisher of the VM Extension</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a7110-130">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="a7110-130">-ProvisioningState</span></span>
<span data-ttu-id="a7110-131">Uzantının sağlama durumu.</span><span class="sxs-lookup"><span data-stu-id="a7110-131">Provisioning state of extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a7110-132">-Publisher</span><span class="sxs-lookup"><span data-stu-id="a7110-132">-Publisher</span></span>
<span data-ttu-id="a7110-133">Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="a7110-133">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a7110-134">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="a7110-134">-SourceBlob</span></span>
<span data-ttu-id="a7110-135">Azure veya AzureStack blob.</span><span class="sxs-lookup"><span data-stu-id="a7110-135">URI to Azure or AzureStack blob.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a7110-136">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="a7110-136">-SubscriptionId</span></span>
<span data-ttu-id="a7110-137">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="a7110-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a7110-138">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a7110-138">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a7110-139">-Supportçoğuluzantıları</span><span class="sxs-lookup"><span data-stu-id="a7110-139">-SupportMultipleExtensions</span></span>
<span data-ttu-id="a7110-140">Birden çok uzantı destekliyorsa doğru.</span><span class="sxs-lookup"><span data-stu-id="a7110-140">True if supports multiple extensions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a7110-141">-Tür</span><span class="sxs-lookup"><span data-stu-id="a7110-141">-Type</span></span>
<span data-ttu-id="a7110-142">Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="a7110-142">Type of extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a7110-143">-Version</span><span class="sxs-lookup"><span data-stu-id="a7110-143">-Version</span></span>
<span data-ttu-id="a7110-144">Kaynağın sürümü.</span><span class="sxs-lookup"><span data-stu-id="a7110-144">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a7110-145">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="a7110-145">-VmOsType</span></span>
<span data-ttu-id="a7110-146">Uzantı işleyicisini dağıtmak için gereken hedef sanal makine işletim sistemi türü.</span><span class="sxs-lookup"><span data-stu-id="a7110-146">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.OSType
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a7110-147">-VMScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="a7110-147">-VMScaleSetEnabled</span></span>
<span data-ttu-id="a7110-148">Uzantının sanal makine ölçek kümesi desteği için etkinleştirilip etkinleştirilmediğini gösteren değer.</span><span class="sxs-lookup"><span data-stu-id="a7110-148">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a7110-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="a7110-149">-Confirm</span></span>
<span data-ttu-id="a7110-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a7110-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7110-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7110-151">-WhatIf</span></span>
<span data-ttu-id="a7110-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a7110-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7110-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a7110-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7110-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7110-154">CommonParameters</span></span>
<span data-ttu-id="a7110-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7110-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7110-156">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a7110-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7110-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7110-157">INPUTS</span></span>

### <span data-ttu-id="a7110-158">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. Api20151201Preview. ımextensionparameters</span><span class="sxs-lookup"><span data-stu-id="a7110-158">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtensionParameters</span></span>

### <span data-ttu-id="a7110-159">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. ıuteadminıdentity</span><span class="sxs-lookup"><span data-stu-id="a7110-159">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="a7110-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7110-160">OUTPUTS</span></span>

### <span data-ttu-id="a7110-161">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. Api20151201Preview.</span><span class="sxs-lookup"><span data-stu-id="a7110-161">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtension</span></span>



## <span data-ttu-id="a7110-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7110-162">NOTES</span></span>

<span data-ttu-id="a7110-163">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a7110-163">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a7110-164">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a7110-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a7110-165">UZANTı <IVMExtensionParameters> : yeni bir sanal makine uzantısı görüntüsü oluşturmak için kullanılan parametreler.</span><span class="sxs-lookup"><span data-stu-id="a7110-165">EXTENSION <IVMExtensionParameters>: Parameters used to create a new Virtual Machine Extension Image.</span></span>
  - <span data-ttu-id="a7110-166">`[ComputeRole <String>]`: Rol hesaplama</span><span class="sxs-lookup"><span data-stu-id="a7110-166">`[ComputeRole <String>]`: Compute role</span></span>
  - <span data-ttu-id="a7110-167">`[IsSystemExtension <Boolean?>]`: Uzantının sistem için olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a7110-167">`[IsSystemExtension <Boolean?>]`: Indicates if the extension is for the system.</span></span>
  - <span data-ttu-id="a7110-168">`[ProvisioningState <ProvisioningState?>]`: Uzantının sağlama durumu.</span><span class="sxs-lookup"><span data-stu-id="a7110-168">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of extension.</span></span>
  - <span data-ttu-id="a7110-169">`[Publisher <String>]`: VM uzantısının yayıncısı</span><span class="sxs-lookup"><span data-stu-id="a7110-169">`[Publisher <String>]`: The publisher of the VM Extension</span></span>
  - <span data-ttu-id="a7110-170">`[SourceBlobUri <String>]`: Azure veya AzureStack blob 'a URI.</span><span class="sxs-lookup"><span data-stu-id="a7110-170">`[SourceBlobUri <String>]`: URI to Azure or AzureStack blob.</span></span>
  - <span data-ttu-id="a7110-171">`[SupportMultipleExtension <Boolean?>]`: Birden çok uzantı destekliyorsa doğru.</span><span class="sxs-lookup"><span data-stu-id="a7110-171">`[SupportMultipleExtension <Boolean?>]`: True if supports multiple extensions.</span></span>
  - <span data-ttu-id="a7110-172">`[VMScaleSetEnabled <Boolean?>]`: Uzantının sanal makine ölçek kümesi desteği için etkinleştirilip etkinleştirilmediğini gösteren değer.</span><span class="sxs-lookup"><span data-stu-id="a7110-172">`[VMScaleSetEnabled <Boolean?>]`: Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>
  - <span data-ttu-id="a7110-173">`[VmosType <OSType?>]`: Uzantı işleyicisini dağıtmak için gereken hedef sanal makine işletim sistemi türü.</span><span class="sxs-lookup"><span data-stu-id="a7110-173">`[VmosType <OSType?>]`: Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

<span data-ttu-id="a7110-174">INPUTOBJECT <IComputeAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="a7110-174">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a7110-175">`[DiskId <String>]`: Kimlik olarak disk Guid 'si.</span><span class="sxs-lookup"><span data-stu-id="a7110-175">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="a7110-176">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="a7110-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a7110-177">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="a7110-177">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="a7110-178">`[MigrationId <String>]`: Geçiş işi GUID adı.</span><span class="sxs-lookup"><span data-stu-id="a7110-178">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="a7110-179">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="a7110-179">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="a7110-180">`[Publisher <String>]`: Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="a7110-180">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="a7110-181">`[QuotaName <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="a7110-181">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="a7110-182">`[Sku <String>]`: SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="a7110-182">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="a7110-183">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="a7110-183">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a7110-184">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a7110-184">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a7110-185">`[Type <String>]`: Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="a7110-185">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="a7110-186">`[Version <String>]`: Kaynağın sürümü.</span><span class="sxs-lookup"><span data-stu-id="a7110-186">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="a7110-187">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7110-187">RELATED LINKS</span></span>

