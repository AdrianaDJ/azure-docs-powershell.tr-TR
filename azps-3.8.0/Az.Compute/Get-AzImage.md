---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
ms.openlocfilehash: 4d1de6553a07cf58fdc109dc5703e37392a27a02
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103676"
---
# <span data-ttu-id="09fcf-101">Get-AzImage</span><span class="sxs-lookup"><span data-stu-id="09fcf-101">Get-AzImage</span></span>

## <span data-ttu-id="09fcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="09fcf-103">Resmin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="09fcf-103">Gets the properties of an image.</span></span>

## <span data-ttu-id="09fcf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="09fcf-104">SYNTAX</span></span>

```
Get-AzImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09fcf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="09fcf-105">DESCRIPTION</span></span>
<span data-ttu-id="09fcf-106">**Get-Azgörüntü** cmdlet 'inin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="09fcf-106">The **Get-AzImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="09fcf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="09fcf-107">EXAMPLES</span></span>

### <span data-ttu-id="09fcf-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="09fcf-108">Example 1</span></span>
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

<span data-ttu-id="09fcf-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Image01 ' adlı resmin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="09fcf-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="09fcf-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="09fcf-110">Example 2</span></span>
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

<span data-ttu-id="09fcf-111">Bu komut, ' ResourceGroup01 ' kaynak grubundaki tüm görüntülerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="09fcf-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="09fcf-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="09fcf-112">Example 3</span></span>
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

<span data-ttu-id="09fcf-113">Bu komut, aboneliğin altındaki tüm görüntülerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="09fcf-113">This command gets the properties of all images under the subscription.</span></span>

### <span data-ttu-id="09fcf-114">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="09fcf-114">Example 4</span></span>
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

<span data-ttu-id="09fcf-115">Bu komut, aboneliğin altındaki "görüntü" ile başlayan tüm görüntülerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="09fcf-115">This command gets the properties of all images under the subscription that start with "Image".</span></span>

## <span data-ttu-id="09fcf-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="09fcf-116">PARAMETERS</span></span>

### <span data-ttu-id="09fcf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09fcf-117">-DefaultProfile</span></span>
<span data-ttu-id="09fcf-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="09fcf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09fcf-119">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="09fcf-119">-Expand</span></span>
<span data-ttu-id="09fcf-120">Genişletme ifade sorgusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="09fcf-120">Specifies the expand expression query.</span></span>

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

### <span data-ttu-id="09fcf-121">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="09fcf-121">-ImageName</span></span>
<span data-ttu-id="09fcf-122">Bir resmin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09fcf-122">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="09fcf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09fcf-123">-ResourceGroupName</span></span>
<span data-ttu-id="09fcf-124">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09fcf-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="09fcf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09fcf-125">CommonParameters</span></span>
<span data-ttu-id="09fcf-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="09fcf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09fcf-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="09fcf-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09fcf-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="09fcf-128">INPUTS</span></span>

### <span data-ttu-id="09fcf-129">System. String</span><span class="sxs-lookup"><span data-stu-id="09fcf-129">System.String</span></span>

## <span data-ttu-id="09fcf-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="09fcf-130">OUTPUTS</span></span>

### <span data-ttu-id="09fcf-131">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psımage</span><span class="sxs-lookup"><span data-stu-id="09fcf-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="09fcf-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="09fcf-132">NOTES</span></span>

## <span data-ttu-id="09fcf-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="09fcf-133">RELATED LINKS</span></span>
