---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95DCD2EC-8327-4A46-B624-289D0A28F7EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4614910b8c0ccd36bb8ef75ee98f662cf69a276a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106354"
---
# <span data-ttu-id="f1b9f-101">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="f1b9f-101">Get-AzureDisk</span></span>

## <span data-ttu-id="f1b9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1b9f-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b9f-103">Azure disk deposundaki diskler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="f1b9f-103">Gets information about disks in the Azure disk repository.</span></span>

## <span data-ttu-id="f1b9f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1b9f-104">SYNTAX</span></span>

```
Get-AzureDisk [[-DiskName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f1b9f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1b9f-105">DESCRIPTION</span></span>
<span data-ttu-id="f1b9f-106">**Get-AzureDisk** cmdlet 'i, geçerli abonelik için Azure disk deposunda depolanan diskler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="f1b9f-106">The **Get-AzureDisk** cmdlet gets information about the disks that are stored in the Azure disk repository for the current subscription.</span></span>
<span data-ttu-id="f1b9f-107">Bu cmdlet, depodaki tüm diskler için bir bilgi listesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="f1b9f-107">This cmdlet returns a list of information for all disks in the repository.</span></span>
<span data-ttu-id="f1b9f-108">Belirli bir diskle ilgili bilgileri görüntülemek için diskin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="f1b9f-108">To view information for a specific disk, specify the name of the disk.</span></span>

## <span data-ttu-id="f1b9f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1b9f-109">EXAMPLES</span></span>

### <span data-ttu-id="f1b9f-110">Örnek 1: diskle ilgili bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="f1b9f-110">Example 1: Get information about a disk</span></span>
```
PS C:\> Get-AzureDisk -DiskName "ContosoDataDisk"
```

<span data-ttu-id="f1b9f-111">Bu komut, disk deposundaki ContosoDataDisk adlı diskle ilgili bilgi verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="f1b9f-111">This command gets information data about the disk named ContosoDataDisk from the disk repository.</span></span>

### <span data-ttu-id="f1b9f-112">Örnek 2: tüm disklerle ilgili bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="f1b9f-112">Example 2: Get information about all disks</span></span>
```
PS C:\> Get-AzureDisk
```

<span data-ttu-id="f1b9f-113">Bu komut, disk deposundaki tüm diskler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="f1b9f-113">This command gets information about all the disks in the disk repository.</span></span>

### <span data-ttu-id="f1b9f-114">Örnek 3: diskle ilgili bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="f1b9f-114">Example 3: Get information about a disk</span></span>
```
PS C:\> Get-AzureDisk | Where-Object {$_.AttachedTo -eq $Null } | Format-Table -AutoSize -Property "DiskName","DiskSizeInGB","MediaLink"
```

<span data-ttu-id="f1b9f-115">Bu komut, şu anda sanal makineye eklenmemiş olan disk deposundaki tüm disklere yönelik verileri alır.</span><span class="sxs-lookup"><span data-stu-id="f1b9f-115">This command gets data for all of the disks in the disk repository that are not currently attached to a virtual machine.</span></span>
<span data-ttu-id="f1b9f-116">Komut tüm diskler hakkında bilgi alır ve her nesneyi **WHERE-nesne** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="f1b9f-116">The command gets information about all of the disks, and passes each object to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="f1b9f-117">Bu cmdlet, **AttachedTo** özelliği için $null değeri olmayan tüm diskleri bırakır.</span><span class="sxs-lookup"><span data-stu-id="f1b9f-117">That cmdlet drops any disk that does not have a value of $Null for the **AttachedTo** property.</span></span>
<span data-ttu-id="f1b9f-118">Komut, **Biçim-Tablo** cmdlet 'ini kullanarak listeyi tablo olarak biçimlendirir.</span><span class="sxs-lookup"><span data-stu-id="f1b9f-118">The command formats the list as a table by using the **Format-Table** cmdlet.</span></span>

## <span data-ttu-id="f1b9f-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1b9f-119">PARAMETERS</span></span>

### <span data-ttu-id="f1b9f-120">-DiskName</span><span class="sxs-lookup"><span data-stu-id="f1b9f-120">-DiskName</span></span>
<span data-ttu-id="f1b9f-121">Bu cmdlet 'in bilgi aldığı disk deposundaki diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1b9f-121">Specifies the name of the disk in the disk repository about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="f1b9f-122">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="f1b9f-122">-InformationAction</span></span>
<span data-ttu-id="f1b9f-123">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1b9f-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f1b9f-124">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f1b9f-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f1b9f-125">'A</span><span class="sxs-lookup"><span data-stu-id="f1b9f-125">Continue</span></span>
- <span data-ttu-id="f1b9f-126">Manıza</span><span class="sxs-lookup"><span data-stu-id="f1b9f-126">Ignore</span></span>
- <span data-ttu-id="f1b9f-127">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="f1b9f-127">Inquire</span></span>
- <span data-ttu-id="f1b9f-128">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="f1b9f-128">SilentlyContinue</span></span>
- <span data-ttu-id="f1b9f-129">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="f1b9f-129">Stop</span></span>
- <span data-ttu-id="f1b9f-130">Biliriz</span><span class="sxs-lookup"><span data-stu-id="f1b9f-130">Suspend</span></span>

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

### <span data-ttu-id="f1b9f-131">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="f1b9f-131">-InformationVariable</span></span>
<span data-ttu-id="f1b9f-132">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1b9f-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f1b9f-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="f1b9f-133">-Profile</span></span>
<span data-ttu-id="f1b9f-134">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1b9f-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f1b9f-135">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="f1b9f-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f1b9f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b9f-136">CommonParameters</span></span>
<span data-ttu-id="f1b9f-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1b9f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1b9f-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1b9f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b9f-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1b9f-139">INPUTS</span></span>

## <span data-ttu-id="f1b9f-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1b9f-140">OUTPUTS</span></span>

## <span data-ttu-id="f1b9f-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1b9f-141">NOTES</span></span>

## <span data-ttu-id="f1b9f-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1b9f-142">RELATED LINKS</span></span>

[<span data-ttu-id="f1b9f-143">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="f1b9f-143">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="f1b9f-144">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="f1b9f-144">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)

[<span data-ttu-id="f1b9f-145">Güncelleştirme-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="f1b9f-145">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


