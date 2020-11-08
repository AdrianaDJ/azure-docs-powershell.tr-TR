---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D04D79CE-F183-4A8D-B925-F640D89377BD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d7c4e6bd9365ccf45b730024b5841e4356f556a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107408"
---
# <span data-ttu-id="9878f-101">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9878f-101">Remove-WAPackVM</span></span>

## <span data-ttu-id="9878f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9878f-102">SYNOPSIS</span></span>
<span data-ttu-id="9878f-103">Sanal makine nesnelerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9878f-103">Removes virtual machine objects.</span></span>

## <span data-ttu-id="9878f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9878f-104">SYNTAX</span></span>

```
Remove-WAPackVM -VM <VirtualMachine> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9878f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9878f-105">DESCRIPTION</span></span>
<span data-ttu-id="9878f-106">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="9878f-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="9878f-107">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9878f-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9878f-108">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9878f-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9878f-109">**Remove-WAPackVM** cmdlet 'i sanal makine nesnelerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9878f-109">The **Remove-WAPackVM** cmdlet removes virtual machine objects.</span></span>

## <span data-ttu-id="9878f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9878f-110">EXAMPLES</span></span>

### <span data-ttu-id="9878f-111">Örnek 1: sanal makineyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="9878f-111">Example 1: Remove a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Remove-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="9878f-112">İlk komut ContosoV126 adındaki sanal makineyi **Get-WAPackVM** cmdlet 'ini kullanarak alır ve bu nesneyi $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9878f-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="9878f-113">İkinci komut, $VirtualMachine depolanan sanal makineyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9878f-113">The second command removes the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="9878f-114">Komut sizden onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9878f-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="9878f-115">Örnek 2: onaysız sanal makineyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="9878f-115">Example 2: Remove a virtual machine without confirmation</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Remove-WAPackVM -VM $VirtualMachine -Force
```

<span data-ttu-id="9878f-116">İlk komut ContosoV126 adındaki sanal makineyi **Get-WAPackVM** cmdlet 'ini kullanarak alır ve bu nesneyi $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9878f-116">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="9878f-117">İkinci komut, $VirtualMachine depolanan sanal makineyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9878f-117">The second command removes the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="9878f-118">Bu komut *Force* parametresini içerir.</span><span class="sxs-lookup"><span data-stu-id="9878f-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="9878f-119">Komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="9878f-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="9878f-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9878f-120">PARAMETERS</span></span>

### <span data-ttu-id="9878f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9878f-121">-Force</span></span>
<span data-ttu-id="9878f-122">Cmdlet 'in bir sanal makineyi onaylamanızı istemeden kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9878f-122">Indicates that the cmdlet removes a virtual machine without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="9878f-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9878f-123">-PassThru</span></span>
<span data-ttu-id="9878f-124">Cmdlet 'in Boole değeri döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="9878f-124">Indicates that the cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="9878f-125">İşlem başarılı olursa cmdlet $True değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="9878f-125">If the operation succeeds, the cmdlet returns a value of $True.</span></span>
<span data-ttu-id="9878f-126">Aksi takdirde, bir $False değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="9878f-126">Otherwise, it returns a value of $False.</span></span>
<span data-ttu-id="9878f-127">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="9878f-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9878f-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="9878f-128">-Profile</span></span>
<span data-ttu-id="9878f-129">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9878f-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9878f-130">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="9878f-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9878f-131">-VM</span><span class="sxs-lookup"><span data-stu-id="9878f-131">-VM</span></span>
<span data-ttu-id="9878f-132">Bir sanal makine belirtir.</span><span class="sxs-lookup"><span data-stu-id="9878f-132">Specifies a virtual machine.</span></span>
<span data-ttu-id="9878f-133">Sanal makine edinmek için **Get-WAPackVM** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9878f-133">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="9878f-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="9878f-134">-Confirm</span></span>
<span data-ttu-id="9878f-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9878f-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9878f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9878f-136">-WhatIf</span></span>
<span data-ttu-id="9878f-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9878f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9878f-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9878f-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9878f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9878f-139">CommonParameters</span></span>
<span data-ttu-id="9878f-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9878f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9878f-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9878f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9878f-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9878f-142">INPUTS</span></span>

## <span data-ttu-id="9878f-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9878f-143">OUTPUTS</span></span>

## <span data-ttu-id="9878f-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9878f-144">NOTES</span></span>

## <span data-ttu-id="9878f-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9878f-145">RELATED LINKS</span></span>

[<span data-ttu-id="9878f-146">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9878f-146">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="9878f-147">Yeni-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9878f-147">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="9878f-148">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9878f-148">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="9878f-149">Özgeçmiş-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9878f-149">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="9878f-150">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9878f-150">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="9878f-151">Başlangıç-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9878f-151">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="9878f-152">Dur-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9878f-152">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="9878f-153">Askıya al-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9878f-153">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


