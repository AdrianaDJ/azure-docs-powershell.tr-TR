---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermimageconfig
schema: 2.0.0
ms.openlocfilehash: ef9fc830b59568ad039b265fb182dbbdbd13a00d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938983"
---
# <span data-ttu-id="cc8e1-101">New-AzureRmImageConfig</span><span class="sxs-lookup"><span data-stu-id="cc8e1-101">New-AzureRmImageConfig</span></span>

## <span data-ttu-id="cc8e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc8e1-102">SYNOPSIS</span></span>
<span data-ttu-id="cc8e1-103">Yapılandırılabilir bir resim nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cc8e1-103">Creates a configurable image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc8e1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cc8e1-104">SYNTAX</span></span>

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc8e1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cc8e1-105">DESCRIPTION</span></span>
<span data-ttu-id="cc8e1-106">**Yeni-AzureRmImageConfig** cmdlet 'i, yapılandırılabilir bir resim nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cc8e1-106">The **New-AzureRmImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="cc8e1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cc8e1-107">EXAMPLES</span></span>

### <span data-ttu-id="cc8e1-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cc8e1-108">Example 1</span></span>
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

<span data-ttu-id="cc8e1-109">İlk komut bir resim nesnesi oluşturur ve $imageConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cc8e1-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="cc8e1-110">Sonraki üç komut, $osDiskVhdUri, $dataDiskVhdUri 1 ve $dataDiskVhdUri 2 değişkenlerine işletim sistemi diskinin ve iki veri diskinin yollarını atar.</span><span class="sxs-lookup"><span data-stu-id="cc8e1-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="cc8e1-111">Bu yaklaşım yalnızca aşağıdaki komutların okunurluğu için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cc8e1-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="cc8e1-112">Sonraki üç komut, $imageConfig depolanan resme bir işletim sistemi diski ve iki veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="cc8e1-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="cc8e1-113">Her diskin URI 'SI $osDiskVhdUri, $dataDiskVhdUri 1 ve $dataDiskVhdUri 2 ' de depolanır.</span><span class="sxs-lookup"><span data-stu-id="cc8e1-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="cc8e1-114">Son komutu, ' ResourceGroup01 ' kaynak grubunda ' ImageName01 ' adlı bir resim oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cc8e1-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="cc8e1-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cc8e1-115">PARAMETERS</span></span>

### <span data-ttu-id="cc8e1-116">-Datadısk</span><span class="sxs-lookup"><span data-stu-id="cc8e1-116">-DataDisk</span></span>
<span data-ttu-id="cc8e1-117">Veri diski nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc8e1-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="cc8e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc8e1-118">-DefaultProfile</span></span>
<span data-ttu-id="cc8e1-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cc8e1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc8e1-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="cc8e1-120">-Location</span></span>
<span data-ttu-id="cc8e1-121">Bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc8e1-121">Specifies a location.</span></span>

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

### <span data-ttu-id="cc8e1-122">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="cc8e1-122">-OsDisk</span></span>
<span data-ttu-id="cc8e1-123">İşletim sistemi disketini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc8e1-123">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="cc8e1-124">-Sourcevirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="cc8e1-124">-SourceVirtualMachineId</span></span>
<span data-ttu-id="cc8e1-125">Kaynak sanal makine KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc8e1-125">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="cc8e1-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="cc8e1-126">-Tag</span></span>
<span data-ttu-id="cc8e1-127">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="cc8e1-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cc8e1-128">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="cc8e1-128">For example:</span></span>

<span data-ttu-id="cc8e1-129">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="cc8e1-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="cc8e1-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="cc8e1-130">-Confirm</span></span>
<span data-ttu-id="cc8e1-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cc8e1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc8e1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc8e1-132">-WhatIf</span></span>
<span data-ttu-id="cc8e1-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cc8e1-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc8e1-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cc8e1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc8e1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc8e1-135">CommonParameters</span></span>
<span data-ttu-id="cc8e1-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cc8e1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc8e1-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc8e1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc8e1-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cc8e1-138">INPUTS</span></span>

### <span data-ttu-id="cc8e1-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cc8e1-139">None</span></span>
<span data-ttu-id="cc8e1-140">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="cc8e1-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cc8e1-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cc8e1-141">OUTPUTS</span></span>

### <span data-ttu-id="cc8e1-142">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psımage</span><span class="sxs-lookup"><span data-stu-id="cc8e1-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="cc8e1-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cc8e1-143">NOTES</span></span>

## <span data-ttu-id="cc8e1-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cc8e1-144">RELATED LINKS</span></span>

