---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/save-azurermvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Save-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Save-AzureRmVMImage.md
ms.openlocfilehash: b6d8d21eea863683912e204403ebe5a75ac40fc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572885"
---
# <span data-ttu-id="7285d-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="7285d-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="7285d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7285d-102">SYNOPSIS</span></span>
<span data-ttu-id="7285d-103">Sanal makineyi Vmımage olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="7285d-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7285d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7285d-104">SYNTAX</span></span>

### <span data-ttu-id="7285d-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7285d-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7285d-106">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="7285d-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7285d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7285d-107">DESCRIPTION</span></span>
<span data-ttu-id="7285d-108">**Save-Azurermvmımage** cmdlet 'i bir sanal makineyi bir vmımage olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="7285d-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="7285d-109">Sanal makine yansıması oluşturmadan önce, sanal makine Sysprep 'i, ardından Set-AzureRmVM cmdlet 'ini kullanarak Genelleştirilmiş olarak işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="7285d-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="7285d-110">Bu cmdlet 'in çıktısı JavaScript nesne gösterimi (JSON) şablonudur.</span><span class="sxs-lookup"><span data-stu-id="7285d-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="7285d-111">Yakalanan telefonunuzdan sanal makineler dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7285d-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="7285d-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7285d-112">EXAMPLES</span></span>

### <span data-ttu-id="7285d-113">Örnek 1: sanal makine yakalama</span><span class="sxs-lookup"><span data-stu-id="7285d-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="7285d-114">İlk komut VirtualMachine07 adındaki sanal makineyi genelleþtirilmiþ olarak işaretler.</span><span class="sxs-lookup"><span data-stu-id="7285d-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>
<span data-ttu-id="7285d-115">İkinci komut, Vmımage olarak VirtualMachine07 adındaki sanal makineyi yakalar.</span><span class="sxs-lookup"><span data-stu-id="7285d-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="7285d-116">**Output** ÖZELLIĞI bir JSON şablonu döndürür.</span><span class="sxs-lookup"><span data-stu-id="7285d-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="7285d-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7285d-117">PARAMETERS</span></span>

### <span data-ttu-id="7285d-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="7285d-118">-AsJob</span></span>
<span data-ttu-id="7285d-119">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="7285d-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7285d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7285d-120">-DefaultProfile</span></span>
<span data-ttu-id="7285d-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7285d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7285d-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="7285d-122">-DestinationContainerName</span></span>
<span data-ttu-id="7285d-123">"Sistem" kapsayıcısı içinde resimlerinizi tutmak istediğiniz kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7285d-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>
<span data-ttu-id="7285d-124">Konteyner yoksa, sizin için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7285d-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="7285d-125">Vmımage 'ı oluşturan sanal sabit diskler (VHD) Bu parametrenin belirttiği kapsayıcıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="7285d-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="7285d-126">VHD 'ler birden çok depolama hesabına yayılmışsa, bu cmdlet her depolama hesabında bu ada sahip bir kapsayıcı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7285d-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="7285d-127">Kaydedilen görüntünün URL 'si: https:// \<storageAccountName\> . blob.Core.Windows.NET/System/Microsoft.COMPUTE/Images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. vhd.</span><span class="sxs-lookup"><span data-stu-id="7285d-127">The URL of the saved image is similar to: https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="7285d-128">-ID</span><span class="sxs-lookup"><span data-stu-id="7285d-128">-Id</span></span>
<span data-ttu-id="7285d-129">Sanal makinenin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7285d-129">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="7285d-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="7285d-130">-Name</span></span>
<span data-ttu-id="7285d-131">Bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="7285d-131">Specifies a name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7285d-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="7285d-132">-Overwrite</span></span>
<span data-ttu-id="7285d-133">Bu cmdlet 'in hedef kapsayıcıda aynı öneke sahip olan tüm VHD 'Lerin üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7285d-133">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="7285d-134">-Yol</span><span class="sxs-lookup"><span data-stu-id="7285d-134">-Path</span></span>
<span data-ttu-id="7285d-135">Yakalanan resmin şablonunun depolandığı dosya yolu.</span><span class="sxs-lookup"><span data-stu-id="7285d-135">The file path in which the template of the captured image is stored.</span></span>

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

### <span data-ttu-id="7285d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7285d-136">-ResourceGroupName</span></span>
<span data-ttu-id="7285d-137">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7285d-137">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7285d-138">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="7285d-138">-VHDNamePrefix</span></span>
<span data-ttu-id="7285d-139">Vmımage 'ın depolama profilini oluşturan blobın adındaki öneki belirtir.</span><span class="sxs-lookup"><span data-stu-id="7285d-139">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>
<span data-ttu-id="7285d-140">Örneğin, işletim sistemi diskinin önek Vhdi öneki, ad Vhdönek-OSDisk ile sonuçlanır. \<guid\> . sahip.</span><span class="sxs-lookup"><span data-stu-id="7285d-140">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="7285d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7285d-141">CommonParameters</span></span>
<span data-ttu-id="7285d-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7285d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7285d-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7285d-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7285d-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7285d-144">INPUTS</span></span>

### <span data-ttu-id="7285d-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7285d-145">System.String</span></span>

### <span data-ttu-id="7285d-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7285d-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7285d-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7285d-147">OUTPUTS</span></span>

### <span data-ttu-id="7285d-148">Microsoft. Azure. Commands. COMPUTE. modeller. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="7285d-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="7285d-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7285d-149">NOTES</span></span>

## <span data-ttu-id="7285d-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7285d-150">RELATED LINKS</span></span>

[<span data-ttu-id="7285d-151">Get-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="7285d-151">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="7285d-152">Get-Azurermvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="7285d-152">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="7285d-153">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="7285d-153">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="7285d-154">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="7285d-154">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="7285d-155">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7285d-155">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)


