---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: 218921922fdd7e4d695a5daeeb30a0e2dd8d1d99
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098518"
---
# <span data-ttu-id="e08a6-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="e08a6-101">Clear-AzContext</span></span>

## <span data-ttu-id="e08a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e08a6-102">SYNOPSIS</span></span>
<span data-ttu-id="e08a6-103">Tüm Azure kimlik bilgilerini, hesap ve abonelik bilgilerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="e08a6-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="e08a6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e08a6-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e08a6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e08a6-105">DESCRIPTION</span></span>
<span data-ttu-id="e08a6-106">Tüm Azure kimlik bilgilerini, hesap ve abonelik bilgilerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="e08a6-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="e08a6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e08a6-107">EXAMPLES</span></span>

### <span data-ttu-id="e08a6-108">Global içeriği Temizle</span><span class="sxs-lookup"><span data-stu-id="e08a6-108">Clear global context</span></span>
```
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="e08a6-109">Herhangi bir PowerShell oturumunun tüm hesap, abonelik ve kimlik bilgisi bilgilerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="e08a6-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="e08a6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e08a6-110">PARAMETERS</span></span>

### <span data-ttu-id="e08a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e08a6-111">-DefaultProfile</span></span>
<span data-ttu-id="e08a6-112">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e08a6-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e08a6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e08a6-113">-Force</span></span>
<span data-ttu-id="e08a6-114">Sormadan genel kapsamdan tüm kullanıcıları ve grupları silme</span><span class="sxs-lookup"><span data-stu-id="e08a6-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="e08a6-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e08a6-115">-PassThru</span></span>
<span data-ttu-id="e08a6-116">Başarı veya başarısızlığı belirten bir değer döndürür</span><span class="sxs-lookup"><span data-stu-id="e08a6-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="e08a6-117">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="e08a6-117">-Scope</span></span>
<span data-ttu-id="e08a6-118">Yalnızca geçerli PowerShell oturumunun veya tüm oturumların bağlamını temizleyin.</span><span class="sxs-lookup"><span data-stu-id="e08a6-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e08a6-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="e08a6-119">-Confirm</span></span>
<span data-ttu-id="e08a6-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e08a6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e08a6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e08a6-121">-WhatIf</span></span>
<span data-ttu-id="e08a6-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e08a6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e08a6-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e08a6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e08a6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e08a6-124">CommonParameters</span></span>
<span data-ttu-id="e08a6-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e08a6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e08a6-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e08a6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e08a6-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e08a6-127">INPUTS</span></span>

### <span data-ttu-id="e08a6-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e08a6-128">None</span></span>

## <span data-ttu-id="e08a6-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e08a6-129">OUTPUTS</span></span>

### <span data-ttu-id="e08a6-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e08a6-130">System.Boolean</span></span>

## <span data-ttu-id="e08a6-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e08a6-131">NOTES</span></span>

## <span data-ttu-id="e08a6-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e08a6-132">RELATED LINKS</span></span>
