---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
ms.openlocfilehash: a9dff8f9661cfc7826adba78eca3d12961b343e6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752676"
---
# <span data-ttu-id="74484-101">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="74484-101">Set-AzVMSourceImage</span></span>

## <span data-ttu-id="74484-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74484-102">SYNOPSIS</span></span>
<span data-ttu-id="74484-103">Sanal makinenin resmini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74484-103">Specifies the image for a virtual machine.</span></span>

## <span data-ttu-id="74484-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="74484-104">SYNTAX</span></span>

### <span data-ttu-id="74484-105">ImageReferenceSkuParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="74484-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74484-106">Imagereferenceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="74484-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="74484-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="74484-107">DESCRIPTION</span></span>
<span data-ttu-id="74484-108">**Set-Azvmsourceımage** cmdlet 'i sanal makine için kullanılacak platform görüntüsünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="74484-108">The **Set-AzVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="74484-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="74484-109">EXAMPLES</span></span>

### <span data-ttu-id="74484-110">Örnek 1: resmin değerlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="74484-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="74484-111">İlk komut, ResourceGroup11 adındaki kaynak grubundaki AvailabilitySet03 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="74484-111">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="74484-112">İkinci komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="74484-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="74484-113">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="74484-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="74484-114">Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.</span><span class="sxs-lookup"><span data-stu-id="74484-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="74484-115">Final komutu, Publisher adı, teklifi, SKU ve sürüm değerlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="74484-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="74484-116">**Get-Azvmımagepublisher** , **Get-Azvmimageteklifini** , **Get-AzVMImageSku** ve **Get-azvmiımage** cmdlet 'leri bu ayarları bulabilir.</span><span class="sxs-lookup"><span data-stu-id="74484-116">The **Get-AzVMImagePublisher** , **Get-AzVMImageOffer** , **Get-AzVMImageSku** , and **Get-AzVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="74484-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="74484-117">PARAMETERS</span></span>

### <span data-ttu-id="74484-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74484-118">-DefaultProfile</span></span>
<span data-ttu-id="74484-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="74484-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74484-120">-ID</span><span class="sxs-lookup"><span data-stu-id="74484-120">-Id</span></span>
<span data-ttu-id="74484-121">KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="74484-121">Specifies the ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74484-122">-Teklif</span><span class="sxs-lookup"><span data-stu-id="74484-122">-Offer</span></span>
<span data-ttu-id="74484-123">Vmımage teklifinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="74484-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="74484-124">Resim teklifi edinmek için Get-AzVMImageOffer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="74484-124">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74484-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="74484-125">-PublisherName</span></span>
<span data-ttu-id="74484-126">Vmımage yayımcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74484-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="74484-127">Yayımcı edinmek için Get-AzVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="74484-127">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74484-128">-STB 'ler</span><span class="sxs-lookup"><span data-stu-id="74484-128">-Skus</span></span>
<span data-ttu-id="74484-129">Vmımage SKU 'SU belirtir.</span><span class="sxs-lookup"><span data-stu-id="74484-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="74484-130">STB 'ler almak için Get-AzVMImageSku cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="74484-130">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74484-131">-Version</span><span class="sxs-lookup"><span data-stu-id="74484-131">-Version</span></span>
<span data-ttu-id="74484-132">Vmımage 'ın bir sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="74484-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="74484-133">En son sürümü kullanmak için belirli bir sürüm yerine en son sürümünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="74484-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74484-134">-VM</span><span class="sxs-lookup"><span data-stu-id="74484-134">-VM</span></span>
<span data-ttu-id="74484-135">Yapılandırılacak yerel sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74484-135">Specifies the local virtual machine object to configure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74484-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74484-136">CommonParameters</span></span>
<span data-ttu-id="74484-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="74484-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74484-138">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="74484-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74484-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="74484-139">INPUTS</span></span>

### <span data-ttu-id="74484-140">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="74484-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="74484-141">System. String</span><span class="sxs-lookup"><span data-stu-id="74484-141">System.String</span></span>

## <span data-ttu-id="74484-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="74484-142">OUTPUTS</span></span>

### <span data-ttu-id="74484-143">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="74484-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="74484-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="74484-144">NOTES</span></span>

## <span data-ttu-id="74484-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="74484-145">RELATED LINKS</span></span>

[<span data-ttu-id="74484-146">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="74484-146">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="74484-147">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="74484-147">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="74484-148">Get-Azvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="74484-148">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="74484-149">Get-Azvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="74484-149">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="74484-150">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="74484-150">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="74484-151">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="74484-151">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

