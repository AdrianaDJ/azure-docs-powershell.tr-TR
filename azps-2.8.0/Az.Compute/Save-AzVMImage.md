---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: 6ce551cb848a1f63129353aee8a388fb19cb8bfd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752739"
---
# <span data-ttu-id="f04be-101">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="f04be-101">Save-AzVMImage</span></span>

## <span data-ttu-id="f04be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f04be-102">SYNOPSIS</span></span>
<span data-ttu-id="f04be-103">Sanal makineyi Vmımage olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="f04be-103">Saves a virtual machine as a VMImage.</span></span>

## <span data-ttu-id="f04be-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f04be-104">SYNTAX</span></span>

### <span data-ttu-id="f04be-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f04be-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f04be-106">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="f04be-106">IdParameterSetName</span></span>
```
Save-AzVMImage [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite] [[-Path] <String>]
 [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f04be-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f04be-107">DESCRIPTION</span></span>
<span data-ttu-id="f04be-108">**Save-AzVMImage** cmdlet 'i bir sanal makineyi vmımage olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="f04be-108">The **Save-AzVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="f04be-109">Sanal makine yansıması oluşturmadan önce, sanal makine Sysprep 'i, ardından Set-AzVM cmdlet 'ini kullanarak Genelleştirilmiş olarak işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f04be-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzVM cmdlet.</span></span>
<span data-ttu-id="f04be-110">Bu cmdlet 'in çıktısı JavaScript nesne gösterimi (JSON) şablonudur.</span><span class="sxs-lookup"><span data-stu-id="f04be-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="f04be-111">Yakalanan telefonunuzdan sanal makineler dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f04be-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="f04be-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f04be-112">EXAMPLES</span></span>

### <span data-ttu-id="f04be-113">Örnek 1: sanal makine yakalama</span><span class="sxs-lookup"><span data-stu-id="f04be-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="f04be-114">İlk komut VirtualMachine07 adındaki sanal makineyi genelleþtirilmiþ olarak işaretler.</span><span class="sxs-lookup"><span data-stu-id="f04be-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>
<span data-ttu-id="f04be-115">İkinci komut, Vmımage olarak VirtualMachine07 adındaki sanal makineyi yakalar.</span><span class="sxs-lookup"><span data-stu-id="f04be-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="f04be-116">**Output** ÖZELLIĞI bir JSON şablonu döndürür.</span><span class="sxs-lookup"><span data-stu-id="f04be-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="f04be-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f04be-117">PARAMETERS</span></span>

### <span data-ttu-id="f04be-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="f04be-118">-AsJob</span></span>
<span data-ttu-id="f04be-119">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="f04be-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f04be-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f04be-120">-DefaultProfile</span></span>
<span data-ttu-id="f04be-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f04be-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04be-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="f04be-122">-DestinationContainerName</span></span>
<span data-ttu-id="f04be-123">"Sistem" kapsayıcısı içinde resimlerinizi tutmak istediğiniz kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f04be-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>
<span data-ttu-id="f04be-124">Konteyner yoksa, sizin için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f04be-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="f04be-125">Vmımage 'ı oluşturan sanal sabit diskler (VHD) Bu parametrenin belirttiği kapsayıcıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="f04be-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="f04be-126">VHD 'ler birden çok depolama hesabına yayılmışsa, bu cmdlet her depolama hesabında bu ada sahip bir kapsayıcı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f04be-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="f04be-127">Kaydedilen görüntünün URL 'si: https:// \< storageAccountName \> . blob.Core.Windows.NET/System/Microsoft.COMPUTE/Images/ \< ımacontainer \> / \< vhdprefix-OSDisk \> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. vhd.</span><span class="sxs-lookup"><span data-stu-id="f04be-127">The URL of the saved image is similar to: https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f04be-128">-ID</span><span class="sxs-lookup"><span data-stu-id="f04be-128">-Id</span></span>
<span data-ttu-id="f04be-129">Sanal makinenin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f04be-129">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f04be-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="f04be-130">-Name</span></span>
<span data-ttu-id="f04be-131">Bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="f04be-131">Specifies a name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f04be-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="f04be-132">-Overwrite</span></span>
<span data-ttu-id="f04be-133">Bu cmdlet 'in hedef kapsayıcıda aynı öneke sahip olan tüm VHD 'Lerin üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f04be-133">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f04be-134">-Yol</span><span class="sxs-lookup"><span data-stu-id="f04be-134">-Path</span></span>
<span data-ttu-id="f04be-135">Yakalanan resmin şablonunun depolandığı dosya yolu.</span><span class="sxs-lookup"><span data-stu-id="f04be-135">The file path in which the template of the captured image is stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f04be-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f04be-136">-ResourceGroupName</span></span>
<span data-ttu-id="f04be-137">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f04be-137">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f04be-138">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="f04be-138">-VHDNamePrefix</span></span>
<span data-ttu-id="f04be-139">Vmımage 'ın depolama profilini oluşturan blobın adındaki öneki belirtir.</span><span class="sxs-lookup"><span data-stu-id="f04be-139">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>
<span data-ttu-id="f04be-140">Örneğin, işletim sistemi diskinin önek Vhdi öneki, ad Vhdönek-OSDisk ile sonuçlanır. \< Guid \> . vhd.</span><span class="sxs-lookup"><span data-stu-id="f04be-140">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f04be-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f04be-141">CommonParameters</span></span>
<span data-ttu-id="f04be-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f04be-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f04be-143">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f04be-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f04be-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f04be-144">INPUTS</span></span>

### <span data-ttu-id="f04be-145">System. String</span><span class="sxs-lookup"><span data-stu-id="f04be-145">System.String</span></span>

### <span data-ttu-id="f04be-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f04be-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f04be-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f04be-147">OUTPUTS</span></span>

### <span data-ttu-id="f04be-148">Microsoft. Azure. Commands. COMPUTE. modeller. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="f04be-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="f04be-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f04be-149">NOTES</span></span>

## <span data-ttu-id="f04be-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f04be-150">RELATED LINKS</span></span>

[<span data-ttu-id="f04be-151">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="f04be-151">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="f04be-152">Get-Azvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="f04be-152">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="f04be-153">Get-Azvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="f04be-153">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="f04be-154">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="f04be-154">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="f04be-155">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="f04be-155">Set-AzVM</span></span>](./Set-AzVM.md)

