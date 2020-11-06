---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
ms.openlocfilehash: cadcaccc2bb93dee5298ca92561c5bef36b5d9ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594773"
---
# <span data-ttu-id="5b762-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="5b762-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="5b762-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b762-102">SYNOPSIS</span></span>
<span data-ttu-id="5b762-103">Sanal makineyi Vmımage olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="5b762-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b762-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5b762-104">SYNTAX</span></span>

### <span data-ttu-id="5b762-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5b762-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b762-106">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="5b762-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b762-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b762-107">DESCRIPTION</span></span>
<span data-ttu-id="5b762-108">**Save-Azurermvmımage** cmdlet 'i bir sanal makineyi bir vmımage olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="5b762-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="5b762-109">Sanal makine yansıması oluşturmadan önce, sanal makine Sysprep 'i, ardından Set-AzureRmVM cmdlet 'ini kullanarak Genelleştirilmiş olarak işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="5b762-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>

<span data-ttu-id="5b762-110">Bu cmdlet 'in çıktısı JavaScript nesne gösterimi (JSON) şablonudur.</span><span class="sxs-lookup"><span data-stu-id="5b762-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="5b762-111">Yakalanan telefonunuzdan sanal makineler dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5b762-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="5b762-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5b762-112">EXAMPLES</span></span>

### <span data-ttu-id="5b762-113">Örnek 1: sanal makine yakalama</span><span class="sxs-lookup"><span data-stu-id="5b762-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="5b762-114">İlk komut VirtualMachine07 adındaki sanal makineyi genelleþtirilmiþ olarak işaretler.</span><span class="sxs-lookup"><span data-stu-id="5b762-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="5b762-115">İkinci komut, Vmımage olarak VirtualMachine07 adındaki sanal makineyi yakalar.</span><span class="sxs-lookup"><span data-stu-id="5b762-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="5b762-116">**Output** ÖZELLIĞI bir JSON şablonu döndürür.</span><span class="sxs-lookup"><span data-stu-id="5b762-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="5b762-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5b762-117">PARAMETERS</span></span>

### <span data-ttu-id="5b762-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b762-118">-DefaultProfile</span></span>
<span data-ttu-id="5b762-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5b762-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b762-120">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="5b762-120">-DestinationContainerName</span></span>
<span data-ttu-id="5b762-121">"Sistem" kapsayıcısı içinde resimlerinizi tutmak istediğiniz kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b762-121">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="5b762-122">Konteyner yoksa, sizin için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5b762-122">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="5b762-123">Vmımage 'ı oluşturan sanal sabit diskler (VHD) Bu parametrenin belirttiği kapsayıcıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="5b762-123">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="5b762-124">VHD 'ler birden çok depolama hesabına yayılmışsa, bu cmdlet her depolama hesabında bu ada sahip bir kapsayıcı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5b762-124">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="5b762-125">Kaydedilen görüntünün URL 'SI şuna benzer:</span><span class="sxs-lookup"><span data-stu-id="5b762-125">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="5b762-126"> https:// \<storageAccountName\> . blob.Core.Windows.NET/System/Microsoft.COMPUTE/Images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. vhd.</span><span class="sxs-lookup"><span data-stu-id="5b762-126">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="5b762-127">-ID</span><span class="sxs-lookup"><span data-stu-id="5b762-127">-Id</span></span>
<span data-ttu-id="5b762-128">Sanal makinenin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b762-128">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="5b762-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="5b762-129">-Name</span></span>
<span data-ttu-id="5b762-130">Bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b762-130">Specifies a name.</span></span>

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

### <span data-ttu-id="5b762-131">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="5b762-131">-Overwrite</span></span>
<span data-ttu-id="5b762-132">Bu cmdlet 'in hedef kapsayıcıda aynı öneke sahip olan tüm VHD 'Lerin üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5b762-132">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="5b762-133">-Yol</span><span class="sxs-lookup"><span data-stu-id="5b762-133">-Path</span></span>
<span data-ttu-id="5b762-134">VHD 'nin yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b762-134">Specifies the path of the VHD.</span></span>

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

### <span data-ttu-id="5b762-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b762-135">-ResourceGroupName</span></span>
<span data-ttu-id="5b762-136">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b762-136">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5b762-137">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="5b762-137">-VHDNamePrefix</span></span>
<span data-ttu-id="5b762-138">Vmımage 'ın depolama profilini oluşturan blobın adındaki öneki belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b762-138">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="5b762-139">Örneğin, işletim sistemi diskinin önek Vhdi öneki, ad Vhdönek-OSDisk ile sonuçlanır. \<guid\> . sahip.</span><span class="sxs-lookup"><span data-stu-id="5b762-139">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="5b762-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b762-140">CommonParameters</span></span>
<span data-ttu-id="5b762-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5b762-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b762-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b762-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b762-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5b762-143">INPUTS</span></span>

## <span data-ttu-id="5b762-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5b762-144">OUTPUTS</span></span>

## <span data-ttu-id="5b762-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5b762-145">NOTES</span></span>

## <span data-ttu-id="5b762-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5b762-146">RELATED LINKS</span></span>

[<span data-ttu-id="5b762-147">Get-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="5b762-147">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="5b762-148">Get-Azurermvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="5b762-148">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="5b762-149">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="5b762-149">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="5b762-150">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="5b762-150">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="5b762-151">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5b762-151">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)


