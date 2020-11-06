---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06a78584437021df570bc5ff2b6ec19e332bffd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571901"
---
# <span data-ttu-id="fab0b-101">Save-AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="fab0b-101">Save-AzureRmProfile</span></span>

## <span data-ttu-id="fab0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fab0b-102">SYNOPSIS</span></span>
<span data-ttu-id="fab0b-103">Geçerli kimlik doğrulama bilgilerini diğer PowerShell oturumlarında kullanılmak üzere kaydeder.</span><span class="sxs-lookup"><span data-stu-id="fab0b-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="fab0b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fab0b-104">SYNTAX</span></span>

```
Save-AzureRmProfile [[-Profile] <AzureRMProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fab0b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fab0b-105">DESCRIPTION</span></span>
<span data-ttu-id="fab0b-106">Save-AzureRmProfile cmdlet 'i diğer PowerShell oturumlarında kullanılacak geçerli kimlik doğrulama bilgilerini kaydeder.</span><span class="sxs-lookup"><span data-stu-id="fab0b-106">The Save-AzureRmProfile cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="fab0b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fab0b-107">EXAMPLES</span></span>

### <span data-ttu-id="fab0b-108">Örnek 1: geçerli oturumun profilini kaydetme</span><span class="sxs-lookup"><span data-stu-id="fab0b-108">Example 1: Saving the current session's profile</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmProfile -Path C:\test.json
```

<span data-ttu-id="fab0b-109">Bu örnek, geçerli oturumun Azure profilini sağlanan JSON dosyasına kaydeder.</span><span class="sxs-lookup"><span data-stu-id="fab0b-109">This example saves the current session's Azure profile to the JSON file provided.</span></span>

### <span data-ttu-id="fab0b-110">Örnek 2: belirli bir profili kaydetme</span><span class="sxs-lookup"><span data-stu-id="fab0b-110">Example 2: Saving a given profile</span></span>
```
PS C:\> Save-AzureRmProfile -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="fab0b-111">Bu örnekte, sağlanan JSON dosyasına cmdlet 'e geçirilen Azure profili kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="fab0b-111">This example saves the Azure profile that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="fab0b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fab0b-112">PARAMETERS</span></span>

### <span data-ttu-id="fab0b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="fab0b-113">-Force</span></span>
<span data-ttu-id="fab0b-114">Varsa, verilen dosyanın üzerine yaz</span><span class="sxs-lookup"><span data-stu-id="fab0b-114">Overwrite the given file if it exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab0b-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="fab0b-115">-Path</span></span>
<span data-ttu-id="fab0b-116">Kimlik doğrulama bilgilerinin kaydedileceği dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="fab0b-116">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab0b-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="fab0b-117">-Profile</span></span>
<span data-ttu-id="fab0b-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fab0b-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fab0b-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="fab0b-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureRMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fab0b-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="fab0b-120">-Confirm</span></span>
<span data-ttu-id="fab0b-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fab0b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fab0b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fab0b-122">-WhatIf</span></span>
<span data-ttu-id="fab0b-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fab0b-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fab0b-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fab0b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fab0b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fab0b-125">CommonParameters</span></span>
<span data-ttu-id="fab0b-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fab0b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fab0b-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fab0b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fab0b-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fab0b-128">INPUTS</span></span>

## <span data-ttu-id="fab0b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fab0b-129">OUTPUTS</span></span>

### <span data-ttu-id="fab0b-130">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="fab0b-130">PSAzureProfile</span></span>

## <span data-ttu-id="fab0b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fab0b-131">NOTES</span></span>

## <span data-ttu-id="fab0b-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fab0b-132">RELATED LINKS</span></span>

[<span data-ttu-id="fab0b-133">Select-AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="fab0b-133">Select-AzureRMProfile</span></span>]()

