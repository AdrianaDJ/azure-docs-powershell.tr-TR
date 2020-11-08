---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C9470E5-21D2-4AF5-9F11-F66F94B133C0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23f4511f8e0439c1581cc388843a37266092f4d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106454"
---
# <span data-ttu-id="4beeb-101">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="4beeb-101">Remove-AzureVMImage</span></span>

## <span data-ttu-id="4beeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4beeb-102">SYNOPSIS</span></span>
<span data-ttu-id="4beeb-103">Görüntü deposundaki bir işletim sistemi yansımasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4beeb-103">Removes an operating system image from the image repository.</span></span>

## <span data-ttu-id="4beeb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4beeb-104">SYNTAX</span></span>

```
Remove-AzureVMImage [-ImageName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4beeb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4beeb-105">DESCRIPTION</span></span>
<span data-ttu-id="4beeb-106">**Remove-AzureVMImage** cmdlet 'i, görüntü deposundaki bir işletim sistemi yansımasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4beeb-106">The **Remove-AzureVMImage** cmdlet removes an operating system image from the image repository.</span></span>
<span data-ttu-id="4beeb-107">Varsayılan olarak, bu cmdlet, ilişkili fiziksel görüntü blob 'unu depolama hesabından silmez.</span><span class="sxs-lookup"><span data-stu-id="4beeb-107">By default, this cmdlet does not delete the associated physical image blob from the storage account.</span></span>
<span data-ttu-id="4beeb-108">İlişkili sanal sabit sürücüyü (VHD) silmek için **Deletevhd** parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4beeb-108">To delete the associated virtual hard drive (VHD), use the **DeleteVHD** parameter.</span></span>

## <span data-ttu-id="4beeb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4beeb-109">EXAMPLES</span></span>

### <span data-ttu-id="4beeb-110">Örnek 1: resim deposundaki bir resmi kaldırma</span><span class="sxs-lookup"><span data-stu-id="4beeb-110">Example 1: Remove an image from the image repository</span></span>
```
PS C:\> Remove-AzureVMImage -ImageName "Image001"
```

<span data-ttu-id="4beeb-111">Bu komut, Image001 adındaki resmi görüntü deposundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4beeb-111">This command removes the image named Image001 from the image repository.</span></span>

### <span data-ttu-id="4beeb-112">Örnek 2: resim deposundaki bir resmi ve ayrıca VHD 'yi kaldırma</span><span class="sxs-lookup"><span data-stu-id="4beeb-112">Example 2: Remove an image from the image repository and also the VHD</span></span>
```
PS C:\> Remove-AzureVMImage -ImageName " Image001" -DeleteVHD
```

<span data-ttu-id="4beeb-113">Bu komut, Image001 adındaki resmi görüntü deposundan kaldırır ve fiziksel VHD görüntüsünü depolama hesabından siler.</span><span class="sxs-lookup"><span data-stu-id="4beeb-113">This command removes the image named Image001 from the image repository and also deletes the physical VHD image from the storage account.</span></span>

### <span data-ttu-id="4beeb-114">Örnek 3: abonelik bağlamını ayarlayın ve tüm resimleri kaldırın</span><span class="sxs-lookup"><span data-stu-id="4beeb-114">Example 3: Set a subscription context and then remove all the images</span></span>
```
PS C:\> $SubsId = &amp;lt;MySubscriptionID&amp;gt;
PS C:\> $Cert = Get-AzureCertificate cert:\LocalMachine\MY\&amp;lt;CertificateThumbprint&amp;gt;
PS C:\> Get-AzureVMImage `
| Where-Object {$_.Label -match "Beta" }`
| Foreach-Object {Remove-AzureVMImage -ImageName $_.name }
```

<span data-ttu-id="4beeb-115">Bu komut, abonelik bağlamını ayarlar ve resim deposundaki, etiketine Beta adını içeren tüm resimleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4beeb-115">This command sets the subscription context and then removes all the images from the image repository whose Label includes the name Beta.</span></span>

## <span data-ttu-id="4beeb-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4beeb-116">PARAMETERS</span></span>

### <span data-ttu-id="4beeb-117">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="4beeb-117">-DeleteVHD</span></span>
<span data-ttu-id="4beeb-118">Bu cmdlet 'in depolama hesabından fiziksel VHD görüntü blob 'unu sildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4beeb-118">Indicates that this cmdlet deletes the physical VHD image blob from the storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4beeb-119">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="4beeb-119">-ImageName</span></span>
<span data-ttu-id="4beeb-120">Görüntü deposundan kaldırılacak işletim sistemini veya sanal makine yansımasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4beeb-120">Specifies the operating system or virtual machine image to remove from the image repository.</span></span>

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

### <span data-ttu-id="4beeb-121">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="4beeb-121">-InformationAction</span></span>
<span data-ttu-id="4beeb-122">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4beeb-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4beeb-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4beeb-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4beeb-124">'A</span><span class="sxs-lookup"><span data-stu-id="4beeb-124">Continue</span></span>
- <span data-ttu-id="4beeb-125">Manıza</span><span class="sxs-lookup"><span data-stu-id="4beeb-125">Ignore</span></span>
- <span data-ttu-id="4beeb-126">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="4beeb-126">Inquire</span></span>
- <span data-ttu-id="4beeb-127">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="4beeb-127">SilentlyContinue</span></span>
- <span data-ttu-id="4beeb-128">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="4beeb-128">Stop</span></span>
- <span data-ttu-id="4beeb-129">Biliriz</span><span class="sxs-lookup"><span data-stu-id="4beeb-129">Suspend</span></span>

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

### <span data-ttu-id="4beeb-130">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="4beeb-130">-InformationVariable</span></span>
<span data-ttu-id="4beeb-131">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="4beeb-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4beeb-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="4beeb-132">-Profile</span></span>
<span data-ttu-id="4beeb-133">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4beeb-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4beeb-134">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="4beeb-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4beeb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4beeb-135">CommonParameters</span></span>
<span data-ttu-id="4beeb-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4beeb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4beeb-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4beeb-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4beeb-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4beeb-138">INPUTS</span></span>

## <span data-ttu-id="4beeb-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4beeb-139">OUTPUTS</span></span>

## <span data-ttu-id="4beeb-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4beeb-140">NOTES</span></span>

## <span data-ttu-id="4beeb-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4beeb-141">RELATED LINKS</span></span>

[<span data-ttu-id="4beeb-142">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="4beeb-142">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="4beeb-143">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="4beeb-143">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="4beeb-144">Save-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="4beeb-144">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="4beeb-145">Güncelleştirme-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="4beeb-145">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


