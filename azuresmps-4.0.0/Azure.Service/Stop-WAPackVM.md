---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4FB7096E-DDA1-474C-BF0C-D910681BE58D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e4ef4660761ab29e738050c0445534602accda6
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107396"
---
# <span data-ttu-id="a7bcb-101">Stop-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="a7bcb-101">Stop-WAPackVM</span></span>

## <span data-ttu-id="a7bcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7bcb-102">SYNOPSIS</span></span>
<span data-ttu-id="a7bcb-103">Sanal makineyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="a7bcb-103">Stops a virtual machine.</span></span>

## <span data-ttu-id="a7bcb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7bcb-104">SYNTAX</span></span>

```
Stop-WAPackVM [-Shutdown] -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a7bcb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7bcb-105">DESCRIPTION</span></span>
<span data-ttu-id="a7bcb-106">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="a7bcb-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="a7bcb-107">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a7bcb-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a7bcb-108">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a7bcb-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a7bcb-109">**Stop-WAPackVM** cmdlet 'i bir sanal makineyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="a7bcb-109">The **Stop-WAPackVM** cmdlet stops a virtual machine.</span></span>

## <span data-ttu-id="a7bcb-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7bcb-110">EXAMPLES</span></span>

### <span data-ttu-id="a7bcb-111">Örnek 1: sanal makineyi durdurma</span><span class="sxs-lookup"><span data-stu-id="a7bcb-111">Example 1: Stop a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Stop-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="a7bcb-112">İlk komut ContosoV126 adındaki sanal makineyi **Get-WAPackVM** cmdlet 'ini kullanarak alır ve bu nesneyi $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a7bcb-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="a7bcb-113">İkinci komut $VirtualMachine depolanan sanal makineyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="a7bcb-113">The second command stops the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="a7bcb-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7bcb-114">PARAMETERS</span></span>

### <span data-ttu-id="a7bcb-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a7bcb-115">-PassThru</span></span>
<span data-ttu-id="a7bcb-116">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="a7bcb-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a7bcb-117">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a7bcb-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a7bcb-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="a7bcb-118">-Profile</span></span>
<span data-ttu-id="a7bcb-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7bcb-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a7bcb-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="a7bcb-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a7bcb-121">-Shutdown</span><span class="sxs-lookup"><span data-stu-id="a7bcb-121">-Shutdown</span></span>
<span data-ttu-id="a7bcb-122">Cmdlet 'in sanal makinenin işletim sistemini kapatadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a7bcb-122">Indicates that the cmdlet shuts down the operating system of the virtual machine.</span></span>

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

### <span data-ttu-id="a7bcb-123">-VM</span><span class="sxs-lookup"><span data-stu-id="a7bcb-123">-VM</span></span>
<span data-ttu-id="a7bcb-124">Bir sanal makine belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7bcb-124">Specifies a virtual machine.</span></span>
<span data-ttu-id="a7bcb-125">Sanal makine edinmek için **Get-WAPackVM** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a7bcb-125">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="a7bcb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7bcb-126">CommonParameters</span></span>
<span data-ttu-id="a7bcb-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7bcb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7bcb-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7bcb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7bcb-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7bcb-129">INPUTS</span></span>

## <span data-ttu-id="a7bcb-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7bcb-130">OUTPUTS</span></span>

## <span data-ttu-id="a7bcb-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7bcb-131">NOTES</span></span>

## <span data-ttu-id="a7bcb-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7bcb-132">RELATED LINKS</span></span>

[<span data-ttu-id="a7bcb-133">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="a7bcb-133">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="a7bcb-134">Yeni-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="a7bcb-134">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="a7bcb-135">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="a7bcb-135">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="a7bcb-136">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="a7bcb-136">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="a7bcb-137">Özgeçmiş-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="a7bcb-137">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="a7bcb-138">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="a7bcb-138">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="a7bcb-139">Başlangıç-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="a7bcb-139">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="a7bcb-140">Askıya al-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="a7bcb-140">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


