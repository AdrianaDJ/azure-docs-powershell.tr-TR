---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9445B7FA-FC72-4F71-BD44-8AA55BE9BA0E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d2a3dbabb5bbe78ed571806aa69b9d79d4782b3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105460"
---
# <span data-ttu-id="ff673-101">Save-AzureServiceProjectPackage</span><span class="sxs-lookup"><span data-stu-id="ff673-101">Save-AzureServiceProjectPackage</span></span>

## <span data-ttu-id="ff673-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff673-102">SYNOPSIS</span></span>
<span data-ttu-id="ff673-103">Hizmet projesini Azure bulut paketine paketler.</span><span class="sxs-lookup"><span data-stu-id="ff673-103">Packages the service project into Azure cloud package.</span></span>

## <span data-ttu-id="ff673-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ff673-104">SYNTAX</span></span>

```
Save-AzureServiceProjectPackage [-Local] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ff673-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ff673-105">DESCRIPTION</span></span>
<span data-ttu-id="ff673-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ff673-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ff673-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ff673-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ff673-108">**Save-AzureServiceProjectPackage** cmdlet 'i, hizmet projesini bir Azure bulut paketine (\*. cspkg) paketler.</span><span class="sxs-lookup"><span data-stu-id="ff673-108">The **Save-AzureServiceProjectPackage** cmdlet packages the service project into an Azure cloud package (\*.cspkg).</span></span>

## <span data-ttu-id="ff673-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ff673-109">EXAMPLES</span></span>

### <span data-ttu-id="ff673-110">Örnek 1: hizmet projesi paketi oluşturma</span><span class="sxs-lookup"><span data-stu-id="ff673-110">Example 1: Create a service project package</span></span>
```
PS C:\> Save-AzureServiceProjectPackage
```

<span data-ttu-id="ff673-111">Bu örnek MyAzureServiceProject adındaki bir hizmet projesi için \*. cspgk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ff673-111">This example creates a \*.cspgk for a service project named MyAzureServiceProject.</span></span>

## <span data-ttu-id="ff673-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ff673-112">PARAMETERS</span></span>

### <span data-ttu-id="ff673-113">-Yerel</span><span class="sxs-lookup"><span data-stu-id="ff673-113">-Local</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff673-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="ff673-114">-Profile</span></span>
<span data-ttu-id="ff673-115">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff673-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ff673-116">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="ff673-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ff673-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff673-117">CommonParameters</span></span>
<span data-ttu-id="ff673-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ff673-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff673-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff673-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff673-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ff673-120">INPUTS</span></span>

## <span data-ttu-id="ff673-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ff673-121">OUTPUTS</span></span>

## <span data-ttu-id="ff673-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ff673-122">NOTES</span></span>

## <span data-ttu-id="ff673-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ff673-123">RELATED LINKS</span></span>

[<span data-ttu-id="ff673-124">Yayımla-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="ff673-124">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)


