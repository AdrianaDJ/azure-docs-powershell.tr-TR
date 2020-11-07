---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/save-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Save-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Save-AzureRmVhd.md
ms.openlocfilehash: db2148be139130f5963214c5e66809a3e66a22ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592036"
---
# <span data-ttu-id="b5537-101">Save-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="b5537-101">Save-AzureRmVhd</span></span>

## <span data-ttu-id="b5537-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5537-102">SYNOPSIS</span></span>
<span data-ttu-id="b5537-103">İndirilen. vhd yansımalarını yerel olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="b5537-103">Saves downloaded .vhd images locally.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5537-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5537-104">SYNTAX</span></span>

### <span data-ttu-id="b5537-105">ResourceGroupParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b5537-105">ResourceGroupParameterSetName</span></span>
```
Save-AzureRmVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5537-106">StorageKeyParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b5537-106">StorageKeyParameterSetName</span></span>
```
Save-AzureRmVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5537-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5537-107">DESCRIPTION</span></span>
<span data-ttu-id="b5537-108">**Save-AzureRmVhd** cmdlet 'i, bir dosyada depolanan bir blob 'dan. vhd resimlerini kaydeder.</span><span class="sxs-lookup"><span data-stu-id="b5537-108">The **Save-AzureRmVhd** cmdlet saves .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="b5537-109">İşlemin kullandığı Downloader iş parçacıklarının sayısını ve var olan bir dosyayı değiştirip değiştirmeyeceğinizi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5537-109">You can specify the number of downloader threads that the process uses and whether to replace a file that already exists.</span></span>
<span data-ttu-id="b5537-110">Bu cmdlet içeriği olduğu gibi indirir.</span><span class="sxs-lookup"><span data-stu-id="b5537-110">This cmdlet downloads content as it is.</span></span>
<span data-ttu-id="b5537-111">Herhangi bir sanal sabit disk (VHD) biçim dönüştürmesi uygulamaz.</span><span class="sxs-lookup"><span data-stu-id="b5537-111">It does not apply any Virtual Hard Disk (VHD) format conversion.</span></span>

## <span data-ttu-id="b5537-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5537-112">EXAMPLES</span></span>

### <span data-ttu-id="b5537-113">Örnek 1: resim Indirme</span><span class="sxs-lookup"><span data-stu-id="b5537-113">Example 1: Download an image</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

<span data-ttu-id="b5537-114">Bu komut. vhd dosyasını indirir ve C:\vhd\win7ımage.vhdyerel yolunda depolar.</span><span class="sxs-lookup"><span data-stu-id="b5537-114">This command downloads a .vhd file, and stores it in the local path C:\vhd\Win7Image.vhd.</span></span>

### <span data-ttu-id="b5537-115">Örnek 2: bir resmi Indirme ve yerel dosyanın üzerine yazma</span><span class="sxs-lookup"><span data-stu-id="b5537-115">Example 2: Download an image and overwrite the local file</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

<span data-ttu-id="b5537-116">Bu komut. vhd dosyasını indirir ve yerel yolda depolar.</span><span class="sxs-lookup"><span data-stu-id="b5537-116">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="b5537-117">Komut, *overwrite* parametresini içerir.</span><span class="sxs-lookup"><span data-stu-id="b5537-117">The command includes the *Overwrite* parameter.</span></span>
<span data-ttu-id="b5537-118">Bu nedenle, C:\vhd\wın7ımage.VHD zaten varsa bu komut bunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b5537-118">Therefore, if C:\vhd\Win7Image.vhd already exists, this command replaces it.</span></span>

### <span data-ttu-id="b5537-119">Örnek 3: belirtilen sayıda iş parçacığı kullanarak görüntü Indirme</span><span class="sxs-lookup"><span data-stu-id="b5537-119">Example 3: Download an image by using a specified number of threads</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

