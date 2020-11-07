---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: b54cfdc68c1f6c400decdac9a1ef0f49823a1712
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753758"
---
# <span data-ttu-id="50933-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="50933-101">Clear-AzContext</span></span>

## <span data-ttu-id="50933-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50933-102">SYNOPSIS</span></span>
<span data-ttu-id="50933-103">Tüm Azure kimlik bilgilerini, hesap ve abonelik bilgilerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="50933-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="50933-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50933-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50933-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="50933-105">DESCRIPTION</span></span>
<span data-ttu-id="50933-106">Tüm Azure kimlik bilgilerini, hesap ve abonelik bilgilerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="50933-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="50933-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50933-107">EXAMPLES</span></span>

### <span data-ttu-id="50933-108">Global içeriği Temizle</span><span class="sxs-lookup"><span data-stu-id="50933-108">Clear global context</span></span>
```
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="50933-109">Herhangi bir PowerShell oturumunun tüm hesap, abonelik ve kimlik bilgisi bilgilerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="50933-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="50933-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50933-110">PARAMETERS</span></span>

### <span data-ttu-id="50933-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50933-111">-DefaultProfile</span></span>
<span data-ttu-id="50933-112">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="50933-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50933-113">-Force</span><span class="sxs-lookup"><span data-stu-id="50933-113">-Force</span></span>
<span data-ttu-id="50933-114">Sormadan genel kapsamdan tüm kullanıcıları ve grupları silme</span><span class="sxs-lookup"><span data-stu-id="50933-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="50933-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="50933-115">-PassThru</span></span>
<span data-ttu-id="50933-116">Başarı veya başarısızlığı belirten bir değer döndürür</span><span class="sxs-lookup"><span data-stu-id="50933-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="50933-117">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="50933-117">-Scope</span></span>
<span data-ttu-id="50933-118">Yalnızca geçerli PowerShell oturumunun veya tüm oturumların bağlamını temizleyin.</span><span class="sxs-lookup"><span data-stu-id="50933-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="50933-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="50933-119">-Confirm</span></span>
<span data-ttu-id="50933-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="50933-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50933-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50933-121">-WhatIf</span></span>
<span data-ttu-id="50933-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="50933-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50933-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="50933-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50933-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50933-124">CommonParameters</span></span>
<span data-ttu-id="50933-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="50933-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50933-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50933-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50933-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50933-127">INPUTS</span></span>

### <span data-ttu-id="50933-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="50933-128">None</span></span>

## <span data-ttu-id="50933-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50933-129">OUTPUTS</span></span>

### <span data-ttu-id="50933-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50933-130">System.Boolean</span></span>

## <span data-ttu-id="50933-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50933-131">NOTES</span></span>

## <span data-ttu-id="50933-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50933-132">RELATED LINKS</span></span>
