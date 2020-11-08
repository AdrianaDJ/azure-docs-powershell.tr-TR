---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CB2936E4-E403-44B3-9CB8-617308E54C50
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9059e5bad8441f25846cf98a12c5e8dada2e814a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107397"
---
# <span data-ttu-id="c11b7-101">New-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="c11b7-101">New-WAPackVNet</span></span>

## <span data-ttu-id="c11b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c11b7-102">SYNOPSIS</span></span>
<span data-ttu-id="c11b7-103">Sanallaştırılmış bir ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c11b7-103">Creates a virtualized network.</span></span>

## <span data-ttu-id="c11b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c11b7-104">SYNTAX</span></span>

```
New-WAPackVNet -LogicalNetwork <LogicalNetwork> -Name <String> [-Description <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c11b7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c11b7-105">DESCRIPTION</span></span>
<span data-ttu-id="c11b7-106">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="c11b7-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="c11b7-107">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c11b7-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c11b7-108">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c11b7-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c11b7-109">**Yeni-WAPackVNet** cmdlet 'i sanallaştırılmış bir ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c11b7-109">The **New-WAPackVNet** cmdlet creates a virtualized network.</span></span>

## <span data-ttu-id="c11b7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c11b7-110">EXAMPLES</span></span>

### <span data-ttu-id="c11b7-111">Örnek 1: sanallaştırılmış ağ oluşturma</span><span class="sxs-lookup"><span data-stu-id="c11b7-111">Example 1: Create a virtualized network</span></span>
```
PS C:\> $LogicalNetwork = Get-WAPackLogicalNetwork -Name "ContosoLogicalNetwork01"
PS C:\> New-WAPackVNet -LogicalNetwork $LogicalNetwork -Name "ContosoVNett01" -Description "A description"
```

<span data-ttu-id="c11b7-112">İlk komut öncelikle yeni bir sanallaştırılmış ağ eklemek istediğimiz mantıksal ağı alır.</span><span class="sxs-lookup"><span data-stu-id="c11b7-112">The first command first retrieves the logical network to which we want to add a new virtualized network.</span></span>
<span data-ttu-id="c11b7-113">Bu mantıksal ağın adı ContosoLogicalNetwork01.</span><span class="sxs-lookup"><span data-stu-id="c11b7-113">This logical network is named ContosoLogicalNetwork01.</span></span>

<span data-ttu-id="c11b7-114">İkinci ve son komutu, daha önce alınan mantıksal ağı, bir adı (ContosoVNett01) ve açıklamayı (bir açıklama) kullanarak sanallaştırılmış bir ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c11b7-114">The second and last command creates a virtualized network using the previously retrieved logical network, a name (ContosoVNett01) and a description (A description).</span></span>

## <span data-ttu-id="c11b7-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c11b7-115">PARAMETERS</span></span>

### <span data-ttu-id="c11b7-116">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="c11b7-116">-Description</span></span>
<span data-ttu-id="c11b7-117">Sanallaştırılmış ağ için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="c11b7-117">Specifies a description for the virtualized network.</span></span>

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

### <span data-ttu-id="c11b7-118">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="c11b7-118">-LogicalNetwork</span></span>
<span data-ttu-id="c11b7-119">Sanallaştırılmış ağla ilişkili bir LogicalNetwork 'i belirtir.</span><span class="sxs-lookup"><span data-stu-id="c11b7-119">Specifies a LogicalNetwork associated with the virtualized network.</span></span>

```yaml
Type: LogicalNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c11b7-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="c11b7-120">-Name</span></span>
<span data-ttu-id="c11b7-121">Sanallaştırılmış ağ için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="c11b7-121">Specifies a name for the virtualized network.</span></span>

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

### <span data-ttu-id="c11b7-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="c11b7-122">-Profile</span></span>
<span data-ttu-id="c11b7-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c11b7-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c11b7-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="c11b7-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c11b7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c11b7-125">CommonParameters</span></span>
<span data-ttu-id="c11b7-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c11b7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c11b7-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c11b7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c11b7-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c11b7-128">INPUTS</span></span>

## <span data-ttu-id="c11b7-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c11b7-129">OUTPUTS</span></span>

## <span data-ttu-id="c11b7-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c11b7-130">NOTES</span></span>

## <span data-ttu-id="c11b7-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c11b7-131">RELATED LINKS</span></span>

[<span data-ttu-id="c11b7-132">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="c11b7-132">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="c11b7-133">Remove-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="c11b7-133">Remove-WAPackVNet</span></span>](./Remove-WAPackVNet.md)


