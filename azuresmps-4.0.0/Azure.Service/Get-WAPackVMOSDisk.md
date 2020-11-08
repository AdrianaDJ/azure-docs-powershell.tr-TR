---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E6E40D1B-A5BC-4B38-9D22-F06A8E4DABDF
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1360f45b751088bd899282cee2e64ce965d11fb
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107352"
---
# <span data-ttu-id="e0f6e-101">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="e0f6e-101">Get-WAPackVMOSDisk</span></span>

## <span data-ttu-id="e0f6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0f6e-102">SYNOPSIS</span></span>
<span data-ttu-id="e0f6e-103">Sanal makinelerin işletim sistemi disk nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="e0f6e-103">Gets operating system disk objects for virtual machines.</span></span>

## <span data-ttu-id="e0f6e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0f6e-104">SYNTAX</span></span>

### <span data-ttu-id="e0f6e-105">Boş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e0f6e-105">Empty (Default)</span></span>
```
Get-WAPackVMOSDisk [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e0f6e-106">FromId</span><span class="sxs-lookup"><span data-stu-id="e0f6e-106">FromId</span></span>
```
Get-WAPackVMOSDisk [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e0f6e-107">FromName</span><span class="sxs-lookup"><span data-stu-id="e0f6e-107">FromName</span></span>
```
Get-WAPackVMOSDisk [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e0f6e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0f6e-108">DESCRIPTION</span></span>
<span data-ttu-id="e0f6e-109">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="e0f6e-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="e0f6e-110">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e0f6e-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e0f6e-111">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e0f6e-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e0f6e-112">**Get-Wapackvmosdısk** cmdlet 'i sanal makinelerin işletim sistemi disk nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="e0f6e-112">The **Get-WAPackVMOSDisk** cmdlet gets operating system disk objects for virtual machines.</span></span>

## <span data-ttu-id="e0f6e-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0f6e-113">EXAMPLES</span></span>

### <span data-ttu-id="e0f6e-114">Örnek 1: bir ad kullanarak işletim sistemi diski edinme</span><span class="sxs-lookup"><span data-stu-id="e0f6e-114">Example 1: Get an operating system disk by using a name</span></span>
```
PS C:\> Get-WAPackVMOSDisk -Name "ContosoOSDisk"
```

<span data-ttu-id="e0f6e-115">Bu komut, ContosoOSDisk adlı bir işletim sistemi diskini alır.</span><span class="sxs-lookup"><span data-stu-id="e0f6e-115">This command gets an operating system disk named ContosoOSDisk.</span></span>

### <span data-ttu-id="e0f6e-116">Örnek 2: bir KIMLIK kullanarak işletim sistemi diski edinme</span><span class="sxs-lookup"><span data-stu-id="e0f6e-116">Example 2: Get an operating system disk by using an ID</span></span>
```
PS C:\> Get-WAPackVMOSDisk -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="e0f6e-117">Bu komut, belirtilen KIMLIĞE sahip işletim sistemi diskini alır.</span><span class="sxs-lookup"><span data-stu-id="e0f6e-117">This command gets the operating system disk that has the specified ID.</span></span>

### <span data-ttu-id="e0f6e-118">Örnek 3: tüm işletim sistemi disklerini alma</span><span class="sxs-lookup"><span data-stu-id="e0f6e-118">Example 3: Get all operating system disks</span></span>
```
PS C:\> Get-WAPackVMOSDisk
```

<span data-ttu-id="e0f6e-119">Bu komut, tüm işletim sistemi disklerini alır.</span><span class="sxs-lookup"><span data-stu-id="e0f6e-119">This command gets all operating system disks.</span></span>

## <span data-ttu-id="e0f6e-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0f6e-120">PARAMETERS</span></span>

### <span data-ttu-id="e0f6e-121">-ID</span><span class="sxs-lookup"><span data-stu-id="e0f6e-121">-ID</span></span>
<span data-ttu-id="e0f6e-122">İşletim sistemi diskinin benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0f6e-122">Specifies the unique ID of an operating system disk.</span></span>

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

### <span data-ttu-id="e0f6e-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="e0f6e-123">-Name</span></span>
<span data-ttu-id="e0f6e-124">İşletim sistemi diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0f6e-124">Specifies the name of an operating system disk.</span></span>

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

### <span data-ttu-id="e0f6e-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="e0f6e-125">-Profile</span></span>
<span data-ttu-id="e0f6e-126">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0f6e-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e0f6e-127">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e0f6e-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e0f6e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0f6e-128">CommonParameters</span></span>
<span data-ttu-id="e0f6e-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0f6e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0f6e-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0f6e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0f6e-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0f6e-131">INPUTS</span></span>

## <span data-ttu-id="e0f6e-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0f6e-132">OUTPUTS</span></span>

## <span data-ttu-id="e0f6e-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0f6e-133">NOTES</span></span>

## <span data-ttu-id="e0f6e-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0f6e-134">RELATED LINKS</span></span>

[<span data-ttu-id="e0f6e-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="e0f6e-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


