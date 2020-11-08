---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CE618AD2-7E28-4012-BF3C-B932B95FFDD5
online version: ''
schema: 2.0.0
ms.openlocfilehash: a07358c37bf30e8d5fc3040cdfd174b800df96e4
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107412"
---
# <span data-ttu-id="6e8ac-101">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="6e8ac-101">Remove-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="6e8ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e8ac-102">SYNOPSIS</span></span>
<span data-ttu-id="6e8ac-103">Statik IP adresi havuzu nesnelerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-103">Removes static IP address pool objects.</span></span>

## <span data-ttu-id="6e8ac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6e8ac-104">SYNTAX</span></span>

```
Remove-WAPackStaticIPAddressPool -StaticIPAddressPool <StaticIPAddressPool> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6e8ac-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6e8ac-105">DESCRIPTION</span></span>
<span data-ttu-id="6e8ac-106">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="6e8ac-107">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6e8ac-108">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="6e8ac-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6e8ac-109">**Remove-Wapackstaticıpaddresspool** cmdlet 'ı statik IP adresi havuzu nesnelerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-109">The **Remove-WAPackStaticIPAddressPool** cmdlet removes static IP address pool objects.</span></span>

## <span data-ttu-id="6e8ac-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6e8ac-110">EXAMPLES</span></span>

### <span data-ttu-id="6e8ac-111">Örnek 1: statik IP adresi havuzunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="6e8ac-111">Example 1: Remove a static IP address pool</span></span>
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool01"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool
```

<span data-ttu-id="6e8ac-112">İlk komut ContosoStaticIPAddressPool01 adlı statik IP adresi havuzunu **Get-Wapackstaticıpaddresspool** cmdlet 'ini kullanarak alır ve bu nesneyi $StaticIPAddressPool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-112">The first command gets the static IP address pool named ContosoStaticIPAddressPool01 by using the **Get-WAPackStaticIPAddressPool** cmdlet, and then stores that object in the $StaticIPAddressPool variable.</span></span>

<span data-ttu-id="6e8ac-113">İkinci komut $StaticIPAddressPool depolanan statik IP adresi havuzunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-113">The second command removes the static IP address pool stored in $StaticIPAddressPool.</span></span>
<span data-ttu-id="6e8ac-114">Komut sizden onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="6e8ac-115">Örnek 2: onay olmadan statik IP adresi havuzunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="6e8ac-115">Example 2: Remove a static IP address pool without confirmation</span></span>
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool02"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool -Force
```

<span data-ttu-id="6e8ac-116">İlk komut ContosoStaticIPAddressPool02 adlı statik IP adresi havuzunu **Get-Wapackstaticıpaddresspool** cmdlet 'ini kullanarak alır ve bu nesneyi $ staticıpaddresspool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-116">The first command gets the static IP address pool named ContosoStaticIPAddressPool02 by using the **Get-WAPackStaticIPAddressPool** cmdlet, and then stores that object in the $ StaticIPAddressPool variable.</span></span>

<span data-ttu-id="6e8ac-117">İkinci komut $StaticIPAddressPool depolanan statik IP adresi havuzunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-117">The second command removes the static IP address pool stored in $StaticIPAddressPool.</span></span>
<span data-ttu-id="6e8ac-118">Bu komut *Force* parametresini içerir.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="6e8ac-119">Komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6e8ac-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6e8ac-120">PARAMETERS</span></span>

### <span data-ttu-id="6e8ac-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6e8ac-121">-Force</span></span>
<span data-ttu-id="6e8ac-122">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6e8ac-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6e8ac-123">-PassThru</span></span>
<span data-ttu-id="6e8ac-124">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6e8ac-125">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6e8ac-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="6e8ac-126">-Profile</span></span>
<span data-ttu-id="6e8ac-127">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6e8ac-128">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6e8ac-129">-Staticıpaddresspool</span><span class="sxs-lookup"><span data-stu-id="6e8ac-129">-StaticIPAddressPool</span></span>
<span data-ttu-id="6e8ac-130">Bir Staticıpaddresspool belirtir.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-130">Specifies a StaticIPAddressPool.</span></span>
<span data-ttu-id="6e8ac-131">Statik IP adresi havuzu edinmek için **Get-Wapackstaticıpaddresspool** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-131">To obtain a static IP address pool, use the **Get-WAPackStaticIPAddressPool** cmdlet.</span></span>

```yaml
Type: StaticIPAddressPool
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e8ac-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e8ac-132">CommonParameters</span></span>
<span data-ttu-id="6e8ac-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e8ac-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e8ac-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e8ac-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6e8ac-135">INPUTS</span></span>

## <span data-ttu-id="6e8ac-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6e8ac-136">OUTPUTS</span></span>

## <span data-ttu-id="6e8ac-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6e8ac-137">NOTES</span></span>

## <span data-ttu-id="6e8ac-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6e8ac-138">RELATED LINKS</span></span>

[<span data-ttu-id="6e8ac-139">Get-Wapackstaticıpaddresspool</span><span class="sxs-lookup"><span data-stu-id="6e8ac-139">Get-WAPackStaticIPAddressPool</span></span>](./Get-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="6e8ac-140">Remove-Wapackstaticıpaddresspool</span><span class="sxs-lookup"><span data-stu-id="6e8ac-140">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


