---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 08A7556E-C07F-4B3B-B9D6-B241C72860FA
online version: ''
schema: 2.0.0
ms.openlocfilehash: b01ac318982b62499164cd54c9d9a51356ad9830
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107385"
---
# <span data-ttu-id="1c783-101">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="1c783-101">Set-WAPackVM</span></span>

## <span data-ttu-id="1c783-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c783-102">SYNOPSIS</span></span>
<span data-ttu-id="1c783-103">Sanal makinenin boyut özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1c783-103">Changes the size properties of a virtual machine.</span></span>

## <span data-ttu-id="1c783-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1c783-104">SYNTAX</span></span>

```
Set-WAPackVM -VM <VirtualMachine> -VMSizeProfile <HardwareProfile> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c783-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1c783-105">DESCRIPTION</span></span>
<span data-ttu-id="1c783-106">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="1c783-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="1c783-107">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="1c783-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="1c783-108">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="1c783-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="1c783-109">**Set-WAPackVM** cmdlet 'i sanal makinenin boyut özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1c783-109">The **Set-WAPackVM** cmdlet changes the size properties of a virtual machine.</span></span>

## <span data-ttu-id="1c783-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1c783-110">EXAMPLES</span></span>

### <span data-ttu-id="1c783-111">Örnek 1: sanal makinenin boyutunu belirtme</span><span class="sxs-lookup"><span data-stu-id="1c783-111">Example 1: Specify the size for a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> Set-WAPackVM -VM $VirtualMachine -VMSizeProfile $SizeProfile
```

<span data-ttu-id="1c783-112">İlk komut ContosoV126 adındaki sanal makineyi **Get-WAPackVM** cmdlet 'ini kullanarak alır ve bu nesneyi $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1c783-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="1c783-113">İkinci komut, **Get-WAPackVMSizeProfile** cmdlet 'ini kullanarak, düz Sizevm adlı boyut profilini alır ve bu nesneyi $SizeProfile değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1c783-113">The second command gets the size profile named MediumSizeVM by using the **Get-WAPackVMSizeProfile** cmdlet, and then stores that object in the $SizeProfile variable.</span></span>

<span data-ttu-id="1c783-114">Son komutu $VirtualMachine depolanan sanal makineye $SizeProfile depolanan boyut profilini atar.</span><span class="sxs-lookup"><span data-stu-id="1c783-114">The final command assigns the size profile stored in $SizeProfile to the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="1c783-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1c783-115">PARAMETERS</span></span>

### <span data-ttu-id="1c783-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1c783-116">-PassThru</span></span>
<span data-ttu-id="1c783-117">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="1c783-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1c783-118">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="1c783-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1c783-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="1c783-119">-Profile</span></span>
<span data-ttu-id="1c783-120">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c783-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1c783-121">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="1c783-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1c783-122">-VM</span><span class="sxs-lookup"><span data-stu-id="1c783-122">-VM</span></span>
<span data-ttu-id="1c783-123">Bir sanal makine belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c783-123">Specifies a virtual machine.</span></span>
<span data-ttu-id="1c783-124">Sanal makine edinmek için **Get-WAPackVM** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1c783-124">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="1c783-125">-VMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="1c783-125">-VMSizeProfile</span></span>
<span data-ttu-id="1c783-126">Bir sanal makinenin bir boyut profilini **HardwareProfile** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c783-126">Specifies a size profile for a virtual machine as a **HardwareProfile** object.</span></span>
<span data-ttu-id="1c783-127">Boyut profili edinmek için **Get-WAPackVMSizeProfile** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1c783-127">To obtain a size profile, use the **Get-WAPackVMSizeProfile** cmdlet.</span></span>

```yaml
Type: HardwareProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c783-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c783-128">CommonParameters</span></span>
<span data-ttu-id="1c783-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1c783-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c783-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c783-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c783-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1c783-131">INPUTS</span></span>

## <span data-ttu-id="1c783-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1c783-132">OUTPUTS</span></span>

## <span data-ttu-id="1c783-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1c783-133">NOTES</span></span>

## <span data-ttu-id="1c783-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1c783-134">RELATED LINKS</span></span>

[<span data-ttu-id="1c783-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="1c783-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="1c783-136">Yeni-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="1c783-136">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="1c783-137">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="1c783-137">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="1c783-138">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="1c783-138">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="1c783-139">Özgeçmiş-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="1c783-139">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="1c783-140">Başlangıç-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="1c783-140">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="1c783-141">Dur-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="1c783-141">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="1c783-142">Askıya al-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="1c783-142">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="1c783-143">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="1c783-143">Get-WAPackVMSizeProfile</span></span>](./Get-WAPackVMSizeProfile.md)


