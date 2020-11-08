---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DBC4A0B8-A34A-47AC-930B-EFE23A95A216
online version: ''
schema: 2.0.0
ms.openlocfilehash: 178349299767eefb1d89c31a0199f53373bd2ae2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105995"
---
# <span data-ttu-id="44e4c-101">New-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="44e4c-101">New-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="44e4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44e4c-102">SYNOPSIS</span></span>
<span data-ttu-id="44e4c-103">Bir Azure RemoteApp şablonu resmini karşıya yükler veya içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="44e4c-103">Uploads or imports an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="44e4c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="44e4c-104">SYNTAX</span></span>

### <span data-ttu-id="44e4c-105">UploadLocalVhd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="44e4c-105">UploadLocalVhd (Default)</span></span>
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> [-Path] <String> [-Resume]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="44e4c-106">AzureVmUpload</span><span class="sxs-lookup"><span data-stu-id="44e4c-106">AzureVmUpload</span></span>
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> -AzureVmImageName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="44e4c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="44e4c-107">DESCRIPTION</span></span>
<span data-ttu-id="44e4c-108">**Yeni-Azureremoteapptemplateımage** cmdlet 'i karşıya yükler veya bir Azure RemoteApp şablonu görüntüsü alır.</span><span class="sxs-lookup"><span data-stu-id="44e4c-108">The **New-AzureRemoteAppTemplateImage** cmdlet uploads or imports an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="44e4c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="44e4c-109">EXAMPLES</span></span>

### <span data-ttu-id="44e4c-110">Örnek 1: şablon görüntüsü oluşturmak için VHD dosyasını karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="44e4c-110">Example 1: Upload a VHD file to create a template image</span></span>
```
PS C:\> New-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -Location "North Europe" -Path "C:\RemoteAppImages\ContosoApps.vhd"
```

<span data-ttu-id="44e4c-111">Bu komut C:\remoteappımages\contosoapps.vhd 'yi karşıya yükler ve Kuzey Avrupa veri merkezinde ContosoApps adlı bir şablon görüntüsü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="44e4c-111">This command uploads C:\RemoteAppImages\ContosoApps.vhd to create a template image named ContosoApps in the North Europe data center.</span></span>

## <span data-ttu-id="44e4c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="44e4c-112">PARAMETERS</span></span>

### <span data-ttu-id="44e4c-113">-AzureVmImageName</span><span class="sxs-lookup"><span data-stu-id="44e4c-113">-AzureVmImageName</span></span>
<span data-ttu-id="44e4c-114">Şablon görüntüsü olarak kullanılacak Azure sanal makinesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="44e4c-114">Specifies the name of an Azure virtual machine to use as a template image.</span></span>

```yaml
Type: String
Parameter Sets: AzureVmUpload
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44e4c-115">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="44e4c-115">-ImageName</span></span>
<span data-ttu-id="44e4c-116">Azure RemoteApp şablonu görüntüsünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="44e4c-116">Specifies the name of an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44e4c-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="44e4c-117">-Location</span></span>
<span data-ttu-id="44e4c-118">Şablon görüntüsünün Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="44e4c-118">Specifies the Azure region of the template image.</span></span>

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

### <span data-ttu-id="44e4c-119">-Yol</span><span class="sxs-lookup"><span data-stu-id="44e4c-119">-Path</span></span>
<span data-ttu-id="44e4c-120">Şablon görüntüsünün dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="44e4c-120">Specifies the file path of the template image.</span></span>

```yaml
Type: String
Parameter Sets: UploadLocalVhd
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44e4c-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="44e4c-121">-Profile</span></span>
<span data-ttu-id="44e4c-122">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="44e4c-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="44e4c-123">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="44e4c-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="44e4c-124">-Özgeçmiş</span><span class="sxs-lookup"><span data-stu-id="44e4c-124">-Resume</span></span>
<span data-ttu-id="44e4c-125">Şablon görüntüsünün karşıya yüklenmesi kesintiye uğrarsa bu cmdlet 'in devam ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="44e4c-125">Indicates that this cmdlet resumes if the upload of a template image is interrupted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UploadLocalVhd
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e4c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44e4c-126">CommonParameters</span></span>
<span data-ttu-id="44e4c-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="44e4c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44e4c-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44e4c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44e4c-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="44e4c-129">INPUTS</span></span>

## <span data-ttu-id="44e4c-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="44e4c-130">OUTPUTS</span></span>

## <span data-ttu-id="44e4c-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="44e4c-131">NOTES</span></span>

## <span data-ttu-id="44e4c-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="44e4c-132">RELATED LINKS</span></span>

[<span data-ttu-id="44e4c-133">Get-Azureremoteapptemplateımage</span><span class="sxs-lookup"><span data-stu-id="44e4c-133">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="44e4c-134">Remove-Azureremoteapptemplateımage</span><span class="sxs-lookup"><span data-stu-id="44e4c-134">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="44e4c-135">Rename-Azureremoteapptemplateımage</span><span class="sxs-lookup"><span data-stu-id="44e4c-135">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


