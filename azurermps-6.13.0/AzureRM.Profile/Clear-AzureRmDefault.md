---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/clear-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
ms.openlocfilehash: a29bf86b4104fb9a3936daad055da0eab4368690
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764604"
---
# <span data-ttu-id="929d3-101">Clear-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="929d3-101">Clear-AzureRmDefault</span></span>

## <span data-ttu-id="929d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="929d3-102">SYNOPSIS</span></span>
<span data-ttu-id="929d3-103">Kullanıcı tarafından geçerli bağlamda ayarlanan Varsayılanları temizler.</span><span class="sxs-lookup"><span data-stu-id="929d3-103">Clears the defaults set by the user in the current context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="929d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="929d3-104">SYNTAX</span></span>

```
Clear-AzureRmDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="929d3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="929d3-105">DESCRIPTION</span></span>
<span data-ttu-id="929d3-106">Clear-AzureRmDefault cmdlet, Kullanıcı tarafından belirtilen geçiş parametrelerine bağlı olarak kullanıcının belirlediği Varsayılanları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="929d3-106">The Clear-AzureRmDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="929d3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="929d3-107">EXAMPLES</span></span>

### <span data-ttu-id="929d3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="929d3-108">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault
```

<span data-ttu-id="929d3-109">Bu komut, kullanıcının geçerli bağlamdaki tüm varsayılanlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="929d3-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="929d3-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="929d3-110">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault -ResourceGroup
```

<span data-ttu-id="929d3-111">Bu komut, geçerli bağlamdaki Kullanıcı tarafından ayarlanan varsayılan kaynak grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="929d3-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="929d3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="929d3-112">PARAMETERS</span></span>

### <span data-ttu-id="929d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="929d3-113">-DefaultProfile</span></span>
<span data-ttu-id="929d3-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="929d3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="929d3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="929d3-115">-Force</span></span>
<span data-ttu-id="929d3-116">Varsayılan belirtilmemişse tüm varsayılanları kaldır</span><span class="sxs-lookup"><span data-stu-id="929d3-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="929d3-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="929d3-117">-PassThru</span></span>
<span data-ttu-id="929d3-118">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="929d3-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="929d3-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="929d3-119">-ResourceGroup</span></span>
<span data-ttu-id="929d3-120">Varsayılan kaynak grubunu temizle</span><span class="sxs-lookup"><span data-stu-id="929d3-120">Clear Default Resource Group</span></span>

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

### <span data-ttu-id="929d3-121">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="929d3-121">-Scope</span></span>
<span data-ttu-id="929d3-122">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="929d3-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="929d3-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="929d3-123">-Confirm</span></span>
<span data-ttu-id="929d3-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="929d3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="929d3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="929d3-125">-WhatIf</span></span>
<span data-ttu-id="929d3-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="929d3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="929d3-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="929d3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="929d3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="929d3-128">CommonParameters</span></span>
<span data-ttu-id="929d3-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="929d3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="929d3-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="929d3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="929d3-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="929d3-131">INPUTS</span></span>

### <span data-ttu-id="929d3-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="929d3-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="929d3-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="929d3-133">OUTPUTS</span></span>

### <span data-ttu-id="929d3-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="929d3-134">System.Boolean</span></span>

## <span data-ttu-id="929d3-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="929d3-135">NOTES</span></span>

## <span data-ttu-id="929d3-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="929d3-136">RELATED LINKS</span></span>