<span data-ttu-id="b5537-120">Bu komut. vhd dosyasını indirir ve yerel yolda depolar.</span><span class="sxs-lookup"><span data-stu-id="b5537-120">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="b5537-121">Komut, *NesneSayısı* parametresi için 32 değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5537-121">The command specifies a value of 32 for the *NumberOfThreads* parameter.</span></span>
<span data-ttu-id="b5537-122">Bu nedenle, cmdlet bu eylem için 32 iş parçacıklarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="b5537-122">Therefore, the cmdlet uses 32 threads for this action.</span></span>

### <span data-ttu-id="b5537-123">Örnek 4: bir resmi Indirme ve depolama tuşunu belirtme</span><span class="sxs-lookup"><span data-stu-id="b5537-123">Example 4: Download an image and specify the storage key</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

<span data-ttu-id="b5537-124">Bu komut. vhd dosyasını indirir ve depolama anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5537-124">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="b5537-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5537-125">PARAMETERS</span></span>

### <span data-ttu-id="b5537-126">-Iş</span><span class="sxs-lookup"><span data-stu-id="b5537-126">-AsJob</span></span>
<span data-ttu-id="b5537-127">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="b5537-127">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b5537-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5537-128">-DefaultProfile</span></span>
<span data-ttu-id="b5537-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b5537-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5537-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="b5537-130">-LocalFilePath</span></span>
<span data-ttu-id="b5537-131">Kaydedilen yansımanın yerel dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5537-131">Specifies the local file path of the saved image.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5537-132">-Iş parçacıkları</span><span class="sxs-lookup"><span data-stu-id="b5537-132">-NumberOfThreads</span></span>
<span data-ttu-id="b5537-133">İndirme sırasında bu cmdlet 'in kullandığı indirme iş parçacıklarının sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5537-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5537-134">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="b5537-134">-OverWrite</span></span>
<span data-ttu-id="b5537-135">Bu cmdlet 'in, varsa *LocalFilePath* dosyası tarafından belirtilen dosyayı değiştirdiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="b5537-135">Indicates that this cmdlet replaces the file specified by *LocalFilePath* file if it exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5537-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5537-136">-ResourceGroupName</span></span>
<span data-ttu-id="b5537-137">Depolama hesabının kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5537-137">Specifies the name of the resource group of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5537-138">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="b5537-138">-SourceUri</span></span>
<span data-ttu-id="b5537-139">Blob 'un içindeki Tekdüzen Kaynak tanımlayıcısını (URI) belirtir `Azure` .</span><span class="sxs-lookup"><span data-stu-id="b5537-139">Specifies the Uniform Resource Identifier (URI) of the blob in `Azure`.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: src, Source

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5537-140">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="b5537-140">-StorageKey</span></span>
<span data-ttu-id="b5537-141">BLOB depolama hesabının depolama anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5537-141">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="b5537-142">Bir anahtar belirtmezseniz, bu cmdlet Azure 'dan *SourceUri* 'deki hesabın depolama anahtarını belirlemeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="b5537-142">If you do not specify a key, this cmdlet attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageKeyParameterSetName
Aliases: sk

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5537-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5537-143">CommonParameters</span></span>
<span data-ttu-id="b5537-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5537-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5537-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5537-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5537-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5537-146">INPUTS</span></span>

### <span data-ttu-id="b5537-147">System. String</span><span class="sxs-lookup"><span data-stu-id="b5537-147">System.String</span></span>

### <span data-ttu-id="b5537-148">System. Uri</span><span class="sxs-lookup"><span data-stu-id="b5537-148">System.Uri</span></span>

## <span data-ttu-id="b5537-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5537-149">OUTPUTS</span></span>

### <span data-ttu-id="b5537-150">Microsoft. Azure. Commands. COMPUTE. model. VhdDownloadContext</span><span class="sxs-lookup"><span data-stu-id="b5537-150">Microsoft.Azure.Commands.Compute.Models.VhdDownloadContext</span></span>

## <span data-ttu-id="b5537-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5537-151">NOTES</span></span>

## <span data-ttu-id="b5537-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5537-152">RELATED LINKS</span></span>

[<span data-ttu-id="b5537-153">Add-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="b5537-153">Add-AzureRmVhd</span></span>](./Add-AzureRMVhd.md)

