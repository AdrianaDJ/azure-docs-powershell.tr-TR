---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: 109f55c1afc1c00d26c47d0131d098158010bd70
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93595228"
---
# <span data-ttu-id="e5fe9-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e5fe9-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="e5fe9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5fe9-102">SYNOPSIS</span></span>
<span data-ttu-id="e5fe9-103">VMImage yayımcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="e5fe9-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5fe9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5fe9-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5fe9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5fe9-105">DESCRIPTION</span></span>
<span data-ttu-id="e5fe9-106">**Get-Azurermvmımagepublisher** cmdlet 'ı VMImage yayımcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="e5fe9-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="e5fe9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5fe9-107">EXAMPLES</span></span>

### <span data-ttu-id="e5fe9-108">Örnek 1: bölge için Vmımage yayımcıları alma</span><span class="sxs-lookup"><span data-stu-id="e5fe9-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="e5fe9-109">Bu komut, Azure profilinizde Merkezi ABD bölgesi için Vmımage örneklerinin yayımcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="e5fe9-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="e5fe9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5fe9-110">PARAMETERS</span></span>

### <span data-ttu-id="e5fe9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5fe9-111">-DefaultProfile</span></span>
<span data-ttu-id="e5fe9-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e5fe9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5fe9-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="e5fe9-113">-Location</span></span>
<span data-ttu-id="e5fe9-114">Vmımage 'ın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5fe9-114">Specifies the location of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5fe9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5fe9-115">CommonParameters</span></span>
<span data-ttu-id="e5fe9-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5fe9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5fe9-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5fe9-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5fe9-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5fe9-118">INPUTS</span></span>

### <span data-ttu-id="e5fe9-119">System. String</span><span class="sxs-lookup"><span data-stu-id="e5fe9-119">System.String</span></span>

## <span data-ttu-id="e5fe9-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5fe9-120">OUTPUTS</span></span>

### <span data-ttu-id="e5fe9-121">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineımagepublisher</span><span class="sxs-lookup"><span data-stu-id="e5fe9-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="e5fe9-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5fe9-122">NOTES</span></span>

## <span data-ttu-id="e5fe9-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5fe9-123">RELATED LINKS</span></span>

[<span data-ttu-id="e5fe9-124">Get-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="e5fe9-124">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="e5fe9-125">Get-Azurermvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="e5fe9-125">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="e5fe9-126">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="e5fe9-126">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="e5fe9-127">Save-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="e5fe9-127">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


