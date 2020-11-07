---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImage.md
ms.openlocfilehash: 5f723ea475ed909ee5445f3788386a2163af697d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762548"
---
# <span data-ttu-id="97e0f-101">New-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="97e0f-101">New-AzureRmImage</span></span>

## <span data-ttu-id="97e0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97e0f-102">SYNOPSIS</span></span>
<span data-ttu-id="97e0f-103">Resim oluşturur.</span><span class="sxs-lookup"><span data-stu-id="97e0f-103">Creates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97e0f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97e0f-104">SYNTAX</span></span>

```
New-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <Image> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97e0f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="97e0f-105">DESCRIPTION</span></span>
<span data-ttu-id="97e0f-106">**Yeni-AzureRmImage** cmdlet 'i bir resim oluşturur.</span><span class="sxs-lookup"><span data-stu-id="97e0f-106">The **New-AzureRmImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="97e0f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97e0f-107">EXAMPLES</span></span>

### <span data-ttu-id="97e0f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="97e0f-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzureRmImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzureRmImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzureRmImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="97e0f-109">İlk komut bir resim nesnesi oluşturur ve $imageConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="97e0f-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="97e0f-110">Sonraki üç komut, $osDiskVhdUri, $dataDiskVhdUri 1 ve $dataDiskVhdUri 2 değişkenlerine işletim sistemi diskinin ve iki veri diskinin yollarını atar.</span><span class="sxs-lookup"><span data-stu-id="97e0f-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="97e0f-111">Bu yaklaşım yalnızca aşağıdaki komutların okunurluğu için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="97e0f-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="97e0f-112">Sonraki üç komut, $imageConfig depolanan resme bir işletim sistemi diski ve iki veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="97e0f-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="97e0f-113">Her diskin URI 'SI $osDiskVhdUri, $dataDiskVhdUri 1 ve $dataDiskVhdUri 2 ' de depolanır.</span><span class="sxs-lookup"><span data-stu-id="97e0f-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="97e0f-114">Son komutu, ' ResourceGroup01 ' kaynak grubunda ' ImageName01 ' adlı bir resim oluşturur.</span><span class="sxs-lookup"><span data-stu-id="97e0f-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="97e0f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97e0f-115">PARAMETERS</span></span>

### <span data-ttu-id="97e0f-116">-Image</span><span class="sxs-lookup"><span data-stu-id="97e0f-116">-Image</span></span>
<span data-ttu-id="97e0f-117">Yerel bir resim nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="97e0f-117">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97e0f-118">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="97e0f-118">-ImageName</span></span>
<span data-ttu-id="97e0f-119">Bir resmin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97e0f-119">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97e0f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97e0f-120">-ResourceGroupName</span></span>
<span data-ttu-id="97e0f-121">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97e0f-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="97e0f-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="97e0f-122">-Confirm</span></span>
<span data-ttu-id="97e0f-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="97e0f-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97e0f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97e0f-124">-WhatIf</span></span>
<span data-ttu-id="97e0f-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97e0f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97e0f-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="97e0f-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97e0f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97e0f-127">CommonParameters</span></span>
<span data-ttu-id="97e0f-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97e0f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97e0f-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97e0f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97e0f-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97e0f-130">INPUTS</span></span>

### <span data-ttu-id="97e0f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="97e0f-131">System.String</span></span>
<span data-ttu-id="97e0f-132">Microsoft. Azure. Management. COMPUTE. modeller. Image</span><span class="sxs-lookup"><span data-stu-id="97e0f-132">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="97e0f-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97e0f-133">OUTPUTS</span></span>

### <span data-ttu-id="97e0f-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="97e0f-134">System.Object</span></span>

## <span data-ttu-id="97e0f-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97e0f-135">NOTES</span></span>

## <span data-ttu-id="97e0f-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97e0f-136">RELATED LINKS</span></span>

