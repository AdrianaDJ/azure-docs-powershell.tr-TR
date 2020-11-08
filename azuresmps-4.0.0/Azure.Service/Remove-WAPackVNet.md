---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 42042533-9F84-4189-8C9F-01FD62F89DC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: db14b17e42d23e481468f563768b606d8baa2802
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107406"
---
# <span data-ttu-id="9e450-101">Remove-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="9e450-101">Remove-WAPackVNet</span></span>

## <span data-ttu-id="9e450-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e450-102">SYNOPSIS</span></span>
<span data-ttu-id="9e450-103">Sanal ağ nesnelerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9e450-103">Removes virtual network objects.</span></span>

## <span data-ttu-id="9e450-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e450-104">SYNTAX</span></span>

```
Remove-WAPackVNet -VNet <VMNetwork> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9e450-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e450-105">DESCRIPTION</span></span>
<span data-ttu-id="9e450-106">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="9e450-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="9e450-107">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9e450-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9e450-108">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9e450-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9e450-109">**Remove-WAPackVNet** cmdlet 'i sanal ağ nesnelerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9e450-109">The **Remove-WAPackVNet** cmdlet removes virtual network objects.</span></span>

## <span data-ttu-id="9e450-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e450-110">EXAMPLES</span></span>

### <span data-ttu-id="9e450-111">Örnek 1: sanallaştırılmış bir ağı kaldırma</span><span class="sxs-lookup"><span data-stu-id="9e450-111">Example 1: Remove a virtualized network</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Remove-WAPackVM -VNet $VNet
```

<span data-ttu-id="9e450-112">İlk komut ContosoVNet01 adlı sanallaştırılmış ağı **Get-WAPackVNet** cmdlet 'ini kullanarak alır ve bu nesneyi $VNET değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9e450-112">The first command gets the virtualized network named ContosoVNet01 by using the **Get-WAPackVNet** cmdlet, and then stores that object in the $VNet variable.</span></span>
<span data-ttu-id="9e450-113">İkinci komut $VNet 'da depolanan sanallaştırılmış ağı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9e450-113">The second command removes the virtualized network stored in $VNet.</span></span>
<span data-ttu-id="9e450-114">Komut sizden onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9e450-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="9e450-115">Örnek 2: bir sanallaştırılmış ağı onaysız kaldırma</span><span class="sxs-lookup"><span data-stu-id="9e450-115">Example 2: Remove a virtualized network without confirmation</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet02"
PS C:\> Remove-WAPackVNet -VNet $VNet -Force
```

<span data-ttu-id="9e450-116">İlk komut **Get-WAPackVNet** cmdlet 'Ini kullanarak ContosoVNet02 adındaki bulut hizmetini alır ve bu nesneyi $VNET değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9e450-116">The first command gets the cloud service named ContosoVNet02 by using the **Get-WAPackVNet** cmdlet, and then stores that object in the $VNet variable.</span></span>
<span data-ttu-id="9e450-117">İkinci komut $VNet 'da depolanan sanallaştırılmış ağı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9e450-117">The second command removes the virtualized network stored in $VNet.</span></span>
<span data-ttu-id="9e450-118">Bu komut *Force* parametresini içerir.</span><span class="sxs-lookup"><span data-stu-id="9e450-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="9e450-119">Komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="9e450-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="9e450-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e450-120">PARAMETERS</span></span>

### <span data-ttu-id="9e450-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9e450-121">-Force</span></span>
<span data-ttu-id="9e450-122">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="9e450-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9e450-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9e450-123">-PassThru</span></span>
<span data-ttu-id="9e450-124">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="9e450-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9e450-125">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="9e450-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9e450-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="9e450-126">-Profile</span></span>
<span data-ttu-id="9e450-127">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e450-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9e450-128">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="9e450-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9e450-129">-VNet</span><span class="sxs-lookup"><span data-stu-id="9e450-129">-VNet</span></span>
<span data-ttu-id="9e450-130">Sanallaştırılmış bir ağ belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e450-130">Specifies a virtualized network.</span></span>
<span data-ttu-id="9e450-131">Sanallaştırılmış bir ağ edinmek için **Get-WAPackVNet** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9e450-131">To obtain a virtualized network, use the **Get-WAPackVNet** cmdlet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e450-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e450-132">CommonParameters</span></span>
<span data-ttu-id="9e450-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e450-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e450-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e450-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e450-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e450-135">INPUTS</span></span>

## <span data-ttu-id="9e450-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e450-136">OUTPUTS</span></span>

## <span data-ttu-id="9e450-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e450-137">NOTES</span></span>

## <span data-ttu-id="9e450-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e450-138">RELATED LINKS</span></span>

[<span data-ttu-id="9e450-139">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="9e450-139">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="9e450-140">Yeni-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="9e450-140">New-WAPackVNet</span></span>](./New-WAPackVNet.md)


