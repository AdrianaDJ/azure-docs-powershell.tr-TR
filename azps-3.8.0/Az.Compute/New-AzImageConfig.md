---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: 56834ad267b4ac60613afc4dbd08499eae212512
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096932"
---
# <span data-ttu-id="fede0-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="fede0-101">New-AzImageConfig</span></span>

## <span data-ttu-id="fede0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fede0-102">SYNOPSIS</span></span>
<span data-ttu-id="fede0-103">Yapılandırılabilir bir resim nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fede0-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="fede0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fede0-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-HyperVGeneration <String>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fede0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fede0-105">DESCRIPTION</span></span>
<span data-ttu-id="fede0-106">**Yeni-Azımageconfig** cmdlet 'i yapılandırılabilir bir resim nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fede0-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="fede0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fede0-107">EXAMPLES</span></span>

### <span data-ttu-id="fede0-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fede0-108">Example 1</span></span>
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

<span data-ttu-id="fede0-109">İlk komut bir resim nesnesi oluşturur ve $imageConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fede0-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="fede0-110">Sonraki üç komut, $osDiskVhdUri, $dataDiskVhdUri 1 ve $dataDiskVhdUri 2 değişkenlerine işletim sistemi diskinin ve iki veri diskinin yollarını atar.</span><span class="sxs-lookup"><span data-stu-id="fede0-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="fede0-111">Bu yaklaşım yalnızca aşağıdaki komutların okunurluğu için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fede0-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="fede0-112">Sonraki üç komut, $imageConfig depolanan resme bir işletim sistemi diski ve iki veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="fede0-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="fede0-113">Her diskin URI 'SI $osDiskVhdUri, $dataDiskVhdUri 1 ve $dataDiskVhdUri 2 ' de depolanır.</span><span class="sxs-lookup"><span data-stu-id="fede0-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="fede0-114">Son komutu, ' ResourceGroup01 ' kaynak grubunda ' ImageName01 ' adlı bir resim oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fede0-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="fede0-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fede0-115">PARAMETERS</span></span>

### <span data-ttu-id="fede0-116">-Datadısk</span><span class="sxs-lookup"><span data-stu-id="fede0-116">-DataDisk</span></span>
<span data-ttu-id="fede0-117">Veri diski nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fede0-117">Specifies the data disk object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fede0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fede0-118">-DefaultProfile</span></span>
<span data-ttu-id="fede0-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fede0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fede0-120">-Hiper VCR</span><span class="sxs-lookup"><span data-stu-id="fede0-120">-HyperVGeneration</span></span>
<span data-ttu-id="fede0-121">Yansımadan oluşturulan sanal makine için HyperVGeneration türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fede0-121">Specifies the HyperVGeneration Type for the virtual machine created from the image.</span></span>  <span data-ttu-id="fede0-122">İzin verilen değerler v1 ve v2.</span><span class="sxs-lookup"><span data-stu-id="fede0-122">Allowed values are V1 and V2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fede0-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="fede0-123">-Location</span></span>
<span data-ttu-id="fede0-124">Bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="fede0-124">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fede0-125">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="fede0-125">-OsDisk</span></span>
<span data-ttu-id="fede0-126">İşletim sistemi disketini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fede0-126">Specifies the operating system Disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageOSDisk
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fede0-127">-Sourcevirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="fede0-127">-SourceVirtualMachineId</span></span>
<span data-ttu-id="fede0-128">Kaynak sanal makine KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fede0-128">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="fede0-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="fede0-129">-Tag</span></span>
<span data-ttu-id="fede0-130">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="fede0-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fede0-131">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="fede0-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fede0-132">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="fede0-132">-ZoneResilient</span></span>
<span data-ttu-id="fede0-133">Bölge esnek özelliğini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="fede0-133">Enable zone resilient</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fede0-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="fede0-134">-Confirm</span></span>
<span data-ttu-id="fede0-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fede0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fede0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fede0-136">-WhatIf</span></span>
<span data-ttu-id="fede0-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fede0-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fede0-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fede0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fede0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fede0-139">CommonParameters</span></span>
<span data-ttu-id="fede0-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fede0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fede0-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fede0-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fede0-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fede0-142">INPUTS</span></span>

### <span data-ttu-id="fede0-143">System. String</span><span class="sxs-lookup"><span data-stu-id="fede0-143">System.String</span></span>

### <span data-ttu-id="fede0-144">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fede0-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fede0-145">Microsoft. Azure. Management. COMPUTE. model. ımasdisk</span><span class="sxs-lookup"><span data-stu-id="fede0-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="fede0-146">Microsoft. Azure. Management. COMPUTE. modeller. ımagedatadısk []</span><span class="sxs-lookup"><span data-stu-id="fede0-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="fede0-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fede0-147">OUTPUTS</span></span>

### <span data-ttu-id="fede0-148">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psımage</span><span class="sxs-lookup"><span data-stu-id="fede0-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="fede0-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fede0-149">NOTES</span></span>

## <span data-ttu-id="fede0-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fede0-150">RELATED LINKS</span></span>
