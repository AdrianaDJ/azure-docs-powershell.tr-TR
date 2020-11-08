---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 047C5FBD-CB0D-47BF-AE03-4DF32B4FAD87
online version: ''
schema: 2.0.0
ms.openlocfilehash: a546c9fdb066aaf1203055fd62d8eb01258569c8
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107356"
---
# <span data-ttu-id="478b9-101">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="478b9-101">Get-WAPackVM</span></span>

## <span data-ttu-id="478b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="478b9-102">SYNOPSIS</span></span>
<span data-ttu-id="478b9-103">Sanal makine nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="478b9-103">Gets virtual machine objects.</span></span>

## <span data-ttu-id="478b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="478b9-104">SYNTAX</span></span>

### <span data-ttu-id="478b9-105">Boş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="478b9-105">Empty (Default)</span></span>
```
Get-WAPackVM [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="478b9-106">FromName</span><span class="sxs-lookup"><span data-stu-id="478b9-106">FromName</span></span>
```
Get-WAPackVM [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="478b9-107">FromId</span><span class="sxs-lookup"><span data-stu-id="478b9-107">FromId</span></span>
```
Get-WAPackVM [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="478b9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="478b9-108">DESCRIPTION</span></span>
<span data-ttu-id="478b9-109">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="478b9-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="478b9-110">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="478b9-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="478b9-111">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="478b9-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="478b9-112">**Get-WAPackVM** cmdlet 'i sanal makine nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="478b9-112">The **Get-WAPackVM** cmdlet gets virtual machine objects.</span></span>

## <span data-ttu-id="478b9-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="478b9-113">EXAMPLES</span></span>

### <span data-ttu-id="478b9-114">Örnek 1: ad kullanarak sanal makine alma</span><span class="sxs-lookup"><span data-stu-id="478b9-114">Example 1: Get a virtual machine by using a name</span></span>
```
PS C:\> Get-WAPackVM -Name "ContosoV126"
```

<span data-ttu-id="478b9-115">Bu komut, ContosoV126 adındaki sanal makineyi alır.</span><span class="sxs-lookup"><span data-stu-id="478b9-115">This command gets the virtual machine named ContosoV126.</span></span>

### <span data-ttu-id="478b9-116">Örnek 2: KIMLIK kullanarak sanal makine edinme</span><span class="sxs-lookup"><span data-stu-id="478b9-116">Example 2: Get a virtual machine by using an ID</span></span>
```
PS C:\> Get-WAPackVM -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="478b9-117">Bu komut belirtilen KIMLIĞE sahip sanal makineyi alır.</span><span class="sxs-lookup"><span data-stu-id="478b9-117">This command gets the virtual machine that has the specified ID.</span></span>

### <span data-ttu-id="478b9-118">Örnek 3: tüm sanal makineleri edinme</span><span class="sxs-lookup"><span data-stu-id="478b9-118">Example 3: Get all virtual machines</span></span>
```
PS C:\> Get-WAPackVM
```

<span data-ttu-id="478b9-119">Bu komut tüm sanal makineleri alır.</span><span class="sxs-lookup"><span data-stu-id="478b9-119">This command gets all virtual machines.</span></span>

## <span data-ttu-id="478b9-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="478b9-120">PARAMETERS</span></span>

### <span data-ttu-id="478b9-121">-ID</span><span class="sxs-lookup"><span data-stu-id="478b9-121">-ID</span></span>
<span data-ttu-id="478b9-122">Sanal makinenin benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="478b9-122">Specifies the unique ID of a virtual machine.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="478b9-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="478b9-123">-Name</span></span>
<span data-ttu-id="478b9-124">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="478b9-124">Specifies the name of a virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="478b9-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="478b9-125">-Profile</span></span>
<span data-ttu-id="478b9-126">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="478b9-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="478b9-127">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="478b9-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="478b9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="478b9-128">CommonParameters</span></span>
<span data-ttu-id="478b9-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="478b9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="478b9-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="478b9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="478b9-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="478b9-131">INPUTS</span></span>

## <span data-ttu-id="478b9-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="478b9-132">OUTPUTS</span></span>

## <span data-ttu-id="478b9-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="478b9-133">NOTES</span></span>

## <span data-ttu-id="478b9-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="478b9-134">RELATED LINKS</span></span>

[<span data-ttu-id="478b9-135">Yeni-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="478b9-135">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="478b9-136">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="478b9-136">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="478b9-137">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="478b9-137">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="478b9-138">Özgeçmiş-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="478b9-138">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="478b9-139">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="478b9-139">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="478b9-140">Başlangıç-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="478b9-140">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="478b9-141">Dur-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="478b9-141">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="478b9-142">Askıya al-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="478b9-142">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="478b9-143">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="478b9-143">Get-WAPackVMOSDisk</span></span>](./Get-WAPackVMOSDisk.md)


