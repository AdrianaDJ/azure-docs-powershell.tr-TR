---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
ms.openlocfilehash: 5c6200f6d68760cbd93460b38cb72a379845e622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763346"
---
# <span data-ttu-id="e30ef-101">Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="e30ef-101">Save-AzureRmContext</span></span>

## <span data-ttu-id="e30ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e30ef-102">SYNOPSIS</span></span>
<span data-ttu-id="e30ef-103">Geçerli kimlik doğrulama bilgilerini diğer PowerShell oturumlarında kullanılmak üzere kaydeder.</span><span class="sxs-lookup"><span data-stu-id="e30ef-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e30ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e30ef-104">SYNTAX</span></span>

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e30ef-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e30ef-105">DESCRIPTION</span></span>
<span data-ttu-id="e30ef-106">Save-AzureRmContext cmdlet 'i diğer PowerShell oturumlarında kullanılacak geçerli kimlik doğrulama bilgilerini kaydeder.</span><span class="sxs-lookup"><span data-stu-id="e30ef-106">The Save-AzureRmContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="e30ef-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e30ef-107">EXAMPLES</span></span>

### <span data-ttu-id="e30ef-108">Örnek 1: geçerli oturumun içeriği kaydediliyor</span><span class="sxs-lookup"><span data-stu-id="e30ef-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

<span data-ttu-id="e30ef-109">Bu örnek, geçerli oturumun Azure bağlamını sağlanan JSON dosyasına kaydeder.</span><span class="sxs-lookup"><span data-stu-id="e30ef-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="e30ef-110">Örnek 2: verilen bağlamı kaydetme</span><span class="sxs-lookup"><span data-stu-id="e30ef-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzureRmContext -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="e30ef-111">Bu örnek, sağlanan JSON dosyasına cmdlet 'e geçirilen Azure bağlamını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="e30ef-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="e30ef-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e30ef-112">PARAMETERS</span></span>

### <span data-ttu-id="e30ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e30ef-113">-DefaultProfile</span></span>
<span data-ttu-id="e30ef-114">Azure ile iletişim için kullanılan kimlik bilgileri, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e30ef-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30ef-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e30ef-115">-Force</span></span>
<span data-ttu-id="e30ef-116">Varsa, verilen dosyanın üzerine yaz</span><span class="sxs-lookup"><span data-stu-id="e30ef-116">Overwrite the given file if it exists</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30ef-117">-Yol</span><span class="sxs-lookup"><span data-stu-id="e30ef-117">-Path</span></span>
<span data-ttu-id="e30ef-118">Kimlik doğrulama bilgilerinin kaydedileceği dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e30ef-118">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30ef-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="e30ef-119">-Profile</span></span>
<span data-ttu-id="e30ef-120">Bu cmdlet 'in okuduğu Azure bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e30ef-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="e30ef-121">Bağlam belirtmezseniz, bu cmdlet yerel varsayılan içerikten okur.</span><span class="sxs-lookup"><span data-stu-id="e30ef-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e30ef-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="e30ef-122">-Confirm</span></span>
<span data-ttu-id="e30ef-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e30ef-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30ef-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e30ef-124">-WhatIf</span></span>
<span data-ttu-id="e30ef-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e30ef-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e30ef-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e30ef-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30ef-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e30ef-127">CommonParameters</span></span>
<span data-ttu-id="e30ef-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e30ef-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e30ef-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e30ef-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e30ef-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e30ef-130">INPUTS</span></span>

### <span data-ttu-id="e30ef-131">Microsoft. Azure. Commands. Common. Authentication. modeller. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="e30ef-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>

## <span data-ttu-id="e30ef-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e30ef-132">OUTPUTS</span></span>

### <span data-ttu-id="e30ef-133">Microsoft. Azure. Commands. Profile. modeller. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="e30ef-133">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="e30ef-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e30ef-134">NOTES</span></span>

## <span data-ttu-id="e30ef-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e30ef-135">RELATED LINKS</span></span>

