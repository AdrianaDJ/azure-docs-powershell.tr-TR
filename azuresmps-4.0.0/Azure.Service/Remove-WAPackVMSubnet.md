---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7766E3D-D8C2-42F1-840A-8EA633E98500
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8a85934deb617b4f0d8e85ee3162222f16dd294
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107407"
---
# <span data-ttu-id="f3c16-101">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="f3c16-101">Remove-WAPackVMSubnet</span></span>

## <span data-ttu-id="f3c16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3c16-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c16-103">Sanal makine alt ağ nesnelerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f3c16-103">Removes virtual machine subnet objects.</span></span>

## <span data-ttu-id="f3c16-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f3c16-104">SYNTAX</span></span>

```
Remove-WAPackVMSubnet -VMSubnet <VMSubnet> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3c16-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f3c16-105">DESCRIPTION</span></span>
<span data-ttu-id="f3c16-106">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="f3c16-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="f3c16-107">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f3c16-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f3c16-108">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f3c16-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f3c16-109">**Remove-WAPackVMSubnet** cmdlet 'i sanal makine alt ağ nesnelerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f3c16-109">The **Remove-WAPackVMSubnet** cmdlet removes virtual machine subnet objects.</span></span>

## <span data-ttu-id="f3c16-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f3c16-110">EXAMPLES</span></span>

### <span data-ttu-id="f3c16-111">Örnek 1: sanal makine alt ağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="f3c16-111">Example 1: Remove a virtual machine subnet</span></span>
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet01"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet
```

<span data-ttu-id="f3c16-112">İlk komut ContosoVMSubnet01 adındaki sanal makine alt ağını **Get-WAPackVMSubnet** cmdlet 'ini kullanarak alır ve bu nesneyi $VMSubnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f3c16-112">The first command gets the virtual machine subnet named ContosoVMSubnet01 by using the **Get-WAPackVMSubnet** cmdlet, and then stores that object in the $VMSubnet variable.</span></span>

<span data-ttu-id="f3c16-113">İkinci komut, $VMSubnet depolanan sanal makine alt ağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f3c16-113">The second command removes the virtual machine subnet stored in $VMSubnet.</span></span>
<span data-ttu-id="f3c16-114">Komut sizden onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f3c16-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="f3c16-115">Örnek 2: onaysız sanal makineyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="f3c16-115">Example 2: Remove a virtual machine without confirmation</span></span>
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet02"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet -Force
```

<span data-ttu-id="f3c16-116">İlk komut **Get-WAPackVMSubnet** cmdlet 'Ini kullanarak ContosoVMSubnet02 adındaki bulut hizmetini alır ve bu nesneyi $VMSubnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f3c16-116">The first command gets the cloud service named ContosoVMSubnet02 by using the **Get-WAPackVMSubnet** cmdlet, and then stores that object in the $VMSubnet variable.</span></span>

<span data-ttu-id="f3c16-117">İkinci komut, $VMSubnet depolanan sanal makine alt ağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f3c16-117">The second command removes the virtual machine subnet stored in $VMSubnet.</span></span>
<span data-ttu-id="f3c16-118">Bu komut *Force* parametresini içerir.</span><span class="sxs-lookup"><span data-stu-id="f3c16-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="f3c16-119">Komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="f3c16-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f3c16-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f3c16-120">PARAMETERS</span></span>

### <span data-ttu-id="f3c16-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f3c16-121">-Force</span></span>
<span data-ttu-id="f3c16-122">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f3c16-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f3c16-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f3c16-123">-PassThru</span></span>
<span data-ttu-id="f3c16-124">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="f3c16-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f3c16-125">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="f3c16-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f3c16-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="f3c16-126">-Profile</span></span>
<span data-ttu-id="f3c16-127">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3c16-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f3c16-128">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="f3c16-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f3c16-129">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="f3c16-129">-VMSubnet</span></span>
<span data-ttu-id="f3c16-130">Bir sanal makine alt ağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3c16-130">Specifies a virtual machine subnet.</span></span>
<span data-ttu-id="f3c16-131">Sanal makine alt ağı edinmek için **Get-WAPackVMSubnet** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f3c16-131">To obtain a virtual machine subnet, use the **Get-WAPackVMSubnet** cmdlet.</span></span>

```yaml
Type: VMSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c16-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c16-132">CommonParameters</span></span>
<span data-ttu-id="f3c16-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f3c16-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c16-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3c16-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c16-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f3c16-135">INPUTS</span></span>

## <span data-ttu-id="f3c16-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f3c16-136">OUTPUTS</span></span>

## <span data-ttu-id="f3c16-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f3c16-137">NOTES</span></span>

## <span data-ttu-id="f3c16-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f3c16-138">RELATED LINKS</span></span>

[<span data-ttu-id="f3c16-139">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="f3c16-139">Get-WAPackVMSubnet</span></span>](./Get-WAPackVMSubnet.md)

[<span data-ttu-id="f3c16-140">Yeni-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="f3c16-140">New-WAPackVMSubnet</span></span>](./New-WAPackVMSubnet.md)


