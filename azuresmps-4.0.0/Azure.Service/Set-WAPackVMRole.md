---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 69FBF1E7-E69A-42B5-AC17-C7CF8CAB3C9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da323d5284de94aaadfc92abdf819f861695335
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107383"
---
# <span data-ttu-id="7db83-101">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="7db83-101">Set-WAPackVMRole</span></span>

## <span data-ttu-id="7db83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7db83-102">SYNOPSIS</span></span>
<span data-ttu-id="7db83-103">Sanal makine rolünün örnek sayımı özelliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7db83-103">Changes the instance count property of a virtual machine role.</span></span>

## <span data-ttu-id="7db83-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7db83-104">SYNTAX</span></span>

```
Set-WAPackVMRole -VMRole <VMRole> -InstanceCount <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7db83-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7db83-105">DESCRIPTION</span></span>
<span data-ttu-id="7db83-106">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="7db83-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="7db83-107">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7db83-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7db83-108">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7db83-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7db83-109">**Set-WAPackVMRole** cmdlet 'i, sanal makine rolünün örnek sayımı özelliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7db83-109">The **Set-WAPackVMRole** cmdlet changes the instance count property of a virtual machine role.</span></span>

## <span data-ttu-id="7db83-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7db83-110">EXAMPLES</span></span>

### <span data-ttu-id="7db83-111">Örnek 1: sanal makine rolü için örnek sayımını belirtme</span><span class="sxs-lookup"><span data-stu-id="7db83-111">Example 1: Specify the instance count for a virtual machine role</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Set-WAPackVMRole -VMRole $VMRole -InstanceCount 3
```

<span data-ttu-id="7db83-112">İlk komut ContosoVMRole01 adındaki sanal makine rolünü **Get-WAPackVMRole** cmdlet 'ini kullanarak alır ve bu nesneyi $VMRole değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7db83-112">The first command gets the virtual machine role named ContosoVMRole01 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="7db83-113">İkinci ve son komutu, $VMRole depolanan sanal makine rolünün yeni örnek sayısını 3 olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7db83-113">The second and final command sets the new instance count of the virtual machine role stored in $VMRole to 3.</span></span>

## <span data-ttu-id="7db83-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7db83-114">PARAMETERS</span></span>

### <span data-ttu-id="7db83-115">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="7db83-115">-InstanceCount</span></span>
<span data-ttu-id="7db83-116">Sanal makine rolü için örnek sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7db83-116">Specifies the instance count for a virtual machine role.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7db83-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7db83-117">-PassThru</span></span>
<span data-ttu-id="7db83-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="7db83-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7db83-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="7db83-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7db83-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="7db83-120">-Profile</span></span>
<span data-ttu-id="7db83-121">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7db83-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7db83-122">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="7db83-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7db83-123">-VMRole</span><span class="sxs-lookup"><span data-stu-id="7db83-123">-VMRole</span></span>
<span data-ttu-id="7db83-124">Sanal makine rolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7db83-124">Specifies a virtual machine role.</span></span>
<span data-ttu-id="7db83-125">Sanal makine rolü edinmek için **Get-WAPackVMRole** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7db83-125">To obtain a virtual machine role, use the **Get-WAPackVMRole** cmdlet.</span></span>

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7db83-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7db83-126">CommonParameters</span></span>
<span data-ttu-id="7db83-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7db83-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7db83-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7db83-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7db83-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7db83-129">INPUTS</span></span>

## <span data-ttu-id="7db83-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7db83-130">OUTPUTS</span></span>

## <span data-ttu-id="7db83-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7db83-131">NOTES</span></span>

## <span data-ttu-id="7db83-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7db83-132">RELATED LINKS</span></span>

[<span data-ttu-id="7db83-133">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="7db83-133">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="7db83-134">Yeni-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="7db83-134">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="7db83-135">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="7db83-135">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)


