---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
ms.openlocfilehash: 4d1de6553a07cf58fdc109dc5703e37392a27a02
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108450"
---
# <span data-ttu-id="ae69b-101">Get-AzImage</span><span class="sxs-lookup"><span data-stu-id="ae69b-101">Get-AzImage</span></span>

## <span data-ttu-id="ae69b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae69b-102">SYNOPSIS</span></span>
<span data-ttu-id="ae69b-103">Resmin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="ae69b-103">Gets the properties of an image.</span></span>

## <span data-ttu-id="ae69b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ae69b-104">SYNTAX</span></span>

```
Get-AzImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae69b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae69b-105">DESCRIPTION</span></span>
<span data-ttu-id="ae69b-106">**Get-Azgörüntü** cmdlet 'inin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="ae69b-106">The **Get-AzImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="ae69b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ae69b-107">EXAMPLES</span></span>

### <span data-ttu-id="ae69b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ae69b-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="ae69b-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Image01 ' adlı resmin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="ae69b-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="ae69b-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ae69b-110">Example 2</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01'

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="ae69b-111">Bu komut, ' ResourceGroup01 ' kaynak grubundaki tüm görüntülerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="ae69b-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="ae69b-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="ae69b-112">Example 3</span></span>
```
PS C:\> Get-AzImage

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup02
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup02/prov
                       iders/Microsoft.Compute/images/Image03
Name                 : Image03
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="ae69b-113">Bu komut, aboneliğin altındaki tüm görüntülerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="ae69b-113">This command gets the properties of all images under the subscription.</span></span>

### <span data-ttu-id="ae69b-114">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="ae69b-114">Example 4</span></span>
```
PS C:\> Get-AzImage -Name "Image*"

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup02
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup02/prov
                       iders/Microsoft.Compute/images/Image03
Name                 : Image03
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="ae69b-115">Bu komut, aboneliğin altındaki "görüntü" ile başlayan tüm görüntülerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="ae69b-115">This command gets the properties of all images under the subscription that start with "Image".</span></span>

## <span data-ttu-id="ae69b-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ae69b-116">PARAMETERS</span></span>

### <span data-ttu-id="ae69b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae69b-117">-DefaultProfile</span></span>
<span data-ttu-id="ae69b-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ae69b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae69b-119">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="ae69b-119">-Expand</span></span>
<span data-ttu-id="ae69b-120">Genişletme ifade sorgusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae69b-120">Specifies the expand expression query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae69b-121">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="ae69b-121">-ImageName</span></span>
<span data-ttu-id="ae69b-122">Bir resmin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae69b-122">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="ae69b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae69b-123">-ResourceGroupName</span></span>
<span data-ttu-id="ae69b-124">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae69b-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="ae69b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae69b-125">CommonParameters</span></span>
<span data-ttu-id="ae69b-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ae69b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae69b-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ae69b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae69b-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ae69b-128">INPUTS</span></span>

### <span data-ttu-id="ae69b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ae69b-129">System.String</span></span>

## <span data-ttu-id="ae69b-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ae69b-130">OUTPUTS</span></span>

### <span data-ttu-id="ae69b-131">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psımage</span><span class="sxs-lookup"><span data-stu-id="ae69b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="ae69b-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ae69b-132">NOTES</span></span>

## <span data-ttu-id="ae69b-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ae69b-133">RELATED LINKS</span></span>
