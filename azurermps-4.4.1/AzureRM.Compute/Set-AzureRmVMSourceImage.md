---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMSourceImage.md
ms.openlocfilehash: 88b8af8cd16ab4868a10c5ff1aa3759a6d771a6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586927"
---
# <span data-ttu-id="37330-101">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="37330-101">Set-AzureRmVMSourceImage</span></span>

## <span data-ttu-id="37330-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37330-102">SYNOPSIS</span></span>
<span data-ttu-id="37330-103">Sanal makinenin resmini belirtir.</span><span class="sxs-lookup"><span data-stu-id="37330-103">Specifies the image for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37330-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="37330-104">SYNTAX</span></span>

### <span data-ttu-id="37330-105">ImageReferenceSkuParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="37330-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37330-106">Imagereferenceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="37330-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37330-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="37330-107">DESCRIPTION</span></span>
<span data-ttu-id="37330-108">**Set-Azurermvmsourceımage** cmdlet 'i, sanal makine için kullanılacak platform görüntüsünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="37330-108">The **Set-AzureRmVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="37330-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="37330-109">EXAMPLES</span></span>

### <span data-ttu-id="37330-110">Örnek 1: resmin değerlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="37330-110">Example 1: Set values for an image</span></span>
```
PS C:\> AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="37330-111">İlk komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet03 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="37330-111">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="37330-112">İkinci komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="37330-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="37330-113">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="37330-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="37330-114">Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.</span><span class="sxs-lookup"><span data-stu-id="37330-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="37330-115">Final komutu, Publisher adı, teklifi, SKU ve sürüm değerlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="37330-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="37330-116">**Get-Azurermvmımagepublisher** , Get-Azurermvmımageteklifini, Get-AzureRmVMImageSku ve **Get-azurermvmıımage** cmdlet 'leri bu ayarları bulabilir. **Get-AzureRmVMImageOffer** **Get-AzureRmVMImageSku**</span><span class="sxs-lookup"><span data-stu-id="37330-116">The **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** , and **Get-AzureRmVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="37330-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="37330-117">PARAMETERS</span></span>

### <span data-ttu-id="37330-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37330-118">-DefaultProfile</span></span>
<span data-ttu-id="37330-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="37330-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37330-120">-ID</span><span class="sxs-lookup"><span data-stu-id="37330-120">-Id</span></span>
<span data-ttu-id="37330-121">KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="37330-121">Specifies the ID.</span></span>

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

### <span data-ttu-id="37330-122">-Teklif</span><span class="sxs-lookup"><span data-stu-id="37330-122">-Offer</span></span>
<span data-ttu-id="37330-123">Vmımage teklifinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="37330-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="37330-124">Resim teklifi edinmek için Get-AzureRmVMImageOffer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="37330-124">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="37330-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="37330-125">-PublisherName</span></span>
<span data-ttu-id="37330-126">Vmımage yayımcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37330-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="37330-127">Yayımcı edinmek için Get-AzureRmVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="37330-127">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="37330-128">-STB 'ler</span><span class="sxs-lookup"><span data-stu-id="37330-128">-Skus</span></span>
<span data-ttu-id="37330-129">Vmımage SKU 'SU belirtir.</span><span class="sxs-lookup"><span data-stu-id="37330-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="37330-130">STB 'ler almak için Get-AzureRmVMImageSku cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="37330-130">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="37330-131">-Version</span><span class="sxs-lookup"><span data-stu-id="37330-131">-Version</span></span>
<span data-ttu-id="37330-132">Vmımage 'ın bir sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="37330-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="37330-133">En son sürümü kullanmak için belirli bir sürüm yerine en son sürümünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="37330-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="37330-134">-VM</span><span class="sxs-lookup"><span data-stu-id="37330-134">-VM</span></span>
<span data-ttu-id="37330-135">Yapılandırılacak yerel sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="37330-135">Specifies the local virtual machine object to configure.</span></span>

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

### <span data-ttu-id="37330-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37330-136">CommonParameters</span></span>
<span data-ttu-id="37330-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="37330-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37330-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37330-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37330-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="37330-139">INPUTS</span></span>

## <span data-ttu-id="37330-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="37330-140">OUTPUTS</span></span>

## <span data-ttu-id="37330-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="37330-141">NOTES</span></span>

## <span data-ttu-id="37330-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="37330-142">RELATED LINKS</span></span>

[<span data-ttu-id="37330-143">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="37330-143">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="37330-144">Get-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="37330-144">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="37330-145">Get-Azurermvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="37330-145">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="37330-146">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="37330-146">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="37330-147">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="37330-147">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="37330-148">Yeni-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="37330-148">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


