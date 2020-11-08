---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 16A34F31-1C61-4911-8C1F-9F82683524A1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 775d2deff8a83e758d48fb9328bf4156b142d20c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106393"
---
# <span data-ttu-id="186b9-101">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="186b9-101">Add-AzureDisk</span></span>

## <span data-ttu-id="186b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="186b9-102">SYNOPSIS</span></span>
<span data-ttu-id="186b9-103">Azure disk deposuna bir disk ekler.</span><span class="sxs-lookup"><span data-stu-id="186b9-103">Adds a disk to the Azure disk repository.</span></span>

## <span data-ttu-id="186b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="186b9-104">SYNTAX</span></span>

```
Add-AzureDisk [-DiskName] <String> [-MediaLocation] <String> [-Label <String>] [-OS <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="186b9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="186b9-105">DESCRIPTION</span></span>
<span data-ttu-id="186b9-106">**Add-AzureDisk** cmdlet 'i geçerli abonelikteki Azure disk deposuna bir disk ekler.</span><span class="sxs-lookup"><span data-stu-id="186b9-106">The **Add-AzureDisk** cmdlet adds a disk to the Azure disk repository in the current subscription.</span></span>
<span data-ttu-id="186b9-107">Bu cmdlet bir sistem diski veya veri diski ekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="186b9-107">This cmdlet can add a system disk or a data disk.</span></span>
<span data-ttu-id="186b9-108">Sistem diski eklemek için *OS* parametresini kullanarak bir işletim sistemi türü belirtin.</span><span class="sxs-lookup"><span data-stu-id="186b9-108">To add a system disk, specify an operating system type by using the *OS* parameter.</span></span>

## <span data-ttu-id="186b9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="186b9-109">EXAMPLES</span></span>

### <span data-ttu-id="186b9-110">Örnek 1: Windows işletim sistemini kullanan bir başlangıç disketi ekleme</span><span class="sxs-lookup"><span data-stu-id="186b9-110">Example 1: Add a startup disk that uses the Windows operating system</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyWinDisk" -MediaLocation "http://contosostorage.blob.core.azure.com/vhds/winserver-system.vhd" -Label "StartupDisk" -OS "Windows"
```

<span data-ttu-id="186b9-111">Bu komut, disk deponuza bir sistem diski ekler.</span><span class="sxs-lookup"><span data-stu-id="186b9-111">This command adds a system disk to your disk repository.</span></span>
<span data-ttu-id="186b9-112">Sistem diski Windows işletim sistemini kullanır.</span><span class="sxs-lookup"><span data-stu-id="186b9-112">The system disk uses the Windows operating system.</span></span>

### <span data-ttu-id="186b9-113">Örnek 2: veri disketi ekleme</span><span class="sxs-lookup"><span data-stu-id="186b9-113">Example 2: Add a data disk</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyDataDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/winserver-data.vhd" -Label "DataDisk"
```

<span data-ttu-id="186b9-114">Bu komut, veri disketi ekler.</span><span class="sxs-lookup"><span data-stu-id="186b9-114">This command adds a data disk.</span></span>

### <span data-ttu-id="186b9-115">Örnek 3: Linux sistem diski ekleme</span><span class="sxs-lookup"><span data-stu-id="186b9-115">Example 3: Add a Linux system disk</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyLinuxDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/linuxsys.vhd" -OS "Linux"
```

<span data-ttu-id="186b9-116">Bu komut, bir Linux sistem diski ekler.</span><span class="sxs-lookup"><span data-stu-id="186b9-116">This command adds a Linux system disk.</span></span>

## <span data-ttu-id="186b9-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="186b9-117">PARAMETERS</span></span>

### <span data-ttu-id="186b9-118">-DiskName</span><span class="sxs-lookup"><span data-stu-id="186b9-118">-DiskName</span></span>
<span data-ttu-id="186b9-119">Bu cmdlet 'in eklediği diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="186b9-119">Specifies the name of the disk that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="186b9-120">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="186b9-120">-InformationAction</span></span>
<span data-ttu-id="186b9-121">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="186b9-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="186b9-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="186b9-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="186b9-123">'A</span><span class="sxs-lookup"><span data-stu-id="186b9-123">Continue</span></span>
- <span data-ttu-id="186b9-124">Manıza</span><span class="sxs-lookup"><span data-stu-id="186b9-124">Ignore</span></span>
- <span data-ttu-id="186b9-125">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="186b9-125">Inquire</span></span>
- <span data-ttu-id="186b9-126">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="186b9-126">SilentlyContinue</span></span>
- <span data-ttu-id="186b9-127">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="186b9-127">Stop</span></span>
- <span data-ttu-id="186b9-128">Biliriz</span><span class="sxs-lookup"><span data-stu-id="186b9-128">Suspend</span></span>

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

### <span data-ttu-id="186b9-129">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="186b9-129">-InformationVariable</span></span>
<span data-ttu-id="186b9-130">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="186b9-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="186b9-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="186b9-131">-Label</span></span>
<span data-ttu-id="186b9-132">Bu cmdlet 'in eklediği disk için bir disk etiketi belirtir.</span><span class="sxs-lookup"><span data-stu-id="186b9-132">Specifies a disk label for the disk that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="186b9-133">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="186b9-133">-MediaLocation</span></span>
<span data-ttu-id="186b9-134">Azure depolama birimindeki diskin fiziksel konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="186b9-134">Specifies the physical location of the disk in Azure Storage.</span></span>
<span data-ttu-id="186b9-135">Bu değer, geçerli abonelik ve depolama hesabındaki bir blob sayfasına başvurur.</span><span class="sxs-lookup"><span data-stu-id="186b9-135">This value refers to a blob page in the current subscription and storage account.</span></span>

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

### <span data-ttu-id="186b9-136">-İşletim sistemi</span><span class="sxs-lookup"><span data-stu-id="186b9-136">-OS</span></span>
<span data-ttu-id="186b9-137">Sistem diskinin işletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="186b9-137">Specifies the operating system type for a system disk.</span></span>
<span data-ttu-id="186b9-138">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="186b9-138">Valid values are:</span></span> 

- <span data-ttu-id="186b9-139">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="186b9-139">Windows</span></span> 
- <span data-ttu-id="186b9-140">UX</span><span class="sxs-lookup"><span data-stu-id="186b9-140">Linux</span></span> 

<span data-ttu-id="186b9-141">Bu parametreyi belirtmezseniz cmdlet, diski veri diski olarak ekler.</span><span class="sxs-lookup"><span data-stu-id="186b9-141">If you do not specify this parameter, the cmdlet adds the disk as a data disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="186b9-142">-Profil</span><span class="sxs-lookup"><span data-stu-id="186b9-142">-Profile</span></span>
<span data-ttu-id="186b9-143">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="186b9-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="186b9-144">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="186b9-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="186b9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="186b9-145">CommonParameters</span></span>
<span data-ttu-id="186b9-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="186b9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="186b9-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="186b9-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="186b9-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="186b9-148">INPUTS</span></span>

## <span data-ttu-id="186b9-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="186b9-149">OUTPUTS</span></span>

### <span data-ttu-id="186b9-150">DiskContext</span><span class="sxs-lookup"><span data-stu-id="186b9-150">DiskContext</span></span>

## <span data-ttu-id="186b9-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="186b9-151">NOTES</span></span>

## <span data-ttu-id="186b9-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="186b9-152">RELATED LINKS</span></span>

[<span data-ttu-id="186b9-153">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="186b9-153">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="186b9-154">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="186b9-154">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)

[<span data-ttu-id="186b9-155">Güncelleştirme-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="186b9-155">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


