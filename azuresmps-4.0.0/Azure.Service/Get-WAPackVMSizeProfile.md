---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 48211644-1B92-443D-A992-BDF517D89341
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49b4039e07cf9f393a85c9592598ad870586fd06
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107430"
---
# <span data-ttu-id="d84da-101">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="d84da-101">Get-WAPackVMSizeProfile</span></span>

## <span data-ttu-id="d84da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d84da-102">SYNOPSIS</span></span>
<span data-ttu-id="d84da-103">Boyut profili nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="d84da-103">Gets size profile objects.</span></span>

## <span data-ttu-id="d84da-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d84da-104">SYNTAX</span></span>

### <span data-ttu-id="d84da-105">Boş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d84da-105">Empty (Default)</span></span>
```
Get-WAPackVMSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d84da-106">FromId</span><span class="sxs-lookup"><span data-stu-id="d84da-106">FromId</span></span>
```
Get-WAPackVMSizeProfile [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d84da-107">FromName</span><span class="sxs-lookup"><span data-stu-id="d84da-107">FromName</span></span>
```
Get-WAPackVMSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d84da-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d84da-108">DESCRIPTION</span></span>
<span data-ttu-id="d84da-109">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="d84da-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="d84da-110">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d84da-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d84da-111">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d84da-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d84da-112">**Get-WAPackVMSizeProfile** cmdlet 'i sanal makinelerin boyut profili nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="d84da-112">The **Get-WAPackVMSizeProfile** cmdlet gets size profile objects for virtual machines.</span></span>

## <span data-ttu-id="d84da-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d84da-113">EXAMPLES</span></span>

### <span data-ttu-id="d84da-114">Örnek 1: ad kullanarak boyut profili alma</span><span class="sxs-lookup"><span data-stu-id="d84da-114">Example 1: Get a size profile by using a name</span></span>
```
PS C:\> Get-WAPackVMSizeProfile -Name "ContosoSizeProfile07"
```

<span data-ttu-id="d84da-115">Bu komut, ContosoSizeProfile07 adlı boyut profilini alır.</span><span class="sxs-lookup"><span data-stu-id="d84da-115">This command gets the size profile named ContosoSizeProfile07.</span></span>

### <span data-ttu-id="d84da-116">Örnek 2: bir KIMLIK kullanarak boyut profili alma</span><span class="sxs-lookup"><span data-stu-id="d84da-116">Example 2: Get a size profile by using an ID</span></span>
```
PS C:\> Get-WAPackVMSizeProfile -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="d84da-117">Bu komut belirtilen KIMLIĞE sahip olan boyut profilini alır.</span><span class="sxs-lookup"><span data-stu-id="d84da-117">This command gets the size profile that has the specified ID.</span></span>

### <span data-ttu-id="d84da-118">Örnek 3: tüm boyut profillerini alma</span><span class="sxs-lookup"><span data-stu-id="d84da-118">Example 3: Get all size profiles</span></span>
```
PS C:\> Get-WAPackVMSizeProfile
```

<span data-ttu-id="d84da-119">Bu komut, tüm boyut profillerini alır.</span><span class="sxs-lookup"><span data-stu-id="d84da-119">This command gets all the size profiles.</span></span>

## <span data-ttu-id="d84da-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d84da-120">PARAMETERS</span></span>

### <span data-ttu-id="d84da-121">-ID</span><span class="sxs-lookup"><span data-stu-id="d84da-121">-ID</span></span>
<span data-ttu-id="d84da-122">Boyut profilinin benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d84da-122">Specifies the unique ID of a size profile.</span></span>

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

### <span data-ttu-id="d84da-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="d84da-123">-Name</span></span>
<span data-ttu-id="d84da-124">Boyut profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d84da-124">Specifies the name of a size profile.</span></span>

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

### <span data-ttu-id="d84da-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="d84da-125">-Profile</span></span>
<span data-ttu-id="d84da-126">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d84da-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d84da-127">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="d84da-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d84da-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d84da-128">CommonParameters</span></span>
<span data-ttu-id="d84da-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d84da-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d84da-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d84da-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d84da-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d84da-131">INPUTS</span></span>

## <span data-ttu-id="d84da-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d84da-132">OUTPUTS</span></span>

## <span data-ttu-id="d84da-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d84da-133">NOTES</span></span>

## <span data-ttu-id="d84da-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d84da-134">RELATED LINKS</span></span>

[<span data-ttu-id="d84da-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="d84da-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


