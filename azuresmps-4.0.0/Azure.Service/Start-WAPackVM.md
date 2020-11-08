---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8A6B4C8C-B990-443B-9157-B5C35824269A
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2d87c92f18c3aeb25aad210922dea0c93287fa6
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107424"
---
# <span data-ttu-id="7cc4d-101">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7cc4d-101">Start-WAPackVM</span></span>

## <span data-ttu-id="7cc4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cc4d-102">SYNOPSIS</span></span>
<span data-ttu-id="7cc4d-103">Sanal makineyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="7cc4d-103">Starts a virtual machine.</span></span>

## <span data-ttu-id="7cc4d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7cc4d-104">SYNTAX</span></span>

```
Start-WAPackVM -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7cc4d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7cc4d-105">DESCRIPTION</span></span>
<span data-ttu-id="7cc4d-106">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="7cc4d-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="7cc4d-107">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7cc4d-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7cc4d-108">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7cc4d-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7cc4d-109">**Start-WAPackVM** cmdlet 'i bir sanal makine başlatır.</span><span class="sxs-lookup"><span data-stu-id="7cc4d-109">The **Start-WAPackVM** cmdlet starts a virtual machine.</span></span>

## <span data-ttu-id="7cc4d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7cc4d-110">EXAMPLES</span></span>

### <span data-ttu-id="7cc4d-111">Örnek 1: sanal makine başlatma</span><span class="sxs-lookup"><span data-stu-id="7cc4d-111">Example 1: Start a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Start-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="7cc4d-112">İlk komut ContosoV126 adındaki sanal makineyi **Get-WAPackVM** cmdlet 'ini kullanarak alır ve bu nesneyi $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7cc4d-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="7cc4d-113">İkinci komut $VirtualMachine depolanan sanal makineyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="7cc4d-113">The second command starts the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="7cc4d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7cc4d-114">PARAMETERS</span></span>

### <span data-ttu-id="7cc4d-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7cc4d-115">-PassThru</span></span>
<span data-ttu-id="7cc4d-116">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="7cc4d-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7cc4d-117">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="7cc4d-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7cc4d-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="7cc4d-118">-Profile</span></span>
<span data-ttu-id="7cc4d-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cc4d-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7cc4d-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="7cc4d-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7cc4d-121">-VM</span><span class="sxs-lookup"><span data-stu-id="7cc4d-121">-VM</span></span>
<span data-ttu-id="7cc4d-122">Bir sanal makine belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cc4d-122">Specifies a virtual machine.</span></span>
<span data-ttu-id="7cc4d-123">Sanal makine edinmek için **Get-WAPackVM** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7cc4d-123">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="7cc4d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cc4d-124">CommonParameters</span></span>
<span data-ttu-id="7cc4d-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7cc4d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cc4d-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cc4d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cc4d-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7cc4d-127">INPUTS</span></span>

## <span data-ttu-id="7cc4d-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7cc4d-128">OUTPUTS</span></span>

## <span data-ttu-id="7cc4d-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7cc4d-129">NOTES</span></span>

## <span data-ttu-id="7cc4d-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7cc4d-130">RELATED LINKS</span></span>

[<span data-ttu-id="7cc4d-131">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7cc4d-131">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="7cc4d-132">Yeni-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7cc4d-132">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="7cc4d-133">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7cc4d-133">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="7cc4d-134">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7cc4d-134">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="7cc4d-135">Özgeçmiş-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7cc4d-135">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="7cc4d-136">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7cc4d-136">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="7cc4d-137">Dur-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7cc4d-137">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="7cc4d-138">Askıya al-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7cc4d-138">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


