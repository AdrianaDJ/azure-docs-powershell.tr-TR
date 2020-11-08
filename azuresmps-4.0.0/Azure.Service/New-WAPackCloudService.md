---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA2E37AB-F137-4A62-9ABC-90565305A23B
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6d1bbac3db6f69f5cdda14870de20eee7f8170b
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107357"
---
# <span data-ttu-id="0d03f-101">New-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="0d03f-101">New-WAPackCloudService</span></span>

## <span data-ttu-id="0d03f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d03f-102">SYNOPSIS</span></span>
<span data-ttu-id="0d03f-103">Bulut hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0d03f-103">Creates a cloud service.</span></span>

## <span data-ttu-id="0d03f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d03f-104">SYNTAX</span></span>

```
New-WAPackCloudService -Name <String> -Label <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0d03f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d03f-105">DESCRIPTION</span></span>
<span data-ttu-id="0d03f-106">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="0d03f-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="0d03f-107">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="0d03f-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0d03f-108">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0d03f-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0d03f-109">**Yeni-WAPackCloudService** cmdlet 'i bir bulut hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0d03f-109">The **New-WAPackCloudService** cmdlet creates a cloud service.</span></span>

## <span data-ttu-id="0d03f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d03f-110">EXAMPLES</span></span>

### <span data-ttu-id="0d03f-111">Örnek 1: bulut hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="0d03f-111">Example 1: Create a cloud service</span></span>
```
PS C:\> New-WAPackCloudService -Name "ContosoCloudService01" -Label "A label"
```

<span data-ttu-id="0d03f-112">Bu komut, etiketle ContosoCloudService01 adlı bir bulut hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0d03f-112">The command creates a cloud service named ContosoCloudService01 with a label.</span></span>

## <span data-ttu-id="0d03f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d03f-113">PARAMETERS</span></span>

### <span data-ttu-id="0d03f-114">Etiketli</span><span class="sxs-lookup"><span data-stu-id="0d03f-114">-Label</span></span>
<span data-ttu-id="0d03f-115">Bulut hizmeti için bir etiket belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d03f-115">Specifies a label for the cloud service.</span></span>

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

### <span data-ttu-id="0d03f-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="0d03f-116">-Name</span></span>
<span data-ttu-id="0d03f-117">CloudService için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d03f-117">Specifies a name for the cloudservice.</span></span>

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

### <span data-ttu-id="0d03f-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="0d03f-118">-Profile</span></span>
<span data-ttu-id="0d03f-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d03f-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0d03f-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="0d03f-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0d03f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d03f-121">CommonParameters</span></span>
<span data-ttu-id="0d03f-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d03f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d03f-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d03f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d03f-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d03f-124">INPUTS</span></span>

## <span data-ttu-id="0d03f-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d03f-125">OUTPUTS</span></span>

## <span data-ttu-id="0d03f-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d03f-126">NOTES</span></span>

## <span data-ttu-id="0d03f-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d03f-127">RELATED LINKS</span></span>

[<span data-ttu-id="0d03f-128">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="0d03f-128">Get-WAPackCloudService</span></span>](./Get-WAPackCloudService.md)

[<span data-ttu-id="0d03f-129">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="0d03f-129">Remove-WAPackCloudService</span></span>](./Remove-WAPackCloudService.md)


