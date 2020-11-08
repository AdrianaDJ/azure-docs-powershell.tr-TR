---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E4660D0A-26CB-488C-9A29-3ED94A0DCDA2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e62cb7ed272a5c0d5ff4ff0ecbafe30a0c5ee9e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105461"
---
# <span data-ttu-id="fa8f2-101">Save-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="fa8f2-101">Save-AzureVhd</span></span>

## <span data-ttu-id="fa8f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa8f2-102">SYNOPSIS</span></span>
<span data-ttu-id="fa8f2-103">. Vhd resimlerinin indirilmesini mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="fa8f2-103">Enables download of .vhd images.</span></span>

## <span data-ttu-id="fa8f2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa8f2-104">SYNTAX</span></span>

```
Save-AzureVhd [-Source] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfThreads] <Int32>] [[-StorageKey] <String>]
 [-OverWrite] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fa8f2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa8f2-105">DESCRIPTION</span></span>
<span data-ttu-id="fa8f2-106">**Save-AzureVhd** cmdlet 'i, dosya içinde saklandıkları blob 'dan. vhd görüntülerinin indirilmesini mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="fa8f2-106">The **Save-AzureVhd** cmdlet enables download of .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="fa8f2-107">Belirtilen dosya yolunda zaten var olan dosyayı kullanan veya üzerine yazılan Downloader iş parçacıklarının sayısını belirterek indirme işlemini yapılandırmak için parametreler içerir.</span><span class="sxs-lookup"><span data-stu-id="fa8f2-107">It has parameters to configure the download process by specifying the number of downloader threads that are used or overwriting the file which already exists in the specified file path.</span></span>

<span data-ttu-id="fa8f2-108">**Save-AzureVhd** hiçbir VHD biçim dönüştürmesi yapmaz ve BLOB olduğu gibi indirilir.</span><span class="sxs-lookup"><span data-stu-id="fa8f2-108">**Save-AzureVhd** does not do any VHD format conversion and the blob is downloaded as it is.</span></span>

## <span data-ttu-id="fa8f2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa8f2-109">EXAMPLES</span></span>

### <span data-ttu-id="fa8f2-110">Örnek 1: VHD dosyasını Indirme</span><span class="sxs-lookup"><span data-stu-id="fa8f2-110">Example 1: Download a VHD file</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="fa8f2-111">Bu komut. vhd dosyasını indirir.</span><span class="sxs-lookup"><span data-stu-id="fa8f2-111">This command downloads a .vhd file.</span></span>

### <span data-ttu-id="fa8f2-112">Örnek 2: bir VHD dosyasını Indirme ve yerel dosyanın üzerine yazma</span><span class="sxs-lookup"><span data-stu-id="fa8f2-112">Example 2: Download a VHD file and overwrite the local file</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="fa8f2-113">Bu komut. vhd dosyasını indirir ve Hedef yoldaki dosyaların üzerine yazar.</span><span class="sxs-lookup"><span data-stu-id="fa8f2-113">This command downloads a .vhd file and overwrites any file in the destination path.</span></span>

### <span data-ttu-id="fa8f2-114">Örnek 3: bir VHD dosyası Indirin ve iş parçacıklarının sayısını belirtin</span><span class="sxs-lookup"><span data-stu-id="fa8f2-114">Example 3: Download a VHD file and specify the number of threads</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="fa8f2-115">Bu komut. vhd dosyasını indirir ve iş parçacıklarının sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa8f2-115">This command downloads a .vhd file and specifies the number of threads.</span></span>

### <span data-ttu-id="fa8f2-116">Örnek 4: bir VHD dosyasını Indirin ve depolama anahtarını belirtin</span><span class="sxs-lookup"><span data-stu-id="fa8f2-116">Example 4: Download a VHD file and specify the storage key</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw=="
```

<span data-ttu-id="fa8f2-117">Bu komut. vhd dosyasını indirir ve depolama anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa8f2-117">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="fa8f2-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa8f2-118">PARAMETERS</span></span>

### <span data-ttu-id="fa8f2-119">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="fa8f2-119">-InformationAction</span></span>
<span data-ttu-id="fa8f2-120">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa8f2-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fa8f2-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fa8f2-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fa8f2-122">'A</span><span class="sxs-lookup"><span data-stu-id="fa8f2-122">Continue</span></span>
- <span data-ttu-id="fa8f2-123">Manıza</span><span class="sxs-lookup"><span data-stu-id="fa8f2-123">Ignore</span></span>
- <span data-ttu-id="fa8f2-124">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="fa8f2-124">Inquire</span></span>
- <span data-ttu-id="fa8f2-125">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="fa8f2-125">SilentlyContinue</span></span>
- <span data-ttu-id="fa8f2-126">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="fa8f2-126">Stop</span></span>
- <span data-ttu-id="fa8f2-127">Biliriz</span><span class="sxs-lookup"><span data-stu-id="fa8f2-127">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa8f2-128">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="fa8f2-128">-InformationVariable</span></span>
<span data-ttu-id="fa8f2-129">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa8f2-129">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa8f2-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="fa8f2-130">-LocalFilePath</span></span>
<span data-ttu-id="fa8f2-131">Yerel dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa8f2-131">Specifies the local file path.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa8f2-132">-Iş parçacıkları</span><span class="sxs-lookup"><span data-stu-id="fa8f2-132">-NumberOfThreads</span></span>
<span data-ttu-id="fa8f2-133">İndirme sırasında bu cmdlet 'in kullandığı indirme iş parçacıklarının sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa8f2-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa8f2-134">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="fa8f2-134">-OverWrite</span></span>
<span data-ttu-id="fa8f2-135">Bu cmdlet 'in, *LocalFilePath* dosyası varsa belirttiği dosyayı sildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa8f2-135">Specifies that this cmdlet deletes the file specified by *LocalFilePath* file if it exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa8f2-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="fa8f2-136">-Profile</span></span>
<span data-ttu-id="fa8f2-137">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa8f2-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fa8f2-138">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="fa8f2-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa8f2-139">-Kaynak</span><span class="sxs-lookup"><span data-stu-id="fa8f2-139">-Source</span></span>
<span data-ttu-id="fa8f2-140">Blob 'daki Tekdüzen Kaynak tanımlayıcısını (URI) belirtir `Azure` .</span><span class="sxs-lookup"><span data-stu-id="fa8f2-140">Specifies the Uniform Resource Identifier (URI) to the blob in `Azure`.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: src

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa8f2-141">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="fa8f2-141">-StorageKey</span></span>
<span data-ttu-id="fa8f2-142">BLOB depolama hesabının depolama anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa8f2-142">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="fa8f2-143">Bu sağlanmadıysa, **Save-AzureVhd** , Azure 'Dan *SourceUri* 'deki hesabın depolama anahtarını belirlemeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="fa8f2-143">If it is not provided, **Save-AzureVhd** attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: sk

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa8f2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa8f2-144">CommonParameters</span></span>
<span data-ttu-id="fa8f2-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa8f2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa8f2-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa8f2-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa8f2-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa8f2-147">INPUTS</span></span>

## <span data-ttu-id="fa8f2-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa8f2-148">OUTPUTS</span></span>

## <span data-ttu-id="fa8f2-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa8f2-149">NOTES</span></span>

## <span data-ttu-id="fa8f2-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa8f2-150">RELATED LINKS</span></span>

[<span data-ttu-id="fa8f2-151">Add-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="fa8f2-151">Add-AzureVhd</span></span>](./Add-AzureVhd.md)


