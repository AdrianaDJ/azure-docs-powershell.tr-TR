---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: f3afbd9b96de51f754dd87dfa42ed6f71e5b3577
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93571033"
---
# <span data-ttu-id="6f9d7-101">Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="6f9d7-101">Save-AzureRmContext</span></span>

## <span data-ttu-id="6f9d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f9d7-102">SYNOPSIS</span></span>
<span data-ttu-id="6f9d7-103">Geçerli kimlik doğrulama bilgilerini diğer PowerShell oturumlarında kullanılmak üzere kaydeder.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="6f9d7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f9d7-104">SYNTAX</span></span>

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="6f9d7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f9d7-105">DESCRIPTION</span></span>
<span data-ttu-id="6f9d7-106">Save-AzureRmContext cmdlet 'i diğer PowerShell oturumlarında kullanılacak geçerli kimlik doğrulama bilgilerini kaydeder.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-106">The Save-AzureRmContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="6f9d7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f9d7-107">EXAMPLES</span></span>

### <span data-ttu-id="6f9d7-108">Örnek 1: geçerli oturumun içeriği kaydediliyor</span><span class="sxs-lookup"><span data-stu-id="6f9d7-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

<span data-ttu-id="6f9d7-109">Bu örnek, geçerli oturumun Azure bağlamını sağlanan JSON dosyasına kaydeder.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="6f9d7-110">Örnek 2: verilen bağlamı kaydetme</span><span class="sxs-lookup"><span data-stu-id="6f9d7-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzureRmContext -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="6f9d7-111">Bu örnek, sağlanan JSON dosyasına cmdlet 'e geçirilen Azure bağlamını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="6f9d7-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f9d7-112">PARAMETERS</span></span>

### <span data-ttu-id="6f9d7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6f9d7-113">-Force</span></span>
<span data-ttu-id="6f9d7-114">Varsa, verilen dosyanın üzerine yaz</span><span class="sxs-lookup"><span data-stu-id="6f9d7-114">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="6f9d7-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="6f9d7-115">-Path</span></span>
<span data-ttu-id="6f9d7-116">Kimlik doğrulama bilgilerinin kaydedileceği dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-116">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9d7-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="6f9d7-117">-Profile</span></span>
<span data-ttu-id="6f9d7-118">Bu cmdlet 'in okuduğu Azure bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-118">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="6f9d7-119">Bağlam belirtmezseniz, bu cmdlet yerel varsayılan içerikten okur.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: AzureRmProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f9d7-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="6f9d7-120">-Confirm</span></span>
<span data-ttu-id="6f9d7-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f9d7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f9d7-122">-WhatIf</span></span>
<span data-ttu-id="6f9d7-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f9d7-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-124">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="6f9d7-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f9d7-125">INPUTS</span></span>

### <span data-ttu-id="6f9d7-126">Microsoft. Azure. Commands. Common. Authentication. modeller. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="6f9d7-126">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>

## <span data-ttu-id="6f9d7-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f9d7-127">OUTPUTS</span></span>

### <span data-ttu-id="6f9d7-128">Microsoft. Azure. Commands. Profile. modeller. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="6f9d7-128">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="6f9d7-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f9d7-129">NOTES</span></span>

## <span data-ttu-id="6f9d7-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f9d7-130">RELATED LINKS</span></span>

