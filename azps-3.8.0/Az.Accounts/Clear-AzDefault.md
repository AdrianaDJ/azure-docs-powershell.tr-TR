---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
ms.openlocfilehash: aae604f28b2a7eebae62d290b3c1ab6905d9a15a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098517"
---
# <span data-ttu-id="a7821-101">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="a7821-101">Clear-AzDefault</span></span>

## <span data-ttu-id="a7821-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7821-102">SYNOPSIS</span></span>
<span data-ttu-id="a7821-103">Kullanıcı tarafından geçerli bağlamda ayarlanan Varsayılanları temizler.</span><span class="sxs-lookup"><span data-stu-id="a7821-103">Clears the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="a7821-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7821-104">SYNTAX</span></span>

```
Clear-AzDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7821-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7821-105">DESCRIPTION</span></span>
<span data-ttu-id="a7821-106">Clear-AzDefault cmdlet, Kullanıcı tarafından belirtilen geçiş parametrelerine bağlı olarak kullanıcının belirlediği Varsayılanları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a7821-106">The Clear-AzDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="a7821-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7821-107">EXAMPLES</span></span>

### <span data-ttu-id="a7821-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a7821-108">Example 1</span></span>
```
PS C:\> Clear-AzDefault
```

<span data-ttu-id="a7821-109">Bu komut, kullanıcının geçerli bağlamdaki tüm varsayılanlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a7821-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="a7821-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a7821-110">Example 1</span></span>
```
PS C:\> Clear-AzDefault -ResourceGroup
```

<span data-ttu-id="a7821-111">Bu komut, geçerli bağlamdaki Kullanıcı tarafından ayarlanan varsayılan kaynak grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a7821-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="a7821-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7821-112">PARAMETERS</span></span>

### <span data-ttu-id="a7821-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7821-113">-DefaultProfile</span></span>
<span data-ttu-id="a7821-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a7821-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7821-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a7821-115">-Force</span></span>
<span data-ttu-id="a7821-116">Varsayılan belirtilmemişse tüm varsayılanları kaldır</span><span class="sxs-lookup"><span data-stu-id="a7821-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="a7821-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a7821-117">-PassThru</span></span>
<span data-ttu-id="a7821-118">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="a7821-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a7821-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a7821-119">-ResourceGroup</span></span>
<span data-ttu-id="a7821-120">Varsayılan kaynak grubunu temizle</span><span class="sxs-lookup"><span data-stu-id="a7821-120">Clear Default Resource Group</span></span>

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

### <span data-ttu-id="a7821-121">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="a7821-121">-Scope</span></span>
<span data-ttu-id="a7821-122">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="a7821-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="a7821-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="a7821-123">-Confirm</span></span>
<span data-ttu-id="a7821-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a7821-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7821-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7821-125">-WhatIf</span></span>
<span data-ttu-id="a7821-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a7821-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7821-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a7821-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7821-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7821-128">CommonParameters</span></span>
<span data-ttu-id="a7821-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7821-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7821-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7821-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7821-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7821-131">INPUTS</span></span>

### <span data-ttu-id="a7821-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a7821-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a7821-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7821-133">OUTPUTS</span></span>

### <span data-ttu-id="a7821-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a7821-134">System.Boolean</span></span>

## <span data-ttu-id="a7821-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7821-135">NOTES</span></span>

## <span data-ttu-id="a7821-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7821-136">RELATED LINKS</span></span>
