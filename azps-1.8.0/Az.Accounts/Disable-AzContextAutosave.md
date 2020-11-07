---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
ms.openlocfilehash: 2147fd87cae8ef87010c54ce42dc33c85a8f6374
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751296"
---
# <span data-ttu-id="d9bfe-101">Disable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="d9bfe-101">Disable-AzContextAutosave</span></span>

## <span data-ttu-id="d9bfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9bfe-102">SYNOPSIS</span></span>
<span data-ttu-id="d9bfe-103">Azure kimlik bilgilerini otomatik kaydetmeyi kapatma.</span><span class="sxs-lookup"><span data-stu-id="d9bfe-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="d9bfe-104">PowerShell penceresini bir sonraki açışınızda oturum açma bilgileriniz unutulan</span><span class="sxs-lookup"><span data-stu-id="d9bfe-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="d9bfe-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9bfe-105">SYNTAX</span></span>

```
Disable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9bfe-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9bfe-106">DESCRIPTION</span></span>
<span data-ttu-id="d9bfe-107">Azure kimlik bilgilerini otomatik kaydetmeyi kapatma.</span><span class="sxs-lookup"><span data-stu-id="d9bfe-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="d9bfe-108">PowerShell penceresini bir sonraki açışınızda oturum açma bilgileriniz unutulan</span><span class="sxs-lookup"><span data-stu-id="d9bfe-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="d9bfe-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9bfe-109">EXAMPLES</span></span>

### <span data-ttu-id="d9bfe-110">Bağlamı otomatik kaydetmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="d9bfe-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzContextAutosave
```

<span data-ttu-id="d9bfe-111">Geçerli Kullanıcı için otomatik kaydetmeyi devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="d9bfe-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="d9bfe-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9bfe-112">PARAMETERS</span></span>

### <span data-ttu-id="d9bfe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9bfe-113">-DefaultProfile</span></span>
<span data-ttu-id="d9bfe-114">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d9bfe-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9bfe-115">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="d9bfe-115">-Scope</span></span>
<span data-ttu-id="d9bfe-116">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler</span><span class="sxs-lookup"><span data-stu-id="d9bfe-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="d9bfe-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="d9bfe-117">-Confirm</span></span>
<span data-ttu-id="d9bfe-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d9bfe-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9bfe-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9bfe-119">-WhatIf</span></span>
<span data-ttu-id="d9bfe-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d9bfe-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9bfe-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d9bfe-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9bfe-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9bfe-122">CommonParameters</span></span>
<span data-ttu-id="d9bfe-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9bfe-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9bfe-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9bfe-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9bfe-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9bfe-125">INPUTS</span></span>

### <span data-ttu-id="d9bfe-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d9bfe-126">None</span></span>

## <span data-ttu-id="d9bfe-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9bfe-127">OUTPUTS</span></span>

### <span data-ttu-id="d9bfe-128">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="d9bfe-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="d9bfe-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9bfe-129">NOTES</span></span>

## <span data-ttu-id="d9bfe-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9bfe-130">RELATED LINKS</span></span>
