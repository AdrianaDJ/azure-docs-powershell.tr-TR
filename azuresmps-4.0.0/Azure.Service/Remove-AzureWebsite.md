---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8062D57E-8381-4715-9AA8-551F15DCC492
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2627bdb2f098d5b09851ec5970dd2a73840d24e6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105483"
---
# <span data-ttu-id="46213-101">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="46213-101">Remove-AzureWebsite</span></span>

## <span data-ttu-id="46213-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46213-102">SYNOPSIS</span></span>
<span data-ttu-id="46213-103">Belirtilen Web sitesini Azure 'dan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="46213-103">Removes the specified website from Azure.</span></span>

## <span data-ttu-id="46213-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46213-104">SYNTAX</span></span>

```
Remove-AzureWebsite [-Force] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46213-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="46213-105">DESCRIPTION</span></span>
<span data-ttu-id="46213-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="46213-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="46213-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="46213-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="46213-108">**Remove-AzureWebsite** cmdlet 'i, belirtilen Web sitesini onay istemiyle birlikte veya sormadan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="46213-108">The **Remove-AzureWebsite** cmdlet removes the specified website from Azure, either with or without a prompt for confirmation.</span></span>

## <span data-ttu-id="46213-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46213-109">EXAMPLES</span></span>

### <span data-ttu-id="46213-110">Örnek 1: geçerli Web sitesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="46213-110">Example 1: Remove the current website</span></span>
```
PS C:\> Remove-AzureWebsite
```

<span data-ttu-id="46213-111">Bu örnekte, Azure 'da geçerli dizinle ilişkilendirilmiş Web sitesi kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="46213-111">This example removes the website in Azure associated with the current directory.</span></span>

### <span data-ttu-id="46213-112">Örnek 2: onaysız Web sitesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="46213-112">Example 2: Remove a website without confirmation</span></span>
```
PS C:\> Remove-AzureWebsite -Name mySite -Force
```

<span data-ttu-id="46213-113">Bu örnekte, onay istemeden Sitem adlı Web sitesi silinir.</span><span class="sxs-lookup"><span data-stu-id="46213-113">This example deletes the website named mySite without prompting for confirmation.</span></span>

## <span data-ttu-id="46213-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46213-114">PARAMETERS</span></span>

### <span data-ttu-id="46213-115">-Force</span><span class="sxs-lookup"><span data-stu-id="46213-115">-Force</span></span>
<span data-ttu-id="46213-116">Belirtilmişse, onay istemeden belirtilen Web sitesini siler.</span><span class="sxs-lookup"><span data-stu-id="46213-116">If specified, deletes the specified website without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46213-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="46213-117">-Name</span></span>
<span data-ttu-id="46213-118">Silinecek Web sitesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46213-118">Specifies the name of the website to delete.</span></span>

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

### <span data-ttu-id="46213-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="46213-119">-Profile</span></span>
<span data-ttu-id="46213-120">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46213-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="46213-121">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="46213-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="46213-122">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="46213-122">-Slot</span></span>
<span data-ttu-id="46213-123">Web sitesinin yuva adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46213-123">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="46213-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="46213-124">-Confirm</span></span>
<span data-ttu-id="46213-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="46213-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46213-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46213-126">-WhatIf</span></span>
<span data-ttu-id="46213-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46213-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46213-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="46213-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46213-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46213-129">CommonParameters</span></span>
<span data-ttu-id="46213-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46213-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46213-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46213-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46213-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46213-132">INPUTS</span></span>

## <span data-ttu-id="46213-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46213-133">OUTPUTS</span></span>

## <span data-ttu-id="46213-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46213-134">NOTES</span></span>

## <span data-ttu-id="46213-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46213-135">RELATED LINKS</span></span>

[<span data-ttu-id="46213-136">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="46213-136">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)


