---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9A1CE31E-0158-441E-BC2D-B5D21C9D9421
online version: ''
schema: 2.0.0
ms.openlocfilehash: a956aa7eaf383b0cf5cdb20b39d2f6b54e292f92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105451"
---
# <span data-ttu-id="3ef1d-101">Save-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="3ef1d-101">Save-AzureVMImage</span></span>

## <span data-ttu-id="3ef1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ef1d-102">SYNOPSIS</span></span>
<span data-ttu-id="3ef1d-103">Durdurulmuş bir Azure sanal makinesinin görüntüsünü yakalar ve kaydeder.</span><span class="sxs-lookup"><span data-stu-id="3ef1d-103">Captures and saves the image of a stopped Azure virtual machine.</span></span>

## <span data-ttu-id="3ef1d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3ef1d-104">SYNTAX</span></span>

```
Save-AzureVMImage [-ServiceName] <String> [-Name] <String> [-ImageName] <String> [[-ImageLabel] <String>]
 [[-OSState] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3ef1d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ef1d-105">DESCRIPTION</span></span>
<span data-ttu-id="3ef1d-106">**Save-AzureVMImage** cmdlet 'i, durdurulmuş bir Azure sanal makinesinin resmini yakalar ve kaydeder.</span><span class="sxs-lookup"><span data-stu-id="3ef1d-106">The **Save-AzureVMImage** cmdlet captures and saves the image of a stopped Azure virtual machine.</span></span>
<span data-ttu-id="3ef1d-107">Windows sanal makinelerinde, yansımayı yakalanmadan hazırlamak için Sysprep aracını çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3ef1d-107">For Windows virtual machines, run the Sysprep tool to prepare the image before it is captured.</span></span>
<span data-ttu-id="3ef1d-108">Yansıma yakalandıktan sonra sanal makine silinir.</span><span class="sxs-lookup"><span data-stu-id="3ef1d-108">After the image is captured, the virtual machine is deleted.</span></span>

## <span data-ttu-id="3ef1d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3ef1d-109">EXAMPLES</span></span>

### <span data-ttu-id="3ef1d-110">Örnek 1: var olan bir sanal makineyi kaydedip bir dağıtımdan silme</span><span class="sxs-lookup"><span data-stu-id="3ef1d-110">Example 1: Save an existing virtual machine and then delete it from a deployment</span></span>
```
PS C:\> Save-AzureVMImage -ServiceName "MyService" -Name "MyVM" -NewImageName "MyBaseImage" -NewImageLabel "MyBaseVM"
```

<span data-ttu-id="3ef1d-111">Bu komut mevcut bir sanal makineyi yakalar ve dağıtımdan siler.</span><span class="sxs-lookup"><span data-stu-id="3ef1d-111">This command captures an existing virtual machine and deletes it from the deployment.</span></span>

## <span data-ttu-id="3ef1d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3ef1d-112">PARAMETERS</span></span>

### <span data-ttu-id="3ef1d-113">-Imagelabel</span><span class="sxs-lookup"><span data-stu-id="3ef1d-113">-ImageLabel</span></span>
<span data-ttu-id="3ef1d-114">Sanal makine görüntüsünün etiketini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1d-114">Specifies the label of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewImageLabel

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1d-115">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="3ef1d-115">-ImageName</span></span>
<span data-ttu-id="3ef1d-116">Sanal makine görüntüsünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1d-116">Specifies the name of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewImageName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1d-117">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="3ef1d-117">-InformationAction</span></span>
<span data-ttu-id="3ef1d-118">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1d-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3ef1d-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3ef1d-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3ef1d-120">'A</span><span class="sxs-lookup"><span data-stu-id="3ef1d-120">Continue</span></span>
- <span data-ttu-id="3ef1d-121">Manıza</span><span class="sxs-lookup"><span data-stu-id="3ef1d-121">Ignore</span></span>
- <span data-ttu-id="3ef1d-122">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="3ef1d-122">Inquire</span></span>
- <span data-ttu-id="3ef1d-123">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="3ef1d-123">SilentlyContinue</span></span>
- <span data-ttu-id="3ef1d-124">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="3ef1d-124">Stop</span></span>
- <span data-ttu-id="3ef1d-125">Biliriz</span><span class="sxs-lookup"><span data-stu-id="3ef1d-125">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1d-126">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="3ef1d-126">-InformationVariable</span></span>
<span data-ttu-id="3ef1d-127">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1d-127">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1d-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="3ef1d-128">-Name</span></span>
<span data-ttu-id="3ef1d-129">Kaynak sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1d-129">Specifies the name of the source virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1d-130">-OSState</span><span class="sxs-lookup"><span data-stu-id="3ef1d-130">-OSState</span></span>
<span data-ttu-id="3ef1d-131">Sanal makine görüntüsünün işlem sistem durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1d-131">Specifies the operation system state for the virtual machine image.</span></span>
<span data-ttu-id="3ef1d-132">Azure 'a sanal makine görüntüsü yakalamayı düşünüyorsanız bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="3ef1d-132">Use this parameter if you intend to capture a virtual machine image to Azure.</span></span>

<span data-ttu-id="3ef1d-133">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="3ef1d-133">Valid values are:</span></span>

- <span data-ttu-id="3ef1d-134">Genelleştirilmiş</span><span class="sxs-lookup"><span data-stu-id="3ef1d-134">Generalized</span></span>
- <span data-ttu-id="3ef1d-135">Antivirüs</span><span class="sxs-lookup"><span data-stu-id="3ef1d-135">Specialized</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1d-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="3ef1d-136">-Profile</span></span>
<span data-ttu-id="3ef1d-137">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1d-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3ef1d-138">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="3ef1d-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1d-139">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="3ef1d-139">-ServiceName</span></span>
<span data-ttu-id="3ef1d-140">Azure hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1d-140">Specifies the name of the Azure service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ef1d-141">CommonParameters</span></span>
<span data-ttu-id="3ef1d-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3ef1d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ef1d-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ef1d-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ef1d-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3ef1d-144">INPUTS</span></span>

## <span data-ttu-id="3ef1d-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3ef1d-145">OUTPUTS</span></span>

## <span data-ttu-id="3ef1d-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3ef1d-146">NOTES</span></span>

## <span data-ttu-id="3ef1d-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3ef1d-147">RELATED LINKS</span></span>

[<span data-ttu-id="3ef1d-148">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="3ef1d-148">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="3ef1d-149">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="3ef1d-149">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="3ef1d-150">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="3ef1d-150">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="3ef1d-151">Güncelleştirme-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="3ef1d-151">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


