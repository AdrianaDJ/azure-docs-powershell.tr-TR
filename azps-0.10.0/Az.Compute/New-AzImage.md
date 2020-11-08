---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzImage.md
ms.openlocfilehash: 25e808926bf58bf11929b8e2d8218f517d1832ca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936978"
---
# <span data-ttu-id="fbcfa-101">New-AzImage</span><span class="sxs-lookup"><span data-stu-id="fbcfa-101">New-AzImage</span></span>

## <span data-ttu-id="fbcfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbcfa-102">SYNOPSIS</span></span>
<span data-ttu-id="fbcfa-103">Görüntü oluşturma.</span><span class="sxs-lookup"><span data-stu-id="fbcfa-103">Creats an image.</span></span>

## <span data-ttu-id="fbcfa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fbcfa-104">SYNTAX</span></span>

```
New-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbcfa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fbcfa-105">DESCRIPTION</span></span>
<span data-ttu-id="fbcfa-106">**Yeni-Azgörüntü** cmdlet 'i bir resim oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fbcfa-106">The **New-AzImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="fbcfa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fbcfa-107">EXAMPLES</span></span>

### <span data-ttu-id="fbcfa-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fbcfa-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="fbcfa-109">İlk komut bir resim nesnesi oluşturur ve $imageConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fbcfa-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="fbcfa-110">Sonraki üç komut, $osDiskVhdUri, $dataDiskVhdUri 1 ve $dataDiskVhdUri 2 değişkenlerine işletim sistemi diskinin ve iki veri diskinin yollarını atar.</span><span class="sxs-lookup"><span data-stu-id="fbcfa-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="fbcfa-111">Bu yaklaşım yalnızca aşağıdaki komutların okunurluğu için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fbcfa-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="fbcfa-112">Sonraki üç komut, $imageConfig depolanan resme bir işletim sistemi diski ve iki veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="fbcfa-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="fbcfa-113">Her diskin URI 'SI $osDiskVhdUri, $dataDiskVhdUri 1 ve $dataDiskVhdUri 2 ' de depolanır.</span><span class="sxs-lookup"><span data-stu-id="fbcfa-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="fbcfa-114">Son komutu, ' ResourceGroup01 ' kaynak grubunda ' ImageName01 ' adlı bir resim oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fbcfa-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="fbcfa-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fbcfa-115">PARAMETERS</span></span>

### <span data-ttu-id="fbcfa-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="fbcfa-116">-AsJob</span></span>
<span data-ttu-id="fbcfa-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="fbcfa-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbcfa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbcfa-118">-DefaultProfile</span></span>
<span data-ttu-id="fbcfa-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fbcfa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbcfa-120">-Image</span><span class="sxs-lookup"><span data-stu-id="fbcfa-120">-Image</span></span>
<span data-ttu-id="fbcfa-121">Yerel bir resim nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbcfa-121">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbcfa-122">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="fbcfa-122">-ImageName</span></span>
<span data-ttu-id="fbcfa-123">Bir resmin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbcfa-123">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="fbcfa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbcfa-124">-ResourceGroupName</span></span>
<span data-ttu-id="fbcfa-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbcfa-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fbcfa-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="fbcfa-126">-Confirm</span></span>
<span data-ttu-id="fbcfa-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fbcfa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbcfa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbcfa-128">-WhatIf</span></span>
<span data-ttu-id="fbcfa-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fbcfa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbcfa-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fbcfa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbcfa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbcfa-131">CommonParameters</span></span>
<span data-ttu-id="fbcfa-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fbcfa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbcfa-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbcfa-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbcfa-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fbcfa-134">INPUTS</span></span>

### <span data-ttu-id="fbcfa-135">System. String</span><span class="sxs-lookup"><span data-stu-id="fbcfa-135">System.String</span></span>
<span data-ttu-id="fbcfa-136">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psımage</span><span class="sxs-lookup"><span data-stu-id="fbcfa-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="fbcfa-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fbcfa-137">OUTPUTS</span></span>

### <span data-ttu-id="fbcfa-138">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psımage</span><span class="sxs-lookup"><span data-stu-id="fbcfa-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="fbcfa-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="fbcfa-139">System.Object</span></span>

## <span data-ttu-id="fbcfa-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fbcfa-140">NOTES</span></span>

## <span data-ttu-id="fbcfa-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fbcfa-141">RELATED LINKS</span></span>
