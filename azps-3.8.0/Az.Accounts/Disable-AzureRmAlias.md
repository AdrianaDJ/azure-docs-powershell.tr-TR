---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
ms.openlocfilehash: 749507ba0bc0eec8aac7600c5262533ceb02a46b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098511"
---
# <span data-ttu-id="4f81f-101">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="4f81f-101">Disable-AzureRmAlias</span></span>

## <span data-ttu-id="4f81f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f81f-102">SYNOPSIS</span></span>
<span data-ttu-id="4f81f-103">Az modüllerle AzureRm önek diğer adlarını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="4f81f-103">Disables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="4f81f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f81f-104">SYNTAX</span></span>

```
Disable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f81f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f81f-105">DESCRIPTION</span></span>
<span data-ttu-id="4f81f-106">Az modüllerle AzureRm önek diğer adlarını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="4f81f-106">Disables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="4f81f-107">-Module belirtilirse, yalnızca listelenen modüllerin diğer adları devre dışı olur.</span><span class="sxs-lookup"><span data-stu-id="4f81f-107">If -Module is specified, only modules listed will have aliases disabled.</span></span> <span data-ttu-id="4f81f-108">Aksi takdirde tüm AzureRm diğer adları devre dışıdır.</span><span class="sxs-lookup"><span data-stu-id="4f81f-108">Otherwise all AzureRm aliases are disabled.</span></span>

## <span data-ttu-id="4f81f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f81f-109">EXAMPLES</span></span>

### <span data-ttu-id="4f81f-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4f81f-110">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias
```

<span data-ttu-id="4f81f-111">Geçerli PowerShell oturumunun tüm AzureRm öneklerini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="4f81f-111">Disables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="4f81f-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4f81f-112">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="4f81f-113">Hem geçerli süreç hem de geçerli kullanıcı için en az. hesaplı diğer adları devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="4f81f-113">Disables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="4f81f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f81f-114">PARAMETERS</span></span>

### <span data-ttu-id="4f81f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f81f-115">-DefaultProfile</span></span>
<span data-ttu-id="4f81f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4f81f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f81f-117">-Modül</span><span class="sxs-lookup"><span data-stu-id="4f81f-117">-Module</span></span>
<span data-ttu-id="4f81f-118">Hangi modüllerin diğer adlarını devre dışı bırakagösterir.</span><span class="sxs-lookup"><span data-stu-id="4f81f-118">Indicates which modules to disable aliases for.</span></span>
<span data-ttu-id="4f81f-119">Hiçbiri belirtilmemişse, varsayılan olarak tüm etkinleştirilmiş modüller kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4f81f-119">If none are specified, default is all enabled modules.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f81f-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4f81f-120">-PassThru</span></span>
<span data-ttu-id="4f81f-121">Belirtilmişse cmdlet tüm devre dışı diğer adları döndürür</span><span class="sxs-lookup"><span data-stu-id="4f81f-121">If specified, cmdlet will return all disabled aliases</span></span>

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

### <span data-ttu-id="4f81f-122">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="4f81f-122">-Scope</span></span>
<span data-ttu-id="4f81f-123">Hangi kapsam diğer adlarının devre dışı bırakılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f81f-123">Indicates what scope aliases should be disabled for.</span></span> <span data-ttu-id="4f81f-124">Varsayılan ' Process '</span><span class="sxs-lookup"><span data-stu-id="4f81f-124">Default is 'Process'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser, LocalMachine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f81f-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="4f81f-125">-Confirm</span></span>
<span data-ttu-id="4f81f-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4f81f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f81f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f81f-127">-WhatIf</span></span>
<span data-ttu-id="4f81f-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f81f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f81f-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4f81f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f81f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f81f-130">CommonParameters</span></span>
<span data-ttu-id="4f81f-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f81f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f81f-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f81f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f81f-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f81f-133">INPUTS</span></span>

### <span data-ttu-id="4f81f-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4f81f-134">None</span></span>

## <span data-ttu-id="4f81f-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f81f-135">OUTPUTS</span></span>

### <span data-ttu-id="4f81f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4f81f-136">System.String</span></span>

## <span data-ttu-id="4f81f-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f81f-137">NOTES</span></span>

## <span data-ttu-id="4f81f-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f81f-138">RELATED LINKS</span></span>
