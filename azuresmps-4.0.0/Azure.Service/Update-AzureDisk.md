---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 849714BC-8B19-453E-B790-A9C38F9D48CB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ef8bd3b1fef6a3af01193a104f6917c4131064f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105425"
---
# <span data-ttu-id="c16bb-101">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="c16bb-101">Update-AzureDisk</span></span>

## <span data-ttu-id="c16bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c16bb-102">SYNOPSIS</span></span>
<span data-ttu-id="c16bb-103">Azure disk deposundaki bir diskin etiketini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c16bb-103">Changes the label of a disk in the Azure disk repository.</span></span>

## <span data-ttu-id="c16bb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c16bb-104">SYNTAX</span></span>

### <span data-ttu-id="c16bb-105">Yeniden boyutlandırma</span><span class="sxs-lookup"><span data-stu-id="c16bb-105">Resize</span></span>
```
Update-AzureDisk [-DiskName] <String> [[-Label] <String>] [-ResizedSizeInGB] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="c16bb-106">NoResize</span><span class="sxs-lookup"><span data-stu-id="c16bb-106">NoResize</span></span>
```
Update-AzureDisk [-DiskName] <String> [-Label] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c16bb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c16bb-107">DESCRIPTION</span></span>
<span data-ttu-id="c16bb-108">**Update-AzureDisk** cmdlet 'i, geçerli Azure aboneliğinin disk deposundaki bir diskle ilişkili etiketi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c16bb-108">The **Update-AzureDisk** cmdlet changes the label that is associated with a disk in the disk repository of the current Azure subscription.</span></span>

## <span data-ttu-id="c16bb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c16bb-109">EXAMPLES</span></span>

### <span data-ttu-id="c16bb-110">Örnek 1: diskin etiketini değiştirme</span><span class="sxs-lookup"><span data-stu-id="c16bb-110">Example 1: Change the label of a disk</span></span>
```
PS C:\> Update-AzureDisk ?DiskName "ContosoOSDisk" -Label "DoNotUse"
```

<span data-ttu-id="c16bb-111">Bu komut, ContosoOSDisk adlı diskin DoNotUse olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c16bb-111">This command changes the label of the disk named ContosoOSDisk to DoNotUse.</span></span>

## <span data-ttu-id="c16bb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c16bb-112">PARAMETERS</span></span>

### <span data-ttu-id="c16bb-113">-DiskName</span><span class="sxs-lookup"><span data-stu-id="c16bb-113">-DiskName</span></span>
<span data-ttu-id="c16bb-114">Bu cmdlet 'in değiştirdiği diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c16bb-114">Specifies the name of the disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c16bb-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="c16bb-115">-InformationAction</span></span>
<span data-ttu-id="c16bb-116">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c16bb-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c16bb-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c16bb-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c16bb-118">'A</span><span class="sxs-lookup"><span data-stu-id="c16bb-118">Continue</span></span>
- <span data-ttu-id="c16bb-119">Manıza</span><span class="sxs-lookup"><span data-stu-id="c16bb-119">Ignore</span></span>
- <span data-ttu-id="c16bb-120">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="c16bb-120">Inquire</span></span>
- <span data-ttu-id="c16bb-121">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="c16bb-121">SilentlyContinue</span></span>
- <span data-ttu-id="c16bb-122">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="c16bb-122">Stop</span></span>
- <span data-ttu-id="c16bb-123">Biliriz</span><span class="sxs-lookup"><span data-stu-id="c16bb-123">Suspend</span></span>

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

### <span data-ttu-id="c16bb-124">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="c16bb-124">-InformationVariable</span></span>
<span data-ttu-id="c16bb-125">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="c16bb-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c16bb-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c16bb-126">-Label</span></span>
<span data-ttu-id="c16bb-127">Disk için yeni etiketi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c16bb-127">Specifies the new label for the disk.</span></span>

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoResize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c16bb-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="c16bb-128">-Profile</span></span>
<span data-ttu-id="c16bb-129">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c16bb-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c16bb-130">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="c16bb-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c16bb-131">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="c16bb-131">-ResizedSizeInGB</span></span>
<span data-ttu-id="c16bb-132">Diskin yeni boyutunu gigabayt cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="c16bb-132">Specifies the new size, in gigabytes, for the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c16bb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c16bb-133">CommonParameters</span></span>
<span data-ttu-id="c16bb-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c16bb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c16bb-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c16bb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c16bb-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c16bb-136">INPUTS</span></span>

## <span data-ttu-id="c16bb-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c16bb-137">OUTPUTS</span></span>

### <span data-ttu-id="c16bb-138">DiskContext</span><span class="sxs-lookup"><span data-stu-id="c16bb-138">DiskContext</span></span>

## <span data-ttu-id="c16bb-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c16bb-139">NOTES</span></span>

## <span data-ttu-id="c16bb-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c16bb-140">RELATED LINKS</span></span>

[<span data-ttu-id="c16bb-141">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="c16bb-141">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="c16bb-142">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="c16bb-142">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="c16bb-143">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="c16bb-143">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)


