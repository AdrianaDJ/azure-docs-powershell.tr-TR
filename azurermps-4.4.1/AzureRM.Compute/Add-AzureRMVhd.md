---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRMVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRMVhd.md
ms.openlocfilehash: 106f6d9ed794ac2e4595f480616fa2c64663e554
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594810"
---
# <span data-ttu-id="52ade-101">Add-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="52ade-101">Add-AzureRmVhd</span></span>

## <span data-ttu-id="52ade-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52ade-102">SYNOPSIS</span></span>
<span data-ttu-id="52ade-103">Azure 'daki bulut depolama hesabında bir şirket içi sanal makineden blob 'a sanal sabit disk yükler.</span><span class="sxs-lookup"><span data-stu-id="52ade-103">Uploads a virtual hard disk from an on-premises virtual machine to a blob in a cloud storage account in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52ade-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52ade-104">SYNTAX</span></span>

```
Add-AzureRmVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52ade-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="52ade-105">DESCRIPTION</span></span>
<span data-ttu-id="52ade-106">**Add-AzureRmVhd** cmdlet 'i, şirket içi sanal sabit diskleri. vhd dosya biçiminde, bir BLOB depolama hesabına sabit sanal sabit diskler olarak yükler.</span><span class="sxs-lookup"><span data-stu-id="52ade-106">The **Add-AzureRmVhd** cmdlet uploads on-premises virtual hard disks, in .vhd file format, to a blob storage account as fixed virtual hard disks.</span></span>
<span data-ttu-id="52ade-107">Kullanılacak olan Uploader iş parçacıklarının sayısını, belirtilen hedef URI 'de var olan bir bloonun üzerine yazacak şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52ade-107">You can configure the number of uploader threads that will be used or overwrite an existing blob in the specified destination URI.</span></span>
<span data-ttu-id="52ade-108">Ayrıca desteklenen şirket içi. vhd dosyasının düzeltme eki yüklenmiş bir sürümünü karşıya yükleyebilir.</span><span class="sxs-lookup"><span data-stu-id="52ade-108">Also supported is the ability to upload a patched version of an on-premises .vhd file.</span></span>
<span data-ttu-id="52ade-109">Bir temel sanal sabit disk zaten karşıya yüklendiğinde, temel görüntüyü içeren fark kayıt disklerini üst öğe olarak yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52ade-109">When a base virtual hard disk has already been uploaded, you can upload differencing disks that use the base image as the parent.</span></span>
<span data-ttu-id="52ade-110">Paylaşılan erişim imzası (SAS) URI 'SI de desteklenir.</span><span class="sxs-lookup"><span data-stu-id="52ade-110">Shared access signature (SAS) URI is supported also.</span></span>

## <span data-ttu-id="52ade-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52ade-111">EXAMPLES</span></span>

### <span data-ttu-id="52ade-112">Örnek 1: VHD dosyası ekleme</span><span class="sxs-lookup"><span data-stu-id="52ade-112">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="52ade-113">Bu komut bir depolama hesabına. vhd dosyası ekler.</span><span class="sxs-lookup"><span data-stu-id="52ade-113">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="52ade-114">Örnek 2: VHD dosyası ekleme ve hedefin üzerine yazma</span><span class="sxs-lookup"><span data-stu-id="52ade-114">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="52ade-115">Bu komut bir depolama hesabına. vhd dosyası ekler.</span><span class="sxs-lookup"><span data-stu-id="52ade-115">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="52ade-116">Komut mevcut bir dosyanın üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="52ade-116">The command overwrites an existing file.</span></span>

### <span data-ttu-id="52ade-117">Örnek 3: VHD dosyası ekleme ve iş parçacıklarının sayısını belirtme</span><span class="sxs-lookup"><span data-stu-id="52ade-117">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="52ade-118">Bu komut bir depolama hesabına. vhd dosyası ekler.</span><span class="sxs-lookup"><span data-stu-id="52ade-118">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="52ade-119">Komut, dosyayı karşıya yüklemek için kullanılacak iş parçacıklarının sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52ade-119">The command specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="52ade-120">Örnek 4: VHD dosyası ekleme ve SAS URI 'sini belirtme</span><span class="sxs-lookup"><span data-stu-id="52ade-120">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="52ade-121">Bu komut bir depolama hesabına. vhd dosyası ekler ve SAS URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="52ade-121">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="52ade-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52ade-122">PARAMETERS</span></span>

### <span data-ttu-id="52ade-123">-Baseımageuritopatch</span><span class="sxs-lookup"><span data-stu-id="52ade-123">-BaseImageUriToPatch</span></span>
<span data-ttu-id="52ade-124">Azure Blob depolamada temel görüntü blob 'una URI 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="52ade-124">Specifies the URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="52ade-125">Bu parametrenin değeri olarak SAS belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="52ade-125">An SAS can be specified as the value for this parameter.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ade-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52ade-126">-DefaultProfile</span></span>
<span data-ttu-id="52ade-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="52ade-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52ade-128">-Hedef</span><span class="sxs-lookup"><span data-stu-id="52ade-128">-Destination</span></span>
<span data-ttu-id="52ade-129">BLOB depolama alanındaki bir blob URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="52ade-129">Specifies the URI of a blob in Blob Storage.</span></span>
<span data-ttu-id="52ade-130">Parametre SAS URI 'yi destekler, ancak düzeltme senaryoları hedefi SAS URI olamaz.</span><span class="sxs-lookup"><span data-stu-id="52ade-130">The parameter supports SAS URI, although patching scenarios destination cannot be an SAS URI.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ade-131">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="52ade-131">-LocalFilePath</span></span>
<span data-ttu-id="52ade-132">Yerel. vhd dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="52ade-132">Specifies the path of the local .vhd file.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ade-133">-Numberofof Loaderthreads</span><span class="sxs-lookup"><span data-stu-id="52ade-133">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="52ade-134">. Vhd dosyası yüklenirken kullanılacak Uploader iş parçacıklarının sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52ade-134">Specifies the number of uploader threads to be used when uploading the .vhd file.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ade-135">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="52ade-135">-OverWrite</span></span>
<span data-ttu-id="52ade-136">Bu cmdlet 'in belirtilen hedef URI 'de var olan bir blobın üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="52ade-136">Indicates that this cmdlet overwrites an existing blob in the specified destination URI, if one exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ade-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52ade-137">-ResourceGroupName</span></span>
<span data-ttu-id="52ade-138">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52ade-138">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="52ade-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52ade-139">CommonParameters</span></span>
<span data-ttu-id="52ade-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52ade-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52ade-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52ade-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52ade-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52ade-142">INPUTS</span></span>

## <span data-ttu-id="52ade-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52ade-143">OUTPUTS</span></span>

## <span data-ttu-id="52ade-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52ade-144">NOTES</span></span>

## <span data-ttu-id="52ade-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52ade-145">RELATED LINKS</span></span>

[<span data-ttu-id="52ade-146">Kaydet-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="52ade-146">Save-AzureRmVhd</span></span>](./Save-AzureRmVhd.md)

