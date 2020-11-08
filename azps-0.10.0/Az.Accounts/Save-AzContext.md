---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: 07e565031a5c29ae1be78246cad95326952007e6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935237"
---
# <span data-ttu-id="f69b3-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="f69b3-101">Save-AzContext</span></span>

## <span data-ttu-id="f69b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f69b3-102">SYNOPSIS</span></span>
<span data-ttu-id="f69b3-103">Geçerli kimlik doğrulama bilgilerini diğer PowerShell oturumlarında kullanılmak üzere kaydeder.</span><span class="sxs-lookup"><span data-stu-id="f69b3-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="f69b3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f69b3-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f69b3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f69b3-105">DESCRIPTION</span></span>
<span data-ttu-id="f69b3-106">Save-AzContext cmdlet 'i diğer PowerShell oturumlarında kullanılacak geçerli kimlik doğrulama bilgilerini kaydeder.</span><span class="sxs-lookup"><span data-stu-id="f69b3-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="f69b3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f69b3-107">EXAMPLES</span></span>

### <span data-ttu-id="f69b3-108">Örnek 1: geçerli oturumun içeriği kaydediliyor</span><span class="sxs-lookup"><span data-stu-id="f69b3-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="f69b3-109">Bu örnek, geçerli oturumun Azure bağlamını sağlanan JSON dosyasına kaydeder.</span><span class="sxs-lookup"><span data-stu-id="f69b3-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="f69b3-110">Örnek 2: verilen bağlamı kaydetme</span><span class="sxs-lookup"><span data-stu-id="f69b3-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="f69b3-111">Bu örnek, sağlanan JSON dosyasına cmdlet 'e geçirilen Azure bağlamını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="f69b3-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="f69b3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f69b3-112">PARAMETERS</span></span>

### <span data-ttu-id="f69b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f69b3-113">-DefaultProfile</span></span>
<span data-ttu-id="f69b3-114">Azure ile iletişim için kullanılan kimlik bilgileri, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f69b3-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f69b3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f69b3-115">-Force</span></span>
<span data-ttu-id="f69b3-116">Varsa, verilen dosyanın üzerine yaz</span><span class="sxs-lookup"><span data-stu-id="f69b3-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="f69b3-117">-Yol</span><span class="sxs-lookup"><span data-stu-id="f69b3-117">-Path</span></span>
<span data-ttu-id="f69b3-118">Kimlik doğrulama bilgilerinin kaydedileceği dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f69b3-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="f69b3-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="f69b3-119">-Profile</span></span>
<span data-ttu-id="f69b3-120">Bu cmdlet 'in okuduğu Azure bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f69b3-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="f69b3-121">Bağlam belirtmezseniz, bu cmdlet yerel varsayılan içerikten okur.</span><span class="sxs-lookup"><span data-stu-id="f69b3-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="f69b3-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="f69b3-122">-Confirm</span></span>
<span data-ttu-id="f69b3-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f69b3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f69b3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f69b3-124">-WhatIf</span></span>
<span data-ttu-id="f69b3-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f69b3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f69b3-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f69b3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f69b3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f69b3-127">CommonParameters</span></span>
<span data-ttu-id="f69b3-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f69b3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f69b3-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f69b3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f69b3-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f69b3-130">INPUTS</span></span>

### <span data-ttu-id="f69b3-131">Microsoft. Azure. Commands. Common. Authentication. modeller. AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="f69b3-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="f69b3-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f69b3-132">OUTPUTS</span></span>

### <span data-ttu-id="f69b3-133">Microsoft. Azure. Commands. Profile. modeller. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="f69b3-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="f69b3-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f69b3-134">NOTES</span></span>

## <span data-ttu-id="f69b3-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f69b3-135">RELATED LINKS</span></span>