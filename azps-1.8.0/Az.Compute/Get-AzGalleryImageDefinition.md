---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
ms.openlocfilehash: 86da7a6f991bf7eeead14ad3414f9210eb7e175d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917467"
---
# <span data-ttu-id="1aace-101">Get-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="1aace-101">Get-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="1aace-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1aace-102">SYNOPSIS</span></span>
<span data-ttu-id="1aace-103">Get veya LIST Galerisi görüntü tanımları.</span><span class="sxs-lookup"><span data-stu-id="1aace-103">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="1aace-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1aace-104">SYNTAX</span></span>

### <span data-ttu-id="1aace-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1aace-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1aace-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="1aace-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageDefinition [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1aace-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1aace-107">DESCRIPTION</span></span>
<span data-ttu-id="1aace-108">Get veya LIST Galerisi görüntü tanımları.</span><span class="sxs-lookup"><span data-stu-id="1aace-108">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="1aace-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1aace-109">EXAMPLES</span></span>

### <span data-ttu-id="1aace-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1aace-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="1aace-111">Galeri resmi tanımını edinin.</span><span class="sxs-lookup"><span data-stu-id="1aace-111">Get the gallery image definition.</span></span>

### <span data-ttu-id="1aace-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1aace-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image*

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image2
Name                : image2
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="1aace-113">"Görüntü" ile başlayan Galeri resim tanımını edinin.</span><span class="sxs-lookup"><span data-stu-id="1aace-113">Get the gallery image definition that starts with "image".</span></span>

### <span data-ttu-id="1aace-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="1aace-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image2
Name                : image2
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="1aace-115">Gallery1 'de Galeri resim tanımlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="1aace-115">Get the gallery image definitions in gallery1.</span></span>

## <span data-ttu-id="1aace-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1aace-116">PARAMETERS</span></span>

### <span data-ttu-id="1aace-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aace-117">-DefaultProfile</span></span>
<span data-ttu-id="1aace-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1aace-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1aace-119">-Gallertadı</span><span class="sxs-lookup"><span data-stu-id="1aace-119">-GalleryName</span></span>
<span data-ttu-id="1aace-120">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="1aace-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1aace-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="1aace-121">-Name</span></span>
<span data-ttu-id="1aace-122">Galeri resim tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="1aace-122">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="1aace-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aace-123">-ResourceGroupName</span></span>
<span data-ttu-id="1aace-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1aace-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1aace-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1aace-125">-ResourceId</span></span>
<span data-ttu-id="1aace-126">Galeri resmi tanımı için kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="1aace-126">The resource ID for the gallery image definition</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1aace-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aace-127">CommonParameters</span></span>
<span data-ttu-id="1aace-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1aace-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aace-129">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1aace-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aace-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1aace-130">INPUTS</span></span>

### <span data-ttu-id="1aace-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1aace-131">System.String</span></span>

## <span data-ttu-id="1aace-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1aace-132">OUTPUTS</span></span>

### <span data-ttu-id="1aace-133">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psgallerimage</span><span class="sxs-lookup"><span data-stu-id="1aace-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="1aace-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1aace-134">NOTES</span></span>

## <span data-ttu-id="1aace-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1aace-135">RELATED LINKS</span></span>