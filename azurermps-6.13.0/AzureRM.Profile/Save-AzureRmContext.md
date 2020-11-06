---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/save-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
ms.openlocfilehash: 451498760d85cc018b8fbade625625ec6ecc1910
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588410"
---
# <span data-ttu-id="d226f-101">Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="d226f-101">Save-AzureRmContext</span></span>

## <span data-ttu-id="d226f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d226f-102">SYNOPSIS</span></span>
<span data-ttu-id="d226f-103">Geçerli kimlik doğrulama bilgilerini diğer PowerShell oturumlarında kullanılmak üzere kaydeder.</span><span class="sxs-lookup"><span data-stu-id="d226f-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d226f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d226f-104">SYNTAX</span></span>

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d226f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d226f-105">DESCRIPTION</span></span>
<span data-ttu-id="d226f-106">Save-AzureRmContext cmdlet 'i diğer PowerShell oturumlarında kullanılacak geçerli kimlik doğrulama bilgilerini kaydeder.</span><span class="sxs-lookup"><span data-stu-id="d226f-106">The Save-AzureRmContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="d226f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d226f-107">EXAMPLES</span></span>

### <span data-ttu-id="d226f-108">Örnek 1: geçerli oturumun içeriği kaydediliyor</span><span class="sxs-lookup"><span data-stu-id="d226f-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

<span data-ttu-id="d226f-109">Bu örnek, geçerli oturumun Azure bağlamını sağlanan JSON dosyasına kaydeder.</span><span class="sxs-lookup"><span data-stu-id="d226f-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="d226f-110">Örnek 2: verilen bağlamı kaydetme</span><span class="sxs-lookup"><span data-stu-id="d226f-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzureRmContext -Profile (Connect-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="d226f-111">Bu örnek, sağlanan JSON dosyasına cmdlet 'e geçirilen Azure bağlamını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="d226f-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="d226f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d226f-112">PARAMETERS</span></span>

### <span data-ttu-id="d226f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d226f-113">-DefaultProfile</span></span>
<span data-ttu-id="d226f-114">Azure ile iletişim için kullanılan kimlik bilgileri, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d226f-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d226f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d226f-115">-Force</span></span>
<span data-ttu-id="d226f-116">Varsa, verilen dosyanın üzerine yaz</span><span class="sxs-lookup"><span data-stu-id="d226f-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="d226f-117">-Yol</span><span class="sxs-lookup"><span data-stu-id="d226f-117">-Path</span></span>
<span data-ttu-id="d226f-118">Kimlik doğrulama bilgilerinin kaydedileceği dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d226f-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="d226f-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="d226f-119">-Profile</span></span>
<span data-ttu-id="d226f-120">Bu cmdlet 'in okuduğu Azure bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d226f-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="d226f-121">Bağlam belirtmezseniz, bu cmdlet yerel varsayılan içerikten okur.</span><span class="sxs-lookup"><span data-stu-id="d226f-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="d226f-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="d226f-122">-Confirm</span></span>
<span data-ttu-id="d226f-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d226f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d226f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d226f-124">-WhatIf</span></span>
<span data-ttu-id="d226f-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d226f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d226f-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d226f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d226f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d226f-127">CommonParameters</span></span>
<span data-ttu-id="d226f-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d226f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d226f-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d226f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d226f-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d226f-130">INPUTS</span></span>

### <span data-ttu-id="d226f-131">Microsoft. Azure. Commands. Common. Authentication. modeller. AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="d226f-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>
<span data-ttu-id="d226f-132">Parametreler: profil (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d226f-132">Parameters: Profile (ByValue)</span></span>

## <span data-ttu-id="d226f-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d226f-133">OUTPUTS</span></span>

### <span data-ttu-id="d226f-134">Microsoft. Azure. Commands. Profile. modeller. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="d226f-134">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="d226f-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d226f-135">NOTES</span></span>

## <span data-ttu-id="d226f-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d226f-136">RELATED LINKS</span></span>
