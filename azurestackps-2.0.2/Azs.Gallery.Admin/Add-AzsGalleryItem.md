---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/add-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: d9ba42966efd4445fa561dff78b69d7e789badb5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106807"
---
# <span data-ttu-id="d3403-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="d3403-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="d3403-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3403-102">SYNOPSIS</span></span>
<span data-ttu-id="d3403-103">Sağlayıcıya sağlayıcı Galerisi öğesi yükler.</span><span class="sxs-lookup"><span data-stu-id="d3403-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="d3403-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3403-104">SYNTAX</span></span>

### <span data-ttu-id="d3403-105">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d3403-105">CreateExpanded (Default)</span></span>
```
Add-AzsGalleryItem [-SubscriptionId <String>] [-GalleryItemUri <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d3403-106">Oluturmak</span><span class="sxs-lookup"><span data-stu-id="d3403-106">Create</span></span>
```
Add-AzsGalleryItem -GalleryItemUriPayload <IGalleryItemUriPayload> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d3403-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3403-107">DESCRIPTION</span></span>
<span data-ttu-id="d3403-108">Sağlayıcıya sağlayıcı Galerisi öğesi yükler.</span><span class="sxs-lookup"><span data-stu-id="d3403-108">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="d3403-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3403-109">EXAMPLES</span></span>

### <span data-ttu-id="d3403-110">Örnek 1: Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="d3403-110">Example 1: Add-AzsGalleryItem</span></span>
```powershell
PS C:\> Add-AzsGalleryItem -GalleryItemUri https://testsa.blob.redmond.ext-n35r1010.masd.stbtest.microsoft.com/testsc/TestUbuntu.Test.1.0.0.azpkg

Name                  Publisher  PublisherDisplayName ItemName ItemDisplayName       Version Summary
----                  ---------  -------------------- -------- ---------------       ------- -------
TestUbuntu.Test.1.0.0 TestUbuntu TestUbuntu           Test     Test.TestUbuntu.1.0.0 1.0.0   Create a simple VM

```

<span data-ttu-id="d3403-111">TestUbuntu. test. 1.0.0 'i galeriye yükler.</span><span class="sxs-lookup"><span data-stu-id="d3403-111">Uploads TestUbuntu.Test.1.0.0 to the gallery.</span></span>

## <span data-ttu-id="d3403-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3403-112">PARAMETERS</span></span>

### <span data-ttu-id="d3403-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3403-113">-DefaultProfile</span></span>
<span data-ttu-id="d3403-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d3403-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d3403-115">-Gallergıuri</span><span class="sxs-lookup"><span data-stu-id="d3403-115">-GalleryItemUri</span></span>
<span data-ttu-id="d3403-116">Önceden çevrimiçi yüklenmiş olan Galeri paketinizin URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="d3403-116">URI for your gallery package that has already been uploaded online.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d3403-117">-Gallergıuripayload</span><span class="sxs-lookup"><span data-stu-id="d3403-117">-GalleryItemUriPayload</span></span>
<span data-ttu-id="d3403-118">Galeri öğesi yükünün konumu.</span><span class="sxs-lookup"><span data-stu-id="d3403-118">Location of gallery item payload.</span></span>
<span data-ttu-id="d3403-119">Oluşturmak için, GALLERıTEMURIPAYLOAD özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d3403-119">To construct, see NOTES section for GALLERYITEMURIPAYLOAD properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItemUriPayload
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d3403-120">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d3403-120">-SubscriptionId</span></span>
<span data-ttu-id="d3403-121">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="d3403-121">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d3403-122">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d3403-122">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d3403-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="d3403-123">-Confirm</span></span>
<span data-ttu-id="d3403-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d3403-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d3403-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3403-125">-WhatIf</span></span>
<span data-ttu-id="d3403-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d3403-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3403-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d3403-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d3403-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3403-128">CommonParameters</span></span>
<span data-ttu-id="d3403-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3403-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3403-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d3403-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3403-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3403-131">INPUTS</span></span>

### <span data-ttu-id="d3403-132">Microsoft. Azure. PowerShell. cmdlet. Gallery. modeller. Api20150401. Igalleryıtemuripayload</span><span class="sxs-lookup"><span data-stu-id="d3403-132">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItemUriPayload</span></span>

## <span data-ttu-id="d3403-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3403-133">OUTPUTS</span></span>

### <span data-ttu-id="d3403-134">Microsoft. Azure. PowerShell. cmdlet. Gallery. modeller. Api20150401. Igalleryıtem</span><span class="sxs-lookup"><span data-stu-id="d3403-134">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItem</span></span>



## <span data-ttu-id="d3403-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3403-135">NOTES</span></span>

<span data-ttu-id="d3403-136">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d3403-136">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d3403-137">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d3403-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d3403-138">GALLERıTEMURIPAYLOAD <IGalleryItemUriPayload> : galeri öğesi yükünün konumu.</span><span class="sxs-lookup"><span data-stu-id="d3403-138">GALLERYITEMURIPAYLOAD <IGalleryItemUriPayload>: Location of gallery item payload.</span></span>
  - <span data-ttu-id="d3403-139">`[GalleryItemUri <String>]`: Önceden çevrimiçi yüklenmiş Galeri paketinizin URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="d3403-139">`[GalleryItemUri <String>]`: URI for your gallery package that has already been uploaded online.</span></span>

## <span data-ttu-id="d3403-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3403-140">RELATED LINKS</span></span>

