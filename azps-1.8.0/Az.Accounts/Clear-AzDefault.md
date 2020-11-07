---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
ms.openlocfilehash: 41d43bcb1164907bc7a06a7de4477f8a719604eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751298"
---
# <span data-ttu-id="778ae-101">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="778ae-101">Clear-AzDefault</span></span>

## <span data-ttu-id="778ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="778ae-102">SYNOPSIS</span></span>
<span data-ttu-id="778ae-103">Kullanıcı tarafından geçerli bağlamda ayarlanan Varsayılanları temizler.</span><span class="sxs-lookup"><span data-stu-id="778ae-103">Clears the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="778ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="778ae-104">SYNTAX</span></span>

```
Clear-AzDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="778ae-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="778ae-105">DESCRIPTION</span></span>
<span data-ttu-id="778ae-106">Clear-AzDefault cmdlet, Kullanıcı tarafından belirtilen geçiş parametrelerine bağlı olarak kullanıcının belirlediği Varsayılanları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="778ae-106">The Clear-AzDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="778ae-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="778ae-107">EXAMPLES</span></span>

### <span data-ttu-id="778ae-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="778ae-108">Example 1</span></span>
```
PS C:\> Clear-AzDefault
```

<span data-ttu-id="778ae-109">Bu komut, kullanıcının geçerli bağlamdaki tüm varsayılanlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="778ae-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="778ae-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="778ae-110">Example 1</span></span>
```
PS C:\> Clear-AzDefault -ResourceGroup
```

<span data-ttu-id="778ae-111">Bu komut, geçerli bağlamdaki Kullanıcı tarafından ayarlanan varsayılan kaynak grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="778ae-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="778ae-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="778ae-112">PARAMETERS</span></span>

### <span data-ttu-id="778ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="778ae-113">-DefaultProfile</span></span>
<span data-ttu-id="778ae-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="778ae-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="778ae-115">-Force</span><span class="sxs-lookup"><span data-stu-id="778ae-115">-Force</span></span>
<span data-ttu-id="778ae-116">Varsayılan belirtilmemişse tüm varsayılanları kaldır</span><span class="sxs-lookup"><span data-stu-id="778ae-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="778ae-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="778ae-117">-PassThru</span></span>
<span data-ttu-id="778ae-118">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="778ae-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="778ae-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="778ae-119">-ResourceGroup</span></span>
<span data-ttu-id="778ae-120">Varsayılan kaynak grubunu temizle</span><span class="sxs-lookup"><span data-stu-id="778ae-120">Clear Default Resource Group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="778ae-121">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="778ae-121">-Scope</span></span>
<span data-ttu-id="778ae-122">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="778ae-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="778ae-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="778ae-123">-Confirm</span></span>
<span data-ttu-id="778ae-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="778ae-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="778ae-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="778ae-125">-WhatIf</span></span>
<span data-ttu-id="778ae-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="778ae-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="778ae-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="778ae-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="778ae-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="778ae-128">CommonParameters</span></span>
<span data-ttu-id="778ae-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="778ae-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="778ae-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="778ae-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="778ae-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="778ae-131">INPUTS</span></span>

### <span data-ttu-id="778ae-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="778ae-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="778ae-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="778ae-133">OUTPUTS</span></span>

### <span data-ttu-id="778ae-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="778ae-134">System.Boolean</span></span>

## <span data-ttu-id="778ae-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="778ae-135">NOTES</span></span>

## <span data-ttu-id="778ae-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="778ae-136">RELATED LINKS</span></span>
