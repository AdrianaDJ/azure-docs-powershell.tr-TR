---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4BAD0DDE-80D4-4A89-AFFB-78C933D2C0D5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76771d8c0e8d06cbe134e920a06be5fc1b109fe2
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107353"
---
# <span data-ttu-id="5a2de-101">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="5a2de-101">Get-WAPackCloudService</span></span>

## <span data-ttu-id="5a2de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a2de-102">SYNOPSIS</span></span>
<span data-ttu-id="5a2de-103">Bulut hizmet nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="5a2de-103">Gets cloud service objects.</span></span>

## <span data-ttu-id="5a2de-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a2de-104">SYNTAX</span></span>

### <span data-ttu-id="5a2de-105">Boş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5a2de-105">Empty (Default)</span></span>
```
Get-WAPackCloudService [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5a2de-106">FromName</span><span class="sxs-lookup"><span data-stu-id="5a2de-106">FromName</span></span>
```
Get-WAPackCloudService [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5a2de-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a2de-107">DESCRIPTION</span></span>
<span data-ttu-id="5a2de-108">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="5a2de-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="5a2de-109">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="5a2de-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="5a2de-110">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="5a2de-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="5a2de-111">**Get-WAPackCloudService** cmdlet 'i bulut hizmet nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="5a2de-111">The **Get-WAPackCloudService** cmdlet gets cloud service objects.</span></span>

## <span data-ttu-id="5a2de-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a2de-112">EXAMPLES</span></span>

## <span data-ttu-id="5a2de-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a2de-113">PARAMETERS</span></span>

### <span data-ttu-id="5a2de-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="5a2de-114">-Name</span></span>
<span data-ttu-id="5a2de-115">Bulut hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a2de-115">Specifies the name of a cloud service.</span></span>

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

### <span data-ttu-id="5a2de-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="5a2de-116">-Profile</span></span>
<span data-ttu-id="5a2de-117">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a2de-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5a2de-118">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="5a2de-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5a2de-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a2de-119">CommonParameters</span></span>
<span data-ttu-id="5a2de-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a2de-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a2de-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a2de-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a2de-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a2de-122">INPUTS</span></span>

## <span data-ttu-id="5a2de-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a2de-123">OUTPUTS</span></span>

## <span data-ttu-id="5a2de-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a2de-124">NOTES</span></span>

## <span data-ttu-id="5a2de-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a2de-125">RELATED LINKS</span></span>

[<span data-ttu-id="5a2de-126">Yeni-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="5a2de-126">New-WAPackCloudService</span></span>](./New-WAPackCloudService.md)

[<span data-ttu-id="5a2de-127">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="5a2de-127">Remove-WAPackCloudService</span></span>](./Remove-WAPackCloudService.md)


