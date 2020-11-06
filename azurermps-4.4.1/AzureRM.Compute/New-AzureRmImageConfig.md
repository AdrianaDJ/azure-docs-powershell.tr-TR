---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
ms.openlocfilehash: a18fe089cba54f6cbf0d70469a17f2d8f797b2e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586978"
---
# <span data-ttu-id="a7d1b-101">New-AzureRmImageConfig</span><span class="sxs-lookup"><span data-stu-id="a7d1b-101">New-AzureRmImageConfig</span></span>

## <span data-ttu-id="a7d1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7d1b-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d1b-103">Yapılandırılabilir bir resim nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a7d1b-103">Creates a configurable image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7d1b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7d1b-104">SYNTAX</span></span>

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7d1b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7d1b-105">DESCRIPTION</span></span>
<span data-ttu-id="a7d1b-106">**Yeni-AzureRmImageConfig** cmdlet 'i, yapılandırılabilir bir resim nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a7d1b-106">The **New-AzureRmImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="a7d1b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7d1b-107">EXAMPLES</span></span>

### <span data-ttu-id="a7d1b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a7d1b-108">Example 1</span></span>
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

<span data-ttu-id="a7d1b-109">İlk komut bir resim nesnesi oluşturur ve $imageConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a7d1b-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="a7d1b-110">Sonraki üç komut, $osDiskVhdUri, $dataDiskVhdUri 1 ve $dataDiskVhdUri 2 değişkenlerine işletim sistemi diskinin ve iki veri diskinin yollarını atar.</span><span class="sxs-lookup"><span data-stu-id="a7d1b-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="a7d1b-111">Bu yaklaşım yalnızca aşağıdaki komutların okunurluğu için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a7d1b-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="a7d1b-112">Sonraki üç komut, $imageConfig depolanan resme bir işletim sistemi diski ve iki veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="a7d1b-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="a7d1b-113">Her diskin URI 'SI $osDiskVhdUri, $dataDiskVhdUri 1 ve $dataDiskVhdUri 2 ' de depolanır.</span><span class="sxs-lookup"><span data-stu-id="a7d1b-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="a7d1b-114">Son komutu, ' ResourceGroup01 ' kaynak grubunda ' ImageName01 ' adlı bir resim oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a7d1b-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a7d1b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7d1b-115">PARAMETERS</span></span>

### <span data-ttu-id="a7d1b-116">-Datadısk</span><span class="sxs-lookup"><span data-stu-id="a7d1b-116">-DataDisk</span></span>
<span data-ttu-id="a7d1b-117">Veri diski nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7d1b-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="a7d1b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d1b-118">-DefaultProfile</span></span>
<span data-ttu-id="a7d1b-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a7d1b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7d1b-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="a7d1b-120">-Location</span></span>
<span data-ttu-id="a7d1b-121">Bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7d1b-121">Specifies a location.</span></span>

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

### <span data-ttu-id="a7d1b-122">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="a7d1b-122">-OsDisk</span></span>
<span data-ttu-id="a7d1b-123">İşletim sistemi disketini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7d1b-123">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="a7d1b-124">-Sourcevirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="a7d1b-124">-SourceVirtualMachineId</span></span>
<span data-ttu-id="a7d1b-125">Kaynak sanal makine KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7d1b-125">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="a7d1b-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a7d1b-126">-Tag</span></span>
<span data-ttu-id="a7d1b-127">Kaynakların ve kaynak gruplarının ad-değer çiftleri kümesiyle etiketlenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7d1b-127">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

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

### <span data-ttu-id="a7d1b-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="a7d1b-128">-Confirm</span></span>
<span data-ttu-id="a7d1b-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a7d1b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7d1b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7d1b-130">-WhatIf</span></span>
<span data-ttu-id="a7d1b-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a7d1b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7d1b-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a7d1b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7d1b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d1b-133">CommonParameters</span></span>
<span data-ttu-id="a7d1b-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7d1b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d1b-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7d1b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d1b-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7d1b-136">INPUTS</span></span>

### <span data-ttu-id="a7d1b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a7d1b-137">System.String</span></span>
<span data-ttu-id="a7d1b-138">System. topluluklar. Hashtable Microsoft. Azure. Management. COMPUTE. modeller. ımasdısk Microsoft. Azure. Management. COMPUTE. modeller. ımagedatadısk []</span><span class="sxs-lookup"><span data-stu-id="a7d1b-138">System.Collections.Hashtable Microsoft.Azure.Management.Compute.Models.ImageOSDisk Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="a7d1b-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7d1b-139">OUTPUTS</span></span>

### <span data-ttu-id="a7d1b-140">Microsoft. Azure. Management. COMPUTE. modeller. Image</span><span class="sxs-lookup"><span data-stu-id="a7d1b-140">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="a7d1b-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7d1b-141">NOTES</span></span>

## <span data-ttu-id="a7d1b-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7d1b-142">RELATED LINKS</span></span>

