---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: b01f8d356d83cb111441cf911750056033422fe8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936880"
---
# <span data-ttu-id="cdbbb-101">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="cdbbb-101">Save-AzVMImage</span></span>

## <span data-ttu-id="cdbbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdbbb-102">SYNOPSIS</span></span>
<span data-ttu-id="cdbbb-103">Sanal makineyi Vmımage olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-103">Saves a virtual machine as a VMImage.</span></span>

## <span data-ttu-id="cdbbb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cdbbb-104">SYNTAX</span></span>

### <span data-ttu-id="cdbbb-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cdbbb-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdbbb-106">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="cdbbb-106">IdParameterSetName</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cdbbb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cdbbb-107">DESCRIPTION</span></span>
<span data-ttu-id="cdbbb-108">**Save-AzVMImage** cmdlet 'i bir sanal makineyi vmımage olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-108">The **Save-AzVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="cdbbb-109">Sanal makine yansıması oluşturmadan önce, sanal makine Sysprep 'i, ardından Set-AzVM cmdlet 'ini kullanarak Genelleştirilmiş olarak işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzVM cmdlet.</span></span>

<span data-ttu-id="cdbbb-110">Bu cmdlet 'in çıktısı JavaScript nesne gösterimi (JSON) şablonudur.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="cdbbb-111">Yakalanan telefonunuzdan sanal makineler dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="cdbbb-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cdbbb-112">EXAMPLES</span></span>

### <span data-ttu-id="cdbbb-113">Örnek 1: sanal makine yakalama</span><span class="sxs-lookup"><span data-stu-id="cdbbb-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="cdbbb-114">İlk komut VirtualMachine07 adındaki sanal makineyi genelleþtirilmiþ olarak işaretler.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="cdbbb-115">İkinci komut, Vmımage olarak VirtualMachine07 adındaki sanal makineyi yakalar.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="cdbbb-116">**Output** ÖZELLIĞI bir JSON şablonu döndürür.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="cdbbb-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cdbbb-117">PARAMETERS</span></span>

### <span data-ttu-id="cdbbb-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="cdbbb-118">-AsJob</span></span>
<span data-ttu-id="cdbbb-119">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-119">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdbbb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdbbb-120">-DefaultProfile</span></span>
<span data-ttu-id="cdbbb-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdbbb-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="cdbbb-122">-DestinationContainerName</span></span>
<span data-ttu-id="cdbbb-123">"Sistem" kapsayıcısı içinde resimlerinizi tutmak istediğiniz kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="cdbbb-124">Konteyner yoksa, sizin için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="cdbbb-125">Vmımage 'ı oluşturan sanal sabit diskler (VHD) Bu parametrenin belirttiği kapsayıcıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="cdbbb-126">VHD 'ler birden çok depolama hesabına yayılmışsa, bu cmdlet her depolama hesabında bu ada sahip bir kapsayıcı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="cdbbb-127">Kaydedilen görüntünün URL 'SI şuna benzer:</span><span class="sxs-lookup"><span data-stu-id="cdbbb-127">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="cdbbb-128"> https:// \< storageAccountName \> . blob.Core.Windows.NET/System/Microsoft.COMPUTE/Images/ \< ımacontainer \> / \< vhdprefix-OSDisk \> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. vhd.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-128">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdbbb-129">-ID</span><span class="sxs-lookup"><span data-stu-id="cdbbb-129">-Id</span></span>
<span data-ttu-id="cdbbb-130">Sanal makinenin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-130">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdbbb-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="cdbbb-131">-Name</span></span>
<span data-ttu-id="cdbbb-132">Bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-132">Specifies a name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdbbb-133">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="cdbbb-133">-Overwrite</span></span>
<span data-ttu-id="cdbbb-134">Bu cmdlet 'in hedef kapsayıcıda aynı öneke sahip olan tüm VHD 'Lerin üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-134">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdbbb-135">-Yol</span><span class="sxs-lookup"><span data-stu-id="cdbbb-135">-Path</span></span>
<span data-ttu-id="cdbbb-136">VHD 'nin yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-136">Specifies the path of the VHD.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdbbb-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdbbb-137">-ResourceGroupName</span></span>
<span data-ttu-id="cdbbb-138">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-138">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdbbb-139">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="cdbbb-139">-VHDNamePrefix</span></span>
<span data-ttu-id="cdbbb-140">Vmımage 'ın depolama profilini oluşturan blobın adındaki öneki belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-140">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="cdbbb-141">Örneğin, işletim sistemi diskinin önek Vhdi öneki, ad Vhdönek-OSDisk ile sonuçlanır. \< Guid \> . vhd.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-141">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdbbb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdbbb-142">CommonParameters</span></span>
<span data-ttu-id="cdbbb-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdbbb-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdbbb-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdbbb-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cdbbb-145">INPUTS</span></span>

### <span data-ttu-id="cdbbb-146">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cdbbb-146">None</span></span>
<span data-ttu-id="cdbbb-147">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="cdbbb-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cdbbb-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cdbbb-148">OUTPUTS</span></span>

### <span data-ttu-id="cdbbb-149">Microsoft. Azure. Commands. COMPUTE. modeller. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="cdbbb-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="cdbbb-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cdbbb-150">NOTES</span></span>

## <span data-ttu-id="cdbbb-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cdbbb-151">RELATED LINKS</span></span>

[<span data-ttu-id="cdbbb-152">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="cdbbb-152">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="cdbbb-153">Get-Azvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="cdbbb-153">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="cdbbb-154">Get-Azvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="cdbbb-154">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="cdbbb-155">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="cdbbb-155">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="cdbbb-156">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="cdbbb-156">Set-AzVM</span></span>](./Set-AzVM.md)


