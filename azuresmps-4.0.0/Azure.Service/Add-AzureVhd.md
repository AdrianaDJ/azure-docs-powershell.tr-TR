---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 99DC239C-EA68-4830-9345-762CD6A3F68C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 320b95add2806f48121151a71bdf36a572fa05a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105718"
---
# <span data-ttu-id="1bc46-101">Add-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="1bc46-101">Add-AzureVhd</span></span>

## <span data-ttu-id="1bc46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bc46-102">SYNOPSIS</span></span>
<span data-ttu-id="1bc46-103">Azure 'daki bulut depolama hesabında bir şirket içi bilgisayardan bir blob 'a VHD dosyası yükler.</span><span class="sxs-lookup"><span data-stu-id="1bc46-103">Uploads a VHD file from an on-premise computer to a blob in a cloud storage account in Azure.</span></span>

## <span data-ttu-id="1bc46-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1bc46-104">SYNTAX</span></span>

```
Add-AzureVhd [-Destination] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfUploaderThreads] <Int32>]
 [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1bc46-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1bc46-105">DESCRIPTION</span></span>
<span data-ttu-id="1bc46-106">**Add-AzureVhd** cmdlet 'i şirket içi sanal sabit DISK (VHD) görüntülerine, sabit. vhd yansımaları olarak bir BLOB depolama hesabına yükler.</span><span class="sxs-lookup"><span data-stu-id="1bc46-106">The **Add-AzureVhd** cmdlet uploads on premise Virtual hard disk (VHD) images to a blob storage account as fixed .vhd images.</span></span>
<span data-ttu-id="1bc46-107">Belirtilen hedef URI 'de zaten varolan bir blob 'un kullanacağı Uploader iş parçacıklarının sayısını belirtmek gibi karşıya yükleme işlemini yapılandırmak için parametreler içerir.</span><span class="sxs-lookup"><span data-stu-id="1bc46-107">It has parameters to configure the upload process such as specifying the number of uploader threads that will be used or overwriting a blob which already exists in the specified destination URI.</span></span>
<span data-ttu-id="1bc46-108">Şirket içi VHD görüntülerinde, daha önce karşıya yüklenen temel görüntülerin karşıya yüklenebilmesi gerekmeden fark Disk görüntülerinin yüklenebilmesi için düzeltme eki senaryosu da desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="1bc46-108">For on premise VHD images, patching scenario is also supported so that diff disk images can be uploaded without having to upload the already uploaded base images.</span></span> <span data-ttu-id="1bc46-109">Paylaşılan erişim Imzası (SAS) URI 'SI de desteklenir.</span><span class="sxs-lookup"><span data-stu-id="1bc46-109">Shared Access Signature (SAS) URI is also supported.</span></span>

## <span data-ttu-id="1bc46-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1bc46-110">EXAMPLES</span></span>

### <span data-ttu-id="1bc46-111">Örnek 1: VHD dosyası ekleme</span><span class="sxs-lookup"><span data-stu-id="1bc46-111">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="1bc46-112">Bu komut bir depolama hesabına. vhd dosyası ekler.</span><span class="sxs-lookup"><span data-stu-id="1bc46-112">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="1bc46-113">Örnek 2: VHD dosyası ekleme ve hedefin üzerine yazma</span><span class="sxs-lookup"><span data-stu-id="1bc46-113">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="1bc46-114">Bu komut bir depolama hesabına. vhd dosyası ekler.</span><span class="sxs-lookup"><span data-stu-id="1bc46-114">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="1bc46-115">Örnek 3: VHD dosyası ekleme ve iş parçacıklarının sayısını belirtme</span><span class="sxs-lookup"><span data-stu-id="1bc46-115">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="1bc46-116">Bu komut bir depolama hesabına. vhd dosyası ekler ve dosyayı karşıya yüklemek için kullanılacak iş parçacıklarının sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1bc46-116">This command adds a .vhd file to a storage account and specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="1bc46-117">Örnek 4: VHD dosyası ekleme ve SAS URI 'sini belirtme</span><span class="sxs-lookup"><span data-stu-id="1bc46-117">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01-09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveOSIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="1bc46-118">Bu komut bir depolama hesabına. vhd dosyası ekler ve SAS URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1bc46-118">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="1bc46-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1bc46-119">PARAMETERS</span></span>

### <span data-ttu-id="1bc46-120">-Baseımageuritopatch</span><span class="sxs-lookup"><span data-stu-id="1bc46-120">-BaseImageUriToPatch</span></span>
<span data-ttu-id="1bc46-121">Azure Blob depolamada temel görüntü blob 'una bir URI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1bc46-121">Specifies an URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="1bc46-122">URI girişinde SAS girişi de desteklenir.</span><span class="sxs-lookup"><span data-stu-id="1bc46-122">SAS in URI input is supported as well.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bc46-123">-Hedef</span><span class="sxs-lookup"><span data-stu-id="1bc46-123">-Destination</span></span>
<span data-ttu-id="1bc46-124">Microsoft Azure Blob depolamada bir blob URI 'SI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1bc46-124">Specifies a URI to a blob in Microsoft Azure Blob Storage.</span></span>
<span data-ttu-id="1bc46-125">URI girişinde SAS desteklenir.</span><span class="sxs-lookup"><span data-stu-id="1bc46-125">SAS in URI input is supported.</span></span>
<span data-ttu-id="1bc46-126">Ancak, düzeltme eki senaryolarında hedef SAS URI 'SI olamaz.</span><span class="sxs-lookup"><span data-stu-id="1bc46-126">However, in patching scenarios the destination cannot be a SAS URI.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bc46-127">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="1bc46-127">-InformationAction</span></span>
<span data-ttu-id="1bc46-128">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1bc46-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1bc46-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1bc46-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1bc46-130">'A</span><span class="sxs-lookup"><span data-stu-id="1bc46-130">Continue</span></span>
- <span data-ttu-id="1bc46-131">Manıza</span><span class="sxs-lookup"><span data-stu-id="1bc46-131">Ignore</span></span>
- <span data-ttu-id="1bc46-132">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="1bc46-132">Inquire</span></span>
- <span data-ttu-id="1bc46-133">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="1bc46-133">SilentlyContinue</span></span>
- <span data-ttu-id="1bc46-134">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="1bc46-134">Stop</span></span>
- <span data-ttu-id="1bc46-135">Biliriz</span><span class="sxs-lookup"><span data-stu-id="1bc46-135">Suspend</span></span>

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

### <span data-ttu-id="1bc46-136">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="1bc46-136">-InformationVariable</span></span>
<span data-ttu-id="1bc46-137">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="1bc46-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1bc46-138">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="1bc46-138">-LocalFilePath</span></span>
<span data-ttu-id="1bc46-139">Türleri. vhd dosyasının dosya yolu.</span><span class="sxs-lookup"><span data-stu-id="1bc46-139">Species the file path of the local .vhd file.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bc46-140">-Numberofof Loaderthreads</span><span class="sxs-lookup"><span data-stu-id="1bc46-140">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="1bc46-141">Karşıya yükleme için kullanılacak iş parçacıklarının sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1bc46-141">Specifies the number of threads to use for upload.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bc46-142">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="1bc46-142">-OverWrite</span></span>
<span data-ttu-id="1bc46-143">Varsa, bu cmdlet 'in belirtilen hedef URI 'de var olan blobu sildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1bc46-143">Specifies that this cmdlet deletes the existing blob in the specified destination URI if it exists.</span></span>

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

### <span data-ttu-id="1bc46-144">-Profil</span><span class="sxs-lookup"><span data-stu-id="1bc46-144">-Profile</span></span>
<span data-ttu-id="1bc46-145">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1bc46-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1bc46-146">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="1bc46-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1bc46-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bc46-147">CommonParameters</span></span>
<span data-ttu-id="1bc46-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1bc46-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bc46-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bc46-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bc46-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1bc46-150">INPUTS</span></span>

## <span data-ttu-id="1bc46-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1bc46-151">OUTPUTS</span></span>

## <span data-ttu-id="1bc46-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1bc46-152">NOTES</span></span>

## <span data-ttu-id="1bc46-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1bc46-153">RELATED LINKS</span></span>

[<span data-ttu-id="1bc46-154">Save-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="1bc46-154">Save-AzureVhd</span></span>](./Save-AzureVhd.md)


