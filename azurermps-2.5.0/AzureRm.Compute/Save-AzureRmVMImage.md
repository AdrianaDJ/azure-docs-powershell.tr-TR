---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/save-azurermvmimage
schema: 2.0.0
ms.openlocfilehash: b781023b424dd23d3d0874893b724744ecb33bda
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940177"
---
# <span data-ttu-id="fed30-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="fed30-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="fed30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fed30-102">SYNOPSIS</span></span>
<span data-ttu-id="fed30-103">Sanal makineyi Vmımage olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="fed30-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fed30-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fed30-104">SYNTAX</span></span>

### <span data-ttu-id="fed30-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fed30-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fed30-106">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="fed30-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fed30-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fed30-107">DESCRIPTION</span></span>
<span data-ttu-id="fed30-108">**Save-Azurermvmımage** cmdlet 'i bir sanal makineyi bir vmımage olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="fed30-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="fed30-109">Sanal makine yansıması oluşturmadan önce, sanal makine Sysprep 'i, ardından Set-AzureRmVM cmdlet 'ini kullanarak Genelleştirilmiş olarak işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="fed30-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>

<span data-ttu-id="fed30-110">Bu cmdlet 'in çıktısı JavaScript nesne gösterimi (JSON) şablonudur.</span><span class="sxs-lookup"><span data-stu-id="fed30-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="fed30-111">Yakalanan telefonunuzdan sanal makineler dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fed30-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="fed30-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fed30-112">EXAMPLES</span></span>

### <span data-ttu-id="fed30-113">Örnek 1: sanal makine yakalama</span><span class="sxs-lookup"><span data-stu-id="fed30-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="fed30-114">İlk komut VirtualMachine07 adındaki sanal makineyi genelleþtirilmiþ olarak işaretler.</span><span class="sxs-lookup"><span data-stu-id="fed30-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="fed30-115">İkinci komut, Vmımage olarak VirtualMachine07 adındaki sanal makineyi yakalar.</span><span class="sxs-lookup"><span data-stu-id="fed30-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="fed30-116">**Output** ÖZELLIĞI bir JSON şablonu döndürür.</span><span class="sxs-lookup"><span data-stu-id="fed30-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="fed30-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fed30-117">PARAMETERS</span></span>

### <span data-ttu-id="fed30-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="fed30-118">-AsJob</span></span>
<span data-ttu-id="fed30-119">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="fed30-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fed30-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fed30-120">-DefaultProfile</span></span>
<span data-ttu-id="fed30-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fed30-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fed30-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="fed30-122">-DestinationContainerName</span></span>
<span data-ttu-id="fed30-123">"Sistem" kapsayıcısı içinde resimlerinizi tutmak istediğiniz kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fed30-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="fed30-124">Konteyner yoksa, sizin için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="fed30-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="fed30-125">Vmımage 'ı oluşturan sanal sabit diskler (VHD) Bu parametrenin belirttiği kapsayıcıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="fed30-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="fed30-126">VHD 'ler birden çok depolama hesabına yayılmışsa, bu cmdlet her depolama hesabında bu ada sahip bir kapsayıcı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fed30-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="fed30-127">Kaydedilen görüntünün URL 'SI şuna benzer:</span><span class="sxs-lookup"><span data-stu-id="fed30-127">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="fed30-128"> https:// \<storageAccountName\> . blob.Core.Windows.NET/System/Microsoft.COMPUTE/Images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. vhd.</span><span class="sxs-lookup"><span data-stu-id="fed30-128">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="fed30-129">-ID</span><span class="sxs-lookup"><span data-stu-id="fed30-129">-Id</span></span>
<span data-ttu-id="fed30-130">Sanal makinenin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fed30-130">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="fed30-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="fed30-131">-Name</span></span>
<span data-ttu-id="fed30-132">Bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="fed30-132">Specifies a name.</span></span>

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

### <span data-ttu-id="fed30-133">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="fed30-133">-Overwrite</span></span>
<span data-ttu-id="fed30-134">Bu cmdlet 'in hedef kapsayıcıda aynı öneke sahip olan tüm VHD 'Lerin üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="fed30-134">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="fed30-135">-Yol</span><span class="sxs-lookup"><span data-stu-id="fed30-135">-Path</span></span>
<span data-ttu-id="fed30-136">VHD 'nin yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="fed30-136">Specifies the path of the VHD.</span></span>

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

### <span data-ttu-id="fed30-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fed30-137">-ResourceGroupName</span></span>
<span data-ttu-id="fed30-138">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fed30-138">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="fed30-139">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="fed30-139">-VHDNamePrefix</span></span>
<span data-ttu-id="fed30-140">Vmımage 'ın depolama profilini oluşturan blobın adındaki öneki belirtir.</span><span class="sxs-lookup"><span data-stu-id="fed30-140">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="fed30-141">Örneğin, işletim sistemi diskinin önek Vhdi öneki, ad Vhdönek-OSDisk ile sonuçlanır. \<guid\> . sahip.</span><span class="sxs-lookup"><span data-stu-id="fed30-141">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="fed30-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fed30-142">CommonParameters</span></span>
<span data-ttu-id="fed30-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fed30-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fed30-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fed30-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fed30-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fed30-145">INPUTS</span></span>

### <span data-ttu-id="fed30-146">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="fed30-146">None</span></span>
<span data-ttu-id="fed30-147">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="fed30-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fed30-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fed30-148">OUTPUTS</span></span>

### <span data-ttu-id="fed30-149">Microsoft. Azure. Commands. COMPUTE. modeller. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="fed30-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="fed30-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fed30-150">NOTES</span></span>

## <span data-ttu-id="fed30-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fed30-151">RELATED LINKS</span></span>

[<span data-ttu-id="fed30-152">Get-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="fed30-152">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="fed30-153">Get-Azurermvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="fed30-153">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="fed30-154">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="fed30-154">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="fed30-155">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="fed30-155">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="fed30-156">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fed30-156">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)


