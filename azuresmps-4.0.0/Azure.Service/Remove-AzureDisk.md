---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 75A50C59-28D1-4D29-A420-D24BF479F79E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29e5e7e0bc2fcc0ce93186cf966f18d6c9c3e372
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106157"
---
# <span data-ttu-id="f8383-101">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="f8383-101">Remove-AzureDisk</span></span>

## <span data-ttu-id="f8383-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8383-102">SYNOPSIS</span></span>
<span data-ttu-id="f8383-103">Azure disk havuzundan bir diski kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f8383-103">Removes a disk from the Azure disk repository.</span></span>

## <span data-ttu-id="f8383-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f8383-104">SYNTAX</span></span>

```
Remove-AzureDisk [-DiskName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f8383-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f8383-105">DESCRIPTION</span></span>
<span data-ttu-id="f8383-106">**Remove-AzureDisk** cmdlet 'i, geçerli abonelikteki Azure disk havuzundan bir diski kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f8383-106">The **Remove-AzureDisk** cmdlet removes a disk from the Azure disk repository in the current subscription.</span></span>
<span data-ttu-id="f8383-107">Varsayılan olarak, bu cmdlet BLOB depolama biriminden sanal sabit disk (VHD) dosyasını silmez.</span><span class="sxs-lookup"><span data-stu-id="f8383-107">By default, this cmdlet does not delete the virtual hard disk (VHD) file from blob storage.</span></span>
<span data-ttu-id="f8383-108">VHD 'yi silmek için *Deletevhd* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="f8383-108">To delete the VHD, specify the *DeleteVHD* parameter.</span></span>

## <span data-ttu-id="f8383-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f8383-109">EXAMPLES</span></span>

### <span data-ttu-id="f8383-110">Örnek 1: diski kaldırma</span><span class="sxs-lookup"><span data-stu-id="f8383-110">Example 1: Remove a disk</span></span>
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk"
```

<span data-ttu-id="f8383-111">Bu komut, disk deposundaki ContosoDataDisk disk adlı diski kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f8383-111">This command removes the disk named ContosoDataDisk disk from the disk repository.</span></span>
<span data-ttu-id="f8383-112">Komut VHD 'YI silmez.</span><span class="sxs-lookup"><span data-stu-id="f8383-112">The command does not delete the VHD.</span></span>

### <span data-ttu-id="f8383-113">Örnek 2: diski kaldırma ve silme</span><span class="sxs-lookup"><span data-stu-id="f8383-113">Example 2: Remove and delete a disk</span></span>
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk" -DeleteVHD
```

<span data-ttu-id="f8383-114">Bu komut, disk deposundaki ContosoDataDisk disk adlı diski kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f8383-114">This command removes the disk named ContosoDataDisk disk from the disk repository.</span></span>
<span data-ttu-id="f8383-115">Bu komut DeleteVHD parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8383-115">This command specifies the DeleteVHD parameter.</span></span>
<span data-ttu-id="f8383-116">Bu nedenle, komut VHD 'yi Azure Storage 'dan siler.</span><span class="sxs-lookup"><span data-stu-id="f8383-116">Therefore, the command deletes the VHD from Azure Storage.</span></span>

## <span data-ttu-id="f8383-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f8383-117">PARAMETERS</span></span>

### <span data-ttu-id="f8383-118">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="f8383-118">-DeleteVHD</span></span>
<span data-ttu-id="f8383-119">Bu cmdlet 'in BLOB depolama 'dan kaldırıldığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="f8383-119">Indicates that this cmdlet removes the VHD from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8383-120">-DiskName</span><span class="sxs-lookup"><span data-stu-id="f8383-120">-DiskName</span></span>
<span data-ttu-id="f8383-121">Bu cmdlet 'in kaldırıldığı disk deposundaki veri diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8383-121">Specifies the name of the data disk in the disk repository that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f8383-122">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="f8383-122">-InformationAction</span></span>
<span data-ttu-id="f8383-123">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8383-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f8383-124">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f8383-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f8383-125">'A</span><span class="sxs-lookup"><span data-stu-id="f8383-125">Continue</span></span>
- <span data-ttu-id="f8383-126">Manıza</span><span class="sxs-lookup"><span data-stu-id="f8383-126">Ignore</span></span>
- <span data-ttu-id="f8383-127">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="f8383-127">Inquire</span></span>
- <span data-ttu-id="f8383-128">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="f8383-128">SilentlyContinue</span></span>
- <span data-ttu-id="f8383-129">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="f8383-129">Stop</span></span>
- <span data-ttu-id="f8383-130">Biliriz</span><span class="sxs-lookup"><span data-stu-id="f8383-130">Suspend</span></span>

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

### <span data-ttu-id="f8383-131">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="f8383-131">-InformationVariable</span></span>
<span data-ttu-id="f8383-132">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8383-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f8383-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="f8383-133">-Profile</span></span>
<span data-ttu-id="f8383-134">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8383-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f8383-135">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="f8383-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f8383-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8383-136">CommonParameters</span></span>
<span data-ttu-id="f8383-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f8383-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8383-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8383-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8383-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f8383-139">INPUTS</span></span>

## <span data-ttu-id="f8383-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f8383-140">OUTPUTS</span></span>

## <span data-ttu-id="f8383-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f8383-141">NOTES</span></span>

## <span data-ttu-id="f8383-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f8383-142">RELATED LINKS</span></span>

[<span data-ttu-id="f8383-143">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="f8383-143">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="f8383-144">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="f8383-144">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="f8383-145">Güncelleştirme-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="f8383-145">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


