---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 53BD6ED4-EA66-448B-8B18-F078C0738AF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90f02a261dc804f46a7ef503879a8ce9f43fad35
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107400"
---
# <span data-ttu-id="01bd9-101">New-WAPackQuickVM</span><span class="sxs-lookup"><span data-stu-id="01bd9-101">New-WAPackQuickVM</span></span>

## <span data-ttu-id="01bd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01bd9-102">SYNOPSIS</span></span>
<span data-ttu-id="01bd9-103">Şablona dayalı bir sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="01bd9-103">Creates a virtual machine based on a template.</span></span>

## <span data-ttu-id="01bd9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01bd9-104">SYNTAX</span></span>

```
New-WAPackQuickVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="01bd9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="01bd9-105">DESCRIPTION</span></span>
<span data-ttu-id="01bd9-106">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="01bd9-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="01bd9-107">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="01bd9-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="01bd9-108">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="01bd9-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="01bd9-109">**Yeni-WAPackQuickVM** cmdlet 'i, şablona dayalı bir sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="01bd9-109">The **New-WAPackQuickVM** cmdlet creates a virtual machine based on a template.</span></span>

## <span data-ttu-id="01bd9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01bd9-110">EXAMPLES</span></span>

### <span data-ttu-id="01bd9-111">Örnek 1: şablona dayalı sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="01bd9-111">Example 1: Create a virtual machine based on a template</span></span>
```
PS C:\> $Credentials = Get-Credential
PS C:\> $TemplateId = Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
PS C:\> New-WAPackQuickVM -Name "VirtualMachine023" -Template $TemplateId -VMCredential $Credentials
```

<span data-ttu-id="01bd9-112">İlk komut bir **PSCredential** nesnesi oluşturur ve $Credentials değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="01bd9-112">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>
<span data-ttu-id="01bd9-113">Cmdlet bir hesap ve parola sorar.</span><span class="sxs-lookup"><span data-stu-id="01bd9-113">The cmdlet prompts you for an account and password.</span></span>
<span data-ttu-id="01bd9-114">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="01bd9-114">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="01bd9-115">İkinci komut **Get-WAPackVMTemplate** cmdlet 'ini kullanarak bir şablon alır.</span><span class="sxs-lookup"><span data-stu-id="01bd9-115">The second command gets a template by using the **Get-WAPackVMTemplate** cmdlet.</span></span>
<span data-ttu-id="01bd9-116">Komut, şablonun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="01bd9-116">The command specifies the ID of a template.</span></span>
<span data-ttu-id="01bd9-117">Komut, şablon nesnesini $TemplateID değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="01bd9-117">The command stores the template object in the $TemplateID variable.</span></span>

<span data-ttu-id="01bd9-118">Son komutu, VirtualMachine023 adlı bir sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="01bd9-118">The final command creates a virtual machine named VirtualMachine023.</span></span>
<span data-ttu-id="01bd9-119">Komut, $TemplateId depolanan şablondaki sanal makineyi temel alır.</span><span class="sxs-lookup"><span data-stu-id="01bd9-119">The command bases the virtual machine on the template stored in $TemplateId.</span></span>

## <span data-ttu-id="01bd9-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01bd9-120">PARAMETERS</span></span>

### <span data-ttu-id="01bd9-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="01bd9-121">-Name</span></span>
<span data-ttu-id="01bd9-122">Sanal makine için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="01bd9-122">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="01bd9-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="01bd9-123">-Profile</span></span>
<span data-ttu-id="01bd9-124">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="01bd9-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="01bd9-125">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="01bd9-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="01bd9-126">-Şablon</span><span class="sxs-lookup"><span data-stu-id="01bd9-126">-Template</span></span>
<span data-ttu-id="01bd9-127">Şablon belirtir.</span><span class="sxs-lookup"><span data-stu-id="01bd9-127">Specifies a template.</span></span>
<span data-ttu-id="01bd9-128">Cmdlet, belirttiğiniz şablona göre bir sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="01bd9-128">The cmdlet creates a virtual machine based on the template that you specify.</span></span>
<span data-ttu-id="01bd9-129">Şablon nesnesi edinmek için **Get-WAPackVMTemplate** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="01bd9-129">To obtain a template object, use the **Get-WAPackVMTemplate** cmdlet.</span></span>

```yaml
Type: VMTemplate
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01bd9-130">-VMCredential</span><span class="sxs-lookup"><span data-stu-id="01bd9-130">-VMCredential</span></span>
<span data-ttu-id="01bd9-131">Yerel yönetici hesabının kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="01bd9-131">Specifies the credential for the local Administrator account.</span></span>
<span data-ttu-id="01bd9-132">**PSCredential** nesnesi almak için **Get-Credential** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="01bd9-132">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="01bd9-133">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="01bd9-133">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01bd9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01bd9-134">CommonParameters</span></span>
<span data-ttu-id="01bd9-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01bd9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01bd9-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01bd9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01bd9-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01bd9-137">INPUTS</span></span>

## <span data-ttu-id="01bd9-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01bd9-138">OUTPUTS</span></span>

## <span data-ttu-id="01bd9-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01bd9-139">NOTES</span></span>

## <span data-ttu-id="01bd9-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01bd9-140">RELATED LINKS</span></span>

[<span data-ttu-id="01bd9-141">Yeni-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="01bd9-141">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="01bd9-142">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="01bd9-142">Get-WAPackVMTemplate</span></span>](./Get-WAPackVMTemplate.md)


