---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E499868E-A745-4CA4-A717-C33C3B94A2C8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b80071bb82ebbb960be5b5b4fcc854dc47c9ed9d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105992"
---
# <span data-ttu-id="82e3a-101">New-AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="82e3a-101">New-AzureRoleTemplate</span></span>

## <span data-ttu-id="82e3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="82e3a-103">Web ve çalışan rolü şablonları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="82e3a-103">Creates web and worker role templates.</span></span>

## <span data-ttu-id="82e3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="82e3a-104">SYNTAX</span></span>

### <span data-ttu-id="82e3a-105">WebRole</span><span class="sxs-lookup"><span data-stu-id="82e3a-105">WebRole</span></span>
```
New-AzureRoleTemplate [-Web] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="82e3a-106">WorkerRole</span><span class="sxs-lookup"><span data-stu-id="82e3a-106">WorkerRole</span></span>
```
New-AzureRoleTemplate [-Worker] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="82e3a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="82e3a-107">DESCRIPTION</span></span>
<span data-ttu-id="82e3a-108">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="82e3a-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="82e3a-109">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="82e3a-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="82e3a-110">**Yeni-AzureRoleTemplate** cmdlet 'i Web ve işçi rol şablonları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="82e3a-110">The **New-AzureRoleTemplate** cmdlet creates web and worker role templates.</span></span>

## <span data-ttu-id="82e3a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="82e3a-111">EXAMPLES</span></span>

### <span data-ttu-id="82e3a-112">Örnek 1: Web rolü şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="82e3a-112">Example 1: Create a web role template</span></span>
```
PS C:\> New-AzureRoleTemplate -Web
```

<span data-ttu-id="82e3a-113">Bu örnek, geçerli dizindeki WebRoleTemplate adlı klasörde yeni bir Web rolü şablonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="82e3a-113">This example creates a new web role template in a folder named WebRoleTemplate in the current directory.</span></span>

### <span data-ttu-id="82e3a-114">Örnek 2: çalışan rolü şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="82e3a-114">Example 2: Create a worker role template</span></span>
```
PS C:\> New-AzureRoleTemplate -Worker
```

<span data-ttu-id="82e3a-115">Bu örnek, geçerli dizindeki WebRoleTemplate adlı klasörde yeni bir çalışan rolü şablonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="82e3a-115">This example creates a new worker role template in a folder named WebRoleTemplate in the current directory.</span></span>

### <span data-ttu-id="82e3a-116">Örnek 3: özel bir dizinde rol şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="82e3a-116">Example 3: Create a role template in a custom directory</span></span>
```
PS C:\> New-AzureRoleTemplate -Web -Output C:\MyWebRoleTemplate
```

<span data-ttu-id="82e3a-117">Bu örnek, geçerli dizin yerine MyWebRoleTemplate adlı dizinde yeni bir Web rolü şablonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="82e3a-117">This example creates a new web role template in directory named MyWebRoleTemplate, instead of in the current directory.</span></span>

## <span data-ttu-id="82e3a-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="82e3a-118">PARAMETERS</span></span>

### <span data-ttu-id="82e3a-119">-Çıktı</span><span class="sxs-lookup"><span data-stu-id="82e3a-119">-Output</span></span>
<span data-ttu-id="82e3a-120">Oluşturulan şablonun çıkış yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="82e3a-120">Specifies the output path of generated template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82e3a-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="82e3a-121">-Profile</span></span>
<span data-ttu-id="82e3a-122">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="82e3a-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="82e3a-123">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="82e3a-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="82e3a-124">-Web</span><span class="sxs-lookup"><span data-stu-id="82e3a-124">-Web</span></span>
<span data-ttu-id="82e3a-125">Web rolü şablonu oluşturmak istediğinizi belirtir.</span><span class="sxs-lookup"><span data-stu-id="82e3a-125">Specifies that you want to create a web role template.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82e3a-126">-Çalışan</span><span class="sxs-lookup"><span data-stu-id="82e3a-126">-Worker</span></span>
<span data-ttu-id="82e3a-127">Bir çalışan rolü oluşturmak istediğinizi belirtir.</span><span class="sxs-lookup"><span data-stu-id="82e3a-127">Specifies that you want to create a worker role template.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WorkerRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82e3a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82e3a-128">CommonParameters</span></span>
<span data-ttu-id="82e3a-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="82e3a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82e3a-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82e3a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82e3a-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="82e3a-131">INPUTS</span></span>

## <span data-ttu-id="82e3a-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="82e3a-132">OUTPUTS</span></span>

## <span data-ttu-id="82e3a-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="82e3a-133">NOTES</span></span>

## <span data-ttu-id="82e3a-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="82e3a-134">RELATED LINKS</span></span>

[<span data-ttu-id="82e3a-135">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="82e3a-135">Add-AzureWebRole</span></span>](./Add-AzureWebRole.md)

[<span data-ttu-id="82e3a-136">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="82e3a-136">Add-AzureWorkerRole</span></span>](./Add-AzureWorkerRole.md)


