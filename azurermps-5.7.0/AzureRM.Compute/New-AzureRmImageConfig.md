---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
ms.openlocfilehash: 7c0f89d9c33dca961b822de62c05158a53195767
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594121"
---
# <span data-ttu-id="5e906-101">New-AzureRmImageConfig</span><span class="sxs-lookup"><span data-stu-id="5e906-101">New-AzureRmImageConfig</span></span>

## <span data-ttu-id="5e906-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e906-102">SYNOPSIS</span></span>
<span data-ttu-id="5e906-103">Yapılandırılabilir bir resim nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5e906-103">Creates a configurable image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e906-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e906-104">SYNTAX</span></span>

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e906-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e906-105">DESCRIPTION</span></span>
<span data-ttu-id="5e906-106">**Yeni-AzureRmImageConfig** cmdlet 'i, yapılandırılabilir bir resim nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5e906-106">The **New-AzureRmImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="5e906-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e906-107">EXAMPLES</span></span>

### <span data-ttu-id="5e906-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5e906-108">Example 1</span></span>
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

<span data-ttu-id="5e906-109">İlk komut bir resim nesnesi oluşturur ve $imageConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5e906-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="5e906-110">Sonraki üç komut, $osDiskVhdUri, $dataDiskVhdUri 1 ve $dataDiskVhdUri 2 değişkenlerine işletim sistemi diskinin ve iki veri diskinin yollarını atar.</span><span class="sxs-lookup"><span data-stu-id="5e906-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="5e906-111">Bu yaklaşım yalnızca aşağıdaki komutların okunurluğu için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5e906-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="5e906-112">Sonraki üç komut, $imageConfig depolanan resme bir işletim sistemi diski ve iki veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="5e906-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="5e906-113">Her diskin URI 'SI $osDiskVhdUri, $dataDiskVhdUri 1 ve $dataDiskVhdUri 2 ' de depolanır.</span><span class="sxs-lookup"><span data-stu-id="5e906-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="5e906-114">Son komutu, ' ResourceGroup01 ' kaynak grubunda ' ImageName01 ' adlı bir resim oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5e906-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="5e906-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e906-115">PARAMETERS</span></span>

### <span data-ttu-id="5e906-116">-Datadısk</span><span class="sxs-lookup"><span data-stu-id="5e906-116">-DataDisk</span></span>
<span data-ttu-id="5e906-117">Veri diski nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e906-117">Specifies the data disk object.</span></span>

```yaml
Type: ImageDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e906-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="5e906-118">-Location</span></span>
<span data-ttu-id="5e906-119">Bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e906-119">Specifies a location.</span></span>

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

### <span data-ttu-id="5e906-120">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="5e906-120">-OsDisk</span></span>
<span data-ttu-id="5e906-121">İşletim sistemi disketini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e906-121">Specifies the operating system Disk.</span></span>

```yaml
Type: ImageOSDisk
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e906-122">-Sourcevirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="5e906-122">-SourceVirtualMachineId</span></span>
<span data-ttu-id="5e906-123">Kaynak sanal makine KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e906-123">Specifies the source virtual machine ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e906-124">Etiketli</span><span class="sxs-lookup"><span data-stu-id="5e906-124">-Tag</span></span>
<span data-ttu-id="5e906-125">Kaynakların ve kaynak gruplarının ad-değer çiftleri kümesiyle etiketlenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e906-125">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e906-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="5e906-126">-Confirm</span></span>
<span data-ttu-id="5e906-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5e906-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e906-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e906-128">-WhatIf</span></span>
<span data-ttu-id="5e906-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e906-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e906-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5e906-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e906-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e906-131">CommonParameters</span></span>
<span data-ttu-id="5e906-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e906-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e906-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e906-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e906-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e906-134">INPUTS</span></span>

### <span data-ttu-id="5e906-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5e906-135">System.String</span></span>
<span data-ttu-id="5e906-136">System. topluluklar. Hashtable Microsoft. Azure. Management. COMPUTE. modeller. ımasdısk Microsoft. Azure. Management. COMPUTE. modeller. ımagedatadısk []</span><span class="sxs-lookup"><span data-stu-id="5e906-136">System.Collections.Hashtable Microsoft.Azure.Management.Compute.Models.ImageOSDisk Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="5e906-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e906-137">OUTPUTS</span></span>

### <span data-ttu-id="5e906-138">Microsoft. Azure. Management. COMPUTE. modeller. Image</span><span class="sxs-lookup"><span data-stu-id="5e906-138">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="5e906-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e906-139">NOTES</span></span>

## <span data-ttu-id="5e906-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e906-140">RELATED LINKS</span></span>

