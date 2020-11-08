---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 37C788AC-B369-432B-8276-27FFB0B4CF10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d2913877a9f68621bb5c1c930443a46e91e5935
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107391"
---
# <span data-ttu-id="f4ce5-101">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="f4ce5-101">Get-WAPackVMTemplate</span></span>

## <span data-ttu-id="f4ce5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4ce5-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ce5-103">Sanal makine şablonlarını alır.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-103">Gets virtual machine templates.</span></span>

## <span data-ttu-id="f4ce5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4ce5-104">SYNTAX</span></span>

### <span data-ttu-id="f4ce5-105">Boş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f4ce5-105">Empty (Default)</span></span>
```
Get-WAPackVMTemplate [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f4ce5-106">FromId</span><span class="sxs-lookup"><span data-stu-id="f4ce5-106">FromId</span></span>
```
Get-WAPackVMTemplate [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f4ce5-107">FromName</span><span class="sxs-lookup"><span data-stu-id="f4ce5-107">FromName</span></span>
```
Get-WAPackVMTemplate [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f4ce5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4ce5-108">DESCRIPTION</span></span>
<span data-ttu-id="f4ce5-109">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="f4ce5-110">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f4ce5-111">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f4ce5-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f4ce5-112">**Get-WAPackVMTemplate** cmdlet 'i sanal makine şablonlarını alır.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-112">The **Get-WAPackVMTemplate** cmdlet gets virtual machine templates.</span></span>

## <span data-ttu-id="f4ce5-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4ce5-113">EXAMPLES</span></span>

### <span data-ttu-id="f4ce5-114">Örnek 1: ad kullanarak sanal makine şablonu alma</span><span class="sxs-lookup"><span data-stu-id="f4ce5-114">Example 1: Get a virtual machine template by using a name</span></span>
```
PS C:\> Get-WAPackVMTemplate -Name "ContosoTemplate04"
```

<span data-ttu-id="f4ce5-115">Bu komut, ContosoTemplate04 adlı sanal makine şablonunu alır.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-115">This command gets the virtual machine template named ContosoTemplate04.</span></span>

### <span data-ttu-id="f4ce5-116">Örnek 2: KIMLIK kullanarak sanal makine şablonu alma</span><span class="sxs-lookup"><span data-stu-id="f4ce5-116">Example 2: Get a virtual machine template by using an ID</span></span>
```
PS C:\> Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="f4ce5-117">Bu komut belirtilen KIMLIĞE sahip sanal makine şablonunu alır.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-117">This command gets the virtual machine template that has the specified ID.</span></span>

### <span data-ttu-id="f4ce5-118">Örnek 3: tüm sanal makine şablonlarını edinin</span><span class="sxs-lookup"><span data-stu-id="f4ce5-118">Example 3: Get all virtual machine templates</span></span>
```
PS C:\> Get-WAPackVMTemplate
```

<span data-ttu-id="f4ce5-119">Bu komut, tüm sanal makine şablonlarını alır.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-119">This command gets all the virtual machine templates.</span></span>

## <span data-ttu-id="f4ce5-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4ce5-120">PARAMETERS</span></span>

### <span data-ttu-id="f4ce5-121">-ID</span><span class="sxs-lookup"><span data-stu-id="f4ce5-121">-ID</span></span>
<span data-ttu-id="f4ce5-122">Şablonun benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-122">Specifies the unique ID of a template.</span></span>

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

### <span data-ttu-id="f4ce5-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="f4ce5-123">-Name</span></span>
<span data-ttu-id="f4ce5-124">Şablonun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-124">Specifies the name of a template.</span></span>

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

### <span data-ttu-id="f4ce5-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="f4ce5-125">-Profile</span></span>
<span data-ttu-id="f4ce5-126">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f4ce5-127">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f4ce5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ce5-128">CommonParameters</span></span>
<span data-ttu-id="f4ce5-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ce5-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4ce5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ce5-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4ce5-131">INPUTS</span></span>

## <span data-ttu-id="f4ce5-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4ce5-132">OUTPUTS</span></span>

## <span data-ttu-id="f4ce5-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4ce5-133">NOTES</span></span>

## <span data-ttu-id="f4ce5-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4ce5-134">RELATED LINKS</span></span>

[<span data-ttu-id="f4ce5-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f4ce5-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


