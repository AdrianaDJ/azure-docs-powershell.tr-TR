---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E712421A-FA69-46E7-A0DE-F2734D767F2D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8355e0a1d36a6c1dc5b2ca8172cde5bf94480bbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106532"
---
# <span data-ttu-id="deb3a-101">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="deb3a-101">Get-AzureVMImage</span></span>

## <span data-ttu-id="deb3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="deb3a-102">SYNOPSIS</span></span>
<span data-ttu-id="deb3a-103">Görüntü deposundaki bir veya birden çok işletim sistemi veya sanal makine görüntüsünün özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="deb3a-103">Gets the properties on one or a list of operating systems or a virtual machine image in the image repository.</span></span>

## <span data-ttu-id="deb3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="deb3a-104">SYNTAX</span></span>

```
Get-AzureVMImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="deb3a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="deb3a-105">DESCRIPTION</span></span>
<span data-ttu-id="deb3a-106">**Get-AzureVMImage** cmdlet 'i, görüntü deposundaki bir veya bir işletim sistemi veya sanal makine görüntüsünün özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="deb3a-106">The **Get-AzureVMImage** cmdlet gets properties on one or a list of operating systems or a virtual machine image in the image repository.</span></span>
<span data-ttu-id="deb3a-107">Cmdlet, depodaki tüm resimler için veya resim adı sağlanmışsa belirli bir görüntüyle ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="deb3a-107">The cmdlet returns information for all images in the repository, or about a specific image if its image name is provided.</span></span>

## <span data-ttu-id="deb3a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="deb3a-108">EXAMPLES</span></span>

### <span data-ttu-id="deb3a-109">Örnek 1: geçerli görüntü deposundaki belirli bir resim nesnesini edinin.</span><span class="sxs-lookup"><span data-stu-id="deb3a-109">Example 1: Get a specific image object from the current image repository.</span></span>
```
PS C:\> Get-AzureVMImage -ImageName Image001
```

<span data-ttu-id="deb3a-110">Bu komut, Image001 adındaki resim nesnesini geçerli görüntü deposundan alır.</span><span class="sxs-lookup"><span data-stu-id="deb3a-110">This command gets the image object named Image001 from the current image repository.</span></span>

### <span data-ttu-id="deb3a-111">Örnek 2: geçerli görüntü deposundaki tüm resimleri alma</span><span class="sxs-lookup"><span data-stu-id="deb3a-111">Example 2: Get all images from the current image repository</span></span>
```
PS C:\> Get-AzureVMImage
```

<span data-ttu-id="deb3a-112">Bu komut, geçerli görüntü deposundaki tüm resimleri alır.</span><span class="sxs-lookup"><span data-stu-id="deb3a-112">This command retrieves all the images from the current image repository.</span></span>

### <span data-ttu-id="deb3a-113">Örnek 3: abonelik bağlamını ayarlayın ve tüm resimleri alın</span><span class="sxs-lookup"><span data-stu-id="deb3a-113">Example 3: Set the subscription context and then get all the images</span></span>
```
PS C:\> $SubsId = <MySubscriptionID>
C:\PS>$Cert = Get-AzureCertificate cert:\LocalMachine\MY\<CertificateThumbprint>
C:\PS>$MyOSImages = Get-AzureVMImage
```

<span data-ttu-id="deb3a-114">Bu komut, abonelik bağlamını ayarlar ve resim deposundaki tüm resimleri alır.</span><span class="sxs-lookup"><span data-stu-id="deb3a-114">This command sets the subscription context and then retrieves all the images from the image repository.</span></span>

## <span data-ttu-id="deb3a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="deb3a-115">PARAMETERS</span></span>

### <span data-ttu-id="deb3a-116">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="deb3a-116">-ImageName</span></span>
<span data-ttu-id="deb3a-117">Görüntü deposundaki işletim sisteminin veya sanal makine görüntüsünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="deb3a-117">Specifies the name of the operating system or virtual machine image in the image repository.</span></span>
<span data-ttu-id="deb3a-118">Bu parametreyi belirtmezseniz, tüm resimler döndürülür.</span><span class="sxs-lookup"><span data-stu-id="deb3a-118">If you do not specify this parameter, all the images are returned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="deb3a-119">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="deb3a-119">-InformationAction</span></span>
<span data-ttu-id="deb3a-120">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="deb3a-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="deb3a-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="deb3a-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="deb3a-122">'A</span><span class="sxs-lookup"><span data-stu-id="deb3a-122">Continue</span></span>
- <span data-ttu-id="deb3a-123">Manıza</span><span class="sxs-lookup"><span data-stu-id="deb3a-123">Ignore</span></span>
- <span data-ttu-id="deb3a-124">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="deb3a-124">Inquire</span></span>
- <span data-ttu-id="deb3a-125">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="deb3a-125">SilentlyContinue</span></span>
- <span data-ttu-id="deb3a-126">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="deb3a-126">Stop</span></span>
- <span data-ttu-id="deb3a-127">Biliriz</span><span class="sxs-lookup"><span data-stu-id="deb3a-127">Suspend</span></span>

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

### <span data-ttu-id="deb3a-128">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="deb3a-128">-InformationVariable</span></span>
<span data-ttu-id="deb3a-129">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="deb3a-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="deb3a-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="deb3a-130">-Profile</span></span>
<span data-ttu-id="deb3a-131">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="deb3a-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="deb3a-132">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="deb3a-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="deb3a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deb3a-133">CommonParameters</span></span>
<span data-ttu-id="deb3a-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="deb3a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deb3a-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deb3a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deb3a-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="deb3a-136">INPUTS</span></span>

## <span data-ttu-id="deb3a-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="deb3a-137">OUTPUTS</span></span>

## <span data-ttu-id="deb3a-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="deb3a-138">NOTES</span></span>

## <span data-ttu-id="deb3a-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="deb3a-139">RELATED LINKS</span></span>

[<span data-ttu-id="deb3a-140">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="deb3a-140">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="deb3a-141">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="deb3a-141">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="deb3a-142">Save-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="deb3a-142">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="deb3a-143">Güncelleştirme-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="deb3a-143">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


