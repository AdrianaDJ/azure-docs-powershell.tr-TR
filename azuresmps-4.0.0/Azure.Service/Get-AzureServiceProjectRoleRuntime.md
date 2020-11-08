---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CEFFEF9F-4500-447E-99F1-FE053AED880A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e5b65a88e41ce08ec1d60bc140828963950f447
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105598"
---
# <span data-ttu-id="02230-101">Get-AzureServiceProjectRoleRuntime</span><span class="sxs-lookup"><span data-stu-id="02230-101">Get-AzureServiceProjectRoleRuntime</span></span>

## <span data-ttu-id="02230-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02230-102">SYNOPSIS</span></span>
<span data-ttu-id="02230-103">Role yüklenecek çalışma zamanlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="02230-103">Get the runtimes available to install in a role.</span></span>

## <span data-ttu-id="02230-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02230-104">SYNTAX</span></span>

```
Get-AzureServiceProjectRoleRuntime [-Runtime <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="02230-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="02230-105">DESCRIPTION</span></span>
<span data-ttu-id="02230-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="02230-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="02230-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="02230-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="02230-108">Bir role yüklenecek olan çalışma zamanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="02230-108">Gets the runtimes available to install in a role.</span></span>

## <span data-ttu-id="02230-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02230-109">EXAMPLES</span></span>

## <span data-ttu-id="02230-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02230-110">PARAMETERS</span></span>

### <span data-ttu-id="02230-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="02230-111">-Profile</span></span>
<span data-ttu-id="02230-112">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="02230-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="02230-113">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="02230-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="02230-114">-Runtime</span><span class="sxs-lookup"><span data-stu-id="02230-114">-Runtime</span></span>
<span data-ttu-id="02230-115">Çalışma zamanının adı.</span><span class="sxs-lookup"><span data-stu-id="02230-115">The name of the runtime.</span></span>
<span data-ttu-id="02230-116">Çalışma zamanı belirtilmişse, bu çalışma zamanının yalnızca Windows Azure 'da rolünüze yüklenebilecek belirli sürümleri döndürülür.</span><span class="sxs-lookup"><span data-stu-id="02230-116">If a runtime specified, only the specific versions of that runtime available to install in your role in Windows Azure will be returned.</span></span>

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

### <span data-ttu-id="02230-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02230-117">CommonParameters</span></span>
<span data-ttu-id="02230-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02230-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02230-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02230-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02230-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02230-120">INPUTS</span></span>

## <span data-ttu-id="02230-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02230-121">OUTPUTS</span></span>

## <span data-ttu-id="02230-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02230-122">NOTES</span></span>

## <span data-ttu-id="02230-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02230-123">RELATED LINKS</span></span>

[<span data-ttu-id="02230-124">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="02230-124">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="02230-125">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="02230-125">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="02230-126">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="02230-126">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)

[<span data-ttu-id="02230-127">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="02230-127">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


