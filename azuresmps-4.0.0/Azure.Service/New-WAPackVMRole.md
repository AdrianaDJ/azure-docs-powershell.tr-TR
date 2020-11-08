---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6617AA59-CDD1-4BA9-84A7-F3914BF1D4B7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 14e201dc916f15b63b0e825f4ca2e37015aaa9bc
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107390"
---
# <span data-ttu-id="15715-101">New-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="15715-101">New-WAPackVMRole</span></span>

## <span data-ttu-id="15715-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15715-102">SYNOPSIS</span></span>
<span data-ttu-id="15715-103">Sanal makine rolü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15715-103">Creates a virtual machine role.</span></span>

## <span data-ttu-id="15715-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15715-104">SYNTAX</span></span>

### <span data-ttu-id="15715-105">Hızlı oluştur (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="15715-105">QuickCreate (Default)</span></span>
```
New-WAPackVMRole -Name <String> -Label <String> -ResourceDefinition <VMRoleResourceDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="15715-106">Fromchoparlör hizmeti</span><span class="sxs-lookup"><span data-stu-id="15715-106">FromCloudService</span></span>
```
New-WAPackVMRole -Name <String> -Label <String> -ResourceDefinition <VMRoleResourceDefinition>
 -CloudService <CloudService> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="15715-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="15715-107">DESCRIPTION</span></span>
<span data-ttu-id="15715-108">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="15715-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="15715-109">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="15715-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="15715-110">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="15715-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="15715-111">**Yeni-WAPackVMRole** cmdlet 'i sanal makine rolü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15715-111">The **New-WAPackVMRole** cmdlet creates a virtual machine role.</span></span>

## <span data-ttu-id="15715-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15715-112">EXAMPLES</span></span>

### <span data-ttu-id="15715-113">Örnek 1: sanal makine rolü oluşturma (WAP)</span><span class="sxs-lookup"><span data-stu-id="15715-113">Example 1: Create a virtual machine role (emulating WAP behavior)</span></span>
```
PS C:\> New-WAPackVMRole -Name "ContosoVMRole01" -Label "ContosoVMRoleLabel01" -ResourceDefinition $resdef
```

<span data-ttu-id="15715-114">Herhangi bir bulut hizmeti belirttiğimiz (WAP, WAP davranışı), komut, sanal makine rolüyle aynı ada sahip olacak bir bulut hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15715-114">Since we do not specify any cloud service (emulating WAP behavior), the command will create a cloud service for us which will have the same name as the virtual machine role.</span></span>
<span data-ttu-id="15715-115">Bu durumda aşağıdaki komut, ContosoVMRole01 adında bir sanal makine rolü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15715-115">In this case, the following command will create a virtual machine role with the name ContosoVMRole01, label ContosoVMRoleLabel01.</span></span>
<span data-ttu-id="15715-116">Burada kullanılan kaynak tanımının PowerShell 'den el ile oluşturulması gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="15715-116">Note that the resource definition being used here has to be manually created though PowerShell.</span></span>

## <span data-ttu-id="15715-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15715-117">PARAMETERS</span></span>

### <span data-ttu-id="15715-118">-CloudService</span><span class="sxs-lookup"><span data-stu-id="15715-118">-CloudService</span></span>
<span data-ttu-id="15715-119">Sanal makine rolü için bir bulut hizmeti belirtir.</span><span class="sxs-lookup"><span data-stu-id="15715-119">Specifies a cloud service for the virtual machine role.</span></span>

```yaml
Type: CloudService
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15715-120">Etiketli</span><span class="sxs-lookup"><span data-stu-id="15715-120">-Label</span></span>
<span data-ttu-id="15715-121">Sanal makine rolü için bir etiket belirtir.</span><span class="sxs-lookup"><span data-stu-id="15715-121">Specifies a label for the virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15715-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="15715-122">-Name</span></span>
<span data-ttu-id="15715-123">Sanal makine rolü için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="15715-123">Specifies a name for the virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15715-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="15715-124">-Profile</span></span>
<span data-ttu-id="15715-125">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="15715-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="15715-126">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="15715-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="15715-127">-ResourceDefinition</span><span class="sxs-lookup"><span data-stu-id="15715-127">-ResourceDefinition</span></span>
<span data-ttu-id="15715-128">Sanal makine rolü için bir kaynak tanımı belirtir.</span><span class="sxs-lookup"><span data-stu-id="15715-128">Specifies a resource definition for the virtual machine role.</span></span>

```yaml
Type: VMRoleResourceDefinition
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15715-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15715-129">CommonParameters</span></span>
<span data-ttu-id="15715-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15715-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15715-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15715-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15715-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15715-132">INPUTS</span></span>

## <span data-ttu-id="15715-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15715-133">OUTPUTS</span></span>

## <span data-ttu-id="15715-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15715-134">NOTES</span></span>

## <span data-ttu-id="15715-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15715-135">RELATED LINKS</span></span>

[<span data-ttu-id="15715-136">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="15715-136">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="15715-137">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="15715-137">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)

[<span data-ttu-id="15715-138">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="15715-138">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


