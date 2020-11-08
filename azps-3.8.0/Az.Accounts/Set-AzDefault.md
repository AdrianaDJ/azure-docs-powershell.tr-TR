---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
ms.openlocfilehash: 25fd0e1cd651f70fa0900c528f9e5297a8eaf2df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097474"
---
# <span data-ttu-id="98fdb-101">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="98fdb-101">Set-AzDefault</span></span>

## <span data-ttu-id="98fdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98fdb-102">SYNOPSIS</span></span>
<span data-ttu-id="98fdb-103">Geçerli bağlamda varsayılan ayarlar</span><span class="sxs-lookup"><span data-stu-id="98fdb-103">Sets a default in the current context</span></span>

## <span data-ttu-id="98fdb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="98fdb-104">SYNTAX</span></span>

```
Set-AzDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98fdb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="98fdb-105">DESCRIPTION</span></span>
<span data-ttu-id="98fdb-106">Set-AzDefault cmdlet 'i geçerli içerikte Varsayılanları ekler veya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="98fdb-106">The Set-AzDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="98fdb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="98fdb-107">EXAMPLES</span></span>

### <span data-ttu-id="98fdb-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="98fdb-108">Example 1</span></span>
```
PS C:\> Set-AzDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="98fdb-109">Bu komut, varsayılan kaynak grubunu Kullanıcı tarafından belirtilen kaynak grubuyla ayarlar.</span><span class="sxs-lookup"><span data-stu-id="98fdb-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="98fdb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="98fdb-110">PARAMETERS</span></span>

### <span data-ttu-id="98fdb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98fdb-111">-DefaultProfile</span></span>
<span data-ttu-id="98fdb-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="98fdb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98fdb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="98fdb-113">-Force</span></span>
<span data-ttu-id="98fdb-114">Belirtilen varsayılan yoksa yeni bir kaynak grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="98fdb-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="98fdb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98fdb-115">-ResourceGroupName</span></span>
<span data-ttu-id="98fdb-116">Varsayılan olarak ayarlanan kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="98fdb-116">Name of the resource group being set as default</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98fdb-117">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="98fdb-117">-Scope</span></span>
<span data-ttu-id="98fdb-118">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="98fdb-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="98fdb-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="98fdb-119">-Confirm</span></span>
<span data-ttu-id="98fdb-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="98fdb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98fdb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98fdb-121">-WhatIf</span></span>
<span data-ttu-id="98fdb-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="98fdb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98fdb-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="98fdb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98fdb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98fdb-124">CommonParameters</span></span>
<span data-ttu-id="98fdb-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="98fdb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98fdb-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98fdb-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98fdb-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="98fdb-127">INPUTS</span></span>

### <span data-ttu-id="98fdb-128">System. String</span><span class="sxs-lookup"><span data-stu-id="98fdb-128">System.String</span></span>

## <span data-ttu-id="98fdb-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="98fdb-129">OUTPUTS</span></span>

### <span data-ttu-id="98fdb-130">Microsoft. Azure. Commands. Profile. modeller. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="98fdb-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="98fdb-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="98fdb-131">NOTES</span></span>

## <span data-ttu-id="98fdb-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="98fdb-132">RELATED LINKS</span></span>
