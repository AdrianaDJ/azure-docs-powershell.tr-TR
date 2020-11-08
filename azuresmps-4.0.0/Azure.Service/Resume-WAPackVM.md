---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5E85F58B-7C70-4F4A-B218-08F9AF512B76
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8aba9c72e3911f59db88e9be4262ee90ea460a5c
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107395"
---
# <span data-ttu-id="9e9de-101">Resume-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9e9de-101">Resume-WAPackVM</span></span>

## <span data-ttu-id="9e9de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e9de-102">SYNOPSIS</span></span>
<span data-ttu-id="9e9de-103">Duraklatılan sanal makineleri sürdürür.</span><span class="sxs-lookup"><span data-stu-id="9e9de-103">Resumes paused virtual machines.</span></span>

## <span data-ttu-id="9e9de-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e9de-104">SYNTAX</span></span>

```
Resume-WAPackVM -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9e9de-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e9de-105">DESCRIPTION</span></span>
<span data-ttu-id="9e9de-106">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="9e9de-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="9e9de-107">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9e9de-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9e9de-108">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9e9de-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9e9de-109">**Özgeçmiş-WAPackVM** cmdlet 'i duraklatılan sanal makineleri sürdürür.</span><span class="sxs-lookup"><span data-stu-id="9e9de-109">The **Resume-WAPackVM** cmdlet resumes paused virtual machines.</span></span>

## <span data-ttu-id="9e9de-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e9de-110">EXAMPLES</span></span>

### <span data-ttu-id="9e9de-111">Örnek 1: sanal makineyi sürdürme</span><span class="sxs-lookup"><span data-stu-id="9e9de-111">Example 1: Resume a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Resume-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="9e9de-112">İlk komut ContosoV126 adındaki sanal makineyi **Get-WAPackVM** cmdlet 'ini kullanarak alır ve bu nesneyi $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9e9de-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="9e9de-113">İkinci komut $VirtualMachine depolanan sanal makineyi sürdürür.</span><span class="sxs-lookup"><span data-stu-id="9e9de-113">The second command resumes the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="9e9de-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e9de-114">PARAMETERS</span></span>

### <span data-ttu-id="9e9de-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9e9de-115">-PassThru</span></span>
<span data-ttu-id="9e9de-116">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="9e9de-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9e9de-117">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="9e9de-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9e9de-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="9e9de-118">-Profile</span></span>
<span data-ttu-id="9e9de-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e9de-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9e9de-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="9e9de-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9e9de-121">-VM</span><span class="sxs-lookup"><span data-stu-id="9e9de-121">-VM</span></span>
<span data-ttu-id="9e9de-122">Bir sanal makine belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e9de-122">Specifies a virtual machine.</span></span>
<span data-ttu-id="9e9de-123">Sanal makine edinmek için **Get-WAPackVM** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9e9de-123">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

```yaml
Type: VirtualMachine
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e9de-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e9de-124">CommonParameters</span></span>
<span data-ttu-id="9e9de-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e9de-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e9de-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e9de-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e9de-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e9de-127">INPUTS</span></span>

## <span data-ttu-id="9e9de-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e9de-128">OUTPUTS</span></span>

## <span data-ttu-id="9e9de-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e9de-129">NOTES</span></span>

## <span data-ttu-id="9e9de-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e9de-130">RELATED LINKS</span></span>

[<span data-ttu-id="9e9de-131">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9e9de-131">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="9e9de-132">Yeni-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9e9de-132">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="9e9de-133">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9e9de-133">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="9e9de-134">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9e9de-134">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="9e9de-135">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9e9de-135">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="9e9de-136">Başlangıç-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9e9de-136">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="9e9de-137">Dur-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9e9de-137">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="9e9de-138">Askıya al-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9e9de-138">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


